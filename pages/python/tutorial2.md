---
layout: default
parent: Python
title:  "Tutorial 2"
nav_order: 2
mathjax: true
permalink: /python2
---

# Tutorial 2: Basic Functions & Derivatives

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hongvin/kix1001/blob/master/python/tutorial2.ipynb)

---

#### Housekeeping: Importing required libraries
Sympy: SymPy is a Python library for symbolic mathematics. We will use this library to solve all the tutorials.


```python
import sympy as sy
from sympy.plotting import plot,plot_implicit
from sympy.abc import c,x,y                       # variable x,y
from sympy.solvers import solve                   # Solving equations
from sympy import sin,cos
from sympy import diff, idiff                     # Solving differentiation
sy.init_printing(use_latex=True)                  # Show it in natural display
```

---

### Q1: Find $$y'$$ for $$(x-y)^2=x+y-1$$ by using implicit differentiation.

---


```python
eqn = (x-y)**2-x-y+1
idiff(eqn,y,x)
```

<div class="code-example" markdown="1">
$$\displaystyle \frac{2 x - 2 y - 1}{2 x - 2 y + 1}$$
</div>

---

### Q2: Implicit differentiation to find an equation of the tangent line to the curve $$5x^2+10xy^2+5y=20$$ at point $$(2,2)$$.

---

```python
eqn = 5*x**2+10*x*y**2+5*y-20
yp = idiff(eqn,y,x)
display('Differential equation, y\':',yp)
m = yp.subs({x:2,y:2})
print('At point (2,2), the gradient is: ', m)
interception = solve(sy.Eq(2,m*2+c),c)[0]
display('The equation is: ',sy.Eq(y,m*x+interception))
```
<div class="code-example" markdown="1">
    "Differential equation, y':"

$$\displaystyle - \frac{2 x + 2 y^{2}}{4 x y + 1}$$

    At point (2,2), the gradient is:  -12/17

    'The equation is: '

$$\displaystyle y = \frac{58}{17} - \frac{12 x}{17}$$
</div>

---    

### Q3: $$y\cos{x}=1+\sin{(xy)}$$. Find $$\frac{dy}{dx}$$ by implicit differentiation.

---

```python
eqn = y*cos(x)-1-sin(x*y)
idiff(eqn,y,x)
```

<div class="code-example" markdown="1">
$$\displaystyle - \frac{y \left(\sin{\left(x \right)} + \cos{\left(x y \right)}\right)}{x \cos{\left(x y \right)} - \cos{\left(x \right)}}$$
</div>

---

### Q4: Find $$\frac{dy}{dx}$$ by implicit differentiation $$4\cos{x}\sin{y}=1$$.

---

```python
eqn = 4*cos(x)*sin(y)-1
idiff(eqn,y,x)
```

<div class="code-example" markdown="1">
$$\displaystyle \tan{\left(x \right)} \tan{\left(y \right)}$$
</div>

---

### Q5: An open box is to be made from cutting a square from each corner of a 12 in by 12 in piece of metal and then folding up the sides. What size square should be cut from each corner to produce a box of maximum volume?

---

```python
eqn = 4*x**3-48*x**2+144*x
a=solve(diff(eqn))
print('Possible value of x: ',a)
print('When a = {}, V = {}'.format(a[0],eqn.subs(x,a[0])))
print('When a = {}, V = {}'.format(a[1],eqn.subs(x,a[1])))
```

<div class="code-example" markdown="1">
    Possible value of x:  [2, 6]
    When a = 2, V = 128
    When a = 6, V = 0
</div>

---

### Q6: We are going to fence in a rectangular field. If we look at the field from above the cost of the vertical sides are RM 10/ft, the cost of the bottom is RM2/ft and the cost of the top is RM 7 /ft. If we have RM 700 determind the dimensions of the field that will maximize the enclosed area. 

---

```python
x=sy.symbols('x')
area = x*(35-(9/20)*x)
ans_x = solve(diff(area))[0]
ans_y = 35-9/20*ans_x
(ans_x,ans_y)
```

<div class="code-example" markdown="1">
$$\displaystyle \left( 38.8888888888889, \  17.5\right)$$
</div>