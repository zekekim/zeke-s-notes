---
reference: algebra chapter 0
section: 1.2
date: 2022-09-28
tags:
---
# Functions between sets

## Definition

A **function** is $b\in B$ which is an image of any given element $a \in A$
$$f(a)=b\: or \: b=f(a)$$

It is often thought in terms of its graph, that a function is its graph $\Gamma_{f}$.
$$\Gamma_{f} := \{(a,b) \in A \times B \: | \: b = f(a)\}\subseteq A \times B$$

But this leaves room for misinterpretation of one condition, which is:
$$(\forall a \in A)(\exists ! b \in B) (a,b) \in \Gamma_{f} \: or \: f(a)=b$$
Meaning that there must be only one output for every input.

You can notate a function as:
$$A \stackrel{f}{\longrightarrow} B, f: A \rightarrow B, a \leftrightarrow f(a)$$

$B^{A}:=$ the collection of all $f:A \rightarrow B$. Since f is defined as a graph of a certain mapping of $A$ onto $B$, it can be seen that

$$B^{A} \subseteq A \times B$$

## Functions for Set A

### Identity Function

$$id_{A}:A\rightarrow A$$
or
$$(\forall a \in A) id_{A}(a) = a$$

### Subsets

For a set $S$,

$$f(S) := {b \in B \: | \: (\exists a \in A) \: b = f(a)}$$

$\therefore f(S)$ is the subset $B$, or the range is $B$.

The largest subset $B$ can be is $f(A)$ which is also called the image of f or $im(f)$.

$$f|_{s}(s) = f(s)$$

This denotes that $f$ is restricted by $s$.

$$(\forall s \in S): f|_{s}, f:S \rightarrow B$$

Helper comparison:
$$f(A) = im(f), f(S) = im(f|_{s})$$


