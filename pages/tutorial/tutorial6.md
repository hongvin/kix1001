---
layout: default
parent: Tutorial
title:  "Tutorial 6"
nav_order: 6
mathjax: true
permalink: /tutorial6
---

# Tutorial 6: Matrix Algebra

---
[Tutorial PDF]({{ site.url }}/pdf/tutorial/tutorial6.pdf){: .btn .btn-purple }
[Solution PDF]({{ site.url }}/pdf/solution/tutorial6.pdf){: .btn .btn-green }

---

## Q1: Let $$A=\begin{bmatrix}5 & -2 & 0\\-2 & 6 & 2\\0 & 2 & 7\end{bmatrix}$$, $$X=\begin{bmatrix}-x\\0\\x\end{bmatrix}$$ and $$B=\begin{bmatrix}2 & 2 & -1\\2 & -1 & 2\\-1 & 2 & 2\end{bmatrix}$$

## (a) Find the value of $$x$ such that $$X^{T} AX=144$$

## (b) Show that $$B^{T} AB=27\begin{bmatrix}1 & 0 & 0\\0 & 2 & 0\\0 & 0 & 3\end{bmatrix}$$

---
### Solution

#### <u> Question (a) </u>

$$\begin{aligned}
X^{T} AX & =\begin{bmatrix}
-x & 0 & x
\end{bmatrix}\begin{bmatrix}
5 & -2 & 0\\
-2 & 6 & 2\\
0 & 2 & 7
\end{bmatrix}\begin{bmatrix}
-x\\
0\\
x
\end{bmatrix}\\
 & =\begin{bmatrix}
-5x+0+0 & 2x+0+2x & 0+0+7x
\end{bmatrix}\begin{bmatrix}
-x\\
0\\
x
\end{bmatrix}\\
 & =12x^{2}
\end{aligned}$$

$$\therefore X^{T} AX=144\rightwhitearrow 12x^{2} =144\Longrightarrow x=\pm 2\sqrt{3}$$

#### <u> Question (b) </u>

$$\begin{aligned}
B^{T} AB & =\begin{bmatrix}
2 & 2 & -1\\
2 & -1 & 2\\
-1 & 2 & 2
\end{bmatrix}\begin{bmatrix}
5 & -2 & 0\\
-2 & 6 & 2\\
0 & 2 & 7
\end{bmatrix}\begin{bmatrix}
2 & 2 & -1\\
2 & -1 & 2\\
-1 & 2 & 2
\end{bmatrix}\\
 & =\begin{bmatrix}
6 & 6 & -3\\
12 & -6 & 12\\
-9 & 18 & 18
\end{bmatrix}\begin{bmatrix}
2 & 2 & -1\\
2 & -1 & 2\\
-1 & 2 & 2
\end{bmatrix}\\
 & =3\begin{bmatrix}
2 & 2 & -1\\
4 & -2 & 4\\
-3 & 6 & 6
\end{bmatrix}\begin{bmatrix}
2 & 2 & -1\\
2 & -1 & 2\\
-1 & 2 & 2
\end{bmatrix}\\
 & =3\begin{bmatrix}
9 & 0 & 0\\
0 & 18 & 0\\
0 & 0 & 27
\end{bmatrix}\\
 & =27\begin{bmatrix}
1 & 0 & 0\\
0 & 2 & 0\\
0 & 0 & 3
\end{bmatrix}
\end{aligned}$$

---

## Q2: Let $$A=\begin{bmatrix} 6 & -1 & 1\\ 0 & 13 & -16\\ 0 & 8 & -11 \end{bmatrix}$$ and $$x=\begin{bmatrix} 10.5\\ 21.0\\ 10.5 \end{bmatrix}$$

## (a) Determine a scalar $$r$$ such that $$Ax=rx$$

## (b) Is it true $$A^{T} x=rx$$ for the value of $$r$$ determined in part (a)

---
### Solution

$$\begin{aligned}
\begin{bmatrix}
6 & -1 & 1\\
0 & 13 & -16\\
0 & 8 & -11
\end{bmatrix}\begin{bmatrix}
10.5\\
21.0\\
10.5
\end{bmatrix} & =r\begin{bmatrix}
10.5\\
21.0\\
10.5
\end{bmatrix}\\
\begin{bmatrix}
525\\
1050\\
525
\end{bmatrix} & =r\begin{bmatrix}
10.5\\
21.0\\
10.5
\end{bmatrix}\\
\mathbf{r} & \mathbf{=} 5
\end{aligned}$$

