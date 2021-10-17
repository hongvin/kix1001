---
layout: default
parent: MATLAB
title:  "Tutorial 1"
nav_order: 4
mathjax: true
permalink: /matlab1
---

# Tutorial 1: Basic Functions & Derivatives

---

[Download MATLAB Live Script]({{ site.url }}/matlab/tutorial1.mlx){: .btn .btn-purple }
---

## Limits

The fundamental idea in calculus is to make calculations on functions as a variable "gets close to" a certain value. 

In MATLAB, we can use the Symbolic Math Toolbox software to calculate the limits of functions directly. The commands are:

```matlab
syms x
limit((x^2-25)/(x^2+x-30), x, 5)
```

which will return

```bash
ans = 

  10
  ──
  11
```

From the command above, we can see there is two lines. The first line `syms x` tells MATLAB that the variable we are going to use is $$x$$. The second line `limit((x^2-25)/(x^2+x-30), x, 5)` tells MATLAB that we want to solve the limit for the equation, with $$x\rightarrow5$$. The first parameter in `limit` function is the equation, the second parameter and third parameter is the variable and limit, respectively.

Some more examples:

| Mathematical Operation | MATLAB Command |
|:---|:---|
| $$\lim _{x \rightarrow 0} f(x)$$ | `limit(f)` or `limit(f,x,0)` |
| $$\lim _{x \rightarrow a} f(x)$$ | `limit(f,x,a)` or `limit(f,a)` |
| $$\lim _{x \rightarrow a-} f(x)$$ | `limit(f,x,a, 'left')` |
| $$\lim _{x \rightarrow a+} f(x)$$ | `limit(f,x,a, 'right')` |

---

$$\lim _{x \rightarrow 5} \frac{x^{2}-25}{x^{2}+x-30}$$ 

```matlab
syms x
limit((x^2-25)/(x^2+x-30), x, 5)
```

---

$$\lim _{x \rightarrow 9} \frac{\sqrt{x}-3}{x-9}$$ 

```matlab
syms x
limit((sqrt(x)-3)/(x-9), x, 9)
```

---

$$\lim _{x \rightarrow 0} \frac{\sqrt{2+x}-\sqrt{2}}{x}$$

```matlab
syms x
limit((sqrt(2+x)-sqrt(2))/(x), x, 0)
```

---

$$\lim _{\theta \rightarrow \frac{\pi}{2}} \frac{\tan{\theta}}{\sec{\theta}}$$

```matlab
syms x
limit((tan(x))/(sec(x)), x, pi/2)
```

---

$$\lim _{\theta \rightarrow 0} \frac{\cos{\theta}-1}{\sin{\theta}}$$

```matlab
syms x
limit((cos(x)-1)/sin(x),x,0)
```

---

### If $$2x\leq g(x)\leq x^2-x+2$$ for all $$x$$, evaluate  $$\lim_{x \rightarrow 1} g(x)$$.

```matlab
syms x
solve(limit(2*x,x,1)<=x,x<=limit(x^2-x+2,x,1))
```

We use `solve` to solve the two inequalities.

---

## Differentiation

Example below shows the simple command for differentiation.

```matlab
syms x
f=sin(x);
diff(f)
```

The command `diff(f)` differentiate `f` with respect to `x`, and produces:

```bash
ans =
 
cos(x)
```

To take the second derivative of `f`, use:

```matlab
diff(f,2)
```

or

```matlab
diff(diff(f))
```

This will produce:

```bash
ans =
 
-sin(x)
```

_Note, there are partial derivative, and derivative at given value, which did not discuss here since Tutorial 1 did not cover yet._

---

$$y=\sqrt{3x^2-2x+3}$$

```matlab
syms x
diff(sqrt(3*x^2-2*x+3))
```

Remember that you can use `pretty` to print the equation nicely!

---

$$y=5\sqrt[3]{x^2+\sqrt{x^3}}$$

```matlab
syms x
diff(5*nthroot((x^2+sqrt(x^3)),3))
```

Here, cube-root are being invoked through `nthroot(x,3)`. You could use `x^(1/3)` too. The same applies for $$n$$-th root, with `nthroot(x,n)` and `x^(1/n)`.

---

$$y=\ln{\cos{x^2}}$$

```matlab
syms x
diff(log(cos(x^2)))
```

Here $$\ln{x}$$ is being called as `log(x)` in MATLAB. In MATLAB, `Y = log(X)` returns the natural logarithm $$\ln(x)$$ of each element in array `X`.

---

$$y=\log{(4+\cos{x})}$$

```matlab
syms x
diff(log10(4+cos(x)))
```

Note: `log10` is the common logarithm with base 10. You will get 

```bash
         sin(x)
- --------------------
  log(10) (cos(x) + 4)
```

as your answer. Note that the `log(10)` is actually $$\ln(10)$$, and $$\frac{1}{\ln(10)}=\log(e)$$.

---

$$10e^{2xy}=e^{15y}+e^{13x}$$

```matlab
syms y(x) DY;
eqn=10*exp(2*x*y)==exp(15*y)+exp(13*x);
dy=diff(y);
deqn = diff(eqn,x);
Deqn = subs(deqn, dy, DY);
DYsol = simplify( solve(Deqn, DY) );
disp(DY == DYsol)
```

Implicit differentiation takes more steps! We first define two symbol, `y(x)` and `DY`. Then, we type in the equation in `eqn` variable. Note that we can't have two `=` in one line, so to store a equation, we replace the `=` with `==`, where `eqn` now store the equation. Line 3 define `dy` as $$\frac{dy}{dx}$$, and line four differentiate the equation with respect to `x`. Line 5 substitute the `y(x)` in differentiated equation with `DY`, then simplified and solve the equation with respect to `DY`. Finally, we display the equation. Note that MATLAB might not be a better choice for some question, since it was not designed to handle such equation. Alternatively, you can use Mathematica, which is more suitable.

---

$$f(x)=2x(\arctan{5x})^2+6\tan{(\cos{6x})}$$

```matlab
syms x
diff(2*x*(atan(5*x))^2+6*tan(cos(6*x)))
```

Note $$\arctan(x)$$ is `atan(x)` in MATLAB.

---

$$y=4x\sinh^{-1}{(\frac{x}{6})}+\tanh^{-1}{(\cos{10x})}$$

```matlab
syms x
diff(4*x*asinh(x/6)+atanh(cos(10*x)))
```

Note $$\sinh^{-1}(x)$$ and $$\tanh^{-1}(x)$$ are `asinh(x)` and `atanh(x)` in MATLAB, respectively.

---

$$y=\frac{1}{\sin^{-1}{x}}$$

```matlab
syms x
diff(1/(asin(x)))
```

---

$$y=(x^3-1)^{100}$$

```matlab
syms x
diff((x^3-1)^100)
```

---

#### References

1. <https://www.mathworks.com/help/symbolic/limits.html>
2. <https://www.mathworks.com/help/symbolic/differentiation.html>
3. <https://www.mathworks.com/help/matlab/ref/log.html>
4. <https://www.mathworks.com/help/matlab/ref/log10.html>
5. <https://www.mathworks.com/help/symbolic/solve.html>