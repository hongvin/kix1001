---
layout: default
parent: Tutorial
title:  "Tutorial 3"
nav_order: 3
mathjax: true
permalink: /tutorial3
---

# Tutorial 3: Partial Derivatives & Engineering Applications of Partial Derivatives

---
[Tutorial PDF]({{ site.url }}/pdf/tutorial/tutorial3.pdf){: .btn .btn-purple }
[Solution PDF]({{ site.url }}/pdf/solution/tutorial3.pdf){: .btn .btn-green }

[Class Recording](https://drive.google.com/file/d/1o14hb12aRSKYOLGxTzHV7-FyKZ8cXd2l/view?usp=sharing){: .btn .btn-outline }
[Class Whiteboard]({{ site.url }}/pdf/whiteboard/tutorial3.png){: .btn .btn-outline }

---

## Q1: Find the partial derivatives $$(\frac{\partial f}{\partial y})$$ and $$(\frac{\partial f}{\partial x})$$ of these functions using the limit definition.

(a) $$f(x,y)=x^2-4xy+y^2$$ 
(b) $$f(x,y)=2x^3+3xy-y^2$$ 

---
### Solution 
#### <u>Question (a)</u>

$$\begin{aligned}
\frac{\partial f}{\partial x}&= \lim_{h \rightarrow 0} \frac{f(x+h,y)-f(x,y)}{h} \\
&= \lim_{h \rightarrow 0} \frac{(x+h)^2-4(x+h)y+y^2-(x^2-4xy+y^2)}{h} \\
&= \lim_{h \rightarrow 0} \frac{x^2+2xh+h^2-4xy-4hy+y^2-(x^2-4xy+y^2)}{h} \\
&= \lim_{h \rightarrow 0} \frac{2xh+h^2-4hy}{h} \\
&= \lim_{h \rightarrow 0} (2x+h-4y) \\
&= \boldsymbol{2x-4y}
\end{aligned}$$

$$\begin{aligned}
\frac{\partial f}{\partial y}&= \lim_{h \rightarrow 0} \frac{f(x,y+h)-f(x,y)}{h} \\
&= \lim_{h \rightarrow 0} \frac{x^2-4x(y+h)+(y+h)^2-(x^2-4xy+y^2)}{h} \\
&= \lim_{h \rightarrow 0} \frac{x^2-4xy-4xh+y^2+2yh+h^2-(x^2-4xy+y^2)}{h} \\
&= \lim_{h \rightarrow 0} \frac{-4xh+2yh+h^2}{h} \\
&= \lim_{h \rightarrow 0} (-4x+2y+h) \\
&= \boldsymbol{-4x+2y}
\end{aligned}$$

#### <u>Question (b)</u>

$$\begin{aligned}
\frac{\partial f}{\partial x} &= \lim_{h \rightarrow 0} \frac{f(x+h,y)-f(x,y)}{h} \\
&= \lim_{h \rightarrow 0} \frac{h(6x^2+6xh+2h^2+3y)}{h} \\
&= \lim_{h \rightarrow 0} (6x^2+6xh+2h^2+3y) \\
&= \boldsymbol{6x^2+3y}
\end{aligned}$$

$$\begin{aligned}
\frac{\partial f}{\partial y} &= \lim_{h \rightarrow 0} \frac{f(x,y+h)-f(x,y)}{h} \\
&= \lim_{h \rightarrow 0} \frac{h(3x-2y-h)}{h} \\
&= \lim_{h \rightarrow 0} (3x-2y-h) \\
&= \boldsymbol{3x-2y}
\end{aligned}$$

---
## Q2: Determine all the first and second order partial derivatives of the function

(a) $$f(x,y) = x^2y^3+3y+x$$

(b) $$f(x,y) = y\sin{x} + x\cos{y}$$

(c) $$f(x,y) = x^4 \sin {3y}$$

(d) $$f(x,y) = e^{xy} (2x - y)$$

(e) $$f(x,y,z) = z^2e^{xy} + x\cos{(y^2z)}$$

---

### Solution

#### <u>Question (a)</u>

$$\begin{aligned}
\frac{\partial f}{\partial x}&= \boldsymbol{2xy^3+1} \\
\frac{\partial f}{\partial y}&= \boldsymbol{3x^2y^2+3} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{2y^3} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{6xy^2} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{6xy^2} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{6x^2y} \\
\end{aligned}$$


#### <u>Question (b)</u>

$$\begin{aligned}
\frac{\partial f}{\partial x}&= \boldsymbol{y\cos{x}+\cos{y}} \\
\frac{\partial f}{\partial y}&= \boldsymbol{\sin{x}-x\sin{y}} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{-y\sin{x}} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{\cos{x}-\sin{y}} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{\cos{x}-\sin{y}} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{-x\cos{y}} \\
\end{aligned}$$


#### <u>Question (c)</u>

$$\begin{aligned}
\frac{\partial f}{\partial x}&= \boldsymbol{4x^3\sin{3y}} \\
\frac{\partial f}{\partial y}&= \boldsymbol{3x^4\cos{3y}} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{12x^2\sin{3y}} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{12x^3\cos{3y}} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{12x^3\cos{3y}} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{-9x^4\sin{3y}} \\
\end{aligned}$$

#### <u>Question (d)</u>

$$\begin{aligned}
\frac{\partial f}{\partial x}&= \boldsymbol{e^{xy}(2xy-y^2+2)} \\
\frac{\partial f}{\partial y}&= \boldsymbol{e^{xy}(2x^2-xy-1)} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{e^{xy}(2xy^2-y^3+4y)} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{e^{xy}(2x^3y-xy^2+4x-2y)} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{e^{xy}(2x^2y-xy^2+4x-2y)} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{e^{xy}(2x^3-x^2y-2x)} \\
\end{aligned}$$

#### <u>Question (e)</u>

$$\begin{aligned}
\frac{\partial f}{\partial x}&= \boldsymbol{yz^2e^{xy}+\cos{(y^2z)}} \\
\frac{\partial f}{\partial y}&= \boldsymbol{xz^2e^{xy}-2xyz\sin{(y^2z)}} \\
\frac{\partial f}{\partial z}&= \boldsymbol{2ze^{xy}-xy^2\sin{(y^2z)}} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{y^2z^2e^{xy}} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{x^2z^2e^{xy}-2xz\sin{(y^2z)-4xy^2z^2\cos{(y^2z)}}} \\
\frac{\partial}{\partial z}\left(\frac{\partial f}{\partial z}\right)&= \boldsymbol{2e^{xy}-xy^4\cos{(y^2z)}} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial y}\right)&=\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial x}\right)= \boldsymbol{z^{2} e^{xy} +z^{2} xye^{xy} -2yz\sin\left( y^{2} z\right)} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial z}\right)&= \frac{\partial}{\partial z}\left(\frac{\partial f}{\partial y}\right) = \boldsymbol{2xze^{xy}-2xy\sin{(y^2z)}-2xy^3z\cos{(y^2z)}} \\
\frac{\partial}{\partial z}\left(\frac{\partial f}{\partial x}\right)&= \frac{\partial}{\partial x}\left(\frac{\partial f}{\partial z}\right) = \boldsymbol{2yze^{xy}-y^2\sin{(y^2z)}} \\
\end{aligned}$$