(a) $$r=5$$

(b) No.

---

## Q3: Solve each of the following systems of linear equations using Gaussian Elimination technique.

## (a)  $$\begin{aligned} x+2y+3z & =9\\2x-y+z & =8\\3x-z & =3\end{aligned}$$

## (b)  $$\begin{aligned} -3x+2y-6z & =6\\ 5x+7y-5z & =6\\ x+4y-2z & =8 \end{aligned}$$

## (c)  $$\begin{aligned} 2x+y+3z & =1\\ 2x+6y+8z & =3\\ 6x+8y+18z & =5 \end{aligned}$$

## (d)  $$\begin{aligned} 2x-3y+z & =5\\ 3x+2y-z & =7\\ x+4y-5z & =3 \end{aligned}$$

## (e)  $$\begin{aligned} x+y+z & =6\\ 2x-y+z & =3\\ 3x-z & =0 \end{aligned}$$

---
### Solution

#### <u> Question (a) </u>

$$\begin{bmatrix}
1 & 2 & 3 & 9\\
2 & -1 & 1 & 8\\
1 & 0 & -1 & 3
\end{bmatrix}\xrightarrow{ \begin{array}{l}
R_{2}\rightarrow R_{2} -2R_{1}\\
R_{3}\rightarrow R_{3} -3R_{1}
\end{array}}\begin{bmatrix}
1 & 2 & 3 & 9\\
0 & -5 & -5 & -10\\
0 & -6 & -10 & -24
\end{bmatrix}\xrightarrow{R_{2}\rightarrow -1/5R_{2}}\begin{bmatrix}
1 & 2 & 3 & 9\\
0 & 1 & 1 & 2\\
0 & -6 & -10 & -24
\end{bmatrix}\\
\\
\xrightarrow{R_{3}\rightarrow R_{3} +6R_{2}}\begin{bmatrix}
1 & 2 & 3 & 9\\
0 & 1 & 1 & 2\\
0 & 0 & -4 & -12
\end{bmatrix}\\
\\
\begin{aligned}
-4z & =-12 & \quad y+z & =2 & \quad x+2y+3z & =9\\
\mathbf{z} & \mathbf{=3} & y+3 & =2 & x+2( -1) +3( 3) & =9\\
 &  & \mathbf{y} & \mathbf{=-1} & \mathbf{x} & \mathbf{=2}
\end{aligned}$$

#### <u> Question (b) </u>

$$\begin{bmatrix}
-3 & 2 & -6 & 6\\
5 & 7 & -5 & 6\\
1 & 4 & -2 & 8
\end{bmatrix}\xrightarrow{R_{1}\rightarrow 3R_{3} +1}\begin{bmatrix}
0 & 14 & -12 & 30\\
5 & 7 & -5 & 6\\
1 & 4 & -2 & 8
\end{bmatrix}\xrightarrow{ \begin{array}{l}
R_{1}\rightarrow 1/2R_{1}\\
R_{2}\rightarrow -5R_{3} +R_{2}
\end{array}}\begin{bmatrix}
0 & 7 & -6 & 15\\
0 & -13 & -5 & -34\\
1 & 4 & -2 & 8
\end{bmatrix}\\
\\
\xrightarrow{ \begin{array}{l}
R_{1}\rightarrow 7R_{2} +R_{1}\\
R_{2}\rightarrow 2R_{1} +R_{2}
\end{array}}\begin{bmatrix}
0 & 0 & 43 & 43\\
0 & 1 & -7 & -4\\
1 & 4 & -2 & 8
\end{bmatrix}\\
\\
\begin{aligned}
43z & =43 & \quad y-7z & =-4 & \quad x+4y-2z & =8\\
\mathbf{z} & \mathbf{= 1} & y-7 & =-4 & x+4( 3) -2( 1) & =8\\
 &  & \mathbf{y} & \mathbf{= 3} & \mathbf{x} & \mathbf{=-2}
\end{aligned}$$

#### <u> Question (c) </u>

