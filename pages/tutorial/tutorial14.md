---
layout: default
parent: Tutorial
title:  "Tutorial 14"
nav_order: 14
mathjax: true
permalink: /tutorial14
---

# Tutorial 14: Frobenius Method

---
[Tutorial PDF]({{ site.url }}/pdf/tutorial/tutorial14.pdf){: .btn .btn-purple }
[Solution PDF]({{ site.url }}/pdf/solution/tutorial14.pdf){: .btn .btn-green }

---

## Part 1: Using method of reduction of order, find $$y_2$$ such that $$y_1, y_2$$ form a basis.

1. $$2t^2y''+ty'-3y=0$$;&emsp;$$y_1(t)=t^{-1}, t\neq0$$
2. $$t^2y''-(t^2+2t)y'+(t+2)y=0$$;&emsp;$$y_1(t)=t$$
3. $$y''+6y'+9y=0$$;&emsp;$$y_1(t)=e^{-3t}$$
4. $$(x-1)y''-xy'+y=0$$;&emsp;$$y_1(x)=e^x,x>1$$
5. $$xy''-y'+4x^3y=0$$;&emsp;$$y_1(x)=\sin x^2, x>0$$.

---
### Solution Part 1
#### <u>Question (1)</u>

$$\begin{aligned}
y_2(t)&=v(t)y_1(t)\\
y_2(t)&=t^{-1}v \\
y_2'(t)&=-t^{-2}v+t^{-1}v'\\
y_2''(t)&=2t^{-3}v-2t^{-2}v'+t^{-1}v''
\end{aligned}$$

Substituting back yields,

$$\begin{aligned}
2t^2(2t^{-3}v-2t^{-2}v'+t^{-1}v'')+t(-t^{-2}v+t^{-1}v')-3(t^{-1}v)&=0 \\
2tv''+(-4+1)v'+(4t^{-1}-t^{-1}-3t^{-1})v&=0 \\
\color{red} {\scriptsize {[\triangle \text{ Ignoring the non-differentiated terms}]}}\\
2tv''-3v'&=0
\end{aligned}$$

Changing variables, $$w=v'\rightarrow w'=v''$$, Thus,

$$\begin{aligned}
2tw'-3w&=0\\
2t\frac{dw}{dt}&=3w\\
\int\frac{1}{3w}dw&=\int\frac{1}{2t}dt\\
\frac{1}{3}\ln|w|&=\frac{1}{2}\ln|t|+C\\
\ln|w|&=\ln t^{\frac{3}{2}}+C\\
w&=Ct^{\frac{3}{2}}
\end{aligned}$$

And, $$v'=w=Ct^{\frac{3}{2}} \rightarrow v=\int Ct^{\frac{3}{2}}dt=\frac{2}{5}Ct^{\frac{2}{5}}+K$$.

Letting $$C=\frac{5}{2}$$ and $$K=0$$, $$v(t)=t^{\frac{5}{2}}\rightarrow y_2(t)=t^{-1}t^{\frac{5}{2}}=t^{\frac{3}{2}}$$

$$\therefore \boldsymbol{y_2(t)=t^{\frac{3}{2}}}$$.

The $$y(t)$$ is: $$y(t)=C_1t^{-1}+C_2t^{\frac{3}{2}}$$

---
#### <u>Question (2)</u>

$$\begin{aligned}
y_2(t)&=v(t)y_1(t)\\
y_2(t)&=tv \\
y_2'(t)&=v+tv'\\
y_2''(t)&=v'+v'+tv''=2v'+tv''
\end{aligned}$$

Substituting back yields,

$$\begin{aligned}
t^2(2v'+tv'')-(t^2+2t)(v+tv')+(t+2)(tv)&=0 \\
2t^2v'+t^3v''-t^2v-t^3v'-2tv-2t^2v'+t^2v+2tv&=0 \\
v'(2t^2-t^3-2t^2)+v''(t^3)-t^2v+t^2v-2tv+2tv&=0\\
t^3v''-t^3v'&=0\\
v''-v'&=0
\end{aligned}$$

A solution to the equation is $$v'=e^t$$. Integrate this yield $$v(t)=e^t$$. 

$$\therefore \boldsymbol{y_2(t)=te^t}$$.

The $$y(t)$$ is: $$y(t)=C_1t+C_2te^{t}$$

---
#### <u>Question (3)</u>

$$\begin{aligned}
y_2(t)&=v(t)y_1(t)\\
y_2(t)&=ve^{-3t}\\
y_2'(t)&=v'e^{-3t}-3e^{-3t}v\\
y_2''(t)&=v''e^{-3t}-6v'e^{-3t}+9ve^{-3t}
\end{aligned}$$

Substituting back yields,