---
## Q3: Find both partial derivatives for each of the following two variables functions.

(a) $$f(x,y) = \log{x} + 3y + 1$$

(b) $$f(x,y) = ye^{x+y}$$

(c) $$h(x,y) = x\sin{y}-y\cos{x}$$

(d) $$p(x,y) = x^y+y^2$$

(e) $$U(x,y) = \frac{9y^3}{x-y}$$

---
### Solution
#### <u>Question (a)</u>

$$\begin{aligned}
\frac{df}{dx}&=\boldsymbol{\frac{1}{x}} \\
\frac{df}{dy}&=\boldsymbol{3}
\end{aligned}$$

#### <u>Question (b)</u>

$$\begin{aligned}
\frac{dg}{dx}&=\boldsymbol{ye^{x+y}} \\
\frac{dg}{dy}&=\boldsymbol{e^{x+y}+ye^{x+y}}
\end{aligned}$$

#### <u>Question (c)</u>

$$\begin{aligned}
\frac{dh}{dx}&=\boldsymbol{\sin{y}+y\sin{x}} \\
\frac{dh}{dy}&=\boldsymbol{x\cos{y}-\cos{x}}
\end{aligned}$$

#### <u>Question (d)</u>

$$\begin{aligned}
\frac{dp}{dx}&=\boldsymbol{yx^{y-1}} \\
\frac{dp}{dy}&=\boldsymbol{x^y\ln{x}+2y}
\end{aligned}$$

#### <u>Question (e)</u>

$$\begin{aligned}
\frac{dU}{dx}&=\frac{(x-y)(0)-9y^3(1)}{(x-y)^2}=\boldsymbol{\frac{-9y^3}{(x-y)^2}} \\
\frac{dU}{dy}&=\frac{(x-y)(27y^2)-9y^3(-1)}{(x-y)^2}=\boldsymbol{\frac{27xy^2-18y^3}{(x-y)^2}}
\end{aligned}$$

---

## Q4: Compute the first and second partial derivatives of $$z$$.

$$z=\frac{x}{y^2}+\frac{1}{x^3}+\log{(x+y)}$$

---
### Solution

$$\begin{aligned}
\frac{\partial z}{\partial x}&=\boldsymbol{\frac{1}{y^2}-\frac{3}{x^4}+\frac{1}{x+y}} \\
\frac{\partial z}{\partial y}&=\boldsymbol{\frac{-2x}{y^3}+\frac{1}{x+y}} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{\frac{12}{x^5}+\frac{-1}{(x+y)^2}} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial x}\right)&= \boldsymbol{\frac{-2}{y^3}+\frac{-1}{(x+y)^2}} \\
\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{\frac{-2}{y^3}+\frac{-1}{(x+y)^2}} \\
\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial y}\right)&= \boldsymbol{\frac{6x}{y^4}+\frac{-1}{(x+y)^2}} \\
\end{aligned}$$

---

## Q5: For $$f(x,y,z)$$, use the implicit function theorem to find $$\frac{dy}{dx}$$ and $$\frac{dy}{dz}$$:

(a) $$f(x,y,z) = x^2y^3+z^2+xyz$$

(b) $$f(x,y,z) = x^3z^2+y^3+4xyz$$

(c) $$f(x,y,z) = 3x^2y^3+xz^2y^2+y^3zx^4+y^2z$$

---
### Solution

#### <u>Question (a)</u>

$$\begin{aligned}
\frac{dy}{dx}&=-\frac{fx}{fy}=\boldsymbol{-\frac{2xy^3+yz}{3x^2y^2+xz}} \\
\frac{dy}{dz}&=-\frac{fz}{fy}=\boldsymbol{-\frac{2z+xy}{3x^2y^2+xz}} \\
\end{aligned}$$

#### <u>Question (b)</u>

$$\begin{aligned}
\frac{dy}{dx}&=-\frac{fx}{fy}=\boldsymbol{-\frac{3x^2z^2+4yz}{3y^2+4xz}} \\
\frac{dy}{dz}&=-\frac{fz}{fy}=\boldsymbol{-\frac{2x^3z+4xy}{3y^2+4xz}} \\
\end{aligned}$$

#### <u>Question (c)</u>

