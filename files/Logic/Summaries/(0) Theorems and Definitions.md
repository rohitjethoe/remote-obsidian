---
title: Reasoning and Logic
---
[[#Definitions]]
- 2.1: [[#Definition 2.1 AND, OR and NOT.]]
- 2.2: [[#Definition 2.2 Conditional, Bi-conditional and Exclusive OR]]
- 2.4: [[#Definition 2.4 Tautology, Contradiction, Contingency]]
- 2.5: [[#Definition 2.5 Logical equivalence in terms of Tautology]]
- 2.6: [[#Definition 2.6 DNF]]
- 2.10: [[#Definition 2.10 P if Q is a tautology]]
- 2.11: [[#Definition 2.11 Formal proof]]
[[#Theorems]]
- 2.1: [[#Theorem 2.1 First Substitution Law]]
- 2.2: [[#Theorem 2.2 Second Substitution Law]]
[[#Lectures]]
- 1.2: [[#Lecture 1.2 Propositional Calculus]]

## Definitions
---
#### Definition 2.1: AND, OR and NOT.
---
Let $p$ and $q$ be propositions. Then $p \lor q$, $p \land q$ and $\neg p$ are propositions, whose truth values are given by the rules
- $p \land q$ is true when both $p$ is true and $q$ is true, and in no other case
- $p \lor q$ is true when either $p$ is true, or $q$ is true, or both $p$ and $q$ are true, and in no other case
- $\neg p$ is true when $p$ is false, and in no other case

#### Definition 2.2: Conditional, Bi-conditional and Exclusive OR 
---
For any propositions $p$ and $q$, we define the propositions $p \rightarrow q$, $p \leftrightarrow q$ and $p \oplus q$ according to the truth table:

#### Definition 2.4: Tautology, Contradiction, Contingency
---
- A compound proposition is said to be a **tautology** if it is $\mathbb{T}$ for all situations
- A compound proposition is said to be a **contradiction** if it is $\mathbb{F}$ for all situations
- A compound proposition is said to be a **contingency** if it is neither a tautology nor a contradiction

#### Definition 2.5: Logical equivalence in terms of Tautology
---
- Two compound propositions, $P$ and $Q$ are **logically equivalent** if and only if the proposition $P \leftrightarrow Q$ is a tautology.

#### Definition 2.6: DNF
---
- A compound proposition is said to be in **disjunctive normal form**, or DNF, if it is a disjunction of conjunctions of simple terms.
- If each propositional variable occurs at most once in each conjunction
- And if each conjunction occurs at most once in the disjunction
#### Definition 2.10: P if Q is a tautology
---
- Let $P$ and $Q$ be any formulas 
- The notation $P \Rightarrow Q$ is used to mean that $P \rightarrow Q$ is a tautology.
- That is, in all cases where $P$ is true, $Q$ is also true. We then say $Q$ can be **logically deduced** from $P$ or that $P$ **logically implies** $Q$

#### Definition 2.11: Formal proof
---
A **formal proof** = shows that an argument is valid and consists of a sequence of propositions, s.t.
-  The last proposition in the sequence is **the conclusion of the argument**
- And every proposition in the sequence is either **a premise** or **follows by logical deductions from preceding propositions**

## Theorems
---
#### Theorem 2.1: First Substitution Law
---
- Suppose that $Q$ is any proposition and $p$ is a propositional variable
- Consider any tautology.
- If $Q$ is substituted in all places where $p$ in the tautology, then the result is also a tautology

#### Theorem 2.2: Second Substitution Law
---
- Suppose that $P$ and $Q$ are any propositions such that $P \equiv Q$
- Suppose that $R$ is any compound proposition in which $(P)$ occurs as a sub-proposition
- Let $R'$ be the proposition that is obtained by substituting $(Q)$ for that occurence of $(P)$ in $R$. Then $R \equiv R'$

## Lectures
---
### Lecture 1.2: Propositional Calculus
---
#### Definition: Literals
---
- A **literal** is a propositional variable or the negation of it: $p, \neg p, q, \neg s, ...$

#### Theorem: DNF
---
- Every formula in propositional calculus can be rewritten to DNF, a disjunction of conjunctions of literals.

#### Definition: Complementary Literals
---
- Two literals are called **complementary** iff one is the negation of the other
- $(p, \neg p), (q, \neg q), ...$

#### Theorem: Conjunctive Normal Form
---
- Every formula in propositional calculus can be rewritten to CNF, a conjunction of disjunction of literals.
- For instance: $(p \lor \neg q) \land (q \lor \neg r \lor \neg s) \land (\neg p \lor r) \land ...$
