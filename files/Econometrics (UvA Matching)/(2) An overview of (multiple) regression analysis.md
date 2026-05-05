---
title: Econometrics (UvA Matching)
---
### Extending the Notation
---
The general case: **multiple regression**
$$Y_i = \beta_0 + \beta_1 X_{1i} + \beta_2 X_{2i} + \beta_3 X_{3i} + \epsilon_i \text{ where } \{i \in 1,2,...,N\}$$
Each of the slope coefficients gives the impact of a one-unit increase in the corresponding $X$ variable on $Y$, holding the other included independent variables constant (i.e. **ceteris paribus**)
- Ceteris paribus is a Latin phrase meaning all other things being equal

As an (implicit) consequence of this, the impact of variables that are **not included** in the regression are **not held constant**

If a variable is not included in the equation, than it's impact is not held constant in the estimation of the regression coëfficiënts.

### Wage Regression
---
Let wages ($\text{WAGE}$) depend on:
- years of experience ($\text{EXP}$)
- years of education ($\text{EDU}$)
- gender of the worker ($\text{GEND}$: $1$ if male, $0$ if female)

Substituting into the **multiple regression** equation yields:
$$\text{WAGE } = \beta_0 + \beta_1 \text{EXP}_i + \beta_2 \text{EDU}_i + \beta_3 \text{GEND}_i + \epsilon_i$$

### Indexing Conventions
---
- Subscript "$i$" for data on individuals (i.e. "**cross section**" data)
	- Could represent a person or a firm
	- $i$ = individuals
- Subscript "$t$" for **time series** data (e.g. series of years, months or days—e.g. daily exchange rates)
	- $t$ = time
- Subscript "$it$" when we have **both** (for example, "panel data")
	- A group of persons, e.g. students over time

### Estimated Regression Equation
---
The regression equation considered so far is the "**true**" —but unknown—**theoretical** regression equation

Instead of "true", might think about this as the **population** regression against the **sample/estimated** regression

How do we obtain the empirical counterpart of the theoretical regression model?
$$Y_i = \beta_0 + \beta_1 X_i + \epsilon_i$$
- It has to be **estimated**
- This regression equation is purely abstract in nature
	- $\beta_0$ and $\beta_1$ are unknown
	- We have to estimate their values using data on $Y$ and $X$

The empirical counterpart to $Y_i = \beta_0 + \beta_1 X_i + \epsilon_i$ is:
$$\hat{Y}_i = \hat{\beta}_0 + \hat{\beta}_1X_i$$
- The signs on top of the estimates are denoted "hat", so that we have "$Y$-hat"
- For each sample we get a **different** set of estimated regression coefficients
- $\hat{Y}_i$ is the **estimated** value of $Y_i$ (i.e. the dependent variable for observation $i$); similarly it is the **prediction** of $E(Y_i|X_i)$
- The **closer** $\hat{Y}_i$ is to the **observed** value of $Y_i$, the better is the "**fit**" of the equation

Similarly, the **smaller** the estimated error term $e_i$ (also called **"residual"**), the better is the fit.

This can also be seen from the fact that:
$$e_i = Y_i - \hat{Y}_i$$
- This residual in an empirical counterpart of the error term
Note difference with the error term, $\epsilon_i$ given as:
$$\epsilon_i = Y_i - E[Y_i|X_i]$$
- The error term is un-observable and is therefore indicated by greek letter $\epsilon$ because it depends on unknown parameters

### Explain Housing Prices
---
Houses are not homogenous products, so how to appraise a house against a given asking price?

Many real-estate appraisers actually use regression analysis for this

Suppose the asking price was **230.000 USD**
- Is this fair / too much / too little?
- Depends on size of house (higher size, higher price)
- Collect cross-sectional data on prices (in thousands of USD) and sizes (in square feet) for, say, 43 houses
- Then we say this yields the following estimated regression line
$$\widehat{\text{PRICE}} = 40.0 + 0.138 \cdot \text{SIZE}_i$$
- If size increases by 1 square feet, price increases by 138 USD

We simplified a lot in this example by assuming that **only** size matters for housing prices

### Key Terms
---
- Regression analysis
- Dependent variable
- Independent (or explanatory) variable(s)
- Causality
- Stochastic error term
- Linear
- Intercept term
- Slope coefficient
- Multiple regression model
- Expected value
- Time series
- Cross-sectional data set

### Oefenvragen
---
**Q:** Als een geschatte regressielijn een intercept heeft van 10 en een hellingscoëfficiënt van 4, dan is wanneer _X_ = 2 de werkelijke waarde van Y
**A:** 18

**Q:** Een regressieanalyse tussen de verkoop (in €1000) en reclame (in €100) resulteerde in de volgende kleinste kwadraten regressielijn $\hat{Y} = 75 + 6X$
**A:** 4875 EUR

**Q:** Het residu wordt gedefinieerd als het verschil tussen
**A:** De werkelijke waarde van $Y$ en de geschatte waarde van $Y$

1a) Per feet vanaf de putt gaat het percentage van geslaagde putts met 4.1% omlaag.  
  
1b) Expected value  
  
1c)  
83.6 - (4.1 * 10) = 42.6

83.6 - (4.1 * 1) = 79.5

83.6 - (4.1 * 25) = -18.9

De resultaten van 10 feet en 1 feet lijken realistisch, die van 25 feet niet.  
  
1d) Dat procentuele waardes van kansen enkel tussen 0 en 100 kunnen liggen, maar dat onze functie een waarde schatte die onder de 0 ligt.

2a) 
- Als het inkomen met 1 USD stijgt dan stijgt de verwachte gift met 0,001 USD, wat mij een redelijk bedrag lijkt omdat dat ongeveer 0.1% is van het inkomen
- Voor ieder extra belletje stijgt de verwachte donatie met 4.62 USD, wat mij onredelijk lijkt omdat het een stuk hoger is dan de minimale donatie per alumni van 2.29 USD

2b) Omdat de waardes geschat moeten worden, dus spreek uit als 'hat'-GIFT.

2c)  Nee, de stochastic error hoort bij de unobservable relatie

2d) De coëfficient van het inkomen wordt 1 en derest van de coëfficienten blijven onveranderd. De donatie t.o.v. het inkomen moet evenredig groeien om hetzelfde effect weer te geven. Per belletje wordt nogsteeds 4.62 USD gedoneerd en de minimale jaarlijkse donatie blijft 2.29

2e) Tijdsduur van het belletje; per minuut dat er is gesproken hoe meer wordt gedoneerd in USD