$$\begin{aligned}
\frac{dy}{dx}&=-\frac{fx}{fy}=\boldsymbol{-\frac{6xy^3+y^2z^2+4x^3y^3z}{9x^2y^2+2xyz^2+3x^4y^2z+2yz}} \\
\frac{dy}{dz}&=-\frac{fz}{fy}=\boldsymbol{-\frac{2xy^2z+x^4y^3+y^2}{9x^2y^2+2xyz^2+3x^4y^2z+2yz}} \\
\end{aligned}$$

---
## Q6: Find $$\frac{\partial F}{\partial s}$$ and $$\frac{\partial F}{\partial t}$$,if applicable, for the following composite functions.

(a) $$F = \sin (x + y)$$ where $$x = 2st$$ and $$y = s^2 + t^2$$.

(b) $$F = e^x\cos y$$ where $$x = s^2 - t^2$$ and $$y = 2st$$. 

(c) $$F = 5x - 3y^2 + 7z^3$$ where $$x = 2s + 3t$$, $$y = s - t$$ and $$z = 4s + t$$.

(d) $$F = \ln (x^2 + y)$$ where $$x = \exp (s+t^2)$$ and $$y = s^2 + t$$.

(e) $$F = x^2y^2$$ where $$x = s \cos t$$ and $$y = s \sin t$$.

(f) $$F = xy + yz^2$$ where $$x = e^t$$, $$y = e^t \sin t$$ and $$z = e^t \cos t$$.

---
### Solution:

#### <u>Question (a)</u>

$$\begin{aligned}
\frac{\partial F}{\partial s}&=\frac{\partial F}{\partial x}\frac{\partial x}{\partial s}+\frac{\partial F}{\partial y} \frac{\partial y}{\partial s} \\
&=\cos (x+y)(2t)+\cos (x+y)(2s) \\
&=2t\cos (2st+s^2+t^2)+2s\cos (st+s^2+t^2) \\
&= \boldsymbol{2\cos ((s+t)^2)(s+t)}
\end{aligned}$$

$$\begin{aligned}
\frac{\partial F}{\partial t}&=\frac{\partial F}{\partial x}\frac{\partial x}{\partial t}+\frac{\partial F}{\partial y} \frac{\partial y}{\partial t} \\
&=\cos (x+y)(2s)+\cos (x+y)(2t) \\
&= \boldsymbol{2\cos ((s+t)^2)(s+t)}
\end{aligned}$$

#### <u>Question (b)</u>

$$\begin{aligned}
\frac{\partial F}{\partial s}&=\frac{\partial F}{\partial x}\frac{\partial x}{\partial s}+\frac{\partial F}{\partial y} \frac{\partial y}{\partial s} \\
&=e^x\cos{y}(2s)+(-\sin y)e^x(2t) \\
&= 2se^x\cos y-2te^x\sin y \\
&= \boldsymbol{2se^{s^2-t^2}\cos 2st-2te^{s^2-t^2}\sin 2st}
\end{aligned}$$

$$\begin{aligned}
\frac{\partial F}{\partial t}&=\frac{\partial F}{\partial x}\frac{\partial x}{\partial t}+\frac{\partial F}{\partial y} \frac{\partial y}{\partial t} \\
&=e^x\cos{y}(2t)+(-\sin y)e^x(2s) \\
&= 2te^x\cos y-2se^x\sin y \\
&= \boldsymbol{-2te^{s^2-t^2}\cos 2st-2se^{s^2-t^2}\sin 2st}
\end{aligned}$$

#### <u>Question (c)</u>

$$\begin{aligned}
\frac{\partial F}{\partial s}&=\frac{\partial F}{\partial x}\frac{\partial x}{\partial s}+\frac{\partial F}{\partial y} \frac{\partial y}{\partial s}+\frac{\partial F}{\partial z} \frac{\partial z}{\partial s} \\
&=5(2)+(-6y)(1)+21z^2(4)\\
&=10-6y+84z^2\\
&=10-6(s-t)+84(4s+t)^2\\
&=10-6s+6t+84(16s^2+8st+t^2)\\
&= \boldsymbol{10-6s-6t+1344s^2+672st+84t^2}
\end{aligned}$$

$$\begin{aligned}
\frac{\partial F}{\partial t}&=\frac{\partial F}{\partial x}\frac{\partial x}{\partial t}+\frac{\partial F}{\partial y} \frac{\partial y}{\partial t}+\frac{\partial F}{\partial z} \frac{\partial z}{\partial t} \\
&=5(3)-6y(-1)+21z^2(1) \\
&=15+6y+21z^2\\
&=15+6(s-t)+21(4s-t)^2\\
&=15+6s-6t+21(16s^2+8st+t^2)\\
&= \boldsymbol{15+6s-6t+336s^2+168st+21t^2}
\end{aligned}$$

#### <u>Question (d)</u>

$$\begin{aligned}
\frac{\partial F}{\partial s} & =\frac{\partial F}{\partial x}\frac{\partial x}{\partial s} +\frac{\partial F}{\partial y}\frac{\partial y}{\partial s}\\
 & =\frac{2x}{x^{2} +y} e^{s+t^{2}} +\frac{1}{x^{2} +y} 2s\\
 & =\mathbf{\frac{2}{x^{2} +y}\left( xe^{s+t^{2}} +s\right)}
\end{aligned}$$

$$\begin{aligned}
\frac{\partial F}{\partial t} & =\frac{\partial F}{\partial x}\frac{\partial x}{\partial t} +\frac{\partial F}{\partial y}\frac{\partial y}{\partial t}\\
 & =\frac{2x}{x^{2} +y} 2te^{s+t^{2}} +\frac{1}{x^{2} +y}( 1)\\
 & =\mathbf{\frac{1}{x^{2} +y}\left( 4xte^{s+t^{2}} +1\right)}
