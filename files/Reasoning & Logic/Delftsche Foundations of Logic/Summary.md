---
title: Delftsche Foundations Summary
tags:
  - CSE1300
date: 2025-12-24
---
# 2: Logic
***
## 2.1: Propositional Logic
---
### 2.1.1: Propositions
---
A **proposition** = a statement with a truth value, either $\mathbb{T}$ or $\mathbb{F}$
- Represented using lowercase letters (**propositonal variables**)

### 2.1.2: Logical Operators
---
A **logical operator** = can be applied to propositions, to produce new propositions
- AND ($\land$) is referred to as **conjunction**
- OR ($\lor$) is referred to as **disjunction**
- NOT ($\neg$) is referred to as **negation**

| $p$ | $q$ | $p \land q$ | $p \lor q$ | $\neg p$ |
| --- | --- | ----------- | ---------- | -------- |
| 0   | 0   | 0           | 0          | 1        |
| 0   | 1   | 0           | 1          | 1        |
| 1   | 0   | 0           | 1          | 0        |
| 1   | 1   | 1           | 1          | 0        |

**Logical operators** are also referred to as **logical connectives**.

### 2.1.4: Logical Equivalence
---
A **situation** = a possible combination of values of the propositional variables
- 
A **truth table** = compares values of propositions for all possible situations

If there are $n$ variables, then there are $2^n$ different assignments of propositional values, i.e. $2^n$ situations

Two compound propositions are **logically equivalent** if they always have the same output values.

