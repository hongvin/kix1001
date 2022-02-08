---
layout: default
parent: Tutorial
title:  "Tutorial 13"
nav_order: 13
mathjax: true
permalink: /tutorial13
---

# Tutorial 13: Frobenius Method

---
[Tutorial PDF]({{ site.url }}/pdf/tutorial/tutorial13.pdf){: .btn .btn-purple }

---

## Q1: Find the radius of convergence and interval of cinvergence for the given power series.

## (a)  $$\sum _{n=1}^{\infty }\frac{2^{n}}{n} x^{n}$$

## (b)  $$\sum _{n=1}^{\infty }\frac{( -1)^{n}}{4^{n}}( x+3)^{n}$$

## (c)  $$\sum _{n=0}^{\infty }\frac{( 100)^{n}}{n!}( x+7)^{n}$$

## (d)  $$\sum _{n=0}^{\infty } n!( 2x+1)^{n}$$

---
### Solution

#### <u> Question (a) </u>

$$\lim _{n\rightarrow \infty }\left\vert \frac{a_{n} +1}{a_{n}}\right\vert =\lim _{n\rightarrow \infty }\left\vert \frac{2^{n+1} x^{n+1} /( n+1)}{2^{n} x^{n} /n}\right\vert =\lim _{n\rightarrow \infty }\frac{2n}{n+1}\vert x\vert =2\vert x\vert$$

The series is absolutely convergent for $$2\vert x\vert < 1$$ or $$\vert x\vert < \frac{1}{2}$$. At $$x=-\frac{1}{2}$$, the series $$\sum _{n=1}^{\infty }\frac{( -1)^{n}}{n}$$ converges by the alternating series test. At $$x=\frac{1}{2}$$, the series $$\sum _{n=1}^{\infty }\frac{1}{n}$$ is the harmonic series which diverges. Thus, the given series converges on $$\left[ -\frac{1}{2} ,\frac{1}{2}\right]$$.

#### <u> Question (b) </u>

$$\begin{aligned}
L & =\lim _{n\rightarrow \infty }\left\vert \frac{( -1)^{n+1}( n+1)( x+3)^{n+1}}{4^{n+1}}\frac{4^{n}}{( -1)^{n}( n)( x+3)^{n}}\right\vert \\
 & =\lim _{n\rightarrow \infty }\left\vert \frac{-( n+1)( x+3)}{4n}\right\vert \\
 & =\vert x+3\vert \lim _{n\rightarrow \infty }\frac{n+1}{4n}\\
 & =\frac{1}{4}\vert x+3\vert 
\end{aligned}$$

$$\frac{1}{4}\vert x+3\vert < 1\Longrightarrow \vert x+3\vert < 4$$	series converges
$$\frac{1}{4}\vert x+3\vert  >1\Longrightarrow \vert x+3\vert  >4$$	series diverges

The radius of convergence for this power series is $$R=4$$.

$$\begin{aligned}
-4 & < x+3< 4\\
-7 & < x< 1
\end{aligned}$$

#### <u> Question (c) </u>

$$\lim _{n\rightarrow \infty }\left\vert \frac{a_{n+1}}{a_{n}}\right\vert =\lim _{n\rightarrow \infty }\left\vert \frac{100^{n+1}( x+7)^{n+1} /( n+1) !}{100^{n}( x+7)^{n} /n!}\right\vert =\lim _{n\rightarrow \infty }\frac{100}{n+1}\vert x+7\vert =0$$

The series is absolutely convergent on $$( -\infty ,\infty )$$.

#### <u> Question (d) </u>

$$\begin{aligned}
L & =\lim _{n\rightarrow \infty }\left\vert \frac{( n+1) !( 2x+1)^{n+1}}{n!( 2x+1)^{n}}\right\vert \\
 & =\lim _{n\rightarrow \infty }\left\vert \frac{( n+1) n!( 2x+1)}{n!}\right\vert \\
 & =\vert 2x+1\vert \lim _{n\rightarrow \infty }( n+1)
\end{aligned}$$

At this point we need to be careful. Yje limit is infinite, but there is that term with the $$x$$'s in front of the limit. We will have $$L=\infty  >1$$ provided $$x\neq -\frac{1}{2}$$ will only converge if $$x=-\frac{1}{2}$$.

The radius of convergence is $$R=0$$ and the interval of convergence is $$x=-\frac{1}{2}$$.

---

## Q2: Rewrite the given power series by shifting the index, so that its general term involves $$x^{k}$$.

## (a)   $$\sum _{n=3}^{\infty }( 2n-1) c_{n} x^{n-3}$$

## (b)   $$\sum _{n=3}^{\infty }\frac{3^{n}}{( 2n) !} x^{n-3}$$

## (c)   $$\sum _{n=3}^{\infty }\frac{( -1)^{n}}{( 2n+1) !} x^{2n+1}$$

---
### Solution

#### <u> Question (a) </u>