\end{aligned}$$

#### <u>Question (e)</u>


$$\begin{aligned}
\frac{\partial F}{\partial s} & =\frac{\partial F}{\partial x}\frac{\partial x}{\partial s} +\frac{\partial F}{\partial y}\frac{\partial y}{\partial s}\\
 & =2xy^{2}\cos t+2x^{2} y\sin t\\
 & =2( s\cos t)\left( s^{2}\sin^{2} t\right)(\cos t) +2\left( s^{2}\cos^{2} t\right)( s\sin t)(\sin t)\\
 & =2s^{3}\cos^{2} t\sin^{2} t+2s^{3}\cos^{2} t\sin^{2} t\\
 & =4s^{3}\cos^{2} t\sin^{2} t\\
 & =4s^{3}(\cos t\sin t)^{2}\\
 & =4s^{3}\left(\frac{1}{2}\sin 2t\right)^{2}\\
 & =\mathbf{s^{3}(\sin 2t)^{2}}
\end{aligned}$$

$$\begin{aligned}
\frac{\partial F}{\partial t} & =\frac{\partial F}{\partial x}\frac{\partial x}{\partial t} +\frac{\partial F}{\partial y}\frac{\partial y}{\partial t}\\
 & =2xy^{2}( -s\sin t) +2x^{2} y( s\cos t)\\
 & =2x^{2} ys\cos t-2xy^{2} s\sin t\\
 & =2\left( s^{2}\cos^{2} t\right)( s\sin t) s\cos t-2( s\cos t)\left( s^{2}\sin^{2} t\right) s\sin t\\
 & =2s^{4}\cos^{3} t\sin t-2s^{4}\cos t\sin^{3} t\\
 & =2s^{4}(\cos t\sin t)\left(\cos^{2} t-\sin^{2} t\right)\\
 & =2s^{4}\left(\frac{1}{2}\sin 2t\right)(\cos 2t)\\
 & =\mathbf{s^{4}\sin 2t\cos 2t}
\end{aligned}$$

#### <u>Question (f)</u>

$$\begin{aligned}
\frac{dF}{dt} & =\frac{\partial F}{\partial x}\frac{\partial x}{\partial t} +\frac{\partial F}{\partial y}\frac{\partial y}{\partial t} +\frac{\partial F}{\partial z}\frac{\partial z}{\partial t}\\
 & =ye^{t} +\left( x+z^{2}\right)\left( e^{t}\cos t+\sin^{t} e^{t}\right) +2yz\left( -e^{t}\sin t+\cos te^{t}\right)\\
 & =ye^{t} +xe^{t}\cos t+x\sin^{t} e^{t} +z^{2} e^{t}\cos t+z^{2}\sin te^{t} -2yze^{t}\sin t+2yz\cos te^{t}\\
 & =ye^{t} +e^{t}\cos t\left( x+z^{2} +2yz\right) +e^{t}\sin t\left( x+z^{2} -2yz\right)\\
 & =e^{t}\sin t\cdot e^{t} +e^{t}\cos t\left( e^{t} +e^{2t}\cos t+2e^{2t}\sin t\cos t\right)\\
 & \ \ \ \ \ +e^{t}\sin t\left( e^{t} +e^{2t}\cos^{2} t-2e^{2t}\sin t\cos t\right)\\
 & =e^{2t}\sin t+e^{2t}\cos t+e^{3t}\cos^{3} t+2e^{2t}\sin t\cos^{2} t+e^{2t}\sin t+e^{3t}\sin t\cos^{2} t\\
 & \ \ \ \ \ -2e^{3} t\sin^{2} t\cos t\\
 & =2e^{2t}\sin t+e^{2t}\cos t+e^{3t}\cos^{3} t+3e^{3t}\sin t\cos^{2} t-2e^{3t}\sin^{2} t\cos t\\
 & =\mathbf{e^{2t}( 2\sin t+\cos t) +e^{3t}\left(\cos^{3} t+3\sin t\cos^{2} t-2\sin^{2} t\cos t\right)}
\end{aligned}$$

---

## Q7: Find $$\frac{dy}{dx}$$ and $$\frac{dy}{dz}$$ (if applicable) for each of the following.

(a) $$y^{x} +1=0$$

(b) $$7x^{2} +2xy^{2} +9y^{4} =0$$

(c) $$x^{3} z^{2} +y^{3} +4xyz=0$$

(d) $$3x^{2} y^{3} +xz^{2} y^{2} +y^{3} zx^{4} +y^{2} z=0$$

(e) $$y^{5} +x^{2} y^{3} =1+y\exp\left( x^{2}\right)$$

---
### Solution

#### <u> Question (a) </u>

$$\begin{aligned}
\frac{dy}{dx} & =-\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial y}} =-\frac{-y^{x}\ln y}{xy^{x-1}} =\mathbf{-\frac{y}{x}\ln y}
\end{aligned}$$

Let $$z=y^{x} \Longrightarrow \ln z=x\ln y$$,

$$\begin{aligned}
\frac{1}{z}\frac{dy}{dx} & =\ln y\\
\frac{dy}{dx} & =z\ln y\\
 & =\mathbf{y^{2}\ln y}
\end{aligned}$$

#### <u> Question (b) </u>

$$\begin{aligned}
\frac{dy}{dx} & =-\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial y}} =\mathbf{-\frac{14x+2y^{2}}{36y^{2} +4xy}}
\end{aligned}$$

#### <u> Question (c) </u>

$$\begin{aligned}
\frac{dy}{dx} & =-\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial y}} =\mathbf{-\frac{3x^{2} z^{2} +4yz}{3y^{2} +4xz}}\\
\frac{dy}{dz} & =-\frac{\frac{\partial F}{\partial z}}{\frac{\partial F}{\partial y}} =\mathbf{-\frac{2x^{3} z+4xy}{3y^{2} +4xz}}
\end{aligned}$$

