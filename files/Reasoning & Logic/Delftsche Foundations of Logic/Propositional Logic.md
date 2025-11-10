---

---
---
## 2 Logic
---
[Delftsche Foundations Of Logic.pdf](https://books.open.tudelft.nl/home/catalog/view/211/393/640)
[Delftsche Foundations Of Logic.md](https://interactivetextbooks.tudelft.nl/delftse-foundations-of-computation/content/index.html) 

Logical deduction is when conclusions are derived from some set of premises.

---
### 2.1.1 Propositions
---
Humans use **natural language** which is vague & ambigious. To model **natural language** we first consider **propositional logic**.

**A proposition** = a statement with a truth value, either $\mathbb{T}$ or $\mathbb{F}​$

- (Simple) propositions are represented by lowercase letters like $p$, $q$, $r$, etc. 
- Compound propositions are represented by uppercase letters $P$, $Q$ or $R$​.

The discussion has **mathematical generality** $p$ can represent any statement

---
### 2.1.2: Logical Operators
---
**Definition 2.1:**
- $p \land q$ is true when both $p$ and $q$ are true.
- $p \lor q$ is true when either $p$ or $q$ or both are true.
- $\neg p$ is true when $p$ is false.

The operators $\land, \lor, \neg$ are referred to as **conjunction**, **disjunction** and **negation**.


---
### 2.1.4: Logical Equivalences
---
**A truth table** = shows values of a (compound) proposition for each possible combination truth values.

- Each such combination of truth values is called **a situation**

> If there are $n$ variables, there are $2^n$ possible rows to assign truth values.

**Logical equivalence** = if two compound propositions always have the same truth values.


---
### 2.1.5: More logical operators
---
- **Conditional operator** $\rightarrow$
- **Biconditional operator** $\leftrightarrow$
- **Exclusive or operator** $\oplus$

**Definition 2.2**

$$ \begin{array}{|c|c||c||c||c|} \hline p & q & p \rightarrow q & p \leftrightarrow q & p \oplus q\\ \hline 0 & 0 & 1 & 1 & 0 \\ 0 & 1 & 1 & 0 & 1 \\ 1 & 0 & 0 & 0 & 1 \\ 1 & 1 & 1 & 1 & 0 \\ \hline \end{array} $$

**Order of evaluation** of all logical operators:

1. $\neg$
2. $\land$
3. $\lor, \oplus$
4. $\rightarrow$
5. $\leftrightarrow$

---
### 2.1.6: Implications in English
---
$p \rightarrow q$ is called **implication** or **conditional**
- $p$ is the **hypothesis** or **antecedent**
- $q$ is the **conclusion** or **consequent**

$p \rightarrow q$ means that:
- $p$ is **sufficient** for $q$ 
- $q$ is **necessary** for $p$

---
### 2.1.7: More implications
---
Let $p$ stand for **"This is Tuesday"** and let $q$ stand for **"This is Belgium."**

$\neg q \rightarrow \neg p$ is called **contrapositive**
- "If this is not Belgium, then it's not Tuesday.
 

$q \rightarrow p$ is called **converse**
$\neg p \rightarrow \neg q$ is called **inverse**

