---
cards-deck: Linear Algebra
---

# Linear Equation #card 
A **linear equation** of the n variables $x_{1},x_{2},...,x_{n}$ is an equation of the form  
$$a_{1}x_{1}+a_{2}x_{2}+...+a_{n}x_{n}=b$$
where $a_1,a_2,...,a_{n} b \in \mathbb{R}\: or\: \mathbb{C}$.
^1665728911479

## Free Variable #card 
A variable whose value is not restricted in the system.
ex. In the equation $a(x-1)(x-2)=y$, a is a scalar and a **free variable** since its value is not restricted by the system.
^1665728829960


## Basic Variable #card 
A variable that can be expressed in terms of the free variables.
ex. In the equation $\vec{v_{1}} \vec{v_{2}} \vec{v_{3}}$ where $\vec{v_{1}} = 2\vec{v_{2}} 2\vec{v_{3}}$, $\vec{v_{1}}$ is considered the free variable since it can be expressed in terms of the other variables.
^1665728829967

# System of Linear Equations #card 
A set of **m** linear equations of the form:
$$\begin{alignat*}{2}
&a_{11}x_{1} &&+ &&a_{12}x_{2} &&+ &&... &&+ &&a_{1n}x_{n} &&= b_{1}\\
&a_{21}x_{1} &&+ &&a_{22}x_{2} &&+ &&... &&+ &&a_{2n}x_{n} &&= b_{2}\\
&\quad \vdots &&+ &&\quad \vdots &&+ &&\ddots &&+ &&\quad \vdots 
&&= \vdots \\
&a_{m1}x_{1} &&+ &&a_{m2}x_{2} &&+ &&... &&+ &&a_{mn}x_{n} &&= b_{m}
\end{alignat*}$$
^1665728829977

## Solution #card 
Any values of the variables $x_{1}, x_{2},..., x_{n}$ which is a solution to all equations in the system.
^1665728829981

## Solution Set #card 
The set of all solutions.
^1665728829983

## Consistent vs. Inconsistent #card 
A system is **consistent** if the system has at least one solution and **inconsistent** if it has none.
^1665728829987

## What makes a system consistent? #card
Consistent $\iff$ the augmented matrix has no pivot in the rightmost column.
^1665729277951

# Matrix #card
An abstraction of data where the number of rows **m** and columns **n** relate to the number of equations and number of variables respectively.
$$\left[\begin{array}{cccc|c}a_{11} & a_{12} & ... & a_{1n}x_{n} & b_{1} \\
a_{21} & a_{22} & ... & a_{2n} & b_{2}\\
\vdots & \vdots & \ddots & \vdots & \vdots \\ 
a_{m1} & a_{m2} & ... & a_{mn} & b_m
\end{array}\right]$$
^1665728829989

## Reduced Echelon Form #card 
Let $A$ be a matrix. Then $A$ is in **echelon form** if
1. All rows of zeros of $A$ are at the  bottom of $A$.
2. The first nonzero entry of a row (the **leading entry**) is in a column to the right of the leading entry above that enetry.
3. All entries under a leading entry are zeros.
$$\left[\begin{array}{cccccc|c}
1 & 0 & 0 & 0 & ... & * & * \\
0 & 1 & 0 & ... & * & * & * \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & 0 & ... & * & * & *
\end{array}\right]$$
^1665728829990

## Row Reduced Echelon Form #card 
Let $A$ be a matrix. Then $A$ is in **reduced row echelon form** if
1. The matrix $A$ is in echelon form.
2. The leading entry in each nonzero row is 1 (**pivot**).
3. Each leading 1 is the only nonzero entry in that column (**pivot column**).
$$\left[\begin{array}{cccccc|c}
1 & 0 & 0 & 0 & ... & 0 & 0 \\
0 & 1 & 0 & ... & 0 & 0 & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & 0 & ... & 0 & 0 & 0
\end{array}\right]$$
We can recover the solution to the matrix by transforming the matrix $A$ into $rref(A)$ or the **row reduced echelon form** of matrix $A$.
^1665728829993


```{r}
print(dat$sub)

```