#### <u> Question (d) </u>

$$\begin{aligned}
\frac{dy}{dx} & =-\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial y}} =\mathbf{-\frac{6xy^{3} +z^{2} y^{2} +4y^{3} zx^{3}}{9x^{2} y^{2} +2xz^{2} y+3y^{2} zx^{4} +2yz}}\\
\frac{dy}{dz} & =-\frac{\frac{\partial F}{\partial z}}{\frac{\partial F}{\partial y}} =\mathbf{-\frac{2xzy^{2} +y^{3} x^{4} +y^{2}}{9x^{2} y^{2} +2xz^{2} y+3y^{z} x^{4} +2yz}}
\end{aligned}$$

#### <u> Question (e) </u>

$$\begin{aligned}
\frac{dy}{dx} & =-\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial y}} =\mathbf{-\frac{2xy\left( y^{2} -e^{x^{2}}\right)}{5y^{4} +3x^{2} y^{2} -e^{x^{2}}}}
\end{aligned}$$

---

## Q8: (a) Show that the variables $$x$$ and $$y$$ given by $$x=\frac{s+t}{s}$$, $$y=\frac{s+t}{t}$$ are functionally dependent.

##    (b) Obtain the Jacobian $$J$$ of the transformation $$s=2x+y$$, $$t=x-2y$$ and determine the inverse of the transformation $$J_{1}$$. Confirm that $$J_{1} =J^{-1}$$.

##    (c) Show that if $$x+y=u$$ and $$y=uv$$, then $$\frac{\partial ( x,y)}{\partial ( u,v)} =u$$.

##    (d) Verify whether the functions $$u=\frac{x+y}{1-xy}$$ and $$v=\tan^{-1} x+\tan^{-1} y$$ are functionally dependent.

##    (e) If $$x=uv$$, $$y=\frac{u+v}{u-v}$$, find $$\frac{\partial ( u,v)}{\partial ( x,y)}$$.

---

### Solution

#### <u> Question (a) </u>

$$\begin{aligned}
J & =\frac{\partial ( x,y)}{\partial ( s,t)}\\
 & =\left| \begin{matrix}
-\frac{t}{s^{2}} & \frac{1}{t}\\
\frac{1}{s} & -\frac{s}{t^{2}}
\end{matrix}\right| \\
 & =\frac{1}{st} -\frac{1}{st} =0\Longrightarrow \text{Functionally dependent}
\end{aligned}$$

#### <u> Question (b) </u>

$$\begin{aligned}
J & =\frac{\partial ( s,t)}{\partial ( x,y)}\\
 & =\left| \begin{matrix}
2 & 1\\
1 & -2
\end{matrix}\right| \\
 & =-5
\end{aligned}$$

$$ \begin{array}{l}
x=\frac{1}{5}( 2s+t) \quad \quad y=\frac{1}{5}( s-2t)\\
\\
\begin{aligned}
J_{1} & =\frac{\partial ( x,y)}{\partial ( s,t)}\\
 & =\left| \begin{matrix}
\frac{2}{5} & \frac{1}{5}\\
\frac{1}{5} & -\frac{2}{5}
\end{matrix}\right| \\
 & =-\frac{1}{5}
\end{aligned}
\end{array}$$

$$\therefore J_{1} =J^{-1}$$

#### <u> Question (c) </u>

$$ \begin{array}{l}
x+uv=u\Longrightarrow x=u-uv\\
\frac{dx}{du} =1-v\\
\frac{dx}{dv} =-1
\end{array}$$

$$\begin{array}{l}
y=uv\\
\frac{dy}{du} =v\\
\frac{dy}{dv} =u
\end{array}$$

$$\begin{aligned}
\frac{\partial ( x,y)}{\partial ( u,v)} & =\left| \begin{matrix}
\frac{\partial x}{\partial u} & \frac{\partial y}{\partial u}\\
\frac{\partial x}{\partial v} & \frac{\partial y}{\partial v}
\end{matrix}\right| \\
 & =\left| \begin{matrix}
1-v & v\\
-u & u
\end{matrix}\right| \\
 & =u-uv+uv\\
 & =u\ 
\end{aligned}$$

#### <u> Question (d) </u>

$$\begin{aligned}
\frac{\partial ( u,v)}{\partial ( x,y)} & =\left| \begin{matrix}
\frac{\partial u}{\partial x} & \frac{\partial u}{\partial y}\\
\frac{\partial v}{\partial x} & \frac{\partial v}{\partial y}
\end{matrix}\right| =\left| \begin{matrix}
\frac{1+y^{2}}{( 1-xy)^{2}} & \frac{1+x^{2}}{( 1-xy)^{2}}\\
\frac{1}{1+x^{2}} & \frac{1}{1+y^{2}}
\end{matrix}\right| \\
 & =\frac{1}{( 1-xy)^{2}} -\frac{1}{( 1-xy)^{2}}\\
 & =0
\end{aligned}$$

#### <u> Question (e) </u>

$$\begin{aligned}
\frac{\partial ( x,y)}{\partial ( u,v)} & =\left| \begin{matrix}
\frac{\partial x}{\partial u} & \frac{\partial y}{\partial u}\\
\frac{\partial x}{\partial v} & \frac{\partial y}{\partial v}
\end{matrix}\right| =\left| \begin{matrix}
v & u\\
-\frac{2v}{( u-v)^{2}} & -\frac{2u}{( u-v)^{2}}
\end{matrix}\right| \\
 & =\frac{2uv}{( u-v)^{2}} +\frac{2uv}{( u-v)^{2}}\\
 & =\frac{4uv}{( u-v)^{2}}\\
