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
> 12:50-13:26

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
- In English, $p \rightarrow q$ is often expressed as 'if $p$ then $q$'

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

