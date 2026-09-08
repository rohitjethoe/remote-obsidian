---
title: Calculus (6011PN166Y)
---
#### Beweringen
---
Logica kent **connectieven** om beweringen en logische formules samen te stellen
- **Negatie**: $\neg P$
- **Conjunctie**: $P \land Q$
- **Disjunctie**: $P \lor Q$
- **Implicatie**: $P \Rightarrow Q$
- **Equivalentie**: $P \Leftrightarrow Q$

Als er $n$ variabelen zijn, dan zijn er $2^n$ rijen in ons **waarheidstabel**.

#### Verzamelingen
---
Een **verzameling** = een collectie van objecten
- $S = \{\text{koe}, \text{varken}, \text{olifant}\}$
- Objecten zijn de elementen van $S$ en $\text{koe} \in S$ ("koe is een element van $S$")

Veelvoorkomende verzamelingen zijn:
- Lege verzameling: $\emptyset = \{\}$
- Natuurlijke getallen: $\mathbb{N} = \{1,2,3,4,...\}$
- Gehele getallen: $\mathbb{Z} = \{..., -2, -1, 0, 1, 2, ...\}$
- Rationale getallen: $\mathbb{Q} = \{\dfrac{p}{q} : p, q \in \mathbb{Z} \land q \neq 0\}$
- Reële getallen: $\mathbb{R}$
- Gesloten interval: $[a, b] = \{x \in \mathbb{R} : a \le x \le b\}$ 

#### Kwantoren
---
Veelvoorkomende kwantoren zijn:
- Universele kwantoor $\forall x$
- Existentiële kwantoor $\exists x$

1. $\exists n (n \gt 3)$ betekent "er bestaat een getal groter dan 3".
2. $\forall n (n \in \mathbb{N} \Rightarrow n \gt 0)$ betekent "ieder natuurlijk getal is positief".

Voor dit soort uitspraken is **het universum** belangrijk:
- De eerste uitspraak is waar als we $\mathbb{R}$ bekijken maar onwaar als we $[0,1]$ bekijken
	- $\forall n \in \mathbb{N}, n + 1 > n = T$ 

#### Bewijzen met inductie
---
Stel we willen bewijzen dat een uitspraak geldt voor alle natuurlijke getallen. Toon aan dat:
1. De uitspraak geldt voor $n = 1$
2. Als de uitspraak geldt voor $n$, dan ook $n + 1$.

**Claim**: voor alle $n \in \mathbb{N}$ geldt $1 + 2 + ... + n = \dfrac{n(n + 1)}{2}$
- **Basisstap** ($n = 1$): Stel dat $n = 1$. Dat geeft $\dfrac{1(2)}{2} = 1$.
- Neem aan dat $P(n)$ geldt voor een zekere $n$. Dit geeft de **inductiehypothese** $1 + 2 + ... + n = \dfrac{n(n + 1)}{2}$
- **Inductiestap:** gebruik de inductiehypothese om het resultaat voor $n + 1$ te bewijzen

$1 + 2 + ... + n + (n + 1) = \dfrac{n(n+1)}{2} + (n + 1)$
$= \dfrac{n^2 + n}{2} + (n + 1) = \dfrac{n^2 + n}{2} + \dfrac{2(n + 1)}{2} = \dfrac{n^2 + n}{2} + \dfrac{2n + 2}{2}$
$= \dfrac{n^2 + 3n + 2}{2} = \dfrac{(n + 2)(n + 1)}{2}$

- **Conclusie:** het resultaat geldt voor alle $n \in \mathbb{N}$


**Bewijs** dat $2^{3n} - 1$ deelbaar is door $7$ voor alle $n \in \mathbb{N}$

- **Basisstap**: $n = 1$ geeft $2^{3 \cdot 1} - 1 = 2^3 - 1 = 8 - 1 = 7$. Dus voor $n = 1$ is de bewering waar.
- **Inductiehypothese**: Neem aan dat $2^{3n} - 1$ deelbaar is door 7 voor een zekere $n \in \mathbb{N}$. Dan bestaat er een $k \in \mathbb{Z}$ z.d.d. $2^{3n} - 1 = 7k$ 
- **Inductiestap**: bewijs de uitspraak voor $n + 1$

$2^{3(n + 1)} - 1 = 2^{3n + 3} - 1 = 2^{3n} \cdot 2^3 - 1 = 2^{3n} \cdot 8 - 1$
$= 8 \cdot (7k + 1) - 1 = 56k + 7 = 7 \cdot 8k + 7 = 7 \cdot (8k + 1) = 7k'$ met $k' = 8k + 1 \in \mathbb{Z}$

- **Conclusie**: Dus de uitspraak geldt voor $n + 1$. De claim volgt uit het principe van volledige inductie.

**Extra:** Paradox van Russell
- Bekijk de verzameling van verzamelingen die geen element van zichzelf zijn:
- $S = \{K : K \text{ is een verzameling en } K \notin K\}$ 
- Geldt nu $S \in S$?

Stel dat $S \in S$. Dan geldt $S \notin S$ (Tegenspraak). Dus $S \notin S$. Maar dan is $S \in S$. 

- **Conclusie:** de verzameling $S$ bestaat niet! Niet alles is een verzameling.