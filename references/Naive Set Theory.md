---
reference: Algebra Chapter 0
section: chapter 1.1
date: 2022-09-27
tags:
---

# Naive set theory

## 1.1 Sets

**Sets** are a collection of objects

### Notation of Finite Sets

$$A:= \{1,2,3\}$$

This means that $A$ is defined as a set $\{1,2,3 \}$.

> FYI: $:=$ is analogous to $=$

A set is not defined by it's order or the number of elements in the set, rather the elements that are listed, meaning:

$$\{1,2,3\}=\{1,3,2\}=\{1,2,1,3,3,2,3,1,1,2,1,3\}$$

### Notation of Infinite Sets

$$E=\{...,-2,0,2,4,6, ...\}$$

This is for sets that are too big and have a repeating structure to them.

$$A=\{s\in S|s\:satisfies\:P\}$$

The above set reads as $s$ is an element of $S$ such that $s$ satisfies some property $P$. This is usualy how you would see a set since there are such large sets.

A **multiset** is a set in which the elements are allowed to appear with 'multiplicity' or the same element can appear multiple times. For example:

$$\{2,2\}$$

### Popular Sets

- $\emptyset$: the *empty set* which contains no elements.
- $\mathbb{N}$: the set of *natural numbers* or nonnegative integers.
- $\mathbb{Z}$: the set of *integers*.
- $\mathbb{Q}$: the set of *rational numbers*.
- $\mathbb{R}$: the set of *real numbers*.
- $\mathbb{C}$: the set of *complex numbers*.

A **singleton** in set theory is used to refer to any set of just one element, for example $\{1\}$ or $\{2\}$.

### Useful Symbols

- $\exists$ means there *exists* or the **existential quantifier**
- $\forall$ means *for all* or the **universal quantifier**
- $\exists !$ means there *exists* a *UNIQUE*



## 1.2 Inclusion of Sets

Two sets are equal iff they contain the same elements.

### Subset

$S$ is a subset of a set $T$ if every element of $S$ is also an element of $T$ or 

$$s \in S \rightarrow s \in T$$

$$S \subseteq T, S\subset T$$

> The statements above mean the same thing, meaning that you can use both interchangeably. I'm not sure if this is true among all schools of thought.

For all sets $S$, $\emptyset \subseteq S$ and $S \subseteq S$. If both sets are a subset of each other ($S \subseteq T, T \subseteq S$) Then they are equivalent.

### Number of Elements

$|S|$ means the **number of elements** of $S$ and it is equal to $\infty$ if not finite.

### Power Sets

All the known subsets of a set $S$ form a set called the **power set** otherwise known as a **set of parts** of $S$. This is denoted by:

$$\mathcal{P}(S) \: or \: 2^{S}$$

## 1.3 Operations Between Sets

### Standard Operations

- $\cup$: the **union** (OR).
- $\cap$: the **intersection** (AND).
- $\setminus$ the **difference**.
- $\sqcup$ the **disjoint union**.
- $\times$ the **Cartesian product**.

## 1.4 Disjoint Unions, Products

### Disjoint Unions

Using the example sets $S$ and $T$, **disjoint unions** require to 
1. Produce copies of the sets we will call $S'$ and $T'$
2. Keep in mind the property that $S'\cap T' = \emptyset$.
3. Then taking the ordinary union of $S'$ and $T'$, or $S' \cap T' = S \sqcup T$.

### Products

**Products** are like making coordinate pairs of each object in each set.
$$ S \times T:= \{(s,t)\:such\:that\:s\in S, t\in T\}$$

### Relating the Two

When making a copy of $S$ and $T$ to form $S'$ and $T'$ you can satisfy the condition $S'\cap T' = \emptyset$ by finding the product of $S$ and/or $T$ with, for example, a singleton $\{1\}$ and $\{0\}$.

## 1.5 Equivalence Relations, Partitions, Quotients

Equivalence relation in this books is denoted by $\sim$, however it also goes by $\equiv$ and other symbols. Equivalence can be thought of as a diagonal.

### Properties of Equivalence

An **equivalence relation** on a set S is any relation $\sim$ satisfying these three properties.
- **reflexivity**: $(\forall a \in S)\:a\sim a$
- **symmetry**: $(\forall a \in S)(\forall b \in S)\: a\sim b \rightarrow b\sim a$
- **transitivity**: $(\forall a \in S)(\forall b \in S)(\forall c \in S),\: (a \sim b \: and \: b \sim c) \rightarrow a \sim c$

### Partitions
**Partitions** are a set containing a set of disjoint nonempty sets of S.
> In this context disjoint means sharing no element - non-intersecting.

$$\mathcal{P} = \{\{1,4,7\},\{2,5,8\},\{3,6\},\{9\}\}$$

is a partition of the set

$$\{1,2,3,4,5,6,7,8,9\}$$

### Equivalence Classes
**Equivalence classes** are, in simple terms, sets containing equivalent objects or a bin full of equivalent objects.

The **equivalence classes**, therefore, of $A$ w.r.t. $\sim$ is the subset of S defined by

$$[a]_{\sim} := \{b \in S \:| \:b \sim a\}$$

The set of all equivalences is the partition $\mathcal{P}_{\sim}$ of $S$. This is defined as the following relationship, where the *quotient* of the set $S$ w.r.t. the equivalence relation ~ is the set 

$$S/\sim := \mathcal{P}_{\sim}$$

of equivalence classes of elements of $S$ w.r.t. $\sim$.

### Example

Taking the example equivalence relation:

$$A \equiv B\:(mod \: 3)$$

This satisfies all properties of equivalence.
Therefore, the equivalence classes are the set 

$$\mathcal{P}_{\sim} = \{[0]_{\sim},[1]_{\sim}\}$$

Since each equivalence class can be expressed as

$$[0]_{\sim} := \{0, 3, 6, 9, ...\}$$
$$[1]_{\sim} := \{1, 3\pm 1, 6 \pm 1\}$$

## Exercises

- [x] Locate a discussion of Russell's paradox and understand it.
- [ ] Prove that if $\sim$ is a relation on a set $S$, then the corresponding family $\mathcal{P}_{\sim}$ is indeed a partition of $S$: that is, its elements are nonempty, disjoint, and their union is $S$.
- [ ] Given a partition $\mathcal{P}$ on a set $S$, show how to define a relation $\sim$ on $S$ such that $\mathcal{P}$ is the corresponding partition.
- [ ] How many different equivalence relations may be defined on the set $\{1,2,3\}$
- [ ] Give an example of a relation that is reflexive and symmetric but not transitive. What happens if you attempt to use this relation to define a partition on the set?
- [ ] Define a relation $\sim$ on the set $\mathbb{R}$ of real numbers by setting $a\sim b \iff b - a \in \mathbb{Z}$