---
id: w07-heta2-lda-qda-pooling-tradeoff
title: "When does pooling covariance matrices help despite being wrong?"
author: "Heta Patel (heta2)"
---

LDA assumes every class shares the same covariance matrix and pools the data to estimate one $\Sigma$. QDA drops that assumption and estimates a separate $\Sigma_k$ for each class. When the true class covariances genuinely differ, LDA's pooled estimate is biased because it averages two different structures into one. Yet in the Homework 7 simulation (Question 3) we saw that LDA still beats QDA at small values of $\rho$, even though the two classes already have different covariance matrices (one with off-diagonal $\rho$ and the other with $-\rho$). The advantage disappears only as $\rho$ grows large enough for the bias to dominate. Intuitively, QDA must estimate more parameters — a full $p \times p$ covariance matrix per class — so with a small training set its estimates are noisier, and that extra variance can outweigh LDA's bias.

Suppose you have a two-class problem with $p = 5$ predictors and only $n_k = 20$ observations per class, and you suspect the class covariances differ moderately. From the bias-variance perspective, why might LDA's pooled covariance estimate still produce lower test error than QDA's per-class estimates in this setting, even though pooling introduces bias? In your explanation, consider how the number of free parameters each method must estimate compares to the available sample size.