$$\sum _{n=3}^{\infty }( 2n-1) c_{n} x^{n-3} =\sum _{k=0}^{\infty }( 2( k+3) -1) c_{k+3} x^{k} =\mathbf{\sum _{k=0}^{\infty }( 2k+5) c_{k+3} x^{k}}$$

#### <u> Question (b) </u>

$$\sum _{n=3}^{\infty }\frac{3^{n}}{( 2n) !} x^{n-2} =\sum _{k=1}^{\infty }\frac{3^{k+2}}{( 2( k+2)) !} x^{k} =\mathbf{\sum _{k=1}^{\infty }\frac{3^{k+2}}{( 2k+1) !} x^{k}}$$

#### <u> Question (c) </u>

$$\sum _{n=3}^{\infty }\frac{( -1)^{n}}{( 2n+1) !} x^{2n+1} =\sum _{k=7}^{\infty }\frac{( -1)^{\frac{k-1}{2}}}{\left( 2\left(\frac{k-1}{2}\right) +1\right) !} x^{k} =\sum _{k=7}^{\infty }\frac{( -1)^{\frac{k-1}{2}}}{k!} x^{k} =\mathbf{\sum _{k=7}^{\infty }\frac{\sqrt{( -1)^{k-1}}}{k!} x^{k}}$$

---

## Q3: Rewrite the given expression as a single power series whose general term involves $$x^k$$.

## a.   $$\sum _{n=2}^{\infty } n( n-1) C_{n} x^{n} +2\sum _{n=2}^{\infty } n( n-1) c_{n} x^{n-2} +3\sum _{n=1}^{\infty } nc_{n} x^{n}$$

## b.   $$3x^{2}\sum _{n=-2}^{\infty } n( n-1) x^{n-2} +x\sum _{n=1}^{\infty } nx^{n}$$

## c.   $$\sum _{n=1}^{\infty }\frac{3^{n}}{( 2n) !} x^{n-1} +3x^{3}\sum _{n=-1}^{\infty }\frac{( -1)^{n}}{( 2n+1) !} x^{2n+1}$$

---
### Solution

#### <u> Question (a) </u>