\mathbf{\frac{\partial ( u,v)}{\partial ( x,y)}} & \mathbf{=\frac{( u-v)^{2}}{4uv}}
\end{aligned}$$

---

# Total Differential

## Q1: Compute the total differential of $$f( x,y,z) =\ln\left(\frac{xy^{2}}{z^{3}}\right)$$.

---
### Solution

$$dF=\frac{1}{x} dx+\frac{2}{y} dy-\frac{3}{2} dz$$

---

## Q2: The period $$T$$ of a simple pendulum is $$T=2\pi \sqrt{\frac{l}{g}}$$, find the maximum percentage error in $$T$$ due to possible errors up to 1% in $$l$$ and 2% in $$g$$. (Hint: $$\frac{dl}{l} =0.001$$ and $$\frac{dg}{g} =0.002$$)

---
### Solution

$$\begin{aligned}
\log T & =\log 2\pi +\frac{1}{2}\log l-\frac{1}{2}\log g\\
\frac{dT}{T} & =0+\frac{1}{2l} dl-\frac{1}{2g} dg\\
 & =\left(\frac{1}{2}\right)\left(\frac{dl}{l}\right) -\left(\frac{1}{2}\right)\left(\frac{dg}{g}\right)\\
 & =\left(\frac{1}{2}\right)( 0.001) \pm \left(\frac{1}{2}\right)( 0.002)\\
 & =0.0005\pm 0.001
\end{aligned}$$

$$\therefore Max\ error\ =\ 1.5\%$$

---

## Q3: Compute an approximate value of $$( 1.04)^{3.01}$$.

---
### Solution

Let $$f( x,y) =x^{y}$$.

$$\frac{\partial f}{\partial x} =yx^{y-1} \quad \quad \frac{\partial f}{\partial y} =x^{y}\log x$$

$$x=1,\ dx=0.04\quad \quad y=3,\ dy=0.01$$

$$\begin{aligned}
df & =\frac{\partial f}{\partial x} dx+\frac{\partial f}{\partial y} dy\\
 & =yx^{y-1} \ dx+x^{y}\log x\ dy\ \\
 & =3( 1)^{3-1}( 0.004) +1^{3}\log( 1) \ ( 0.01)\\
 & =0.12
\end{aligned}$$

$$\begin{aligned}
( 1.04)^{3.01} & =f( 1,3) +df\\
 & =1+0.12\\
 & =\mathbf{1.12}
\end{aligned}$$

---

## Q4: Suppose one is given a triangle where the angle at one vertex is $$\theta$$ and the lengths of the two sides adjacent to that vertex are $$b$$ and $$c$$. Then the well-known formula for the area of the triangle as 

$$\text{Area} =S=\frac{1}{2} bc\sin \theta $$

## Suppose we measure:

$$\begin{aligned}
b & =4.00\ m\ \pm \ 0.005\ m\\
c & =3.00\ m\ \pm \ 0.005\ m\\
\theta  & =\frac{\pi }{6} \ \pm \ 0.01\ radians
\end{aligned}$$

## Find $$S$$ and estimate the percentage error.

---
### Solution


Area, $$S=\frac{1}{2}( 4)( 3)\sin\left(\frac{\pi }{6}\right) =3$$

$$\begin{aligned}
\frac{\partial S}{\partial b} & =\frac{1}{2} c\sin \theta \\
\frac{\partial S}{\partial c} & =\frac{1}{2} b\sin \theta \\
\frac{\partial S}{\partial \theta } & =\frac{1}{2} bc\cos \theta 
\end{aligned}$$

The error estimate,

$$\begin{aligned}
\text{Max Error} & \leqslant \left| \frac{\partial S}{\partial b} db\right| +\left| \frac{\partial S}{\partial c} dc\right| +\left| \frac{\partial S}{\partial \theta } d\theta \right| \\
 & =\left(\frac{1}{2} \times 3\times \frac{1}{2}\right) \times 0.005+\left(\frac{1}{2} \times 4\times \frac{1}{2}\right) \times 0.005+\left(\frac{1}{2} \times 4\times 3\times \frac{\sqrt{3}}{2}\right) \times 0.01\\
 & =0.06
\end{aligned}$$


The relative error is at most $$\frac{0.06}{3} =0.02$$.

$$\Longrightarrow \text{Percentage Error} =2\%$$.

---

# Tangent planes and normal to surfaces in three dimensions

## Find the equations of the tangent plane and normal line to the following surfaces at the points indicated:

## Q1: $$x^{2} +2y^{2} +3z^{2} =6$$ at $$(1,1,1)$$.

---
### Solution

Partial derivation yields: 

$$\frac{\partial f}{\partial x} =2x\quad \quad \frac{\partial f}{\partial y} =4y\quad \quad \frac{\partial f}{\partial z} =6z$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{( 1,1,1)} =2\quad \quad \frac{\partial f}{\partial y}_{( 1,1,1)} =4\quad \quad \frac{\partial f}{\partial z}_{( 1,1,1)} =6$$

Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
2( x-1) +4( y-1) +6( z-1) & =0\\
2x-2+4y-4+6z-6 & =0\\
\mathbf{x+2y+3z} & \mathbf{=6}
\end{aligned}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\frac{x-1}{2} & =\frac{y-1}{4} =\frac{z-1}{6}\\
\mathbf{\frac{x-1}{1}} & \mathbf{=\frac{y-1}{2} =\frac{z-1}{3}}
\end{aligned}$$

---

## Q2: $$2x^{2} +y^{2} -z^{2} =-3$$ at $$(1,2,3)$$.

---
### Solution


Partial derivation yields: 

