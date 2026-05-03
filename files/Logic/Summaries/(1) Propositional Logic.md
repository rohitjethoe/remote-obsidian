---
title: Reasoning and Logic
---
> Brightspace: *Read chapter 2 until section 2.1.2* 
> **Samenvatting digitaal & schriftelijk gemaakt in 35 minuten**

## Ch. 2: Logic
---
**Learning objectives from studiegids.tudelft.nl:**
1. Translate a logically precise claim to and from natural language.
2. Describe the operation of logical connectors and quantifiers.
3. Describe the notion of logical validity.
## Ch. 2.1: Propositional Logic
---
Humans use **natural language** (e.g. Dutch or Flemish) $\rightarrow$ often ambigous and vague
### Ch. 2.1.1: Propositions
---
A **proposition** is a statement which is either $\mathbb{T}$ or $\mathbb{F}$
- Lowercase letters such as $p, q$ and $r$ are used to represent **propositional variables**

The discussion has **mathematical generality** in that $p$ can represent any statement.

### Ch. 2.1.2: Logical Operators
---
Propositions are combined with **logical operators** (also called **logical connectives**)
- Logical operators can be applied to one or more propositions
- The truth value is determined by the operator and by the truth values of the propositions to which it is applied
- In mathematical logic we use symbols to represent logical operators

**Definition 2.1:** Let $p$ and $q$ be propositions. Then $p \lor q$, $p \land q$ and $\neg p$ are propositions, whose truth values are given by the rules
- $p \land q$ is true when both $p$ is true and $q$ is true, and in no other case
- $p \lor q$ is true when either $p$ is true, or $q$ is true, or both $p$ and $q$ are true, and in no other case
- $\neg p$ is true when $p$ is false, and in no other case

The operators $\land, \lor$ and $\neg$ are referred to as **conjunction**, **disjunction** and **negation**

> Brightspace: *Read section 2.1.4*
> **Samenvatting digitaal & schriftelijk gemaakt in 10 minuten**

### Ch. 2.1.4: Logical Equivalence
---
To verify two compound propositions are equal:
- Consider all possible combinations of values of propositional variables
- Check for all such combinations if two compound expressions compute the same value

A **truth table** = shows value of one or more compound propositions for each situation

A **situation** = any possible combination of values of the propositional variables
- In general, if there are $n$ variables, then there are $2^n$ situations

**Logically equivalent** = when two compound propositions always compute the same value

> Brightspace: *Read sections 2.1.5 to 2.1.7* 
> **Samenvatting digitaal & schriftelijk gemaakt in 61 minuten**

### Ch. 2.1.5: More logical operators
---
Other logical operators besides $\land, \lor$ and $\neg$ are: 
- **Conditional operator**: "$\rightarrow$"
- **Biconditional operator**: "$\leftrightarrow$"
- **Exclusive OR operator**: "$\oplus$"

**Definition 2.2:** For any propositions $p$ and $q$, we define the propositions $p \rightarrow q$, $p \leftrightarrow q$ and $p \oplus q$ according to the truth table:

| $p$ | $q$ | $p \rightarrow q$ | $p \leftrightarrow q$ | $p \oplus q$ |
| --- | --- | ----------------- | --------------------- | ------------ |
| 0   | 0   | 1                 | 1                     | 0            |
| 0   | 1   | 1                 | 0                     | 1            |
| 1   | 0   | 0                 | 0                     | 1            |
| 1   | 1   | 1                 | 1                     | 0            |

When these operators are used in absence of parentheses, we use the following precedence rules:
1. $\neg$
2. $\land$
3. $\lor$, $\oplus$
4. $\rightarrow$
5. $\leftrightarrow$

### Ch. 2.1.6: Implications in English
---
The proposition $p \rightarrow q$ is called an **implication** or **conditional**:
- Usually read as '$p$ implies $q$'
- $p$ is called the **hypothesis** or **antecedent**
- $q$ is called the **conclusions** or **consequent**

If the implication $p \rightarrow q$ holds:
- $p$ is **sufficient** for $q$
	- If $p$ is true, then $q$ is also automatically true
- $q$ is **necessary** for $p$
	- Without $q$ being true, $p$ can never be true

In English, $p \rightarrow q$ is often expressed as 'if $p$ then $q$'

### Ch. 2.1.7: More forms of implication
---
$\neg q \rightarrow \neg p$ is called the **contrapositive** of $p \rightarrow q$
- Translates to: "If $q$ is not true, then $p$ is also not true".
- An implication and it's contrapositive are logically equivalent
	- The implication is reversed and both parts are made negative
	- It's meaning still remains the same!

$q \rightarrow p$ is called the **converse** of $p \rightarrow q$
- "If $p$ then $q$" is not logically equivalent to "If $q$ then $p$"
- If you mean that they are both true, you'd say:
	- "If $p$ then $q$, and conversely" or $(p \rightarrow q) \land (q \rightarrow p)$
- An implication and it's converse are not equivalent

$\neg p \rightarrow \neg q$ is called the **inverse** of $p \rightarrow q$
- An implication and it's inverse are also not logically equivalent

> Brightspace: *Read sections 2.2 until 2.2.1* 