$$\begin{bmatrix}
2 & 1 & 3 & 1\\
2 & 6 & 8 & 3\\
6 & 8 & 18 & 5
\end{bmatrix}\xrightarrow{ \begin{array}{l}
R_{2}\rightarrow -R_{1} +R_{2}\\
R_{3}\rightarrow -3R_{1} +R_{3}
\end{array}}\begin{bmatrix}
2 & 1 & 3 & 1\\
0 & 5 & 5 & 2\\
0 & 5 & 9 & 2
\end{bmatrix}\xrightarrow{R_{3}\rightarrow -R_{2} +R_{3}}\begin{bmatrix}
2 & 1 & 3 & 1\\
0 & 5 & 5 & 2\\
0 & 0 & 4 & 0
\end{bmatrix}\\
\\
\begin{aligned}
4z & =0 & \quad 5y+5z & =2 & \quad 2x+y+3z & =1\\
\mathbf{z} & \mathbf{= 0} & 5y & =2 & 2x+( 2/5) +3( 0) & =1\\
 &  & \mathbf{y} & \mathbf{= 2/5} & \mathbf{x} & \mathbf{= 3/5}
\end{aligned}$$

#### <u> Question (d) </u>

$$\begin{bmatrix}
2 & -3 & 1 & -5\\
3 & 2 & -1 & 7\\
1 & 4 & -5 & 3
\end{bmatrix}\xrightarrow{ \begin{array}{l}
R_{2}\rightarrow R_{2} -3R_{3}\\
R_{3}\rightarrow 2R_{3} -R_{1}
\end{array}}\begin{bmatrix}
2 & -3 & 1 & -5\\
0 & -10 & 14 & -2\\
0 & 11 & -11 & 11
\end{bmatrix}\xrightarrow{R_{3}\rightarrow \frac{1}{11} R_{3}}\begin{bmatrix}
2 & -3 & 1 & -5\\
0 & -10 & 14 & -2\\
0 & 1 & -1 & 1
\end{bmatrix}\\
\\
\xrightarrow{R_{3}\rightarrow 10R_{3} +R_{2}}\begin{bmatrix}
2 & -3 & 1 & -5\\
0 & -10 & 14 & -2\\
0 & 0 & 4 & 8
\end{bmatrix}\\
\begin{aligned}
4z & =8 & \quad -10y+14z & =-2 & \quad 2x-3y+z & =-5\\
\mathbf{z} & \mathbf{= 2} & -10y+14( 2) & =-2 & 2x-3( 3) +2 & =-5\\
 &  & \mathbf{y} & \mathbf{= 3} & \mathbf{x} & \mathbf{= 1}
\end{aligned}$$

#### <u> Question (e) </u>

$$\begin{bmatrix}
1 & 1 & 1 & 6\\
2 & -1 & 1 & 3\\
3 & 0 & -1 & 0
\end{bmatrix}\xrightarrow{ \begin{array}{l}
R_{2}\rightarrow R_{2} -2R_{1}\\
R_{3}\rightarrow R_{3} -3R_{1}
\end{array}}\begin{bmatrix}
1 & 1 & 1 & 6\\
0 & -3 & -1 & -9\\
0 & -3 & -4 & -18
\end{bmatrix}\xrightarrow{R_{3}\rightarrow R_{3} -R_{2}}\begin{bmatrix}
1 & 1 & 1 & 6\\
0 & -3 & -1 & -9\\
0 & 0 & -3 & -9
\end{bmatrix}\\
\begin{aligned}
-3z & =-9 & \quad -3y-z & =-9 & \quad x+y+z & =6\\
\mathbf{z} & \mathbf{= 3} & -3y-3 & =-9 & x+2+3 & =6\\
 &  & \mathbf{y} & \mathbf{=2} & \mathbf{x} & \mathbf{= 1}
\end{aligned}$$

---

## Q4: Find the eigenvalues and their associated eigenvectors 

## (a) $$A=\begin{bmatrix} 7 & 0 & -3\\ -9 & -2 & 3\\ 18 & 0 & -8 \end{bmatrix}$$
## (b) $$A=\begin{bmatrix} -5 & 0 & 0\\ 3 & 7 & 0\\ 4 & -2 & 3 \end{bmatrix}$$

---
### Solution

#### <u> Question (a) </u>

Compute $$\det(\mathbf{A} \ −\lambda \mathbf{I})$$ via a cofactor expansion along the second column:

$$\begin{aligned}
\det\begin{vmatrix}
7-\lambda  & 0 & -3\\
-9 & -2-\lambda  & 3\\
18 & 0 & -8-\lambda 
\end{vmatrix} & =( -2-\lambda )\begin{vmatrix}
7-\lambda  & -3\\
18 & -8-\lambda 
\end{vmatrix}\\
 & =( -2-\lambda )[( 7-\lambda )( -8-\lambda ) -18( -3)]\\
 & =( -2-\lambda )\left[ -56-7\lambda +8\lambda +\lambda ^{2} +54\right]\\
 & =( -2-\lambda )\left[ \lambda ^{2} +\lambda -2\right]\\
 & =-( \lambda +2)( \lambda +2)( \lambda -1)\\
 & =-( \lambda +2)^{2}( \lambda -1)