$$\frac{\partial f}{\partial x} =4x\quad \quad \frac{\partial f}{\partial y} =2y\quad \quad \frac{\partial f}{\partial z} =-2z$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{( 1,2,3)} =4\quad \quad \frac{\partial f}{\partial y}_{( 1,2,3)} =4\quad \quad \frac{\partial f}{\partial z}_{( 1,2,3)} =-6$$

Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
4( x-1) +4( y-2) -6( z-3) & =0\\
4x-4+4y-8-6z+18 & =0\\
4x+4y-6z & =-6\\
2\mathbf{x+2y-3z} & \mathbf{=-3}
\end{aligned}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\frac{x-1}{4} & =\frac{y-2}{4} =\frac{z-3}{-6}\\
\mathbf{\frac{x-1}{2}} & \mathbf{=\frac{y-2}{2} =\frac{z-3}{-3}}
\end{aligned}$$

---

## Q3: $$x^{2} +y^{2} -z=1$$ at $$(1,2,4)$$.

---
### Solution


Partial derivation yields: 

$$\frac{\partial f}{\partial x} =2x\quad \quad \frac{\partial f}{\partial y} =2y\quad \quad \frac{\partial f}{\partial z} =-1$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{( 1,2,4)} =2\quad \quad \frac{\partial f}{\partial y}_{( 1,2,4)} =4\quad \quad \frac{\partial f}{\partial z}_{( 1,2,4)} =-1$$

Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
2( x-1) +4( y-2) -1( z-4) & =0\\
2x-2+4y-8-z+4 & =0\\
\mathbf{2x+4y-z} & \mathbf{=6}
\end{aligned}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\mathbf{\frac{x-1}{2}} & \mathbf{=\frac{y-2}{4} =\frac{z-4}{-1}}
\end{aligned}$$

---

## Q4: $$\ln\left(\frac{x}{y}\right) -z^{2}( x-2y) -3z=3$$ at $$(4,2,-1)$$.

---
### Solution

Partial derivation yields: 


$$\frac{\partial f}{\partial x} =\frac{1}{x} -z^{2} \quad \quad \frac{\partial f}{\partial y} =2z^{2} -\frac{1}{y} \quad \quad \frac{\partial f}{\partial z} =-2z( x-2y) -3$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{( 4,2,-1)} =-\frac{3}{4} \quad \quad \frac{\partial f}{\partial y}_{( 4,2,-1)} =\frac{3}{2} \quad \quad \frac{\partial f}{\partial z}_{( 4,2,-1)} =-3$$

Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
-\frac{3}{4}( x-4) +\frac{3}{2}( y-2) -3( z+1) & =0\\
-\frac{3}{4} x+3+\frac{3}{2} y-3-3z-3 & =0\\
\mathbf{-\frac{3}{4} x+\frac{3}{2} y-3z} & \mathbf{=3}
\end{aligned}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\mathbf{\frac{x-4}{-\frac{3}{4}}} & \mathbf{=\frac{y-2}{\frac{3}{2}} =\frac{z+1}{-3}}
\end{aligned}$$

---

## Q5: $$x^{3} z+z^{3} x-2yz=0$$ at $$(1,1,1)$$.

---
### Solution


Partial derivation yields: 

$$\frac{\partial f}{\partial x} =3x^{2} z+z^{3} \quad \quad \frac{\partial f}{\partial y} =-2z\quad \quad \frac{\partial f}{\partial z} =x^{3} +3z^{2} x-2y$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{( 1,1,1)} =4\quad \quad \frac{\partial f}{\partial y}_{( 1,1,1)} =-2\quad \quad \frac{\partial f}{\partial z}_{( 1,1,1)} =2$$

Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
4( x-1) -2( y-1) +2( z-1) & =0\\
4x-4-2y+2+2z-2 & =0\\
4x-2y+2z & =4\\
\mathbf{2x-y+z} & \mathbf{=2}
\end{aligned}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\frac{x-1}{4} & =\frac{y-1}{-2} =\frac{z-1}{2}\\
\mathbf{\frac{x-1}{2}} & \mathbf{=\frac{y-1}{-1} =\frac{z-1}{1}}
\end{aligned}$$

---

## Q6: $$z=5+( x-1)^{2} +( y+2)^{2}$$ at $$(2,0,10)$$.

---
### Solution

$$z=5+( x-1)^{2} +( y+2)^{2} \Longrightarrow ( x-1)^{2} +( y+2)^{2} -z=5$$

Partial derivation yields: 

$$\frac{\partial f}{\partial x} =2( x-1) \quad \quad \frac{\partial f}{\partial y} =2( y+2) \quad \quad \frac{\partial f}{\partial z} =-1$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{( 2,0,10)} =2\quad \quad \frac{\partial f}{\partial y}_{( 2,0,10)} =4\quad \quad \frac{\partial f}{\partial z}_{( 2,0,10)} =-1$$
        
Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
2( x-2) +4( y) -( z-10) & =0\\
2x-4+4y-z+10 & =0\\
\mathbf{2x+4y-z} & \mathbf{=-6}
\end{aligned}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\mathbf{\frac{x-2}{2}} & \mathbf{=\frac{y}{4} =\frac{z-10}{-1}}
\end{aligned}$$

---

## Q7: $$\frac{x^{2}}{12} +\frac{y^{2}}{6} +\frac{z^{2}}{4} =1$$ at $$(1,2,1)$$.

---
### Solution

Partial derivation yields: 

