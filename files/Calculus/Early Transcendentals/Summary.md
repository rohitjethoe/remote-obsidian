---
title: Calculus
tags:
  - CSE1200
---
*Table of Contents*
- [x] **[[#1.1 Functions and continuity]]** 


## 1.1: Functions and continuity
---
*Lecture Slides*

Stewart's Ch: 1.5, 2.2, 2.5

![[Calculus CSE lecture 1 - pre-lecture.pdf]]

### Functions
****
$$f : A \rightarrow B$$
- Has **domain** A and **co-domain** B a subset of real numbers
- The **range** of $f$ is the set of real numbers that are reached by $f$

### Product and Composition
****
The product of two functions $f(x)$ and $g(x)$ is again a function
$$h(x) = f(x)g(x)$$
The composition of two functions $f(x)$ and $g(x)$ is again a function
$$h(x) = (f \circ g)(x) = f(g(x)) $$
### Inverse Functions
****
**Definition:**
Suppose $f$ is a function with domain $D$ and range $R$

A function $g$ is the inverse of $f$ if for all $x$ in $D$ and $y$ in $R$ the following holds:
$$f(x) = y \Leftrightarrow x = g(y)$$
**Proposition:**
A function $f$ is invertible precisely if it is one-to-one, that is:
$$f(x_1) \neq f(x_2) \text{ for all } x_1 \neq x_2$$
- The graph of an inverse function $f^{-1}$ is obtained by reflecting the graph of $f$ about the line $y = x$

### Inverse Trigonometric Functions
****
**Defintion of $arcsin(x)$:**
$$arcsin(x) = y \Leftrightarrow sin(y) = x \land - \dfrac{\pi}{2} \leq y \leq \dfrac{\pi}{2}$$

**Definition of $arccos(x)$:**
$$arccos(x) = y \Leftrightarrow cos(y) = x \land 0 \leq y \leq \pi$$

**Definition of $arctan(x)$:**
$$arctan(x) = y \Leftrightarrow tan(y) = x \land - \dfrac{\pi}{2} \leq y \leq \dfrac{\pi}{2}$$

### Limit of a function: Intuition
****
- $\lim_{x \to a} f(x) = L$ means: "$f(x)$ approaches $L$ as $x$ approaches $a$, but $x \neq a$"
- $\lim_{x \to a^-} f(x) = L$ means: "$f(x)$ approaches $L$ as $x$ approaches $a$ from the left"
- $\lim_{x \to a^+} f(x) = L$ means: "$f(x)$ approaches $L$ as $x$ approaches $a$ from the right"

### Continuity
***
A function $f$: 
- **Continuous** at $x = a$ if $\lim_x \to a f(x) = f(a)$
- **Left continuous** at $x = a$ if $\lim_{x \to a^-} f(x) = f(a)$
- **Right continuous at** $x = a$ if $\lim_{x \to a^+} f(x) = f(a)$

The following are continuous on their maximal domain:
- $x^r$
- $a^x$ and $f(x) = log_a(x)$ for $a \gt 0$ and $a \neq 1$
- $sin(x), tan(x), cos(x), arcsin(x), arctan(x), arccos(x)$
- $\mid x \mid$

### Intermediate Value Theorem
***
Suppose $f$ is continuous on the closed interval $[a, b]$ and let $N$ be any number between $f(a)$ and $f(b)$ where $f(a) \neq f(b)$. Then there exists a number $c$ in $(a, b)$ s.t. $f(c) = N$


### Practice
***
- Find the inverse of a one-to-one function
- Simplify expressions involving (inverses of) trigonometric functions
- Investigate whether a function is continuous at a point