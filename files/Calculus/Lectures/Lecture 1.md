## Assessment
---
**Week 5:** `short answer midterm`
**Week 10:** `open question final exam`

**Grading**:
$$
\dfrac{m + 2 * f}{3} \ge 5.75 \land f \ge 5
$$
with $m = \text{ 'midterm'}$ and $f = \text{'final exam'}$.

## Programme
---
- Functions
- Inverse Functions
- Inverse Trigonometric Functions
- The Limit of a Function
- Continuity

**Stewart's Calculus:** Ch 1.5, Ch 2.2, Ch 2.5

Practice the topics of this lecture to be able to:
1. find the inverse of a one-to-one function
2. simplify expressions involving trigonometric functions
3. investigate whether a function is continuous at a point

---
**Functions**
<hr style="margin-top: 8px" />

For us a function is:
$$f : A \rightarrow B$$
- $A$ = **domain**
- $B$ = **co-domain** (a subset of real numbers.)
- **Range** of $f$ is the set of real numbers that are reached by $f$.

The **product** of two functions $f(x)$ and $g(x)$ is again a function
$$
h(x) = f(x) \cdot g(x)
$$
The **composition** of two functions $f(x)$ and $g(x)$ is again a function
$$
h(x) = (f \circ g)(x) = f(g(x))
$$

---
**Inverse Functions**
<hr style="margin-top: 8px" />

**Definition:**
Suppose $f$ is a function with domain $D$ and range $R$.
A function $g$ is the inverse of $f$ 
if for all $x$ in $D$ and $y$ in $R$ the following holds:

$$
f(x)= y\Leftrightarrow x = g(y)
$$

Inverse function **notation**: $f^{-1}$
- $f(f^{-1}(y)) = y$
- $f^{-1}(f(x)) = x$

A function $f$ has an **inverse** if it is **one-to-one**, that is:
$$
f(x_1) \neq f(x_2) \land x_1 \neq x_2
$$

Find the inverse of a function by:
1. Start with $y = f(x)$
2. Solve for $x$ in terms of $y$
3. Interchange the role of $x$ and $y$ gives $y = f^{-1}(x)$

---
**Inverse Trigonometric Functions**
<hr style="margin-top: 8px" />

- **Definition of $arcsin$ and $sin$:**
$$
arcsin(x) = y \Leftrightarrow sin(y) = x \text{ with } - \dfrac{\pi}{2} \leq y \leq \dfrac{\pi}{2}
$$
- **Definition of $arccos$ and $cos$:**
$$
arccos(x) = y \Leftrightarrow cos(y) = x \text{ with } 0 \leq y \leq \pi
$$
- **Definition of $arctan$ and $tan$:**
$$
arctan(x) = y \Leftrightarrow tan(y) = x \text{ with } - \dfrac{\pi}{2} \leq y \leq \dfrac{\pi}{2}
$$
---
**Limit of a Function**
<hr style="margin-top: 8px" />

**$f(x)$ approaches $L$ as $x$ approaches $a$:
$$\lim_{x \to a} f(x) = L$$

$f(x)$ approaches $L$ as $x$ approaches $a$ **from the right**:
$$
\lim_{x \to a^+}
$$

$f(x)$ approaches $L$ as $x$ approaches $a$ **from the left**:
$$
\lim_{x \to a^-}
$$

**Theorem:**
$$
\lim_{x \to a}f(x) = L \Leftrightarrow \lim_{x \to a^+}f(x) = L = \lim_{x \to a^-}f(x)
$$

---
**Continuity**
<hr style="margin-top: 8px" />

A function $f$ is <u>continuous</u> at $x = a$ if: $\lim_{x \to a} f(x) = f(a)$

The following functions are continuous at their maximal domain:
- $x^r$
- $a^x$ and $f(x) = log_a(x)$ for $a > 0$ and $a \neq 1$
- $sin(x), tan(x), cos(x), arcsin(x), arctan(x), arccos(x)$
- $| x |$

A function $f$ is <u>left continuous</u> at $x = a$ if: $\lim_{x \to a^-} f(x) = f(a)$

A function $f$ is <u>right continuous</u> at $x = a$ if: $\lim_{x \to a^+} f(x) = f(a)$

---
**Intermediate values**
<hr style="margin-top: 8px" />

**Intermediate value theorem**:
Suppose $f$ is continuous on $[a, b]$ and let $N$ be any number between $f(a)$ and $f(b)$, where $f(a) \neq f(b)$. Then there exists number $c$ in $(a, b)$ such that $f(c) = N$


## Questions
---
1) **Find the inverse**:

![[Screenshot 2025-11-16 at 21.28.49.png]]

2) **Find the inverse**:
![[Screenshot 2025-11-16 at 21.29.12.png]]

3) **Find the inverse**:
![[Screenshot 2025-11-16 at 21.29.49.png]]

4) **Arcsin**
![[Screenshot 2025-11-16 at 21.41.52.png]]

5) **Arctan**
![[Screenshot 2025-11-16 at 21.42.05.png]]

6) **Simplifying expressions**
![[Screenshot 2025-11-16 at 21.42.28.png]]

7) **Practice**
![[Screenshot 2025-11-16 at 21.42.49.png]]

8) Continuity
![[Screenshot 2025-11-18 at 15.32.50.png]]

9) Continuity
![[Screenshot 2025-11-18 at 15.33.13.png]]