\end{aligned}$$

Thus $$A$$ has two distinct eigenvalues, $$\lambda _{1} =−2$$ and $$\lambda _{2} =1$$.

When $$\lambda _{1} =1$$,

$$\begin{aligned}
\begin{bmatrix}
6 & 0 & -3\\
-9 & -3 & 3\\
18 & 0 & -9
\end{bmatrix}\begin{bmatrix}
x_{1}\\
x_{2}\\
x_{3}
\end{bmatrix} & =\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}\\
\begin{bmatrix}
6x_{1} -3x_{2}\\
-9x_{1} -3x_{2} +3x_{3}\\
18x_{1} -9x_{3}
\end{bmatrix} & =\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}
\end{aligned}$$


$$\Longrightarrow \ x_{3} =2x_{1} \ \ \text{and} \ \ \ x_{2} =x_{3} -3x_{1}$$

$$\Longrightarrow \ x_{3} =2x_{1} \ \ \ \text{and} \ \ \ x_{2} =-x_{1}$$

When $$\lambda _{2} =−2$$,

$$\begin{aligned}
\begin{bmatrix}
9 & 0 & -3\\
-9 & 0 & 3\\
18 & 0 & -6
\end{bmatrix}\begin{bmatrix}
x_{1}\\
x_{2}\\
x_{3}
\end{bmatrix} & =\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}\\
\begin{bmatrix}
9x_{1} -3x_{3}\\
-9x_{1} +3x_{3}\\
18x_{1} -6x_{3}
\end{bmatrix} & =\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}
\end{aligned}$$


#### <u> Question (b) </u>

Compute $$\det(\mathbf{A} \ −\lambda \mathbf{I})$$ via a cofactor expansion along the first row

$$\begin{aligned}
\det\begin{vmatrix}
-5-\lambda  & 0 & 0\\
3 & 7-\lambda  & 0\\
4 & -2 & 3-\lambda 
\end{vmatrix} & =( -5-\lambda )\begin{vmatrix}
7-\lambda  & 0\\
-2 & 3-\lambda 
\end{vmatrix}\\
 & =( -5-\lambda )[( 7-\lambda )( 3-\lambda ) -2( 0)]\\
 & =( -5-\lambda )\left[ 21-7\lambda -3\lambda +\lambda ^{2}\right]\\
 & =( -5-\lambda )\left[ \lambda ^{2} -10\lambda -21\right]\\
 & =( -\lambda -5)( \lambda -7)( \lambda -3)
\end{aligned}$$

Thus $$A$$ has three eigenvalues, $$\lambda _{1} =−5$$, $$\lambda _{2} =7$$, $$\lambda _{3} =3$$.

When $$\lambda _{1} =-5$$,

$$\begin{aligned}
\begin{bmatrix}
0 & 0 & 0\\
3 & 12 & 0\\
4 & -2 & 8
\end{bmatrix}\begin{bmatrix}
x_{1}\\
x_{2}\\
x_{3}
\end{bmatrix} & =\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}\\
\begin{bmatrix}
0\\
3x_{1} +12x_{2}\\
4x_{1} -2x_{2} +8x_{3}
\end{bmatrix} & =\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}
\end{aligned}$$

$$\Longrightarrow \ x_{1} =-4x_{2} \ \ \text{and} \ \ \ x_{2} =x_{3} -3x_{1}$$

$$\Longrightarrow \ x_{3} =2x_{1} \ \ \ \text{and} \ \ \ x_{2} =-x_{1}$$

When $$\lambda _{1} =−2$$,

$$\begin{aligned}
\begin{bmatrix}
-3 & 0 & 0\\
3 & 5 & 0\\
4 & -2 & 1
\end{bmatrix}\begin{bmatrix}
x_{1}\\
x_{2}\\
x_{3}
\end{bmatrix} & =\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}\\
\begin{bmatrix}
-3x_{1}\\
3x_{1} +5x_{2}\\
4x_{1} -2x_{2} +x_{3}
\end{bmatrix} & =\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}
\end{aligned}$$

$$\Longrightarrow \ x_{3} =3x_{1}$$

