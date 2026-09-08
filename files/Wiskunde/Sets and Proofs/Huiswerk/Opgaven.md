---
title: Verzamelingen en Getallen (5121VEGE6Y)
---

**Opgave 1.1:**
Laat zien dat $\neg (P \land Q)$ logisch equivalent is aan $\neg P \lor \neg Q$. Wat betekent deze uitspraak in woorden?

| $P$ | $Q$ | $\neg (P \land Q)$ | $\neg P \lor \neg Q$ |
| --- | --- | ------------------ | -------------------- |
| $F$ | $F$ | $T$                | $T$                  |
| $F$ | $T$ | $T$                | $T$                  |
| $T$ | $F$ | $T$                | $T$                  |
| $T$ | $T$ | $F$                | $F$                  |
De waarheidstabellen geven dezelfde uitkomsten, dus $\neg (P \land Q) \equiv \neg P \lor \neg Q$.

**Opgave 1.2:**
Welke van de volgende beweringen zijn logisch equivalent? Vind de paren.

**Opgave 1.3:** Bepaal de waarheidstabel van $\neg (P \rightarrow Q)$. Geef een equivalente logische formule waar $\rightarrow$ niet voorkomt.

| $P$ | $Q$ | $\neg (P \rightarrow Q)$ | $P \land \neg Q$ |
| --- | --- | ------------------------ | ---------------- |
| $F$ | $F$ | $F$                      | $F$              |
| $F$ | $T$ | $F$                      | $F$              |
| $T$ | $F$ | $T$                      | $T$              |
| $T$ | $T$ | $F$                      | $F$              |
De waarheidstabellen geven dezelfde uitkomsten dus $\neg (P \rightarrow Q) \equiv P \land \neg Q$

**Opgave 1.4:** 
(a) Zij $n$ een geheel getal ($\mathbb{Z}$). Bewijs als $n^2$ deelbaar is door $3$, dan is $n$ deelbaar door $3$.

**Opgave 1.5:**
(a) Stel dat $x$ en $y$ oneven zijn. Bewijs dat $x \cdot y$ oneven is.

**Definitie van oneven**: Als $x$ oneven is dan is $x = 2k + 1$ met een geheel getal $k$

**Bewijs.**
- Als $x, y$ oneven zijn dan is $x = 2k + 1$ en $y = 2l + 1$ met gehele getallen $k, l$.
- $x \cdot y$ geeft $(2k + 1)(2l + 1) = 4kl + 2k + 2l + 1 = 2(2kl + k + l) + 1$
- Omdat $k,l \in \mathbb{Z}$, geldt $m = 2kl + k + l \in \mathbb{Z}$. Dan krijgen we $x \cdot y = 2m + 1$
- Dus $x \cdot y$ is oneven.
$\square$

(b) Stel dat $x \cdot y$ even is. Bewijs dat $x$ of $y$ even moet zijn.

**Definitie van even**: Als $x$ even is dan is $x = 2k$.