$$\begin{aligned}
(v''e^{-3t}-6v'e^{-3t}+9ve^{-3t})+6(v'e^{-3t}-3e^{-3t}v)+9(ve^{-3t}) &= 0 \\
\color{red} {\scriptsize{[\triangle \text{ Ignoring the non-differentiated terms}]}}\\
v''e^{-3t}&=0\\
\end{aligned}$$

This gives two possibilities, $$v''=0$$ or $$e^{-3t}=0$$. However, $$e^{-3t}=0$$ only true if $$t=\infty$$.

$$\begin{aligned}
v''&=0\\
\frac{d}{dt}(\frac{dv}{dt})&=0\\
\int\int d(dv)&=\int\int dt\\
\int v&=\int Adt\\
v&=At+B
\end{aligned}$$

Pick $$A$$ and $$B$$ so that second linearly independent solution is obtained.

- If $$A=0$$, $$y_2=Be^{-3t}$$. $$y_1$$ and $$y_2$$ are linearly dependent.
- If $$B=0$$, $$y_2=Ate^{-3t}$$. $$y_1$$ and $$y_2$$ are linearly independent. This is chosen and let $$A=1$$.

$$\boldsymbol{\therefore y_2(t)=te^{-3t}}$$

The $$y(t)$$ is: $$y(t)=(C_1t+C_2)e^{-3t}$$

---
#### <u>Question (4)</u>

$$\begin{aligned}
y_2(x)&=v(x)y_1(x)\\
y_2(x)&=ve^{x}\\
y_2'(x)&=v'e^{x}+ve^{x}\\
y_2''(x)&=v''e^x+2v'e^x+ve^x
\end{aligned}$$

Substituting back yields,

$$\begin{aligned}
(x-1)(v''e^x+2v'e^x+ve^x)-x(v'e^{x}+ve^{x})+ve^x&=0\\
v''xe^x+2xv'e^x+vxe^x-v''e^x-2v'e^x-ve^x-v'xe^x+vxe^x+ve^x&=0\\
v''(xe^x-e^x)+v'(2xe^x-2e^x-xe^x)+vxe^x-ve^x+ve^x&=0 \\ \scriptsize{[\triangle \text{ Ignoring the non-differentiated terms}]} \\
e^x[v''(x-1)+v'(x-2)]&=0\\
v''(x-1)+ v'(x-2)&=0
\end{aligned}$$

Let $$u=v'$$ and that $$u'=v''$$,

$$\begin{aligned}
u'(x-1)+u(x-2)&=0\\
u'(x-1)&=-u(x-2)\\
u'\frac{x-1}{x-2}&=-u\\
\frac{du}{dx}\frac{x-1}{x-2}&=-u\\
\frac{du}{u}&=-\frac{x-2}{x-1}dx\\
\int\frac{du}{u}&=-\int\frac{x-2}{x-1}dx\\
\ln|u|&=-\int\frac{x-1-1}{x-1}dx\\
\ln|u|&=\int(-1+\frac{1}{x-1})dx\\
\ln|u|&=-x+\ln|x-1|+C\\
u&=e^{-x+\ln|x-1|+C}\\
u&=C_1(x-1)e^{-x}
\end{aligned}$$

$$\begin{aligned}
v(x)&=C_1\int(x-1)e^{-x}dx\\
&=C_1[-(x-1)e^{-x}+\int e^{-x}dx]\\
&=C_1[-xe^{-x}+e^{-x}-e^{-x}]+C_2\\
&=C_1xe^{-x}+C_2
\end{aligned}$$

Let$$C_1=1$$ and $$C_2=0$$,

$$v(x)=xe^{-x}$$

Thus, $$y_2(t)=v(x)y_1(x)=xe^{-x}e^{x}$$.

$$\boldsymbol{\therefore y_2(x)=x}$$

The $$y(x)$$ is: $$y(x)=C_1e^x+C_2x$$

---
#### <u>Question (5)</u>

$$\begin{aligned}
y_2(t)&=v(t)y_1(t)\\
y_2(t)&=v\sin x^2\\
y_2'(t)&=v'\sin x^2 +2xv\cos x^2\\
y_2''(t)&=v''\sin x^2+2xv'\cos x^2 +(2v+2xv')\cos x^2-4x^2v\sin x^2 \\
&=v''\sin x^2+4xv'\cos x^2 +2v\cos x^2 -4x^2v\sin x^2
\end{aligned}$$

Substituting back yields,

