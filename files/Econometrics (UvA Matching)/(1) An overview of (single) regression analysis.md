---
title: Econometrics (UvA Matching)
---
### What is Econometrics?
---
Econometrics means **“Economics Measurement”**

**Econometrics** = the **quantitative measurement** and **analysis** of actual economic and business phenomena

It involves 3 subfields:
- Economic Theory (micro, macro and financial economics)
- Statistics
- Mathematics

**Micro-economics**: investigates individual consumers and producers

**Macro-economics**: investigates economic aggregates (like all companies or households in a particular countries) 

**Financial economics**: investigates investments like stock markets, interest rates and inflation

We want to take **equations**, calculate **derivates** to find optimal situations and do a **dynamic analysis** of tracing changes in economic changes over time.

3 major uses of econometrics:
- Describing economics reality
- Testing hypotheses about economic theory
- Forecasting future economic activity

The researcher first asks questions and then uses econometrics to answer them.

Price elasticity = what will happen to the price if the demand goes up? 

### Example
---
Consider the general and purely theoretical relationship
$$Q = f(P, P_s, Y_d)$$
- $Q$ = quantity demanded
- $P$ = price of the product
- $P_s$ = price of a substitute
- $D$ = disposable income

### What is Regression Analysis
---
**Economic theory** can give us the direction of a change (e.g. the change in demand for iPhones following a price decrease/increase)

But what if we want to know not just “how” but als “how much?” Then we’ll need:
- Sample of data
- Way to estimate such a relationship: **regression analysis**

**Regression analysis** = a **statistical technique** that attempts to explain movements in one variable, the **dependent** variable, as a function of movements in a set of other variables, the **independent** (or **explanatory**) variables, through the quantification of a single equation

$$Q = f(P, P_s, Y_d)$$
- $Q$ is the **dependent** variable
- $P, P_s, Y_d$ are the **independent** variables

Don’t be deceived by the words **dependent** and **independent**

A statistically signifcant regression result does **not necessarily** imply **causality**

We also need:
- Economic theory
- Common sense

### Single-Equation Linear Models
---
The simplest example is:
$$ Y = \beta_0 + \beta_1X $$
The $\beta$'s are denoted "**coefficients**"
- $\beta_0$ is the "**constant**" or "**intercept**" term
- $\beta_1$ is the "**slope coefficient**": the amount that $Y$ will change when $X$ increases by one unit
- For a linear model, $\beta_1$ is constant over the entire function

When the equation is **not linear**, use substitution:
- $Y = \beta_0 + \beta_1 X^2$
- $Z = X^2$
- $Y = \beta_0 + \beta_1 Z$
- This redefined equation is now **linear** (in $\beta_0, \beta_1$ and $Y,Z$)

### Coefficients of the Regression Line
---
If $X$ were to increase by one unit from $X_1$ to $X_2$ the difference is indicated by $\Delta X$ 

The value of $Y$ now increases from $Y_1$ to $Y_2$ and the difference is indicated by $\Delta Y$

For linear regression models **the response** in the predicted value of $Y$ is constant and is equal to $\beta_1$

$\beta_1$ = the ratio of the change in $\Delta Y$ to the change in $\Delta X$ 
$$
\text{Slope } = \dfrac{\Delta Y}{\Delta X}
$$

### Single-Equation Linear Models
---
Is $Y = \beta_0 + \beta_1 X$ a complete description of origins of variations in $Y$? No:
- Other potentially important explanatory variables may be missing (e.g. $X_2, X_3$)
- Measurement error
- Incorrect functional form
- Purely random and totally unpredictable occurrences

Inclusion of a “**stochastic error term**” ($\epsilon$) effectively “takes care” of all these sources of variation in $Y$ that are NOT captured by $X$
$$
Y = \beta_0 + \beta_1 X + \epsilon
$$
- Sometimes called disturbance term

Two components in
$$
Y = \beta_0 + \beta_1 X + \epsilon
$$
- **deterministic** component $\beta_0 + \beta_1 X$
- **stochastic/random** component $\epsilon$

Why "**deterministic**"?
- Indicates the value of $Y$ that is determined by a given value of $X$ (which is assumes to be non-stochastic)
- Alternatively, the deterministic component can be thought of as the **expected value** of $Y$ **given** $X$ —namely $E(Y|X)$— the **mean (or average)** value of the $Y$s associated with a **particular value** of $X$

### Aggregate Consumption Function
---
Aggregate consumption as a function of aggregate income may be lower (or higher) than it would otherwise have been due to:
- **Consumer uncertainty** — hard to measure, i.e. is an omitted variable
- Observed consumption may be different from actual consumption due to **measurement error**
- Human behavior always contains some element(s) of pure chance; unpredictable, i.e. random events may increase or decrease consumption at any given time
- The "true" consumption function may be **nonlinear** but a linear one is estimated

Whenever one or more of these factors are at play, the observed $Y$ will differ from the $Y$ predicted from the deterministic part, $\beta_0 + \beta_1 X$

For these reasons, an error-term must be added to all regression equations.

### Extending the Notation
---
Include reference to the number of observations:
- Single-equation linear case:
$$Y_i = \beta_0 + \beta_1 X_i + \epsilon_i (i = 1,2,...,N)$$
- So there are really $N$ equations, one for each observation
- The coefficients, $\beta_0$ and $\beta_1$, are the same
- The values of $Y, X, \epsilon$ **differ** across observations

### Oefenvragen
---
**Q:** Welke van de volgende situaties is een voorbeeld van **causaliteit**?
**A:** De lunch overslaan veroorzaakt honger

**Q:** Welke van deze voorbeelden is GEEN voorbeeld van causaliteit
**A:** Paraplu's veroorzaken regenstormen

**Q:** Beslis of je positieve (+), negatieve (-) of ambigue (?) relaties verwacht tussen de volgende paren afhankelijke en onafhankelijke variabelen (respectievelijk)
**A:**
- i) Netto-investeringen in Nederland in een bepaald jaar en het BBP (Bruto Binnenlands Product) in dat jaar (+)
- ii) De hoeveelheid haar op het hoofd van een mannelijke professor en de leeftijd van die professor (-)
- iii) Het aantal ares graan dat in een seizoen geplant wordt en de prijs van graan aan het begin van dat seizoen (+)
- iv) Het groeipercentage van het BBP in een jaar en de gemiddelde haarlengte in dat jaar (?)

**Q:** Stel $X_1=5$ en $X_2=7$, terwijl $Y_1=5$ en $Y_2=6$. Bepaal de intercept
**A:** De intercept is 2.5 en de helling is 0.5

**Q:** Waarom wordt de foutterm $\epsilon$ gebruikt?
**A:** Het vertegenwoordigt mogelijk verwaarloosde niet-lineariteit, de invloed van weggelaten verklarende variables en een mogelijke meetfout

**Q:** Kunnen we lineaire regressietechnieken toepassen op de volgende vergelijking? 
$$Y = \beta_0 + \beta_1 sin(X)$$
**A:** Ja, maar we moeten de variabele $sin(X)$ herdefiniëren


