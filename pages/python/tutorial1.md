---
layout: default
parent: Python
title:  "Tutorial 1"
nav_order: 1
mathjax: true
permalink: /python1
---

# Tutorial 1: Basic Functions & Derivatives


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hongvin/kix1001/blob/master/python/tutorial1.ipynb)


---

#### Housekeeping: Importing required libraries

Sympy: SymPy is a Python library for symbolic mathematics. We will use this library to solve all the tutorials.


```python
import sympy as sy
from sympy.abc import x                           # variable x
from sympy.solvers import solve                   # Solving equations
from sympy import sqrt,tan,sin,cos,sec,pi,root,ln
from sympy import log,exp,atan,asinh,atanh,asin   # Import all required math function
from sympy import diff, idiff                     # Solving differentiation
sy.init_printing(use_latex=True)                  # Show it in natural display
```

##### How to use `sympy` to solve limit questions?

1. Declare the symbol to be used in the function. For example, if you wanted to use the symbol $$x$$, just use `x` as usual because we have import the variable `x` earlier. Alternatively, you can declare $$x$$ such that `x = sy.symbols('x')`. This will make the variable `x` a representation of $$x$$ in the function to be solved. Note that `sy` is used because we import `sympy` as `sy`.
2. Type the function. For example, if the function is $$\frac{1}{x}$$, type it as `1/x`. Note, for power, python uses `**` instead of `^`.
3. Solve the limit with `sympy` library by using `sy.limit(function,symbol,limit)`. `sy.limit` takes three parameters, which are the function, the symbols used in the function and the limit. The return of this fuction will be the answer.

---
##### How to use `sympy` to solve derivative questions?
Just `diff(function,symbol)`!

---

##### Some cheat sheet!

To make sure if you input the equation correctly, you can use the `display(function)` function. For example,

```python
x = sqrt(x)
display(x)
```
will return:

<div class="code-example" markdown="1">
 $$\sqrt{x}$$ 
</div>

The representation of mathematics function in Python:

|Mathematics Function|Python representation|
| :---: | :---: |
| $$x^2$$ |`x**2`|
| $$\sqrt{x}$$ |`sqrt(x)`|
| $$\sqrt[3]{x}$$ |`root(x,3)`|
| $$\tan{x}$$ |`tan(x)`|
| $$\sec{x}$$ |`sec(x)`|
| $$\pi$$ |`pi`|

_Note that the `sqrt`, `tan`, `sec`, `pi` used in this notebook are from `sympy` library, not from `math` library._

##### That's it! Let's use this knowledge and solve them.
---

### Q1: Find the limit of $$\lim _{x \rightarrow 5} \frac{x^{2}-25}{x^{2}+x-30}$$.


```python
lim = 5
func = (x**2-25)/(x**2+x-30)
sy.limit(func,x,lim)
```



<div class="code-example" markdown="1">
 $$\frac{10}{11}$$
</div>


### Q2: Find the limit of $$\lim _{x \rightarrow 9} \frac{\sqrt{x}-3}{x-9}$$.



```python
lim = 9
func = (sqrt(x)-3)/(x-9)
sy.limit(func,x,lim)
```



<div class="code-example" markdown="1">
 $$\frac{1}{6}$$
</div>


### Q3: Find the limit of $$\lim _{x \rightarrow 0} \frac{\sqrt{2+x}-\sqrt{2}}{x}$$.



```python
lim = 0
func = (sqrt(2+x)-sqrt(2))/(x)
sy.limit(func,x,lim)
```



<div class="code-example" markdown="1">
 $$\frac{\sqrt{2}}{4}$$
</div>


### Q4: Find the limit of $$\lim _{\theta \rightarrow \frac{\pi}{2}} \frac{\tan{\theta}}{\sec{\theta}}$$.



```python
lim = pi/2
func = tan(x)/sec(x)
sy.limit(func,x,lim)
```



<div class="code-example" markdown="1">
 $$1$$
</div>


### Q5: Find the limit of $$\lim _{\theta \rightarrow 0} \frac{\cos{\theta}-1}{\sin{\theta}}$$.



```python
lim = 0
func = (cos(x)-1)/sin(x)
sy.limit(func,x,lim)
```