$$\begin{aligned}
x(v''\sin x^2+4xv'\cos x^2+2v\cos x^2-4x^2v\sin x^2)&-\\v'\sin x^2-2xv\cos x^2+4x^3(v\sin x^2)&=0\\
xv''\sin x^2+(4x^2\cos x^2-\sin x^2)v'&=0
\end{aligned}$$

Let $$w=v'$$ and so $$w'=v''$$.

$$\begin{aligned}
xw'sin x^2+(4x^2\cos x^2-\sin x^2)w&=0\\
w'+\frac{(4x^2\cos x^2-\sin x^2)w}{x\sin x^2}&=0\\
\frac{dw}{dx}&=\frac{(4x^2\cos x^2-\sin x^2)w}{x\sin x^2}\\
\frac{dw}{w}&=\int \frac{1}{x}dx -\int 4x\frac{\cos x^2}{\sin x^2}dx\\
\ln|w|&=\ln|x|-\ln|(\sin x^2)^2|+C\\
&=\ln\left|\frac{x}{(\sin x^2)^2}\right|\\
w&=C\frac{x}{(\sin x^2)^2}
\end{aligned}$$

Therefore,

$$\begin{aligned}
v'(x)&=w=C\frac{x}{(\sin x^2)^2}\\
v(x)&=\int C\frac{x}{(\sin x^2)^2}dx\\
&=-\frac{1}{2}C\cot x^2+A
\end{aligned}$$

Let $$C=-2$$ and $$K=0$$,

$$v(x)=\cot x^2$$

$$\boldsymbol{\therefore y_2(t)=\cot x^2\sin x^2=\cos x^2}$$

The $$y(t)$$ is: $$y(t)=C_1\sin x^2+C_2\cos x^2$$

---

## Part 2: Discuss whether two Frobenius series solutions exist or do not exist for the following equations. 

1. $$2x^2y''+x(x+1)y'-(\cos x)y=0$$
2. $$x^4y''-(x^2\sin x)y'+2(1-\cos x)y=0$$

---
### Solution Part 2
#### <u>Question (1)</u>

$$\begin{aligned}
2x^2y''+x(x+1)y'-(\cos x)y&=0\\
x^2y''+\frac{(x+1)xy'}{2}-\frac{\cos x}{2}y&=0\\
\end{aligned}$$

$$p(x)=\frac{x+1}{2} \Rightarrow p(0)=\frac{1}{2}$$

$$q(x)=\frac{-\cos x}{2} \Rightarrow q(0)=-\frac{1}{2}$$

Substituting $$r$$ to find $$r_1$$ and $$r_2$$.

$$r^2+(p(0)-1)r+q(0)=2r^2-r-1=0$$

$$\Rightarrow r_1=1, r_2=-\frac{1}{2}$$.

$$\therefore r_1-r_2=1-(-\frac{1}{2})=\frac{3}{2} \text{ }\triangleright \text{ not a zero or positive integer}$$. 

**Two Frobenius series solutions exist.**

---

#### <u>Question (2)</u>

$$\begin{aligned}
x^4y''-(x^2\sin x)y'+2(1-\cos x)y&=0\\
x^2y''-\frac{\sin x}{x}xy'+2\frac{1-\cos x}{x^2}y&=0\\
\end{aligned}$$

$$p(x)=\frac{-\sin x}{x} \Rightarrow p(0)=-1$$

$$q(x)=\frac{2(1-\cos x)}{x^2} \Rightarrow q(0)=1$$

Substituting $$r$$ to find $$r_1$$ and $$r_2$$.

$$r^2+(p(0)-1)r+q(0)=r^2-2r-1=0$$

$$\Rightarrow r_1=1, r_2=1$$.

**One Frobenius series solution exists since $$r_1=r_2$$.**

---

## Part 3: Apply Frobenius Method to find the basis of solutions of the following differential equations.

1. $$2xy''+y'+y=0$$
2. $$xy''+2y'+xy=0$$
3. $$xy''+(1-2x)y'+(x-1)y=0$$
4. $$2ty''+(1+t)y'+y=0$$
5. $$x(1-x)y''-3xy'-y=0$$

---
### Solution Part 3
#### <u>Question (1)</u>

$$x=0$$ is a regular singular solution.
Assuming the solution is $$y=\sum \limits_{k=0}^\infty a_kx^{k+r}$$.

$$\begin{aligned}
y&=\sum \limits_{k=0}^\infty a_kx^{k+r}\\
y'&=\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}\\
y''&=\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-2}
\end{aligned}$$

Substituting back yields,

$$\begin{aligned}
2x\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-2}+\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}+\sum \limits_{k=0}^\infty a_kx^{k+r}&=0\\
2\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-1}+\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}+\sum \limits_{k=0}^\infty a_kx^{k+r}&=0 \text{ }\\
\color{red} {\scriptsize {[\triangle { \text{ Removing the } x \text{ from the first term}}}]}\\
2\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k-1}+\sum \limits_{k=0}^\infty (k+r)a_kx^{k-1}+\sum \limits_{k=0}^\infty a_kx^{k}&=0 \\
\color{red}{\scriptsize{[\triangle { \text{ Diving out } x^r}}]} \\
2\sum \limits_{n=-1}^\infty (n+r+1)(n+r)a_{n+1}x^n+\sum \limits_{n=-1}^\infty (n+r+1)a_{n+1}x^n+\sum \limits_{n=0}^\infty a_nx^n&=0 \\
\color{red} {\scriptsize{[\triangle { \text{ Substituting } k \text{ with }n \text{ (change limits)}}]}} \\
2r(r-1)a_0x^{-1}+2\sum \limits_{n=0}^\infty (n+r+1)(n+r)a_{n+1}x^n&+\\
ra_0x^{-1}+\sum \limits_{n=0}^\infty (n+r+1)a_{n+1}x^n+\sum \limits_{n=0}^\infty a_nx^n&=0 \\
\color{red} {\scriptsize{[\triangle { \text{ Taking out all terms to make sure }  n=0}]}} \\
\end{aligned}$$

