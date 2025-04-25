# Government Spending Perception Analysis

## Introduction

This project investigates how citizens perceive the government's use of tax money. Specifically, it addresses the questions:
- Is tax money used wisely?
- How many cents out of every tax dollar do people believe the government wastes?
- What comes to mind when people think of government waste?

We analyze these perceptions using regression models, examining how they relate to political affiliation, income, media consumption, tax payment behavior, and other socioeconomic factors.

The approach follows guidance from _"Regression and Other Stories"_ by Gelman, Hill, and Vehtari (2020), with an emphasis on Bayesian modeling, model diagnostics, and interpretability.

## Data

The dataset includes variables such as:
- `is_money_used_wisely`: binary or ordinal responses about the perception of tax usage.
- `wastecent`: numeric estimate (0–100) of how many cents per dollar are believed to be wasted.
- `wastethink`: open-text responses about what respondents associate with waste.
- Demographic and behavioral variables: political affiliation, income, tax status, media habits, etc.

These variables allow us to explore both quantitative and qualitative insights into public trust and perception of government spending.

## Project Goals

- Identify key predictors of waste perception.
- Estimate how political and economic variables shape these beliefs.
- Build interpretable and validated regression models using Bayesian tools.

## Modeling Approach

We employ Bayesian regression models, including:

- **Linear regression** (e.g., modeling `wastecent` as a function of political affiliation, income, etc.)
- **Logistic regression** (e.g., binary classification for "Is money used wisely?")
- **Models with interactions**, allowing relationships to differ by political group, income level, etc.

### Prior Selection

Priors are chosen based on domain knowledge or weakly informative defaults:
- Normal(0, 1) for standardized predictors
- Cauchy(0, 2.5) for logistic regression coefficients

## Implementation

Models are implemented using:

- [`brms`](https://paul-buerkner.github.io/brms/)
- [`rstanarm`](https://mc-stan.org/rstanarm/)
- [`rstan`](https://mc-stan.org/)
- [`JAGS`](https://mcmc-jags.sourceforge.io/)