$$\begin{align*}
& \sum _{n=2}^{\infty } n( n-1) c_{n} x^{n} +2\sum _{n=2}^{\infty } n( n-1) c_{n} x^{n-2} +3\sum _{n=1}^{\infty } nc_{n} x_{n}\\
&= 2\cdot 2\cdot 1c_{2} x^{0} +2\cdot 3\cdot 2c_{3} x'+3\cdot 1\cdot c_{1} x'+\underbrace{ \sum _{n=2}^{\infty } n( n-1) c_{n}}_{k=n} x^{n}_{k=n} +2\underbrace{ \sum _{n=4}^{\infty } n( n-1) c_{n} x^{n-2}}_{k=n-2} +3\underbrace{ \sum _{n=2}^{\infty } nc_{n} x^{n}}_{k=n}\\
&= 4c_{2} +( 12c_{3} +( 12c_{3} +3c_{1}) x+\sum _{n=2}^{\infty } k( k-1) c_{k} x^{k} +2\sum _{n=2}^{\infty }( k+2)( k+1) x_{k+2} x^{k} +3\sum _{n=2}^{\infty } kc_{k} x^{k}\\
&= 4c_{2} +( 3c_{1} +12c_{3}) x+\sum _{n=2}^{\infty }([ k( k-1) +3k] c_{k} +2( k+2)( k+1) x_{k+2}) x^{k}\\
&= 4c_{2} +( 3c_{1} +12c_{3}) x+\sum _{n=2}^{\infty }[ k( k+2) c_{k} +2( k+1)( k+2) c_{k+2}] x^{k}
\end{align*}$$

#### <u> Question (b) </u>

$$3x^{2}\sum _{n=-2}^{\infty } n( n-1) x^{n-2} +x\sum _{n=1}^{\infty } nx^{n} =3\sum _{n=-2}^{\infty } n( n-1) x^{n} +\sum _{n=1}^{\infty } nx^{n+1} =3\sum _{k=-2}^{\infty } k( k-1) x^{k} +\sum _{k=2}^{\infty }( k-1) x^{k} \tag{1}$$

Solving first part of Eq(1),

$$\begin{aligned}
\sum _{k=-2}^{\infty } k( k-1) x^{k} & =-2( -2-1) x^{-2} +( -1)( -1-1) x^{-1} +0+1( 1-1) x^{1} +\sum _{k=2}^{\infty } k( k-1) x^{k}\\
 & =\frac{6}{x^{2}} +\frac{2}{x} +\sum _{k=2}^{\infty } k( k-1) x^{k}
\end{aligned}$$

Substitute back to Eq (1),

$$\begin{aligned}
\therefore 3\left[\frac{6}{x^{2}} +\frac{2}{x} +\sum _{k=2}^{\infty } k( k-1) x^{k}\right] +\sum _{k=2}^{\infty }( k-1) x^{k} & =\frac{18}{x^{2}} +\frac{6}{x} +\sum _{k=2}^{\infty }[ 3k( k-1) +( k-1)] x^{k}\\
 & =\frac{18}{x^{2}} +\frac{6}{x} +\sum _{k=2}^{\infty }[( k-1)( 3k+1)] x^{k}
\end{aligned}$$

#### <u> Question (c) </u>

$$\begin{aligned}
\sum _{n=1}^{\infty }\frac{3^{n}}{( 2n) !} x^{n-1} +2x^{3}\sum _{n=-1}^{\infty }\frac{( -1)^{n}}{( 2n+1) !} x^{2n+1} & =\sum _{n=1}^{\infty }\frac{3^{n}}{( 2n) !} x^{n-1} +2\sum _{n=-1}^{\infty }\frac{( -1)^{n}}{( 2n+1) !} x^{2n+4}\\
 & =\sum _{k=0}^{\infty }\frac{3^{k+1}}{( 2( k+1)) !} x^{k} +2\sum _{k=2}^{\infty }\frac{( -1)^{\frac{k-4}{2}}}{\left( 2\left(\frac{k-4}{2}\right) +1\right) !} x^{k}\\
 & =\sum _{k=0}^{\infty }\frac{3^{k+1}}{( 2k+2) !} x^{k} +2\sum _{k=2}^{\infty }\frac{( -1)^{\frac{k-4}{2}}}{( k-3) !} x^{k}
\end{aligned} \tag{2}$$

Solving first part of Eq (2),

$$\begin{aligned}
\sum _{k=0}^{\infty }\frac{3^{k+1}}{( 2k+2) !} x^{k} & =\frac{3^{1}}{4!} x^{0} +\frac{3^{2}}{4!} x^{1} +\sum _{k=2}^{\infty }\frac{3^{k+1}}{( 2k+2) !}\\
 & =\frac{3}{2} +\frac{3}{8} x+\sum _{k=2}^{\infty }\frac{3^{k+1}}{( 2k+2) !} x^{k}
\end{aligned}$$

Subtitute back to Eq (2),

$$\begin{aligned}
\therefore \frac{3}{2} +\frac{3}{8} x+\sum _{k=2}^{\infty }\frac{3^{k+1}}{( 2k+2) !} x^{k} +2\sum _{k=2}^{\infty }\frac{( -1)^{\frac{k-4}{2}}}{( k-3) !} x^{k} & =\frac{3}{2} +\frac{3}{8} x+\sum _{k=2}^{\infty }\left[\frac{3^{k+2}}{( 2k+2) !} +\frac{2( -1)^{\frac{k-4}{2}}}{( k-3) !}\right] x^{k}\\
 & =\frac{3}{2} +\frac{3}{8} x+\sum _{k=2}^{\infty }\left[\frac{3^{k+2}}{( 2k+2) !} +\frac{2\sqrt{( -1)^{k-4}}}{( k-3) !}\right] x^{k}
\end{aligned}$$

---

## Q4: Find two power series solutions of given differential equation about the ordinary point $$x=0$$.

## a.   $$y''+xy'+y=0$$

## b.   $$( x-1) y''+y'=0$$

## c.   $$y''+e^{x} y'-y=0$$

## d.   $$\left( x^{2} +1\right) y''+xy'-y=0$$

---
### Solution

#### <u> Question (a) </u>

Let $$y( x) =\sum _{n=0}^{\infty } c_{n} x^{n} \Longrightarrow \ y'( x) =\sum _{n=1}^{\infty } nc_{n} x^{n-1}$$ and $$y''( x) =\sum _{n=2}^{\infty }( n+2)( n+1) c_{n+2} x^{n}$$.

The differential equation becomes 

$$\begin{aligned}
\sum _{n=0}^{\infty }( n+2)( n+1) c_{n+2} x^{n} +x\sum _{n=1}^{\infty } nc_{n} x^{n-1} +\sum _{n=0}^{\infty } c_{n} x^{n} & =0\\
\sum _{n=0}^{\infty }[( n+2)( n+1) c_{n+2} +nc_{n} +c_{n}] x^{n} & =0\\
\color{red} {\scriptsize { \text{[} \triangle \text{Since} \sum _{n=1}^{\infty }nc_{n}x^{n} = \sum _{n=0}^{\infty } nc_{n}x^{n} \text{]}}} & 
\end{aligned}$$

Equating coefficients gives,

$$( n+2)( n+1) c_{n+2} +( n+1) c_{n} =0$$

Thus, the recursion relation is,

$$c_{n+2} =\frac{-( n+1) c_{n}}{( n+2)( n+1)} =-\frac{c_{n}}{n+2} ,\quad n=0,1,2,...$$

Then, the even coefficients are given by $$c_{2} =-\frac{c_{0}}{2} ,\quad c_{4} =-\frac{c_{2}}{4} =\frac{c_{0}}{2\cdot 4} ,\quad c_{6} =-\frac{c_{4}}{6} =-\frac{c_{0}}{2\cdot 4\cdot 6}$$. Hence,

$$c_{2n} =( -1)^{n}\frac{c_{0}}{2\cdot 4\cdot \cdot \cdot 2n} =\frac{( -1)^{n} c_{0}}{2^{n} n!}$$

The odd coefficients are $$c_{3} =-\frac{c_{1}}{3} ,\quad c_{5} =-\frac{c_{3}}{5} =\frac{c_{1}}{3\cdot 5} ,\quad c_{7} =-\frac{c_{5}}{7} =-\frac{c_{1}}{3\cdot 5\cdot 7}$$. Hence,

$$c_{2n+1} =( -1)^{n}\frac{c_{1}}{3\cdot 5\cdot 7\cdot \cdot \cdot ( 2n+1)} =\frac{( -2)^{n} n!c_{1}}{( 2n+1) !}$$

The solution is,

$$\mathbf{y( x) =c_{0}\sum _{n=0}^{\infty }\frac{( -1)^{n}}{2^{n} n!} x^{2n} +c_{1}\sum _{n=0}^{\infty }\frac{( -2)^{n} n!}{( 2n+1) !} x^{2n+1}}$$

#### <u> Question (b) </u>

Subtituting $$y=\sum _{n=0}^{\infty } c_{n} x^{n}$$ into the differential equation,

$$\begin{aligned}
( x-1) y''+y' & =\underbrace{ \sum _{n=2}^{\infty } n( n-1) c_{n} x^{n-1}}_{k=n-1} -\underbrace{ \sum _{n=2}^{\infty } n( n-1) c_{n} x^{n-2}}_{k=n-2} +\underbrace{ \sum _{n=1}^{\infty } nc_{n} x^{n-1}}_{k=n-1}\\
 & ={ \sum _{k=1}^{\infty }( k+1) kc_{k+1} x^{k} -\sum _{k=0}^{\infty }( k+2)( k+1) c_{k+2} x^{k} +\sum _{k=0}^{\infty }( k+1) c_{k+1} x^{k}}\\
 & =-2c_{2} +c_{1} +{ \sum _{k=1}^{\infty }[( k+1) kc_{k+1} -( k+2)( k+1) c_{k+2} +( k+1) c_{k+1}] x^{k} =0}
\end{aligned}$$

Thus,

$$\begin{aligned}
-2c_{2} +c_{1} & =0\\
( k+1)^{2} c_{k+1} -( k+2)( k+1) c_{k+2} & =0
\end{aligned}$$

and

$$\begin{aligned}
c_{2} & =\frac{1}{2} c_{1}\\
c_{k+2} & =\frac{k+1}{k+2} c_{k+1} ,\quad k=1,2,3,...
\end{aligned}$$

Choosing $$c_{0} =1$$ and $$c_{1} =0$$, we find $$c_{2} =c_{3} =c_{4} =...=0$$. For $$c_{0} =0$$ and $$c_{1} =1$$, we obtain

$$c_{2} =\frac{1}{2} ,\quad c_{3} =\frac{1}{3} ,\quad c_{4} =\frac{1}{4}$$

Thus, the two solutions are

$$\mathbf{y_{1} =1\quad \quad y_{2} =x+\frac{1}{2} x^{2} +\frac{1}{3} x^{3} +\frac{1}{4} x^{4} +...}$$

#### <u> Question (c) </u>

Substituting $$y=\sum _{n=0}^{\infty } c_{n} x^{n}$$ into the differential equation we have,

$$\begin{aligned}
y''-( x+1) y'-y & =\underbrace{ \sum _{n=2}^{\infty } n( n-1) c_{n} x^{n-2}}_{k=n-2} -\underbrace{ \sum _{n=1}^{\infty } nc_{n} x^{n}}_{k=n} -\underbrace{ \sum _{n=1}^{\infty } nc_{n} x^{n-1}}_{k=n-1} -\underbrace{ \sum _{n=0}^{\infty } c_{n} x^{n}}_{k=n}\\
 & =\sum _{k=0}^{\infty }( k+2)( k+1) c_{k+2} x^{k} -\sum _{k=1}^{\infty } kc_{k} x^{k} -\sum _{k=0}^{\infty }( k+1) c_{k+1} x^{k} -\sum _{k=0}^{\infty } c_{k} x^{k}\\
 & =2c_{2} -c_{1} -c_{0} +\sum _{k=1}^{\infty }[( k+2)( k+1) c_{k+2} -( k+1) c_{k+1} -( k+1) c_{k}] x^{k} =0
\end{aligned}$$

Thus,

$$\begin{aligned}
2c_{2} -c_{1} -c_{0} & =0\\
( k+2)( k+1) c_{k+2} -( k-1)( c_{k+1} +c_{k}) & =0
\end{aligned}$$

and,

$$\begin{aligned}
c_{2} & =\frac{c_{1} +c_{0}}{2}\\
c_{k+2} & =\frac{c_{k+1} +c_{k}}{k+2} c_{k} ,\quad k=2,3,4,...
\end{aligned}$$

Choosing $$c_{0} =1$$ and $$c_{1} =0$$, we find,

$$c_{2} =\frac{1}{2} ,\quad \quad c_{3} =\frac{1}{6} ,\quad \quad c_{4} =\frac{1}{6}$$

and so on. For $$c_{0} =0$$ and $$c_{1} =1$$, we obtain,

$$c_{2} =\frac{1}{2} ,\quad \quad c_{3} =\frac{1}{2} ,\quad \quad c_{4} =\frac{1}{4}$$

and so on. Thus, the two solutions are,

$$y_{1} =1+\frac{1}{2} x^{2} +\frac{1}{6} x^{3} +\frac{1}{6} x^{4} +...\quad \quad \text{and} \quad \quad y_{2} =x+\frac{1}{2} x^{2} +\frac{1}{2} x^{3} +\frac{1}{4} x^{4} +...$$

#### <u> Question (d) </u>

Let $$y( x) =\sum _{n=0}^{\infty } c_{n} x^{n} \Longrightarrow \ y''( x) =\sum _{n=0}^{\infty } n( n-1) c_{n} x^{n-2}$$ and $$xy''=\sum _{n=0}^{\infty } nc_{n} x^{n}$$. Thus,

$$\left( x^{2} +1\right) y''=\sum _{n=0}^{\infty } n( n-1c_{n} x^{n} +\sum _{n=0}^{\infty }( n+2)( n+1) c_{n+2} x^{n}$$

The differential equation becomes,

$$\sum _{n=0}^{\infty }[( n+2)( n+1) c_{n+2} +[ n( n-1) +n-1] c_{n}] x^{n} =0$$

The recursion relation is 

$$c_{n+2} =-\frac{( n-1) c_{n}}{n+2} ,\quad n=0,1,2,...$$

Given $$c_{0}$$ and $$c_{1}$$, $$c_{2} =\frac{c_{0}}{2}$$, $$c_{4} =-\frac{c_{0}}{2^{2} \cdot 2!}$$, $$c_{6} =-\frac{3c_{4}}{6} =( -1)^{2}\frac{3c_{0}}{2^{3} \cdot 3!}$$,...

$$c_{2n} =( -1)^{n-1}\frac{1\cdot 3\cdot \cdot \cdot ( 2n-3) c_{0}}{2^{n} n!} =( -1)^{n-1}\frac{( 2n-3) !c_{0}}{2^{n} 2^{n-2} n!( n-2) !} =( -1)^{n-1}\frac{( 2n-3) !c_{0}}{2^{2n-2} n!( n-2) !} \ \text{for} \ n=2,3,...$$

$$c_{3} =\frac{0\cdot c_{1}}{3} =0\Longrightarrow c_{2n+1} =0\ \text{for} \ n=1,2,...$$ Thus the solution is,

$$\mathbf{y( x) =c_{0} +c_{1} x+c_{0}\frac{x^{2}}{2} +c_{0}\sum _{n=2}^{\infty }\frac{( -1)^{n-1}( 2n-3) !}{2^{2n-2} n!( n-2) !} x^{2n}}$$

---

## Q5: Use the power series method to solve the given initial-value problem.

## a.   $$y''-xy'-y=0, y(0)=1, y'(0)=0$$

## b.   $$y''+x^2y'+xy=0, y(0)=0, y'(0)=1$$

## c.   $$(x+1)y''-(2-x)y'+y=0, y(0)=2, y'(0)=-1$$

---
### Solution

#### <u> Question (a) </u>

Let $$y( x) =\sum _{n=0}^{\infty } c_{n} x^{n}$$. Then $$-xy'( x) =-x\sum _{n=1}^{\infty } nc_{n} x^{n-1} =-\sum _{n=1}^{\infty } nc_{n} x^{n} =-\sum _{n=0}^{\infty } nc_{n} x^{n}$$.

$$y''( x) =\sum _{n=0}^{\infty }( n+2)( n+1) c_{n+2} x^{n}$$

The equation $$y''-xy'-y=0$$ becomes

$$\sum _{n=0}^{\infty }[( n+2)( n+1) c_{n+2} -nc_{n} -c_{n}] x^{n} =0$$

Thus, the recursion relation is

$$c_{n+2} =\frac{nc_{n} +c_{n}}{( n+2)( n+1)} =\frac{c_{n}( n+1)}{( n+2)( n+1)} =\frac{c_{n}}{n+2} \ \text{for} \ n=0,1,2,...$$

One of the condition is, $$y( 0) =1$$. But $$y( 0) =\sum _{n=0}^{\infty } c_{n}( 0)^{n} =c_{0} +0+0+...=c_{0}$$, so $$c_{0} =1$$.

Hence, $$c_{2} =\frac{c_{0}}{2} =\frac{1}{2}$$, $$c_{4} =\frac{c_{2}}{4} =\frac{1}{2\cdot 4}$$, $$c_{6} =\frac{c_{4}}{6} =\frac{1}{2\cdot 4\cdot 6}$$,....,$$c_{2n} =\frac{1}{2^{n} n!}$$. The other given condition is $$y'( 0) =0$$.

But $$y'( 0) =\sum _{n=1}^{\infty } nc_{n}( 0)^{n-1} =c_{1} +0+0+...=c_{1}$$. So, $$c_{1} =0$$. 

By the recursion relation, $$c_{3} =\frac{c_{1}}{3} =0$$, $$c_{5} =0$$,...,$$c_{2n+1} =0$$ for $$n=0,1,2,...$$. 

Thus, the solution to the initial-value problem is,

$$y( x) =\sum _{n=0}^{\infty } c_{n} x^{n} =\sum _{n=0}^{\infty } c_{2n} x^{2n} =\sum _{n=0}^{\infty }\frac{x^{2n}}{2^{n} n!} =\sum _{n=0}^{\infty }\frac{\left( x^{2} /2\right)^{n}}{n!} =c^{x^{2} /2}$$

#### <u> Question (b) </u>

Assuming that $$y( x) =\sum _{n=0}^{\infty } c_{n} x^{n}$$, we have $$xy=x\sum _{n=0}^{\infty } c_{n} x^{n} =\sum _{n=0}^{\infty } c_{n} x^{n+1}$$,

$$x^{2} y'=x^{2}\sum _{n=1}^{\infty } nc_{n} x^{n-1} =\sum _{n=0}^{\infty } nc_{n} x^{n+1}$$

$$\begin{aligned}
y''( x) & =\sum _{n=2}^{\infty } n( n-1) c_{n} x^{n-2} =\sum _{n=-1}^{\infty }( n+3)( n+2) c_{n+3} x^{n+1}\\
 & =2c_{2} +\sum _{n=0}^{\infty }( n+3)( n+2) c_{n+3} x^{n+1}
\end{aligned}$$

Thus, the equation $$y''+x^{2} y'+xy=0$$ becomes

$$2c_{2} +\sum _{n=0}^{\infty }[( n+3)( n+2) c_{n+3} +nc_{n} +c_{n}] x^{n+1} =0$$

So, $$c_{2} =0$$ and the recursion relation is,

$$c_{n+3} =\frac{-nc_{n} -c_{n}}{( n+3)( n+2)} =-\frac{( n+1) c_{n}}{( n+3)( n+2)} ,\ n=0,1,2,...$$

Also, $$c_{1} =y'( 0) =1$$, so,

$$\begin{gather*}
c_{4} =-\frac{2c_{1}}{4\cdot 3} =-\frac{2}{4\cdot 3} ,\quad c_{7} =-\frac{5c_{4}}{7\cdot 6} =( -1)^{2}\frac{2\cdot 5}{7\cdot 6\cdot 4\cdot 3} =( -1)^{2}\frac{2^{2} 5^{2}}{7!} ,...\\
\\
c_{3n+1} =( -1)^{n}\frac{2^{2} 5^{2} \cdot \cdot \cdot \cdot ( 3n-1)^{2}}{( 3n+1) !}
\end{gather*}$$

Thus, the solution is, 

$$\mathbf{y( x) =\sum _{n=0}^{\infty } c_{m} x^{n} =x+\sum _{n=1}^{\infty }\left[( -1)^{n}\frac{2^{2} 5^{2} \cdot \cdot \cdot \cdot ( 3n-1)^{2} x^{3n+1}}{( 3n+1) !}\right]}$$

#### <u> Question (c) </u>

Subtituting $$y=\sum _{n=0}^{\infty } c_{n} x^{n}$$ into the differential equation, we have,

$$\begin{aligned}
 & ( x+1) y''-( 2-x) y'+y\\
= & \underbrace{ \sum _{n=2}^{\infty } n( n-1) c_{n} x^{n-1}}_{k=n-1} +\underbrace{ \sum _{n=2}^{\infty } n( n-1) c_{n} x^{n-2}}_{k=n-2} -2\underbrace{ \sum _{n=2}^{\infty } nc_{n} x^{n-1}}_{k=n-1} +\underbrace{ \sum _{n=1}^{\infty } nc_{n} x^{n}}_{k=n} +\underbrace{ \sum _{n=0}^{\infty } c_{n} x^{n}}_{k=n}\\
 & = \sum _{k=1}^{\infty }( k+1) kc_{k+1} x^{k} +\sum _{k=0}^{\infty }( k+2)( k+1) c_{k+2} x^{k} -2\sum _{k=0}^{\infty }( k+1) c_{k+1} x^{k} +\sum _{k=1}^{\infty } kc_{k} x^{k} +\sum _{k=0}^{\infty } c_{k} x^{k}\\
 & =2c_{2} -2c_{1} +c_{0} + \sum _{k=1}^{\infty }[( k+2)( k+1) c_{k+2} -( k+1) c_{k+1} +( k+1) c_{k}] x^{k} =0
\end{aligned}$$

Thus,

$$\begin{aligned}
2c_{2} -2c_{1} +c_{0} & =0\\
( k+2)( k+1) c_{k+2} -( k+1) c_{k+1} +( k+1) c_{k} & =0
\end{aligned}$$

and,

$$\begin{aligned}
c_{2} & =c_{1} -\frac{1}{2} c_{0}\\
c_{k+2} & =\frac{1}{k+2} c_{k+1} -\frac{1}{k+2} c_{k} ,\quad k=1,2,3,...
\end{aligned}$$

Choosing $$c_{0} =1$$ and $$c_{1} =0$$, we find

$$c_{2} =-\frac{1}{2} ,\quad \quad c_{3} =-\frac{1}{6} ,\quad \quad c_{4} =\frac{1}{12}$$

and so on. For $$c_{0} =0$$ and $$c_{1} =1$$, we obtain,

$$c_{2} =1 ,\quad \quad c_{3} =0,\quad \quad c_{4} =-\frac{1}{4}$$

and do on. Thus,

$$y=C_{1}\left( 1-\frac{1}{2} x^{2} -\frac{1}{6} x^{3} +\frac{1}{12} x^{4} +...\right) +C_{2}\left( x+x^{2} -\frac{1}{4} x^{4} +...\right)$$

and

$$y'=C_{1}\left( -x-\frac{1}{2} x^{2} +\frac{1}{3} x^{3} +...\right) +C_{2}\left( 1+2x-x^{3} +...\right)$$

The initital condition imply $$C_{1} =2$$ and $$C_{2} =-1$$, so

$$\begin{aligned}
y & =2\left( 1-\frac{1}{2} x^{2} -\frac{1}{6} x^{3} +\frac{1}{12} x^{4} +...\right) -\left( x+x^{2} -\frac{1}{4} x^{4} +...\right)\\
 & =2-x-2x^{2} -\frac{1}{3} x^{3} +\frac{5}{12} x^{4} +...
\end{aligned}$$

---

## Q6: Determine the singular points of the given differential equation. Classify each singular point as regular or irregular.

## a.   $$x^{3} y''-4x^{2} y'+3y=0$$

## b.   $$\left( x^{2} -9\right)^{2} y''+( x+3) y'+2y=0$$

## c.   $$\left( 2x^{2} -5x-3\right) y''+( 2x+1) y'+\frac{6}{( x-3)} y=0$$

## d.   $$\left( x^{3} -2x^{2} -3x\right)^{2} y''+x( x-3)^{2} y'-( x+1) y=0$$

---
### Solution

#### <u> Question (a) </u>

Dividing the equation with $$x^{3}$$

$$\begin{gather*}
y''+\frac{4x^{2}}{x^{3}} y'+\frac{3}{x^{3}} y=0\\
\\
P( x) =\frac{4}{x} \quad \quad Q( x) =\frac{3}{x^{3}}
\end{gather*}$$

- The factor $$x$$ appears at most to the first power in the denominator of $$P( x)$$, but more that the second power in the denominator of $$Q( x)$$
- $$x=0$$ is irregular singular point

#### <u> Question (b) </u>

Dividing the eqution with $$\left( x^{2} -9\right)^{2} =(( x-3)( x+3))^{2}$$,

$$\begin{gather*}
y''+\frac{( x+3)}{(( x-3)( x+3))^{2}} y'+\frac{2}{(( x-3)( x+3))^{2}} y=0\\
\\
P( x) =\frac{1}{( x-3)^{2}( x+3)} \quad \quad Q( x) =\frac{2}{( x-3)^{2}( x+3)^{2}}
\end{gather*}$$

- The factor $$x\ +\ 3$$ appears at most to the first power in the denominator of $$P( x)$$ and at most to the second power in the denominator of $$Q( x)$$
- $$x\ =\ -3$$ is regular singular point
- The factor $$x\ -\ 3$$ appears more than the first power in the denominator of $$P( x)$$; but at most to the second power in the denominator of $$Q( x)$$
- $$x\ =3$$ is irregular singular point

#### <u> Question (c) </u>

Factor the equation $$\left( 2x^{2} -5x-3\right) =( x-3)( 2x+1)$$,

$$\begin{gather*}
y''+\frac{( 2x+1)}{( x-3)( 2x+1)} y'+\frac{6}{( x-3)^{2}( 2x+1)} y=0\\
\\
P( x) =\frac{1}{( x-3)} \quad \quad Q( x) =\frac{6}{( x-3)^{2}( 2x+1)}
\end{gather*}$$

- The factor $$( x-3)$$ appears at most to the first power in $$P( x)$$ and second power in the denominator of $$Q( x)$$
- $$x\ =\ 3$$ is regular singular point
-The factor $$( 2x+1)$$ appears at to the first power in the denominator of $$Q( x)$$
- $$x\ =\ -\frac{1}{2}$$ is regular singular point

#### <u> Question (d) </u>

Divide the equation with $$\left( x^{3} -2x^{2} -3x\right)^{2} =\left( x\left( x^{2} -2x-3\right)\right)^{2} =x^{2}( x-3)^{2}( x+1)^{2}$$,

$$\begin{gather*}
y''+\frac{x( x-3)^{2}}{x^{2}( x-3)^{2}( x+1)^{2}} y'-\frac{( x+1)}{x^{2}( x-3)^{2}( x+1)^{2}} y=0\\
\\
P( x) =\frac{1}{x( x+1)^{2}} \quad \quad Q( x) =\frac{1}{x^{2}( x-3)^{2}( x+1)}
\end{gather*}$$

- The factor $$x$$ appears at most to the first power in the denominator of $$P( x)$$ and at most to the second power in the denominator of $$Q( x)$$
- $$x\ =\ 0$$ is regular singular point
- The factor $$x\ -\ 3$$ appears to the second power in the denominator of $$Q( x)$$
- $$x\ =\ 3$$ is regular singular point
- The factor $$x\ +\ 1$$ appears to the second power in the denominator of $$P(x)$$ and to the first power in the denominator of $$Q( x)$$
- $$x\ =\ -1$$ is irregular singular point

---

## Q7: ind the indical roots for the given differential equations where $$x=0$$ is a regular singular point.

## a.   $$2xy''-y'+2y=0$$

## b.   $$3xy''+( 2-x) y'-y=0$$

## c.   $$9x^{2} y''+9x^{2} y'+2y=0$$

## d.   $$x^{2} y''+xy'+\left( x^{2} -\frac{4}{9}\right) y=0$$

## e.   $$xy''+( 1-x) y'-y=0$$

---
### Solution

#### <u> Question (a) </u>

Divide the equation with $$2x$$,

$$y''-\frac{1}{2x} y'+\frac{2}{2x} y=y''-\frac{\frac{1}{2}}{x} y'+\frac{1}{x} y=y''-\frac{\frac{1}{2}}{x} y'+\frac{x}{x^{2}} y=0$$

Hence, $$b_{0} =-\frac{1}{2}$$ and $$r_{2} =0$$,

$$7r( r-1) +b_{0} r+c_{0} =r^{2} -r-\frac{1}{2} r+0=r^{2} -\frac{3}{2} r=r\left( r-\frac{3}{2}\right) =0$$

The indical roots are $$r_{1} =\frac{3}{2}$$ and $$r_{2} =0$$.

#### <u> Question (b) </u>

Divide the equation with $$3x$$,

$$y''+\frac{( 2-x)}{3x} y'-\frac{1}{3x} y=y''+\frac{\frac{1}{3}( 2-x)}{x} y'-\frac{\frac{1}{3}}{x} y=y''+\frac{\frac{2}{3} -\frac{1}{3} x}{x} y'-\frac{\frac{1}{3} x}{x^{2}} y=0$$

Hence, $$b_{0} =\frac{2}{3}$$ and $$c_{0} =0$$,

$$r( r-1) +b_{0} r+c_{0} =r^{2} -r+\frac{2}{3} r+0=r^{2} -\frac{1}{3} r=r\left( r-\frac{1}{3}\right) =0$$

The indical roots are $$r_{1} =\frac{1}{3}$$ and $$r_{2} =0$$.

#### <u> Question (c) </u>

Divide the equation with $$9x^{2}$$,

$$y''+\frac{9x^{2}}{9x^{2}} y'+\frac{2}{9x^{2}} y=y''+y'+\frac{\frac{2}{9}}{x^{2}} y=y''+\frac{x}{x} y'+\frac{\frac{2}{9}}{x^{2}} y=0$$

Hence, $$b_{0} =0$$ and $$c_{0} =\frac{2}{9}$$,

$$r( r-1) +b_{0} r+c_{0} =r^{2} -r+\frac{2}{9} =\left( r-\frac{1}{3}\right)\left( r-\frac{2}{3}\right) =0$$

The indical roots are $$r_{1} =\frac{2}{3}$$ and $$r_{2} =\frac{1}{3}$$.

#### <u> Question (d) </u>

Divide the equation with $$x^{2}$$,

$$y''+\frac{x}{x^{2}} y'+\frac{\left( x^{2} -\frac{4}{9}\right)}{x^{2}} y=y''+\frac{1}{x} y'+\frac{-\frac{4}{9} +x^{2}}{x^{2}} y=y''+\frac{x}{x} y'+\frac{\frac{2}{9}}{x^{2}} y=0$$

Hence, $$b_{0} =1$$ and $$c_{0} =-\frac{4}{9}$$,

$$r( r-1) +b_{0} r+c_{0} =r^{2} -r+r-\frac{4}{9} =r^{2} -\frac{4}{9} =\left( r+\frac{2}{3}\right)\left( r-\frac{2}{3}\right) =0$$

The indical roots are $$r_{1} =\frac{2}{3}$$ and $$r_{2} =-\frac{2}{3}$$.

#### <u> Question (e) </u>

Divide the equation with $$x$$,

$$y''+\frac{( 1-x)}{x} y'-\frac{1}{x} y=y''+\frac{( 1-x)}{x} y'+\frac{x}{x^{2}} y=0$$

Hence, $$b_{0} =1$$ and $$c_{0} =0$$,

$$r( r-1) +b_{0} r+c_{0} =r^{2} -r+r=r^{2} =0$$

The indical roots are $$r_{1} =0$$ and $$r_{2} =0$$.