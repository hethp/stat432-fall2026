---
id: w10-heta2-mtry-tree-correlation
title: "Why does smaller mtry reduce forest variance?"
author: "Heta Patel (heta2)"
---

In bagging, all trees consider all $p$ predictors at every split. Random forests introduce feature subsampling by selecting split variables from a random subset of $m < p$ candidate predictors (`mtry`). The variance of an average of $B$ identically distributed trees, each with variance $\sigma^2$ and positive pairwise correlation $\rho$, is given by:

$$
\text{Var}(\bar{T}) = \rho \sigma^2 + \frac{1 - \rho}{B} \sigma^2.
$$

As the number of trees $B \to \infty$, the second term approaches zero, but the irreducible floor $\rho \sigma^2$ remains. Although reducing $m$ may make individual trees weaker and slightly increase individual variance $\sigma^2$, it substantially decreases the pairwise tree correlation $\rho$. Under what data conditions (such as the presence of a few dominant predictors) does the reduction in $\rho$ outweigh the increase in $\sigma^2$, and why does setting $m$ too small eventually degrade predictive performance by inflating bias?
