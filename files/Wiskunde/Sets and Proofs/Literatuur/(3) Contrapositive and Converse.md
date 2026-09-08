---
title: Verzamelingen en Getallen (5121VEGE6Y)
---
**Theorem 3.1:** Let $P,Q$ and $R$ denote statement forms. The following are tautologies:
- **Distributive property**:
	- $(P \land (Q \lor R)) \leftrightarrow (P \land Q) \lor (P \land R)$
	- $(P \lor (Q \land R)) \leftrightarrow (P \lor Q) \land (P \lor R)$
- **Associative property:**
	- $P \land (Q \land R) \leftrightarrow (P \land Q) \land R$
	- $P \lor (Q \lor R) \leftrightarrow (P \lor Q) \lor R$
- **Commutative property:**
	- $(P \land Q) \leftrightarrow (Q \land P)$
	- $(P \lor Q) \leftrightarrow (Q \lor P)$

**Exercise 3.2:** Negate the following:
(a) $\neg ((P \land Q) \lor (P \land R)) \equiv \neg (P \land (Q \lor R)) \equiv \neg P \lor \neg (Q \lor R) \equiv \neg P \lor (\neg Q \land \neg R)$
$\equiv (\neg P \lor \neg Q) \land (\neg P \lor \neg R)$
(b) $\neg (P \rightarrow (Q \land R)) \equiv P \land \neg (Q \land R) \equiv P \land (\neg Q \lor \neg R)$
$\equiv (P \land \neg Q) \lor (P \land \neg R)$

The **contrapositive** of an implication is $\neg Q \rightarrow \neg P$ which is logically equivalent to it's implication.

**Theorem 3.3:** Let $x$ be an integer. If $x^2$ is odd, then $x$ is odd.
- An **integer** $x$ **is odd** if there is an integer $n$ such that $x = 2n + 1$
- Assume $x^2 = 2n + 1$ for some integer $n$. We want to show $x = 2m + 1$ for some integer $m$.
- Let $P$ be "$x^2$ is odd" and $Q$ be "$x$ is odd".
- We want to prove $P \rightarrow Q$ which is logically equivalent to $\neg Q \rightarrow \neg P$
- "If $x$ is not odd, then $x^2$ is not odd." or "If $x$ is even, $x^2$ is even."

**Theorem (Contrapositive of 3.3):** Let $x$ be an integer. If $x$ is even, then $x^2$ is even.
- An **integer $x$ is even** if there is an integer $n$ such that $x = 2n$. 
- Assume $x = 2n$, We want to prove $x^2 = 2m$, where $m$ is an integer.

**Proof.**
1. Let $x$ be even. 
2. Then there is an integer $n$ such that $x = 2n$. 
3. Therefore $x^2 = (2n)^2 = 4n^2 = 2(2n^2)$.
4. Let $m = 2n^2$.
5. Then $x^2 = 2m$ and $m$ is an integer. 
6. Therefore $x^2$ is even.
$\square$

This takes care of the original theorem (3.3), since it is equivalent to the one we proved.

Notation is important:
- If we assume $x = 2n$ and accidentally try to show $x^2 = 2n$ (rather than $x^2 = 2m$), we're stuck because we assumed that $x = x^2$ (i.e. our notation would force us to show that $x = 0$ or $x = 1$)
- Begin the proof by what we are assuming and end the proof by what we are concluding.
- Keep checking that $m$ and $n$ are integers, if they weren't integers $x$ would not be even.

The **converse** of an implication is $Q \rightarrow P$, which is not logically equivalent to it's implication
- Often confused by students
- "If I am a Hobbit, then I am under 5 ft tall." = $T$
- "If I am under 5 ft tall, I am a Hobbit" = $F$ 
	- Lot's of children are under 5 ft tall and are not Hobbits.
- "If $x$ is seven, then $x$ is prime." = $T$ for all $x$
- "If $x$ is prime, then $x$ is seven" = $F$
- "If $x$ is not prime, then $x$ is not seven." = $T$ for all $x$

**Definition (prime numbers):**
- An integer $p$ is **prime** if $p > 1$  
- $p$ cannot be written as a product of two positive integers, both different from $p$.

