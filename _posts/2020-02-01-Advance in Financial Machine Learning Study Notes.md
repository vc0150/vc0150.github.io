---
layout: post
title: Advances in Financial Machine Learning Study Notes
---

My study notes for the book written by Marcos Lopez de Prado, Advances in Financial Machine Learning.

#### Structure of Modern Quantitative Asset Managers

- ##### Data Curators
This is the station responsible for collecting, cleaning, indexing, storing, adjusting, and delivering all data to the production chain.
- ##### Feature Analysts
This is the station responsible for transforming raw data into informative signals. These informative signals have some predictive power over financial variables. Team members are experts in information theory, signal extraction and processing, visualization, labeling, weighting, classifiers, and feature importance techniques.
##### Strategists
In this station, informative features are transformed into actual investment algorithms. A strategist will parse through the libraries of features looking for ideas to develop an investment strategy. These features were discovered by different analysts studying a wide range of instruments and asset classes. The goal of the strategist is to make sense of all these observations and to formulate a general theory that explains them.
Therefore, the strategy is merely the experiment designed to test the validity of this theory. Team members are data scientists with a deep knowledge of financial markets and the economy. Remember, the theory needs to explain a large collection of important features. In particular, a theory must identify the economic mechanism that causes an agent to lose money to us. Is it a behavioral bias? Asymmetric information? Regulatory constraints? #####Features may be discovered by a black box, but the strategy is developed in a white box. Gluing together a number of catalogued features does not constitute a theory.
##### Backtesters
##### Deployment Team
##### Portfolio Oversight