For $$a_0$$, $$[2(r^2-r)+r]a_0=0$$.

Since $$a_0\neq0\Rightarrow r(2r-1)=0\Rightarrow r_2=0, r_1=\frac{1}{2}$$

The recurrence relation is then,

$$\begin{aligned}
[2(n+r+1)(n+r)+(n+r+1)]a_{n+1}+a_n&=0\\
(n+r+1)(2n+2r+1)a_{n+1}&=-a_n\\
a_{n+1}&=\frac{-a_n}{(n+r+1)(2n+2r+1)}, n=0,1,2,...
\end{aligned}$$

For $$r=\frac{1}{2}$$, 

$$\begin{aligned}
a_{n+1}&=-\frac{a_n}{(n+\frac{3}{2})(2n+2)} \\ \\
n&=0, a_1=-\frac{a_0}{(\frac{3}{2})(2)}=-\frac{a_0}{3}\\
n&=1, a_2=\frac{a_1}{(\frac{5}{2})(4)}=\frac{a_0}{10\cdot3}\\
n&=2, a_3=-\frac{a_2}{(\frac{7}{2})(6)}=-\frac{a_0}{21\cdot10\cdot3}\\ \\
y_1(x)&=\sum\limits_{k=0}^\infty a_kx^{k+r}=a_0x^{\frac{1}{2}}+a_1x^{\frac{3}{2}}+... \\
y_1(x)&=a_0x^{\frac{1}{2}}-\frac{a_0}{3}x^{\frac{3}{2}}+\frac{a_0}{10\cdot3}x^{\frac{5}{2}}-\frac{a_0}{21\cdot10\cdot3}x^{\frac{7}{2}}+...\\
\boldsymbol{y_1(x)}&=\boldsymbol{a_0x^{\frac{1}{2}}\left[1-\frac{x}{3}+\frac{x^2}{10\cdot3}-\frac{x^3}{21\cdot10\cdot3}+...\right]}
\end{aligned}$$

For $$r=0$$, 

$$\begin{aligned}
a_{n+1}&=-\frac{a_n}{(n+1)(2n+1)} \\ \\
n&=0, a_1=-\frac{a_0}{(1)(1)}=-a_0\\
n&=1, a_2=\frac{a_1}{(2)(3)}=\frac{a_0}{6}\\
n&=2, a_3=-\frac{a_2}{(3)(5)}=-\frac{a_0}{15\cdot6}\\ \\
y_2(x)&=\sum\limits_{k=0}^\infty a_kx^k=a_0x^0+a_1x^1+... \\
y_2(x)&=a_0-a_0x+\frac{a_0}{6}x^2-\frac{a_0}{15\cdot6}x^3+...\\
\boldsymbol{y_2(x)}&=\boldsymbol{a_0\left[1-x+\frac{x^2}{6}-\frac{x^3}{15\cdot6}+...\right]}
\end{aligned}$$

---

#### <u>Question (2)</u>

$$x=0$$ is a regular singular solution.
Assuming the solution is $$y=\sum \limits_{k=0}^\infty a_kx^{k+r}$$.

$$\begin{aligned}
y&=\sum \limits_{k=0}^\infty a_kx^{k+r}\\
y'&=\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}\\
y''&=\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-2}
\end{aligned}$$

Substituting back yields,

$$\begin{aligned}
x\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-2}+2\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}+x\sum \limits_{k=0}^\infty a_kx^{k+r}&=0\\
\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-1}+2\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}+\sum \limits_{k=0}^\infty a_kx^{k+r+1}&=0 \\
\color{red}{\scriptsize{[\triangle { \text{ Removing the } x \text{ from the first term]}}}}\\
\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k-1}+2\sum \limits_{k=0}^\infty (k+r)a_kx^{k-1}+\sum \limits_{k=0}^\infty a_kx^{k+1}&=0 \\
\color{red}{\scriptsize{[\triangle {\text{ Diving out } x^r]}}} \\
\sum \limits_{n=-1}^\infty (n+r+1)(n+r)a_{n+1}x^n+2\sum \limits_{n=-1}^\infty (n+r+1)a_{n+1}x^n+\sum \limits_{n=1}^\infty a_{n-1}x^n&=0 \\
\color{red}{\scriptsize{[\triangle { \text{ Substituting } k \text{ with }n \text{ (change limits)}}]}} \\
r(r-1)a_0x^{-1}+r(r+1)a_1x^0+\sum \limits_{n=1}^\infty (n+r+1)(n+r)a_{n+1}x^n&+\\
2ra_0x^{-1}+2(r+1)a_1x^0+2\sum \limits_{n=1}^\infty (n+r+1)a_{n+1}x^n+\sum \limits_{n=1}^\infty a_{n-1}x^n&=0\\
(r^2-r+2r)a_0x^{-1}+(r^2+r+r+1)a_1x^0&+\\
\sum\limits_{n=1}^\infty \left[((n+r+1)(n+r)+2(n+r+1))a_{n+1}+a_{n-1}\right]x^n&=0 \\
\color{red}{\scriptsize{[\triangle { \text{ Taking out all terms to make sure }  n=0}]}} \\
\end{aligned}$$

