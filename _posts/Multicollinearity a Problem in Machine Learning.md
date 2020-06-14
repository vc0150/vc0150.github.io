---
layout: post
title: Machine Learning Fundamentals
---

### Bias Variance Tradeoff

#### Definition
Total Error = Bias² + Variance + Irreducible errors

**Bias** of an estimator is the the “expected” difference between its estimates and the true values in the data.
Bias[g(xₒ)] = E[g(xₒ)] − f(xₒ)

**Variance** of an estimator is the “expected” value of the squared difference between the estimate of a model and the “expected” value of the estimate(over all the models in the estimator).
Var[g(xₒ)] = E[(g(xₒ) − E[g(xₒ)])²]

#### Bias Variance Decomposition
Err(xₒ) = E[(Y − g(xₒ))² | X = xₒ]
= E[(f + ϵ − g)²]
= E[ϵ²] + E[(f − g)²] + 2.E[(f − g)ϵ]
= E[(ϵ − 0)²] + E[(f − E[g] + E[g] − g)²] + 2.E[fϵ] − 2.E[gϵ]
= E[(ϵ − E[ϵ])²] + E[(f − E[g] + E[g] − g)²] + 0 − 0
= Var(ϵ) + E[(g − E[g])²] + E[(E[g] − f)²] + 2.E[(g − E[g])(E[g] − f)]
= Var(ϵ) + Var(g) + Bias(g)² + 2.{E[g]² − E[gf] − E[g]² + E[gf]}
= σ² + Var(g) + Bias(g)²
