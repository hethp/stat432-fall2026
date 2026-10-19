---
id: w08-heta2-svm-cost-bias-variance
title: "Why can a large SVM cost hurt generalization?"
author: "Heta Patel (heta2)"
---

In a linear SVM, increasing the cost parameter $C$ penalizes margin violations more heavily, which shrinks the slack variables toward zero and can eventually produce a classifier with zero training error. Intuitively, zero training error sounds ideal, but cross-validation often selects a moderate $C$ that allows some violations. From a bias-variance perspective, why does forcing the classifier to respect every training point (large $C$, narrow margin) tend to increase variance more than it reduces bias, and how does the width of the margin act as a regularizer that controls this tradeoff?