$$\frac{\partial f}{\partial x} =\frac{x}{6} \quad \quad \frac{\partial f}{\partial y} =\frac{y}{3} \quad \quad \frac{\partial f}{\partial z} =\frac{z}{2}$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{( 1,2,1)} =\frac{1}{6} \quad \quad \frac{\partial f}{\partial y}_{( 1,2,1)} =\frac{2}{3} \quad \quad \frac{\partial f}{\partial z}_{( 1,2,1)} =\frac{1}{2}$$

Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
\frac{1}{6}( x-1) +\frac{2}{3}( y-2) +\frac{1}{2}( z-1) & =0\\
\frac{1}{6} x-\frac{1}{6} +\frac{2}{3} y-\frac{4}{3} +\frac{1}{2} z-\frac{1}{2} & =0\\
\frac{1}{6} x+\frac{4}{6} y+\frac{3}{6} z-\frac{1}{6} -\frac{8}{6} -\frac{3}{6} & =0\\
\frac{1}{6} x+\frac{4}{6} y+\frac{3}{6} z-2 & =0\\
\mathbf{x+4y+3z} & \mathbf{=12}
\end{aligned}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\frac{x-1}{\frac{1}{6}} & =\frac{y-2}{\frac{2}{3}} =\frac{z-1}{\frac{1}{2}}\\
\frac{x-1}{\frac{1}{6}} & =\frac{y-2}{\frac{4}{6}} =\frac{z-1}{\frac{3}{6}}\\
\mathbf{\frac{x-1}{1}} & \mathbf{=\frac{y-2}{4} =\frac{z-1}{3}}
\end{aligned}$$

---

## Q8: $$ze^{x} +e^{z+1} +xy+y=3$$ at $$(0,3,-1)$$.

---
### Solution

Partial derivation yields: 

$$\frac{\partial f}{\partial x} =ze^{x} +y\quad \quad \frac{\partial f}{\partial y} =x+1\quad \quad \frac{\partial f}{\partial z} =e^{x} +e^{z+1}$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{( 0,3,-1)} =2\quad \quad \frac{\partial f}{\partial y}_{( 0,3,-1)} =1\quad \quad \frac{\partial f}{\partial z}_{( 0,3,-1)} =2$$

Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
2( x) +( y-3) +2( z+1) & =0\\
2x+y-3+2z+2 & =0\\
\mathbf{2x+y+2z} & \mathbf{=1}
\end{aligned}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\mathbf{\frac{x}{2}} & \mathbf{=\frac{y-3}{1} =\frac{z+1}{2}}
\end{aligned}$$

---

## Q9: $$z^{2} =7-x^{2} -2y^{2}$$ at $$(1,1,2)$$.

---
### Solution


$$z^{2} =7-x^{2} -2y^{2} \Longrightarrow x^{2} +2y^{2} +z^{2} =7$$

Partial derivation yields: 


$$\frac{\partial f}{\partial x} =2x\quad \quad \frac{\partial f}{\partial y} =4y\quad \quad \frac{\partial f}{\partial z} =2z$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{( 1,1,2)} =2\quad \quad \frac{\partial f}{\partial y}_{( 1,1,2)} =4\quad \quad \frac{\partial f}{\partial z}_{( 1,1,2)} =4$$

Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
2( x-1) +4( y-1) +4( z-2) & =0\\
2x-2+4y-4+4z-8 & =0\\
2x+4y+4z-14 & =0\\
\mathbf{x+2y+2z} & \mathbf{=7}
\end{aligned}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\frac{x-1}{2} & =\frac{y-1}{4} =\frac{z-2}{4}\\
\mathbf{\frac{x-1}{1}} & \mathbf{=\frac{y-1}{2} =\frac{z-2}{2}}
\end{aligned}$$

---

## Q10: $$z=\frac{x^{2}}{2p} +\frac{y^{2}}{2q}$$ at the point $$\left( 2p^{2} ,2q^{2} ,2p^{3} +2q^{3}\right)$$.

---
### Solution


$$z=\frac{x^{2}}{2p} +\frac{y^{2}}{2q} \Longrightarrow \frac{x^{2}}{2p} +\frac{y^{2}}{2q} -z=0$$

Partial derivation yields: 

$$\frac{\partial f}{\partial x} =\frac{x}{p} \quad \quad \frac{\partial f}{\partial y} =\frac{y}{q} \quad \quad \frac{\partial f}{\partial z} =-1$$

$$\Longrightarrow \ \frac{\partial f}{\partial x}_{\left( 2p^{2} ,2q^{2} ,2p^{3} +2q^{3}\right)} =2p\quad \quad \frac{\partial f}{\partial y}_{\left( 2p^{2} ,2q^{2} ,2p^{3} +2q^{3}\right)} =2q\quad \quad \frac{\partial f}{\partial z}_{\left( 2p^{2} ,2q^{2} ,2p^{3} +2q^{3}\right)} =-1$$
        
Tangent plane:

$$\begin{aligned}
( x-x_{o})\left(\frac{\partial f}{\partial x}\right)_{0} +( y-y_{0})\left(\frac{\partial f}{\partial y}\right)_{0} +( z-z_{0})\left(\frac{\partial f}{\partial z}\right)_{0} & =0\\
2p\left( x-2p^{2}\right) +2q\left( y-2q^{2}\right) -1\left( z-\left( 2p^{3} +2q^{3}\right)\right) & =0\\
2px-4p^{3} +2qy-4q^{3} -z+2p^{3} +2q^{3} & =0\\
2px+2qy-z-2p^{3} -2q^{3} & =0
\end{aligned}\\
\\
\mathbf{\begin{aligned}
z & =2px+2qy-2p^{3} -2q^{3}
\end{aligned}}$$

Normal line:

$$\begin{aligned}
\frac{x-x_{0}}{\left(\frac{\partial f}{\partial x}\right)_{0}} & =\frac{y-y_{0}}{\left(\frac{\partial f}{\partial y}\right)_{0}} =\frac{z-z_{0}}{\left(\frac{\partial f}{\partial z}\right)_{0}}\\
\mathbf{\frac{x-2p^{2}}{2p}} & \mathbf{=\frac{y-2q^{2}}{2q} =\frac{z-2p^{3} -2q^{3}}{-1}}
\end{aligned}$$