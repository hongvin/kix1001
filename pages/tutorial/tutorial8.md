---
layout: default
parent: Tutorial
title:  "Tutorial 8"
nav_order: 8
mathjax: true
permalink: /tutorial8
---

# Tutorial 8: Integration

---
[Tutorial PDF]({{ site.url }}/pdf/tutorial/tutorial8.pdf){: .btn .btn-purple }

[Class Recording](https://drive.google.com/file/d/1WxopwnRqvYD0K82Trp6NzwkMtJZ6-5Cx/view?usp=sharing){: .btn .btn-outline }

---

## Q1: Find $$ \int \ln\left( x^{2} +2\right) dx$$.

---
### Solution

Let $$u=\ln\left( x^{2} +2\right)$$, $$dv=dx$$


| $$\begin{aligned} u & =\ln\left( x^{2} +2\right)\\ du & =\frac{2x}{x^{2} +2} dx \end{aligned}$$ | $$\begin{aligned} dv & =dx\\ v & =x \end{aligned}$$ <br />So,<br />$$\begin{aligned}\int \ln\left( x^{2} +2\right) dx & =x\ln\left( x^{2} +2\right) -2\int \frac{x^{2}}{x^{2} +2} dx\\& =x\ln\left( x^{2} +2\right) -2\int \left( 1-\frac{2}{x^{2} +2}\right) dx\\& =x\ln\left( x^{2} +2\right) -2x+\frac{4}{\sqrt{2}}\tan^{-1}\left(\frac{x}{\sqrt{2}}\right) +C\\& =\mathbf{x\left(\ln\left( x^{2} +2\right) -2\right) +2\sqrt{2}\tan^{-1}\left(\frac{x}{\sqrt{2}}\right) +C}\end{aligned}$$ |

---

## Q2: Find $$\int x^{2}\ln x\ dx$$.

---
### Solution

Let $$u=\ln x$$, $$dv=x^{2} \ dx$$


| $$\begin{aligned} u & =\ln x\\ du & =\frac{dx}{x} \end{aligned}$$ | $$\begin{aligned} dv & =dx\\ v & =\frac{x^{3}}{3} \end{aligned}$$ |
        
So,

$$\begin{aligned}
\int x^{2}\ln x\ dx & =\frac{x^{3}}{3}\ln x-\int \frac{x^{3}}{3}\frac{dx}{x}\\
 & =\frac{x^{3}}{3}\ln x-\frac{1}{3}\int x^{2} dx\\
 & =\mathbf{\frac{x^{3}}{3}\ln x-\frac{1}{9} x^{3} +C}
\end{aligned}$$

---

## Q3: Find $$\int x^{3} e^{x^{2}} dx$$.

---
### Solution

Let $$u=x^{2}$$ and $$dv=xe^{x^{2}} dx$$.

| $$\begin{aligned} u & =x^{2}\\ du & =2x\ dx \end{aligned}$$ | $$dv =xe^{x^{2}}$$ <br />Let $$w=x^{2} \Longrightarrow \frac{dw}{dx} =2x\equiv dx=\frac{dw}{2x}$$ <br />$$\begin{aligned} v & =\int xe^{x^{2}} dx\\ & =\int xe^{w}\frac{dw}{2x}\\ & =\frac{1}{2}\int e^{w} dw\\ & =\frac{1}{2} e^{w}\\ & =\frac{1}{2} e^{x^{2}} \end{aligned}$$ |

So,

$$\begin{aligned}
\int x^{3} e^{x^{2}} \ dx & =\frac{1}{2} x^{2} e^{x^{2}} -\int xe^{x^{2}} dx\\
 & =\frac{1}{2} x^{2} e^{x^{2}} -\frac{1}{2} e^{x^{2}} +C\\
 & =\mathbf{\frac{1}{2} e^{x^{2}}\left( x^{2} -1\right) +C}
\end{aligned}$$

---

## Q4: Find $$\int \frac{( x+1)}{x^{3} +x^{2} -6x} dx$$.

---
### Solution


Factoring the denomenator $$x^{3} +x^{2} -6x=x\left( x^{2} +x-6\right) =x( x-2)(x+3)$$. 

The integrand is now $$\frac{( x+1)}{x(x-2)(x+3)}$$.

Representing the integrand such that:

$$\frac{( x+1)}{x( x-2)( x+3)} =\frac{A}{x} +\frac{B}{x-2} +\frac{C}{x+3} \tag{1}$$

Multiplying equation (1) with $$x( x-2)( x+3)$$,

$$x+1=A( x-2)( x+3) +Bx( x+3) +Cx( x-2)$$


Let $$x=0$$ in (2),   $$1=A( -2)( 3) +B( 0)( 3) +C( 0)( -2) \ \Rightarrow \ 1=-6A$$.   So, $$A=-\frac{1}{6}$$.

Let $$x=2$$ in (2),   $$3=A( 0)( 5) +B( 2)( 5) +C( 2)( 0) \ \ \Rightarrow \ 3=10B$$.   So, $$B=\frac{3}{10}$$.

Let $$x=-3$$ in (2),   $$-2=A( -5)( 0) +B( -3)( 0) +C( -3)( -5) \ \Rightarrow \ -2=15C$$.    So, $$C=-\frac{2}{15}$$.

Therefore,

$$\begin{aligned}
\int \frac{( x+1)}{x^{3} +x^{2} -6x} \ dx & =\int \left( -\frac{1}{6}\frac{1}{x} +\frac{3}{10}\frac{1}{x-2} -\frac{2}{15}\frac{1}{x+3}\right) \ dx\\
 & =\mathbf{-\frac{1}{6}\ln |x|\ +\frac{3}{10}\ln |x-2|-\frac{2}{15}\ln |x+3|\ +C}
\end{aligned}$$

---

## Q5: Find $$\int \frac{x^{3} +x^{2} +x+2}{x^{4} +3x^{2} +2} dx$$.

---
### Solution

Factoring the denomenator $$x^{4} +3x^{2} +2=\left( x^{2} +1\right)\left( x^{2} +2\right)$$. 

The integrand is now $$\frac{x^{3} +x^{2} +x+2}{\left( x^{2} +1\right)\left( x^{2} +2\right)}$$.



Representing the integrand such that:

$$\frac{x^{3} +x^{2} +x+2}{\left( x^{2} +1\right)\left( x^{2} +2\right)} =\frac{Ax+B}{x^{2} +1} +\frac{Cx+D}{x^{2} +2} \tag{1}$$


Multiplying equation (1) with $$\left( x^{2} +1\right)\left( x^{2} +2\right)$$,

$$\begin{aligned}
x^{3} +x^{2} +x+2 & =( Ax+B)\left( x^{2} +2\right) +( Cx+D)\left( x^{2} +1\right)\\
 & =Ax^{3} +2Ax+Bx^{2} +2B+Cx^{3} +Cx+Dx^{2} +D\\
 & =( A+C) x^{3} +( B+D) x^{2} +( 2A+C) x+( 2B+D)
\end{aligned} \tag{2}$$

Comparing LHS and RHS of equation (2),

$$\begin{aligned}
A+C & =1\\
B+D & =1\\
2A+C & =1\\
2B+D & =2
\end{aligned}$$

Solving equation (3) simultaneously to obtain $$A=0$$, $$B=1$$, $$C=1$$, $$D=0$$

Therefore,

$$\begin{aligned}
\int \frac{x^{3} +x^{2} +x+2}{\left( x^{2} +1\right)\left( x^{2} +2\right)} dx & =\int \left(\frac{1}{x^{2} +1} +\frac{x}{x^{2} +2}\right) dx\\
 & =\mathbf{\tan^{-1} x+\frac{1}{2}\ln\left( x^{2} +2\right) +C}
\end{aligned}$$

---

## Q6: Find $$\int \tan^{3}( 3x) \ \sec^{4}( 3x) \ dx$$.

---
### Solution

$$\begin{aligned}
\int \tan^{3}( 3x) \ \sec^{4}( 3x) \ dx & =\int \tan^{3}( 3x) \ \left( 1+\tan^{2}( 3x)\right)\sec^{2}( 3x) \ dx\\
 & =\int \tan^{3}( 3x)\sec^{2}( 3x) \ dx+\int \tan^{5}( 3x)\sec^{2}( 3x) \ dx\\
 & =\frac{1}{3}\frac{1}{4}\tan^{4}( 3x) +\frac{1}{3}\frac{1}{6}\tan^{6}( 3x) +C\\
 & =\mathbf{\frac{1}{12}\tan^{4}( 3x) +\frac{1}{18}\tan^{6}( 3x) +C}
\end{aligned}$$

---

## Q7: Find $$\int \sin^{4}( x)\cos^{7}( x) \ dx$$.

---
### Solution

Using trigonometry identity, $$\sin^{2} x+\cos^{2} x=1\ \Longrightarrow \ \cos^{2} x=1-\sin^{2} x$$

$$\begin{aligned}
\int \sin^{4}( x)\cos^{7}( x) \ dx & =\int \sin^{4}( x)\cos^{6}( x)\cos( x) \ dx\\
 & =\int \sin^{4}( x)\left( 1-sin^{2}( x)\right)^{3}\cos( x) \ dx
\end{aligned}$$


Let $$u=\sin x$$, $$du=\cos( x) \ dx$$,

$$\begin{aligned}
\int \sin^{4}( x)\cos^{7}( x) \ dx & =\int u^{4}\left( 1-u^{2}\right)^{3} \ \ du\\
 & =\int u^{4}\left( 1-u^{2}\right)\left( 1-u^{2}\right)^{2} du\\
 & =\int u^{4}\left( 1-u^{2}\right)\left( 1-2u^{2} +u^{4}\right) du\\
 & =\int u^{4}\left( 1-2u^{2} +u^{4} -u^{2} +2u^{4} -u^{6}\right) du\\
 & =\int u^{4}\left( 1-3u^{2} +3u^{4} -u^{6}\right) du\\
 & =\int u^{4} -3u^{6} +3u^{8} -u^{10} du\\
 & =\frac{1}{5} u^{5} -\frac{3}{7} u^{7} +\frac{3}{9} u^{9} -\frac{1}{11} u^{11} +C
\end{aligned}$$

Substituting back $$u=\sin x$$,


$$\int \sin^{4}( x)\cos^{7}( x) \ dx=\mathbf{\frac{1}{5}\sin^{5} x-\frac{3}{7}\sin^{7} x+\frac{1}{3}\sin^{9} x-\frac{1}{11}\sin^{11} x+C}$$


---

## Q8: Find $$\int \frac{dx}{x^{2}\sqrt{9-x^{2}}}$$.

---
### Solution

Let $$x=3\sin \theta$$, therefore $$\theta =\sin^{-1}\frac{x}{3}$$. Then, $$dx=3\cos \theta \ d\theta$$, and

$$\begin{aligned}
\sqrt{9-x^{2}} & =\sqrt{9-( 3\sin \theta )^{2}}\\
 & =\sqrt{9-9\sin^{2} \theta }\\
 & =3\sqrt{1-\sin^{2} \theta }\\
 & =3\sqrt{\cos^{2} \theta }\\
 & =3\cos \theta 
\end{aligned}$$

Using defination of inverse sine, $$-\frac{\pi }{2} < \theta < \frac{\pi }{2}$$. Therefore, $$\cos \theta  >0$$. 

Thus, $$\cos \theta =\vert \cos \theta \vert =\frac{\sqrt{9-x^{2}}}{3}$$.


Hence,

$$\begin{aligned}
\int \frac{dx}{x^{2}\sqrt{9-x^{2}}} \  & =\int \frac{3\cos \theta \ d\theta }{9\sin^{2} \theta ( 3\cos \theta )}\\
 & =\frac{1}{9}\int \csc^{2} \theta \ d\theta \\
 & =-\frac{1}{9}\cot \theta +C\\
 & =-\frac{1}{9}\frac{\cos \theta }{\sin \theta } +C\\
 & =-\frac{1}{9}\frac{\frac{\sqrt{9-x^{2}}}{3}}{\frac{x}{3}} +C\\
 & =\mathbf{-\frac{1}{9}\frac{\sqrt{9-x^{2}}}{x} +C}
\end{aligned}$$