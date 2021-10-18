---
layout: default
parent: Tutorial
title:  "Tutorial 1"
nav_order: 1
mathjax: true
permalink: /tutorial1
---

# Tutorial 1: Basic Functions & Derivatives

---
[Tutorial PDF]({{ site.url }}/pdf/tutorial/tutorial1.pdf){: .btn .btn-purple }
[Solution PDF]({{ site.url }}/pdf/solution/tutorial1.pdf){: .btn .btn-green }

[Solving using MATLAB]({{ site.url }}/matlab1){: .btn .btn-outline }
[Solving using Python]({{ site.url }}/python1){: .btn .btn-outline }
[Solving using Mathematica]({{ site.url }}/mathematica1){: .btn .btn-outline }

---

## Q1: Find the limit of $$\lim _{x \rightarrow 5} \frac{x^{2}-25}{x^{2}+x-30}$$.
---

### Solution

$$\require{cancel}
\begin{aligned}
\lim _{x \rightarrow 5} \frac{x^{2}-25}{x^{2}+x-30}
&= \lim _{x \rightarrow 5} \frac{\cancel{(x-5)}(x+5)}{\cancel{(x-5)}(x+6)} \\
&= \lim _{x \rightarrow 5} \frac{x+5}{x+6} \\
&= \frac{5+5}{5+6} \\
&= \mathbf{\frac{10}{11}}
\end{aligned}$$



---

## Q2: Find the limit of $$\lim _{x \rightarrow 9} \frac{\sqrt{x}-3}{x-9}$$.
---

### Solution

$$\begin{aligned}
\lim _{x \rightarrow 9} \frac{\sqrt{x}-3}{x-9} 
&= \lim _{x \rightarrow 9} \frac{\sqrt{x}-3}{x-9}\times\frac{\sqrt{x}+3}{\sqrt{x}+3} \\
&= \lim _{x \rightarrow 9} \frac{\cancel{x-9}}{\cancel{(x-9)}(\sqrt{x}+3)} \\
&= \lim _{x \rightarrow 9} \frac{1}{(\sqrt{x}+3)} \\
&= \frac{1}{\sqrt{9}+3} \\
&= \mathbf{\frac{1}{6}}
\end{aligned}$$

---

## Q3: Find the limit of $$\lim _{x \rightarrow 0} \frac{\sqrt{2+x}-\sqrt{2}}{x}$$.
---

### Solution

$$\begin{aligned}
\lim _{x \rightarrow 0} \frac{\sqrt{2+x}-\sqrt{2}}{x} 
&= \lim _{x \rightarrow 0} \frac{\sqrt{2+x}-\sqrt{2}}{x} \times \frac{\sqrt{2+x}+\sqrt{2}}{\sqrt{2+x}+\sqrt{2}} \\
&= \lim _{x \rightarrow 0} \frac{(\sqrt{2+x})^2-(\sqrt{2})^2}{x(\sqrt{2+x}+\sqrt{2})} \\
&= \lim _{x \rightarrow 0} \frac{2+x-2}{x(\sqrt{2+x}+\sqrt{2})} \\
&= \lim _{x \rightarrow 0} \frac{\cancel{x}}{\cancel{x}(\sqrt{2+x}+\sqrt{2})} \\
&= \frac{1}{\sqrt{2}+\sqrt{2}} \\
&= \frac{1}{2\sqrt{2}}\times\frac{\sqrt{2}}{\sqrt{2}} \\
&= \mathbf{\frac{\sqrt{2}}{4}}
\end{aligned}$$

---

## Q4: Find the limit of $$\lim _{\theta \rightarrow \frac{\pi}{2}} \frac{\tan{\theta}}{\sec{\theta}}$$.
---

### Solution

$$\begin{aligned}
\lim _{\theta \rightarrow \frac{\pi}{2}} \frac{\tan{\theta}}{\sec{\theta}} 
&= \lim _{\theta \rightarrow \frac{\pi}{2}} \frac{(\frac{\sin{\theta}}{\cancel{\cos{\theta}}})}{(\frac{1}{\cancel{\cos{\theta}}})} \\
&= \lim _{\theta \rightarrow \frac{\pi}{2}} \sin{\theta} \\
&= \sin{\frac{\pi}{2}} \\
&= \mathbf{1}
\end{aligned}$$

---

## Q5: Find the limit of $$\lim _{\theta \rightarrow 0} \frac{\cos{\theta}-1}{\sin{\theta}}$$.
---

### Solution

