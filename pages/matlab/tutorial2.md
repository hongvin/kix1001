---
layout: default
parent: MATLAB
title:  "Tutorial 2"
nav_order: 5
mathjax: true
permalink: /matlab2
---

# Tutorial 2: Basic Functions & Derivatives

---

[Download MATLAB Live Script]({{ site.url }}/matlab/tutorial2.mlx){: .btn .btn-purple }
[View MATLAB Online](https://drive.matlab.com/sharing/bdf0d855-eb44-4ca2-8faf-98249fc8b406){: .btn .btn-green }

---

### Question 1

```matlab
syms y(x) DY;
eqn=(x-y)^2==x+y-1;
dy=diff(y);
deqn = diff(eqn,x);
Deqn = subs(deqn, dy, DY);
DYsol = simplify( solve(Deqn, DY) );
disp(DY == DYsol)
```

---

### Question 2

```matlab
syms y(x) DY c
eqn=5*x^2+10*x*y^2+5*y==20;
dy=diff(y);
deqn = diff(eqn,x);
Deqn = subs(deqn, dy, DY);
DYsol = simplify( solve(Deqn, DY) );
disp(DY == DYsol)
gradient = subs(subs(DYsol,x,2),y,2) %The gradient
intercept = solve(2==gradient*2+c) % Intersection point
disp(y==gradient*x+intercept)
```

---

### Question 3

```matlab
syms y(x) DY;
eqn=y*cos(x)==1+sin(x*y);
dy=diff(y);
deqn = diff(eqn,x);
Deqn = subs(deqn, dy, DY);
DYsol = simplify( solve(Deqn, DY) );
disp(DY == DYsol)
```

---

### Question 4

```matlab
syms y(x) DY;
eqn=4*cos(x)*sin(y)==1;
dy=diff(y);
deqn = diff(eqn,x);
Deqn = subs(deqn, dy, DY);
DYsol = simplify( solve(Deqn, DY) );
disp(DY == DYsol)
```

---

### Question 5

```matlab
syms x;
eqn = 4*x^3-48*x^2+144*x;
solve(diff(eqn))
% When x = 2
subs(eqn,x,2)
% When x = 6
subs(eqn,x,6)
```

---

### Question 6

```matlab
syms x;
eqn = x*(35-(9/20)*x)
ans_x = solve(diff(eqn))
ans_y = 35-(9/20)*ans_x
```