For $$a_0$$, $$(r^2-r+2r)a_0=0$$.

Since $$a_0\neq0\Rightarrow r^2+r=0\Rightarrow r_1=0, r_2=-1$$

The recurrence relation is then,

$$\begin{aligned}
[(n+r+1)(n+r)+2(n+r+1)]a_{n+1}+a_{n-1}&=0\\
(n+r+1)(n+r+2)a_{n+1}&=-a_{n-1}\\
a_{n+1}&=\frac{-a_{n-1}}{(n+r+1)(n+r+2)}, n=0,1,2,...
\end{aligned}$$

For $$r=0$$, 

$$\begin{aligned}
a_{n+1}&=-\frac{a_{n-1}}{(n+1)(n+2)} \\ \\
n&=0, [(r^2+r)+2(r+1)]a_1=0\Rightarrow a_1=0\\
n&=1, a_2=\frac{-a_0}{3\cdot2}=\frac{-a_0}{3!}\\
n&=2, a_3=-\frac{-a_1}{12}=0\\
n&=3, a_4=\frac{-a_2}{20\cdot3!}=\frac{-a_0}{5!}\\
n&=4, a_5=-\frac{-a_3}{30}=0\\ \\
y_1(x)&=\sum\limits_{k=0}^\infty a_kx^{k+r}=a_0x^0+a_1x^1+... \\
y_1(x)&=a_0+0-\frac{a_0}{3!}x^2+0+\frac{a_0}{5!}+...\\
\boldsymbol{y_1(x)}&=\boldsymbol{a_0(1-\frac{1}{3!}x^2+\frac{1}{5!}x^4+...)}
\end{aligned}$$

For $$r=-1$$, 

$$\begin{aligned}
a_{n+1}&=\frac{-a_{n-1}}{n(n+1)}, n=1,2,3,...\\ \\
n&=0, [(r^2+r)+2(r+1)]a_1=0 \Rightarrow 0\cdot a_1=0\text{ }\triangleright a_1\neq0\text{(unknown)}\\
n&=1, a_2=\frac{-a_0}{1\cdot2}=\frac{-a_0}{2!}\\
n&=2, a_3=-\frac{-a_1}{2\cdot3}=0\\
n&=3, a_4=\frac{-a_2}{3\cdot4}=\frac{a_0}{4!}\\
n&=4, a_5=-\frac{-a_3}{4\cdot5}=\frac{a_1}{5!}\\ \\
y_2(x)&=\sum\limits_{k=0}^\infty a_kx^{k+r}=a_0x^{-1}+a_1x^0+a_2x^1+... \\
y_2(x)&=\frac{1}{x}a_0+a_1-\frac{a_0}{2!}x-\frac{a_1}{3!}x^2+...\\
y_2(x)&=a_0(\frac{1}{x}-\frac{1}{2!}x+\frac{1}{4!}x^3+...)+a_1(1-\frac{x^2}{3!}+\frac{x^4}{5!}+...)\\
\boldsymbol{y_2(x)}&=\boldsymbol{a_0\frac{1}{x}\cos x+a_1\frac{1}{x}\sin x}
\end{aligned}$$

---

#### <u>Question (3)</u>

$$x=0$$ is a regular singular solution.
Assuming the solution is $$y=\sum \limits_{k=0}^\infty a_kx^{k+r}$$.

$$\begin{aligned}
y&=\sum \limits_{k=0}^\infty a_kx^{k+r}\\
y'&=\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}\\
y''&=\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-2}
\end{aligned}$$

Substituting back yields,

