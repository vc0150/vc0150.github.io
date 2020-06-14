---
layout: post
title: Machine Learning Fundamentals
---

### Bias Variance Tradeoff

Total Error = Bias² + Variance + Irreducible errors

Bias of an estimator is the the “expected” difference between its estimates and the true values in the data.
Bias[g(xₒ)] = E[g(xₒ)] − f(xₒ)

Variance of an estimator is the “expected” value of the squared difference between the estimate of a model and the “expected” value of the estimate(over all the models in the estimator).
Var[g(xₒ)] = E[(g(xₒ) − E[g(xₒ)])²]
