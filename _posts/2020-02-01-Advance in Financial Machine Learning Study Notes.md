---
layout: post
title: Advances in Financial Machine Learning Study Notes
---

My study notes for the book written by Marcos Lopez de Prado, Advances in Financial Machine Learning. This post is just for personal study purpose, not for any commercial uses. If you are interested in the contents please [purchase the book](https://www.amazon.com/Advances-Financial-Machine-Learning-Marcos/dp/1119482089).

### Structure of Modern Quantitative Asset Managers

#### - Data Curators
This is the station responsible for collecting, cleaning, indexing, storing, adjusting, and delivering all data to the production chain.
#### - Feature Analysts
This is the station responsible for transforming raw data into informative signals. These informative signals have some predictive power over financial variables. Team members are experts in information theory, signal extraction and processing, visualization, labeling, weighting, classifiers, and feature importance techniques.
#### - Strategists
In this station, informative features are transformed into actual investment algorithms. A strategist will parse through the libraries of features looking for ideas to develop an investment strategy. These features were discovered by different analysts studying a wide range of instruments and asset classes. The goal of the strategist is to make sense of all these observations and to formulate a general theory that explains them.
Therefore, the strategy is merely the experiment designed to test the validity of this theory. Team members are data scientists with a deep knowledge of financial markets and the economy. Remember, the theory needs to explain a large collection of important features. In particular, a theory must identify the economic mechanism that causes an agent to lose money to us. Is it a behavioral bias? Asymmetric information? Regulatory constraints? **Features may be discovered by a black box, but the strategy is developed in a white box. (My favorite line in premable)**  Gluing together a number of catalogued features does not constitute a theory.
#### - Backtesters
This station assesses the profitability of an investment strategy under various scenarios. One of the scenarios of interest is how the strategy would perform if history repeated itself. However, the historical path is merely one of the possible outcomes of a stochastic process, and not necessarily the most likely going forward. Alternative scenarios must be evaluated, consistent with the knowledge of the weaknesses and strengths of a proposed strategy. Team members are data scientists with a deep understanding of empirical and experimental techniques. A good backtester incorporates in his analysis meta-information regarding how the strategy came about. In particular, his analysis must evaluate the probability of backtest overfitting by taking into account the number of trials it took to distill the strategy.
#### - Deployment Team
The deployment team is tasked with integrating the strategy code into the production line. Some components may be reused by multiple strategies, especially when they share common features. Team members are algorithm specialists and hardcore mathematical programmers. Part of their job is to ensure that the deployed solution is logically identical to the prototype they received. It is also the deployment team’s responsibility to optimize the implementation sufficiently, such that production latency is minimized. As production calculations often are time sensitive, this team will rely heavily on process schedulers, automation servers (Jenkins), vectorization, multithreading, multiprocessing, graphics processing unit (GPU-NVIDIA), distributed computin (Hadoop), high-performance computing (Slurm), and parallel computing techniques in general.
##### - Portfolio Oversight
Once a strategy is deployed, it follows a cursus honorum, which entails the following stages or lifecycle:
1. **Embargo:** Initially, the strategy is run on data observed after the end date of the backtest. Such a period may have been reserved by the backtesters, or it may be the result of implementation delays. If embargoed performance is consistent with backtest results, the strategy is promoted to the next stage.
2. **Paper Trading:** At this point, the strategy is run on a live, real-time feed. In this way, performance will account for data parsing latencies, calculation latencies, execution delays, and other time lapses between observation and positioning. Paper trading will take place for as long as it is needed to gather enough evidence that the strategy performs as expected.
3. **Graduation:** At this stage, the strategy manages a real position, whether in isolation or as part of an ensemble. Performance is evaluated precisely, including attributed risk, returns, and costs.
4. **Re-allocation:** Based on the production performance, the allocation to graduated strategies is re-assessed frequently and automatically in the context of a diversified portfolio. In general, a strategy’s allocation follows a concave function. The initial allocation (at graduation) is small. As time passes, and the strategy performs as expected, the allocation is increased. Over time, performance decays, and allocations become gradually smaller.
5. **Decommission:** Eventually, all strategies are discontinued. This happens when they perform below expectations for a sufficiently extended period of time to conclude that the supporting theory is no longer backed by empirical evidence.
In general, it is preferable to release new variations of a strategy and run them in parallel with old versions. Each version will go through the above lifecycle, and old strategies will receive smaller allocations as a matter of diversification, while taking into account the degree of confidence derived from their longer track record.

### Common Pitfalls in Financial Machine Learning
#### 1. The Sisyphus paradigm - Epistemological
**Solution: The meta-strategy paradigm**

#### 2. Research through backtesting - Epistemological
**Solution: Feature importance analysis**

#### 3. Chronological sampling - Data Processing
**Solution: The volume clock**

#### 4. Integer differentiation - Data Processing
**Solution: Fractional differentiiation**

#### 5. Fixed-time horizon labeling - Classification
Label return series using fixed time horizon, why not? 1. time bars do not exhibit good statistical properties. 2. the same threshold for assigning class applied regardless of the observed volatility.
Naive solution: compute dynamic thresholds based on exponentially weighted moving standard deviation.
**Solution: The triple-barrier method**

#### 6. Learning side and size simultaneously - Classification
**Solution: Meta-labeling**

#### 7. Weighting of non-IID samples - Classification
**Solution: Uniqueness weighting: sequential bootstrapping**

#### 8. Cross-validation leakage - Evaluation
**Solution: Purging and embargoing**

#### 9. Walk-forward (historical) backtesting - Evaluation
**Solution: Combinatorical purged cross-validation**

#### 10. Backtest overfitting - Evaluation
**Solution: Backtesting on synthetic data: the deflated Sharpe ratio**