$$\begin{aligned}
\lim _{\theta \rightarrow 0} \frac{\cos{\theta}-1}{\sin{\theta}}
&= \lim _{\theta \rightarrow 0} \frac{\cos{\theta}-1}{\sin{\theta}} \times \frac{\theta}{\theta} \\
&= \lim _{\theta \rightarrow 0} \frac{\cos{\theta}-1}{\theta} \times \frac{\theta}{\sin{\theta}} \\
&= \lim _{\theta \rightarrow 0} \frac{\cos{\theta}-1}{\theta} \times \lim _{\theta \rightarrow 0} \frac{\theta}{\sin{\theta}} \\
&= \lim _{\theta \rightarrow 0} \frac{\cos{\theta}-1}{\theta} \times \frac{1}{\lim _{\theta \rightarrow 0} \frac{\sin{\theta}}{\theta}} \\
&= 0\times1 \\
&= \mathbf{0}
\end{aligned}$$

---

## Q6: If $$2x\leq g(x)\leq x^2-x+2$$ for all $$x$$, evaluate  $$\lim_{x \rightarrow 1} g(x)$$.
---

### Solution

$$\lim_{x \rightarrow 1} 2x \leq \lim_{x \rightarrow 1} g(x) \leq \lim_{x \rightarrow 1} (x^2-x+2)$$

Therefore,

$$2\leq\lim_{x \rightarrow 1} g(x) \leq 2$$

Hence,

$$\lim_{x \rightarrow 1} g(x) = \mathbf{2}$$

---

## Q7: Solve $$y'$$ if $$y=\sqrt{3x^2-2x+3}$$.
---

### Solution

Let $$u=3x^2-2x+3$$, therefore $$\frac{du}{dx}=6x-2$$.

Substitute $$y=\sqrt{u}=u^{\frac{1}{2}}$$, therefore $$\frac{dy}{du}=\frac{1}{2}u^{-\frac{1}{2}}$$.

Putting back together, 

$$\begin{aligned}
\frac{dy}{dx}
&=\frac{dy}{du}\cdot\frac{du}{dx} \\
&= \frac{1}{2}u^{-\frac{1}{2}} \cdot 6x-2 \\
&= \frac{1}{2}(3x^2-2x+3)^{-\frac{1}{2}} \cdot 6x-2 \\
&= \frac{6x-2}{2\sqrt{3x^2-2x+3}} \\
&= \boldsymbol{\frac{3x-1}{\sqrt{3x^2-2x+3}}}
\end{aligned}$$

---

## Q8: Solve $$y'$$ if $$y=5\sqrt[3]{x^2+\sqrt{x^3}}$$.
---

### Solution

$$y=5\sqrt[3]{x^2+\sqrt{x^3}}$$ can be rewrite as $$y=5(x^2+x^{\frac{3}{2}})^{\frac{1}{3}}$$.

Let $$u=x^2+x^{\frac{3}{2}}$$, therefore $$\frac{du}{dx}=2x+\frac{3}{2}x^{\frac{1}{2}}$$.

Substitute $$y=5u^{\frac{1}{3}}$$, therefore $$\frac{dy}{du}=\frac{5}{3}u^{-\frac{2}{3}}$$.

Putting back together, 

$$\begin{aligned}
\frac{dy}{dx}
&=\frac{dy}{du}\cdot\frac{du}{dx} \\
&= \frac{5}{3}u^{-\frac{2}{3}}\cdot\left(2x+\frac{3}{2}x^{\frac{1}{2}}\right) \\
&= \boldsymbol{\frac{5}{3}\left(x^2+x^{\frac{3}{2}}\right)^{-\frac{2}{3}}\cdot\left(2x+\frac{3}{2}x^{\frac{1}{2}}\right)} \\
\end{aligned}$$

Alternatively, the equation can be written as $$\frac{5\left(2x+\frac{3}{2}\sqrt{x}\right)}{3\left(x^2+\sqrt{x^3}\right)^{\frac{2}{3}}} = \frac{5\left(\frac{2x}{3}+\frac{1}{2}\sqrt{x}\right)}{\left(x^2+\sqrt{x^3}\right)^{\frac{2}{3}}} = \frac{5\left(\frac{2x}{3}+\frac{\sqrt{x^3}}{2x}\right)}{\left(x^2+\sqrt{x^3}\right)^{\frac{2}{3}}}$$ 

---

## Q9: Solve $$y'$$ if $$y=\ln{\cos{x^2}}$$.
---

### Solution

Let $$u=\cos{x^2}$$, therefore $$\frac{du}{dx}=(-\sin{x^2})(2x)$$.

Substitute $$y=\ln{u}$$, therefore $$\frac{dy}{du}=\frac{1}{u}$$.

Putting back together, 

$$\begin{aligned}
\frac{dy}{dx}
&= \frac{dy}{du}\cdot\frac{du}{dx} \\
&= \frac{1}{u}\cdot(-\sin{x^2})(2x) \\
&= -\frac{2x\sin{x^2}}{\cos{x^2}} \\
&= \boldsymbol{-2x\tan{x^2}}
\end{aligned}$$

---

## Q10: Differentiate $$y=\log{(4+\cos{x})}$$.
---

### Solution

