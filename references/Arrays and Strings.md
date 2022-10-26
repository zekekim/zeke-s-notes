---
reference: cracking the coding interview
section: IX.1
date: 2022-09-28
tags:
---

## Hash Tables

A **hash table** is a data structure that maps keys to values for highly efficient lookup.

Using a hash table and linked lists to store key, value pairs, you would:

1. Compute the hash code as an `int` or `long`. There may be collisions on the same hash code, meaning multiple values per hash code since there may be an infinite number of keys but a finite number of ints. **RECHECK for understanding**
2. Then map the hash code to an index using a function.
3. Store the key and value in the linked list of the index.

Looking up the value pair by its key you would repeat the same process and get the value in the hash table.

This means that an array can be searched in `O(1)` time, with the worst case being `O(N)` if for some reason your hash function is really inefficient, where `N` is the number of keys.

## ArrayList & Resizeable Arrays

An `ArrayList` is an array-like data structure that resizes itself by a growth factor (often = 2) when it reaches capacity. In other words, it is a **dynamically sized** list.

The amortized insertion runtime is `O(1)`

Think of the example of walking 1 kilometer. You will walk 0.5 kilometers, then 0.25 kilometers, then 0.125 kilometers, and that will add up to always less than 1 kilometer but very close.

Inserting `N` elements therefore takes `O(N)` work total. Each insertion is `O(1)` time.

## StringBuilder

```cpp
String joinWords(String[] words) {
	String sentence = "";
	for (String w: words) {
		sentence = sentence + w;
	}
	return sentence;
}
```

A new copy of the string is made on each concatenation and the two strings are copied over character by character. This means that you copying x characters, then 2x characters, then on and on. Therefore you are running in `O(xn^2)`

```cpp
String joinWords(String[] words) {
	StringBuilder sentence = new StringBuilder();
	for (String w: words) {
		sentence.append(w);
	}
	return sentence.toString();
}
```

The `StringBuilder` is just a better way to concatenate strings - it is the dynamically sized string.

## Interview Questions