## Ch. 2.2: Boolean Algebra
---
**Learning objectives from studiegids.tudelft.nl:**
3. Describe the notion of logical validity.

### Ch. 2.2.1: Basics of Boolean Algebra
---
Boolean algebra deals with manipulating propositions.
- **George Boole** invented algebra of logic in 1854

Instead of numerical values, we only have two logical values: true and false. Written as $\mathbb{T}$ and $\mathbb{F}$ or 1 and 0
- Similar role as constant numbers, such as 1 and $\pi$ 

Boolean algebra uses logical equivalence ($\equiv$) i.o. the equals sign (=)
- Equals sign in ordinary algebra has different roles
- $\equiv$ is used for identities 
- $\leftrightarrow$ is used in equations that may or may not be true

| Laws of Boolean Algebra |                                                                                                                     |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------- |
| Double Negation         | $\neg (\neg p) \equiv p$                                                                                            |
| Excluded middle         | $p \lor \neg p \equiv \mathbb{T}$                                                                                   |
| Contradiction           | $p \land \neg p \equiv \mathbb{T}$                                                                                  |
| Identity laws           | $\mathbb{T} \land p \equiv p$<br>$\mathbb{F} \lor p \equiv p$                                                       |
| Idempotent laws         | $p \land p \equiv p$<br>$p \lor p \equiv p$                                                                         |
| Commutative laws        | $p \land q \equiv q \land p$<br>$p \lor q \equiv q \lor p$                                                          |
| Associative laws        | $(p \land q) \land r \equiv p \land (q \land r)$<br>$(p \lor q) \lor r \equiv p \lor (q \lor r)$                    |
| Distributive laws       | $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$<br>$p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$ |
| DeMorgan's laws         | $\neg (p \land q) \equiv (\neg p) \lor (\neg q)$<br>$\neg (p \lor q) \equiv (\neg p) \land (\neg q)$                |
**Duality** = given any tautology that uses only $\land, \lor$ and $\neg$, another tautology can be obtained from it by interchanging $\land$ with $\lor$ and $\mathbb{T}$ with $\mathbb{F}$

### Ch. 2.2.2: Substitution Laws
---
Propositional variables in the *'Laws of Boolean Algebra'* can stand for any (compound) propositions

$$
\neg (\neg p) \equiv p, \text{ therefore, } \neg(\neg(p \land q)) \equiv p \land q \text{ is also true.}
$$

Because any given proposition, $Q$, has a particular truth value, either $\mathbb{T}$ or $\mathbb{F}$.

**Theorem 2.1:** (First Substitution Law)
- Suppose that $Q$ is any proposition and $p$ is a propositional variable
- Consider any tautology.
- If $(Q)$ is substituted in all places where $p$ in the tautology, then the result is also a tautology

The Second Substitution Law states that you can substitute an expression for a logically equivalent expression, wherever it occurs.

**Theorem 2.2:** (Second Substitution Law)
- Suppose that $P$ and $Q$ are any propositions such that $P \equiv Q$
- Suppose that $R$ is any compound proposition in which $(P)$ occurs as a sub-proposition
- Let $R'$ be the proposition that is obtained by substituting $(Q)$ for that occurence of $(P)$ in $R$. Then $R \equiv R'$

The theorem does not require $(Q)$ to be substituted for every occurence of $(P)$ in $R$. You are free to substitute for just one or two occurences of $(P)$

## HC 1: Propositional Calculus
---
### George Boole
---
- First outlined in 1847
- Now forms the basis of most electro-mechanical processes

### FF
---
**“NOT (coffee or tea)”** is the same as: 
- (b) **“NOT coffee AND NOT tea”**.

If I am correct in saying **“To pass the course R&L, it is necessary that you pass the exam.”**
What cannot happen?
- (c) You do not pass the exam, and you pass R&L

If $p$ is true, which of the following is not necessarily true?
- (c) $p \rightarrow q$ 

Which of the following is **true** if we know that it is true that; If there are puzzles, Stefan is happy
- (c) If there are no puzzles, Stefan is not happy. This is the contrapositive of the original statement which is logically equivalent.

### Equivalent Statements
---
How can we know whether two statements ϕ and ψ are the same?
$$
p \equiv q \text{ or }(p \leftrightarrow q) \text{ when } p \rightarrow q \land q \rightarrow p
$$
How do we show this in general?
1. Prove $\phi \rightarrow \psi$ and $\psi \rightarrow \phi$ 
2. Show that $\phi$ and $\psi$ have the same truth tables
3. Reduce $\phi$ and $\psi$ to a normal form and show that their normal forms are equivalent

### Logical Connectives
---
How many binary connectives $p \star q$ are there?

| $p$ | $q$ | $\star$ |
| --- | --- | ------- |
| 0   | 0   | 0/1     |
| 0   | 1   | 0/1     |
| 1   | 0   | 0/1     |
| 1   | 1   | 0/1     |
4 rows with 2 choices per row: $2^4 = 16$

> Brightspace: *Read sections 2.5.1 and 2.5.2*

## 2.5:
---

### 2.5.1:
---

### 2.5.2:
---