<div class="code-example" markdown="1">
 $$0$$
</div>


### Q6: If $$2x\leq g(x)\leq x^2-x+2$$ for all $$$x$$$, evaluate  $$\lim_{x \rightarrow 1} g(x)$$.



```python
lim = 1
solve([sy.limit(2*x,x,lim)<=x,x<=sy.limit(x**2-x+2,x,lim)])
```



<div class="code-example" markdown="1">
 $$x = 2$$
</div>


### Q7: Solve $$y'$$ if $$y=\sqrt{3x^2-2x+3}$$.



```python
y = sqrt(3*x**2-2*x+3)
diff(y,x)
```



<div class="code-example" markdown="1">
 $$\frac{3 x - 1}{\sqrt{3 x^{2} - 2 x + 3}}$$
</div>


### Q8: Solve $$y'$$ if $$y=5\sqrt[3]{x^2+\sqrt{x^3}}$$.



```python
y = 5*root(x**2+sqrt(x**3),3)
diff(y)
```



<div class="code-example" markdown="1">
 $$\frac{5 \left(\frac{2 x}{3} + \frac{\sqrt{x^{3}}}{2 x}\right)}{\left(x^{2} + \sqrt{x^{3}}\right)^{\frac{2}{3}}}$$
</div>


### Q9: Solve $$y$$ if $$y=\ln{\cos{x^2}}$$.



```python
y = ln(cos(x**2))
diff(y)
```



<div class="code-example" markdown="1">
 $$- \frac{2 x \sin{\left(x^{2} \right)}}{\cos{\left(x^{2} \right)}}$$
</div>


### Q10: Differentiate $$y=\log{(4+\cos{x})}$$.



```python
y = log(4+cos(x),10)
diff(y)
```



<div class="code-example" markdown="1">
 $$- \frac{\sin{\left(x \right)}}{\left(\cos{\left(x \right)} + 4\right) \log{\left(10 \right)}}$$
</div>


### Q11: Find $$y'$$ for $$10e^{2xy}=e^{15y}+e^{13x}$$.



```python
y=sy.symbols('y')
eqn=10*exp(2*x*y)-exp(15*y)-exp(13*x)
idiff(eqn,y,x)
```



<div class="code-example" markdown="1">
 $$\frac{- 20 y e^{2 x y} + 13 e^{13 x}}{5 \left(4 x e^{2 x y} - 3 e^{15 y}\right)}$$
</div>


### Q12: Find $$f'(x)$$ if $$f(x)=2x(\arctan{5x})^2+6\tan{(\cos{6x})}$$.



```python
y = 2*x*(atan(5*x))**2+6*tan(cos(6*x))
diff(y)
```


<div class="code-example" markdown="1">
 $$\frac{20 x \operatorname{atan}{\left(5 x \right)}}{25 x^{2} + 1} - 36 \left(\tan^{2}{\left(\cos{\left(6 x \right)} \right)} + 1\right) \sin{\left(6 x \right)} + 2 \operatorname{atan}^{2}{\left(5 x \right)}$$
</div>


### Q13: Solve $$y'$$ if $$y=4x\sinh^{-1}{(\frac{x}{6})}+\tanh^{-1}{(\cos{10x})}$$.



```python
y = 4*x*asinh(x/6)+atanh(cos(10*x))
diff(y)
```



<div class="code-example" markdown="1">
 $$\frac{2 x}{3 \sqrt{\frac{x^{2}}{36} + 1}} + 4 \operatorname{asinh}{\left(\frac{x}{6} \right)} - \frac{10 \sin{\left(10 x \right)}}{1 - \cos^{2}{\left(10 x \right)}}$$
</div>


### Q14: Differentiate $$y=\frac{1}{\sin^{-1}{x}}$$.



```python
y = 1/(asin(x))
diff(y)
```



<div class="code-example" markdown="1">
 $$- \frac{1}{\sqrt{1 - x^{2}} \operatorname{asin}^{2}{\left(x \right)}}$$
</div>


### Q15: Differentiate $$y=(x^3-1)^{100}$$.



```python
y = (x**3-1)**100
diff(y)
```



<div class="code-example" markdown="1">
 $$300 x^{2} \left(x^{3} - 1\right)^{99}$$
</div>