$$\begin{aligned}
x\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-2}+(1-2x)\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}&+\\
(x-1)\sum \limits_{k=0}^\infty a_kx^{k+r}&=0\\
\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-1}+\sum \limits_{k=0}^\infty (k+r) a_k x^{k+r-1}&-\\
2\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}+(x-1)\sum \limits_{k=0}^\infty a_kx^{k+r}&=0 \\
\color{red}{\scriptsize{[\triangle { \text{ Removing the } x \text{ from the first term]}}}}\\
\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k-1}+\sum\limits_{k=0}^\infty (k+r)a_kx^{k-1}&-\\
2\sum \limits_{k=0}^\infty (k+r)a_kx^{k-1}+\sum \limits_{k=0}^\infty a_kx^{k+1}-\sum\limits_{k=0}^\infty a_kx^k&=0 \\
\color{red}{\scriptsize{[\triangle {\text{ Diving out } x^r]}}} \\
\sum \limits_{n=-1}^\infty (n+r+1)(n+r)a_{n+1}x^n+2\sum \limits_{n=-1}^\infty (n+r+1)a_{n+1}x^n+\sum \limits_{n=1}^\infty a_{n-1}x^n&=0 \\
\color{red}{\scriptsize{[\triangle { \text{ Substituting } k \text{ with }n \text{ (change limits)}}]}} \\
r(r-1)a_0x^{-1}+r(r+1)a_1x^0+\sum \limits_{n=1}^\infty (n+r+1)(n+r)a_{n+1}x^n&+\\
ra_0x^{-1}+(r+1)a_1x^0+\sum \limits_{n=1}^\infty (n+r+1)a_{n+1}x^n-2ra_0x^0&-\\
2\sum \limits_{n=1}^\infty (n+r)a_{n}x^n+\sum\limits_{n=1}^\infty a_{n-1}x^n-a_0x^0-\sum\limits_{n=1}^\infty a_nx^n&=0\\
\end{aligned}$$

For $$a_0$$, $$[(r^2-r)+r]a_0=0$$.

Collecting the non-summation terms,

$$\begin{aligned}
([(r^2+r)+(r+1)]a_1+(-2r-1)a_0)&=0\\
(r^2+2r+1)a_1-(2r+1)a_0&=0 \triangleright \text{will be used to find }a_0, a_1 \text{(Eq 1)}
\end{aligned}$$

Since $$a_0\neq0\Rightarrow r^2=0\Rightarrow r_1=0, r_2=0$$

The recurrence relation is then,

$$\begin{aligned}
([(n+r)(n+r+1)+(n+r+1)]a_{n+1}+a_{n-1}-[2(n+r)+1]a_n)&=0\\
([(n+r+1)(n+r+1)]a_{n+1}+a_{n-1}-[2(n+r+1)a_n])&=0\\
a_{n+1}=\frac{[2(n+r)+1]a_n-a_{n-1}}{(n+r+1)^2}, n=1,2,3... &
\end{aligned}$$

For $$r=0$$, 

$$\begin{aligned}
a_{n+1}&=\frac{(2n+1)a_n-a_{n-1}}{(n+1)^2}, n=1,2,3,... \\ \\
&\text{From Eq(1)}, (0+2(0)+1)a_1-(2(0)+1)a_0=0 \Rightarrow a_1=a_0\\\\
n&=1, a_2=\frac{3a_1-a_0}{2^2}=\frac{3a_0-a_0}{2^2}=\frac{a_0}{2}\\
n&=2, a_3=-\frac{5a_2-a_1}{3^2}=\frac{5(\frac{a_0}{2})-a_1}{3^2}=\frac{a_0}{3!}\\
n&=3, a_4=\frac{7a_3-a_2}{4^2}=\frac{7(\frac{a_0}{3!})-\frac{a_0}{2}}{4^2}=\frac{a_0}{4!}\\
\\
y_1(x)&=\sum\limits_{k=0}^\infty a_kx^{k+r}=a_0x^0+a_1x^1+... \\
y_1(x)&=a_0+a_0x+\frac{a_0}{2!}x^2+\frac{a_0}{3!}x^3<u>...\\
y_1(x)&=a_0(1+x+\frac{1}{2!}x^2+\frac{1}{3!}x^4+...)\\
\boldsymbol{y_1(x)}&=\boldsymbol{a_0e^x}
\end{aligned}$$

For the second $$r=0$$, using reduction of order.

Knowing $$y_1=e^x$$,

$$\begin{aligned}
y_2&=ve^x\\
y_2'&=ve^x+v'e^x\\
y_2''&=ve^x+2v'e^x+v''e^x
\end{aligned}$$