Note that $$\frac{d}{dx} (\log_b(x))=\frac{1}{\ln{(b)}\cdot x}=\frac{1}{x}\cdot\log{e}$$

$$\begin{aligned}
\frac{d}{dx}(\log{4+\cos{x}})
&= \frac{1}{4+\cos{x}}\cdot\log{e} \cdot\frac{d}{dx} (4+\cos{x}) \\
&= \frac{1}{4+\cos{x}}\cdot\log{e} \cdot(-\sin{x}) \\
&= \boldsymbol{\frac{-(\log{e})(\sin{x})}{4+\cos{x}}}
\end{aligned}$$

---

## Q11: Find $$y'$$ for $$10e^{2xy}=e^{15y}+e^{13x}$$.
---

### Solution

$$\begin{aligned}
10e^{2xy}&=e^{15y}+e^{13x} \\
10e^{2xy}(2x\cdot y'+2y)&=e^{15y}(15y')+e^{13x}(13) \\
10e^{2xy}(2x\cdot y'+2y)&=15y'e^{15y}+13e^{13x} \\
(20xe^{2xy}-15e^{15y})y'&=13e^{13x}-20ye^{2xy} \\
\boldsymbol{y'}&=\boldsymbol{\frac{13e^{13x}-20ye^{2xy}}{20xe^{2xy}-15e^{15y}}}
\end{aligned}$$

---

## Q12: Find $$f'(x)$$ if $$f(x)=2x(\arctan{5x})^2+6\tan{(\cos{6x})}$$.
---

### Solution

- $$\frac{d}{dx} (\tan^{-1}{5x})^2=2\tan^{-1}{5x}\cdot\frac{1}{1+(5x)^2}\cdot5=\frac{10\tan^{-1}{5x}}{1+25x^2}$$

- $$\frac{d}{dx} 2x(\tan^{-1}{5x})^2=2x(\frac{10\tan^{-1}{5x}}{1+25x^2})+(\tan^{-1}{5x})^2\cdot2=\frac{20x\tan^{-1}{5x}}{1+25x^2}+2(\tan^{-1}{5x})^2$$

- $$\frac{d}{dx} 6\tan{(\cos{6x})}=6\sec^2{(\cos{6x})} \frac{d}{dx}\cos{6x}=6\sec^2{(\cos{6x})}\cdot(-\sin{6x})\cdot6=-36(\sec^2{(\cos{6x})})\sin{6x}$$

$$\begin{aligned}
\therefore f'(x)=\boldsymbol{\frac{20x\tan^{-1}{5x}}{1+25x^2}+2(\tan^{-1}{5x})^2-36(\sec^2{(\cos{6x})})\sin{6x}}
\end{aligned}$$

---

## Q13: Solve $$y'$$ if $$y=4x\sinh^{-1}{(\frac{x}{6})}+\tanh^{-1}{(\cos{10x})}$$.
---

### Solution

- $$\frac{d}{dx} 4x\sinh^{-1}{(\frac{x}{6})}=4x\left[\frac{1}{\sqrt{1+(\frac{x}{6})^2}}\cdot\frac{1}{6}\right]+\sinh^{-1}{(\frac{x}{6})}\cdot4=\frac{\frac{2x}{3}}{\sqrt{1+\frac{x^2}{36}}}+4\sinh^{-1}{(\frac{x}{6})}$$

- $$\frac{d}{dx} \tanh^{-1}{(\cos{10x})}=\frac{1}{1-(\cos{10x})^2}\cdot\frac{d}{dx}\cos{10x}=\frac{1}{1-\cos^2{10x}}\cdot(-10\sin{10x})=\frac{-10\sin{10x}}{\sin^2{10x}}=-10\csc{10x}$$

$$\begin{aligned}
\therefore f'(x)=\boldsymbol{\frac{\frac{2x}{3}}{\sqrt{1+\frac{x^2}{36}}}+4\sinh^{-1}{(\frac{x}{6})}-10\csc{10x}}
\end{aligned}$$

---

## Q14: Differentiate $$y=\frac{1}{\sin^{-1}{x}}$$.
---

### Solution

$$\frac{d}{dx}(\sin^{-1}{x})=\frac{1}{\sqrt{1-x^2}}$$

$$\begin{aligned}
y&=(\sin^{-1}x)^{-1}\\
y'&=-(\sin^{-1}{x})^{-2}\frac{d}{dx}(\sin^{-1}x) \\
&=\boldsymbol{-\frac{1}{(\sin^{-1}x^2)\sqrt{1-x^2}}}
\end{aligned}$$

---

### Q15: Differentiate $$y=(x^3-1)^{100}$$.
---

### Solution

$$\begin{aligned}
y'&=100(x^3-1)^{99}\frac{d}{dx}(x^3-1) \\
&= 100(x^3-1)^{99}\cdot3x^2 \\
&= \boldsymbol{300x^2(x^3-1)^{99}}
\end{aligned}$$
