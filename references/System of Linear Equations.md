---
context: guptas notes linear algebra
date: 2022-09-28
section: chapter 1
tags: 
---
# System of Linear Equations

## Linear Equations

A **free variable** is a variable whose value is not restricted in the system. A **basic variable** is a variable that can be expressed in terms of the free variables.

A **linear equation** of the n variables $x_{1},x_{2},...,x_{n}$ is an equation of the form

$$a_{1}x_{1}+a_{2}x_{2}+...+a_{n}x_{n}=b$$

where $a_1,a_2,...,a_{n} b \in \mathbb{R}\: or\: \mathbb{C}$.

For a linear equation...
- Each variable must be to the power of 1.
- The coefficient of each variable must be a real number.

## System of Linear Equations

A **system of linear equations** is a set of m equations of the form

$$\begin{alignat*}{2}
&a_{11}x_{1} &&+ &&a_{12}x_{2} &&+ &&... &&+ &&a_{1n}x_{n} &&= b_{1}\\
&a_{21}x_{1} &&+ &&a_{22}x_{2} &&+ &&... &&+ &&a_{2n}x_{n} &&= b_{2}\\
&\quad \vdots &&+ &&\quad \vdots &&+ &&\ddots &&+ &&\quad \vdots 
&&= \vdots \\
&a_{m1}x_{1} &&+ &&a_{m2}x_{2} &&+ &&... &&+ &&a_{mn}x_{n} &&= b_{m}
\end{alignat*}$$

A **solution** to a linear system of equations is any values of the variables $x_{1},x_{2},...,x_{n}$ which is a solution to all equations in the system.

The **solution set** is the set of all solutions.

A system is **consistent** if the system has at least one solution and **inconsistent** if it has none.

## Questions about Linear Systems

There are four main questions about linear systems...
1. Is the linear system consistent (does it have a solution)?
2. If a given linear system is consistent, then is the solution **unique**? If not what is the set of solutions?
3. Is there an algorithm to solve systems of linear equations?
4. How can we effectively describe the set of solutions?

## Matrices

$$\left[\begin{array}{cccc|c}a_{11} & a_{12} & ... & a_{1n}x_{n} & b_{1} \\
a_{21} & a_{22} & ... & a_{2n} & b_{2}\\
\vdots & \vdots & \ddots & \vdots & \vdots \\ 
a_{m1} & a_{m2} & ... & a_{mn} & b_m
\end{array}\right]$$

The number of rows **m** and columns **n** relate to the number of equations and number of variables respectively.

## Questions about Matrices

There are two questions about Matrices...

1. What operations can we perform on the row of matrices?

	1. Switching any 2 rows of the augmented matrix
	2. Multiplying a row of the augmented matrix by a non-zero number
	3. Adding a multiple of one row to another row of the augmented matrix

	This is very, very similar to manipulating a system of linear equations, because it is almost the same!

2. How do we recover the solutions from the matrix?

We can recover the solution to the matrix by transforming the matrix $A$ into $rref(A)$ or the **row reduced echelon form** of matrix $A$.

$$\left[\begin{array}{cccccc|c}
1 & 0 & 0 & 0 & ... & * & * \\
0 & 1 & 0 & ... & * & * & * \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & 0 & ... & * & * & *
\end{array}\right]$$

Which is basically making 1's along the diagonal and 0's everywhere else to the left of the vertical line.

## Defining Echelon Form and Row Reduced Echelon Form

Let $A$ be a matrix. Then $A$ is in **echelon form** if
1. All rows of zeros of $A$ are at the  bottom of $A$.
2. The first nonzero entry of a row (the **leading entry**) is in a column to the right of the leading entry above that enetry.
3. All entries under a leading entry are zeros.

Let $A$ be a matrix. Then $A$ is in **reduced row echelon form** if
1. The matrix $A$ is in echelon form.
2. The leading entry in each nonzero row is 1 (**pivot**).
3. Each leading 1 is the only nonzero entry in that column (**pivot column**).

## Goal of Matrices

Since a system can be solved when in row reduced echelon form, we must reduce the matrix $A$ to $rref(A)$ using **row reduction** for every matrix.

1. Get a 1 in the upper left hand entry.
2. Make the rest of the entries in that column 0.
3. Make the next diagonal entry a 1.
4. Repeat Step 2.
5. Repeat Steps 3 and 4 until you are done.

The notation for row operations are as follows:
1. $R_{i} \longleftrightarrow R_{j}$ means switch the $i^{th}$ and $j^{th}$ rows.
2. $R_{i} \longleftrightarrow cR_{i}$ means multiply the $i^{th}$ row by the number $c$.
3. $R_{i} \longleftrightarrow R_{i} + cR_{j}$ means add $c$ times $j^{th}$ row to $i^{th}$ row.

Referencing **free** and **basic** variables once more, we can write athe solutions by solving for the basic variables in terms of the free variable. This is called **parametric form**.

$$\begin{alignat*}{2}
x_{1} &= &&x_{3} - 2\\
x_{2} &= -2&&x_{3} + 1
\end{alignat*}$$

## No Solution Case

$$\left[\begin{array}{cc|c} 1 & 2 & 1 \\ 0 & 0 & 1 \end{array}\right]$$

In this case, there is no solution, because the bottom of the row of the matrix states that

$$\begin{align*}
x_{1}+ 2x_{2} &= 1\\
0 &= 1
\end{align*} $$

which is a false statement.