Substituting into main equation,
$$\begin{aligned}
x(v+2v'+v'')+(1-2x)(ve^x+v'e^x)+(x-1)ve^x&=0\\
x(v+2v'+v'')+(1-2x)(v+v')+(x-1)v&=0 \\
\color{red}{\scriptsize{\triangle[\text{ Dividing out }e^x]}}\\
xv+2xv'+xv''+v-2xv'+v'-2xv+xv-v&=0\\
v'+xv''&=0\\
xv''&=-v'\\
\frac{v''}{v'}&=-\frac{1}{x}\\
\int\frac{v''}{v'}dv&=-\int\frac{1}{x}dx\\
\ln v'&=-\ln x=\ln x^{-1}\\
v'&=x^{-1}\\
\int v' dv&=\int \frac{1}{x}dx\\
v&=\ln x
\end{aligned}$$

$$\therefore \boldsymbol{y_2(x)=(\ln x)e^x}$$

---

#### <u>Question (4)</u>

$$x=0$$ is a regular singular solution.
Assuming the solution is $$y=\sum \limits_{k=0}^\infty a_kx^{k+r}$$.

$$\begin{aligned}
y&=\sum \limits_{k=0}^\infty a_kx^{k+r}\\
y'&=\sum \limits_{k=0}^\infty (k+r)a_kx^{k+r-1}\\
y''&=\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kx^{k+r-2}
\end{aligned}$$

Substituting back yields,

$$\begin{aligned}
2t\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kt^{k+r-2}+(1-t)\sum \limits_{k=0}^\infty (k+r)a_kt^{k+r-1}&+\\
\sum \limits_{k=0}^\infty a_kt^{k+r}&=0\\
2\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kt^{k+r-1}+\sum \limits_{k=0}^\infty (k+r) a_k t^{k+r-1}&+\\
\sum \limits_{k=0}^\infty (k+r)a_kt^{k+r}+\sum \limits_{k=0}^\infty a_kt^{k+r}&=0 \\
\color{red}{\scriptsize{[\triangle { \text{ Removing the } t \text{ from the first term]}}}}\\
2\sum \limits_{k=0}^\infty (k+r)(k+r-1)a_kt^{k-1}+\sum\limits_{k=0}^\infty (k+r)a_kt^{k-1}&+\\
\sum \limits_{k=0}^\infty (k+r)a_kt^{k}+\sum \limits_{k=0}^\infty a_kt^{k}&=0 \\
\color{red}{\scriptsize{[\triangle {\text{ Diving out } t^r]}}} \\
2\sum \limits_{n=-1}^\infty (n+r+1)(n+r)a_{n+1}t^n+\sum \limits_{n=-1}^\infty (n+r+1)a_{n+1}t^n&+\\
\sum \limits_{n=0}^\infty (n+r)a_{n}t^n+\sum\limits_{n=0}^\infty a_nt^n&=0 \\
\color{red}{\scriptsize{[\triangle { \text{ Substituting } k \text{ with }n \text{ (change limits)}}]}} \\
2r(r-1)a_0t^{-1}+2\sum \limits_{n=0}^\infty (n+r+1)(n+r)a_{n+1}t^n&+\\
ra_0t^{-1}+\sum \limits_{n=0}^\infty (n+r+1)a_{n+1}t^n+\sum \limits_{n=0}^\infty (n+r)a_{n}t^n+\sum\limits_{n=0}^\infty a_{n}t^n&=0\\
\end{aligned}$$

For $$a_0$$, $$[2(r^2-r)+r]a_0=0$$.


Since $$a_0\neq0\Rightarrow 2r^2-r=0\Rightarrow r_1=\frac{1}{2}, r_2=0$$

The recurrence relation is then,

$$\begin{aligned}
[2(n+r)(n+r+1)+(n+r+1)]a_{n+1}+[(n+r)+1]a_n&=0\\
(n+r+1)(2n+2r+1)a_{n+1}&=-[(n+r)+1]a_n\\
a_{n+1}&=\frac{-[(n+r)+1]a_n}
{(n+r+1)(2n+2r+1)}, n=0,1,2,...
\end{aligned}$$

For $$r=-\frac{1}{2}$$, 

$$\begin{aligned}
a_{n+1}&=\frac{a_n}{2n+2}, n=0,1,2,3,... \\ \\
n&=0, a_1=-\frac{a_0}{2}\\
n&=1, a_2=-\frac{a_1}{2\cdot2}=\frac{a_0}{2^2\cdot 2!}\\
n&=2, a_3=-\frac{a_2}{2\cdot3}=-\frac{a_0}{2^3\cdot3!}\\
n&=3, a_4=-\frac{a_3}{2\cdot4}=\frac{a_0}{2^4\cdot4!}\\
\\
y_1(t)&=\sum\limits_{k=0}^\infty a_kt^{k+r}=a_0t^{\frac{1}{2}}+a_1t^{\frac{3}{2}}+... \\
y_1(t)&=a_0t^{\frac{1}{2}}-\frac{a_0}{2!}t^{\frac{3}{2}}+\frac{a_0}{2^2\cdot2!}t^{\frac{5}{2}}-\frac{a_0}{2^3\cdot3!}t^{\frac{7}{2}}+...\\
\boldsymbol{y_1(t)}&=\boldsymbol{a_0t^{\frac{1}{2}} \left(1-\frac{1}{2!}t+\frac{1}{2^2\cdot2!}t^2-\frac{1}{2^3\cdot3!}t^3+... \right)}
\end{aligned}$$

For $$r=0$$, 

$$\begin{aligned}
a_{n+1}&=-\frac{a_n}{2n+1}, n=0,1,2,3,... \\ \\
n&=0, a_1=-a_0\\
n&=1, a_2=-\frac{a_1}{3}=\frac{a_0}{3}\\
n&=2, a_3=-\frac{a_2}{5}=-\frac{a_0}{5\cdot3}\\
n&=3, a_4=-\frac{a_3}{7}=\frac{a_0}{7\cdot5\cdot3}\\
\\
y_2(t)&=\sum\limits_{k=0}^\infty a_kt^{k+r}=a_0+a_1t+a_2t^2+a_3t^3+... \\
y_2(t)&=a_0-a_0t+\frac{a_0}{3}t^2-\frac{a_0}{5\cdot3}t^3+...\\
\boldsymbol{y_2(t)}&=\boldsymbol{a_0\left(1-t+\frac{1}{3}t^2-\frac{1}{5\cdot3}t^3+\frac{1}{7\cdot5\cdot3}t^4-... \right)}
\end{aligned}$$

---

#### <u>Question (5) </u>


The motivation behind Frobenius method is to seek a power series solution to ordinary differential equations.

Let $$y(x) = \displaystyle \sum_{n=0}^{\infty} a_n x^n$$. 

Then we get that 

$$y'(x) = \sum_{n=0}^{\infty} na_n x^{n-1}$$

$$3xy'(x) = \sum_{n=0}^{\infty} 3na_n x^{n}$$

$$y''(x) = \sum_{n=0}^{\infty} n(n-1)a_n x^{n-2}$$

$$xy''(x) = \sum_{n=0}^{\infty} n(n-1)a_n x^{n-1} = \sum_{n=0}^{\infty} n(n+1)a_{n+1} x^{n}$$

$$x^2y''(x) = \sum_{n=0}^{\infty} n(n-1)a_n x^{n}$$

The ODE is $$xy'' - x^2 y'' -3xy' - y = 0$$

Plugging in the appropriate series expansions, we get that

$$\sum_{n=0}^{\infty} \left(n(n+1)a_{n+1} - n(n-1)a_n - 3na_n - a_n\right)x^n = 0$$

Hence, we get that

$$n(n+1)a_{n+1} = (n(n-1) +3n+1)a_n = (n+1)^2 a_n \implies a_{n+1} = \dfrac{n+1}{n}a_n$$

First note that $$a_0 = 0$$. Choose $$a_1$$ arbitrarily. Then we get that $$a_2 = 2a_1$$, $$a_3 = 3a_1$$, $$a_4 = 4a_1$$ and in general, $$a_{n} = na_1$$.

Hence, the solution is given by
$$y_1(x) = a_1 \left(x+2x^2 + 3x^3 + \cdots\right)$$

This power series is valid only within $$\vert x \vert <1$$. In this region, we can simplify the power series to get

$$\begin{aligned}
y_1(x) & = a_1 x \left(1 + 2x + 3x^2 + \cdots \right)\\
& = a_1 x \dfrac{d}{dx} \left(x + x^2 + x^3 + \cdots \right)\\
& = a_1 x \dfrac{d}{dx} \left(\dfrac{x}{1-x}\right)\\
& = a_1 \dfrac{x}{(1-x)^2}
\end{aligned}$$

Taking $$a_1=1$$, $$\boldsymbol{y_1(x)=\frac{x}{(1-x)^2}}$$.

The order reduction method seeks a second basis solution in the form $$y=y_1u$$, where $$y_1(x)=\frac{x}{(1-x)^2}$$ is the already found basis solution. 

$$
x(1-x)[y_1u''+2y_1'u']-3x[y_1u']=0  
\implies \frac{u''}{u'}=\frac{3y_1-2(1-x)y_1'}{(1-x)y_1}
$$

Insert 

$$y_1(x)=\dfrac1{(1-x)^2}-\dfrac1{1-x}$$, 

$$y_1'=\dfrac2{(1-x)^3}-\dfrac1{(1-x)^2}$$, 

$$y_1''=\dfrac{6}{(1-x)^4}-\dfrac{2}{(1-x)^3}$$ 

into that formula to find

$$
\begin{aligned}
\frac{u''}{u'}&=\frac{-\frac1{(1-x)^2}-\frac1{1-x}}{\frac{x}{1-x}}=-\frac{2-x}{x(1-x)}=-\frac{2}x+\frac1{1-x}
\\
\implies u'&=\frac1{x^2(1-x)}=\frac{1+x}{x^2}-\frac1{1-x}
\\
\implies  u&=-\frac1x+\ln|x(1-x)|
\end{aligned}$$

So that the second basis solution is

$$
\boldsymbol{y_2=\frac{x\ln|x(1-x)|-1}{(1-x)^2}}
$$