---

## Q5: Using Cayley-Hamilthon approach, find $$A^{-1}$ for the following matrix:

## (a) $$\begin{bmatrix} 7 & 2 & -2\\ -6 & -1 & 2\\ 6 & 2 & -1 \end{bmatrix}$$

## (b) $$\begin{bmatrix} 2 & 1 & 1\\ 0 & 1 & 0\\ 1 & 1 & 2 \end{bmatrix}$$

---
### Solution

#### <u> Question (a) </u>

$$\begin{aligned}
| A-\lambda I|  & =0\\
\left| \begin{bmatrix}
7 & 2 & -2\\
-6 & -1 & 2\\
6 & 2 & -1
\end{bmatrix} -\lambda \begin{bmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{bmatrix}\right|  & =0\\
( 7-\lambda )[( -1-\lambda )( -1-\lambda ) -4] -2[ -6( -1-A) -12] -2[ -12-6( -1-\lambda )] & =0\\
( 7-\lambda )\left[ 1+\lambda +\lambda +\lambda ^{2} -4\right] -2[ 6+6\lambda -12] -2[ -12+6+6\lambda ] & =0\\
( 7-\lambda )\left( \lambda ^{2} +2\lambda -3\right) -\lambda \left( \lambda ^{2} +2\lambda -3\right) -12\lambda +12-12\lambda +12 & =0\\
7\lambda ^{2} +14\lambda -21-\lambda ^{3} -2\lambda ^{2} +3\lambda -12\lambda +12-12\lambda +12 & =0\\
-\lambda ^{3} +5\lambda ^{2} -7\lambda +3 & =0\\
\lambda ^{3} -5\lambda ^{2} +7\lambda -3 & =0
\end{aligned}$$

Replacing $$\lambda =A$$,

$$\begin{aligned}
A^{3} -5A^{2} +7A-3I & =0\\
A^{2} -5A+7I-3A^{-1} & =0\\
A^{-1} & =\frac{1}{3}\left[ A^{2} -5A+7I\right]
\end{aligned}$$

$$A^{2} =\begin{bmatrix}
7 & 2 & -2\\
-6 & -1 & 2\\
6 & 2 & -1
\end{bmatrix} \cdot \begin{bmatrix}
7 & 2 & -2\\
-6 & -1 & 2\\
6 & 2 & -1
\end{bmatrix} =\begin{bmatrix}
25 & 8 & -8\\
-24 & -7 & 8\\
24 & 8 & -7
\end{bmatrix}$$

$$\begin{aligned}
A^{-1} & =\frac{1}{3}\begin{bmatrix}
25 & 8 & -8\\
-24 & -7 & 8\\
24 & 8 & -7
\end{bmatrix} -5\begin{bmatrix}
7 & 2 & -2\\
-6 & -1 & 2\\
6 & 2 & -1
\end{bmatrix} +7\begin{bmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{bmatrix}\\
 & =\mathbf{\frac{1}{3}\begin{bmatrix}
-3 & -2 & 2\\
6 & 5 & -2\\
-6 & -2 & 5
\end{bmatrix}}
\end{aligned}$$

#### <u> Question (b) </u>

$$\begin{aligned}
| A-\lambda I|  & =0\\
\left| \begin{bmatrix}
2 & 1 & 1\\
0 & 1 & 0\\
1 & 1 & 2
\end{bmatrix} -\lambda \begin{bmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{bmatrix}\right|  & =0\\
( 2-\lambda )[( 1-\lambda )( 2-\lambda ) -0] -0+1[ -( 1-\lambda )] & =0\\
2\left( \lambda ^{2} -3\lambda +2\right) -\lambda \left( \lambda ^{2} +3\lambda +2\right) -1+\lambda  & =0\\
2\lambda ^{2} -6\lambda +4-\lambda ^{3} -3\lambda ^{2} -2\lambda -1+\lambda  & =0\\
-\lambda ^{3} -5\lambda ^{2} -7\lambda +3 & =0\\
\lambda ^{3} -5\lambda ^{2} +7\lambda -3 & =0
\end{aligned}$$

Replacing $$\lambda =A$$,

$$\begin{aligned}
A^{3} +5A^{2} +7A-3I & =0\\
A^{2} -5A+7I-3A^{-1} & =0\\
A^{-1} & =\frac{1}{3}\left[ A^{2} -5A+7I\right]
\end{aligned}$$

$$A^{2} =\begin{bmatrix}
2 & 1 & 1\\
0 & 1 & 0\\
1 & 1 & 2
\end{bmatrix} \cdot \begin{bmatrix}
2 & 1 & 1\\
0 & 1 & 0\\
1 & 1 & 2
\end{bmatrix} =\begin{bmatrix}
5 & 4 & 4\\
0 & 1 & 0\\
4 & 4 & 5
\end{bmatrix}$$

$$\begin{aligned}
A^{-1} & =\frac{1}{3}\begin{bmatrix}
5 & 4 & 4\\
0 & 1 & 0\\
4 & 4 & 5
\end{bmatrix} -5\begin{bmatrix}
2 & 1 & 1\\
0 & 1 & 0\\
1 & 1 & 2
\end{bmatrix} +7\begin{bmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{bmatrix}\\
 & =\mathbf{\frac{1}{3}\begin{bmatrix}
2 & -1 & -1\\
0 & 3 & 0\\
-1 & -1 & 2
\end{bmatrix}}
\end{aligned}$$

---

## Q6: Diagonalize the following matrix, if possible

## (a) $$\begin{bmatrix} 2 & 0 & 0\\ 1 & 2 & 1\\ -1 & 0 & 1 \end{bmatrix}$$

## (b) $$\begin{bmatrix} 2 & 4 & 6\\ 0 & 2 & 2\\ 0 & 0 & 4 \end{bmatrix}$$

---
### Solution

#### <u> Question (a) </u>

**Step 1:** Find the eigenvalue,

$$\det( A-\lambda I) =\det\begin{bmatrix}
2-\lambda  & 0 & 0\\
1 & 2-\lambda  & 1\\
-1 & 0 & 1-\lambda 
\end{bmatrix} =( 2-\lambda )^{2}( 1-\lambda ) =0$$

Eigenvalue: $$\lambda =1$$ and $$\lambda =2$$.

**Step 2:** Find three linearly independent eigenvector.

Basis of $$\lambda =1$$, $$v_{1} =\begin{bmatrix}
0\\
-1\\
1
\end{bmatrix}$$

Basis of $$\lambda =2$$, $$v_{2} =\begin{bmatrix}
0\\
1\\
0
\end{bmatrix}$$, $$v_{2} =\begin{bmatrix}
-1\\
0\\
1
\end{bmatrix}$$

**Step 3:** Construct $$P$$ from Step 2:

$$P=\begin{bmatrix}
0 & 0 & -1\\
-1 & 1 & 0\\
1 & 0 & 1
\end{bmatrix}$$

**Step 4:** Construct $$D$$ from corresponding eigenvalue:

$$D=\begin{bmatrix}
1 & 0 & 0\\
0 & 2 & 0\\
0 & 0 & 2
\end{bmatrix}$$

**Step 5:** Verify $$AP=PD$$:

$$\begin{aligned}
AP & =\begin{bmatrix}
2 & 0 & 0\\
1 & 2 & 1\\
-1 & 0 & 1
\end{bmatrix}\begin{bmatrix}
0 & 0 & -1\\
-1 & 1 & 0\\
1 & 0 & 1
\end{bmatrix} =\begin{bmatrix}
0 & 0 & -2\\
-1 & 2 & 0\\
1 & 0 & 2
\end{bmatrix}\\
PD & =\begin{bmatrix}
0 & 0 & -1\\
-1 & 1 & 0\\
1 & 0 & 1
\end{bmatrix}\begin{bmatrix}
1 & 0 & 0\\
0 & 2 & 0\\
0 & 0 & 2
\end{bmatrix} =\begin{bmatrix}
0 & 0 & -2\\
-1 & 2 & 0\\
1 & 0 & 2
\end{bmatrix}
\end{aligned}$$

#### <u> Question (b) </u>

**Step 1:** Find the eigenvalue,

Since the matrix is triangle,

Eigenvalue: $$\lambda =2$$ and $$\lambda =4$$.

**Step 2:** Find three linearly independent eigenvector.

Basis of $$\lambda =2$$, $$v_{1} =\begin{bmatrix}
1\\
0\\
0
\end{bmatrix}$$

Basis of $$\lambda =4$$, $$v_{2} =\begin{bmatrix}
5\\
1\\
1
\end{bmatrix}$$

Every eigenvector of $$A$$ is a multiple of $$v_{1}$$ or $$v_{2}$$. There are not three linearly independent eigenvector of $$A$$. $$A$$ is not diagonalizable.