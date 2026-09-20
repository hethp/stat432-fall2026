---
id: w04-heta2-lasso-sparsity-geometry
title: "Why lasso zeros out but ridge does not"
author: "Heta Patel (heta2)"
---

The lasso and ridge penalties both shrink coefficients toward zero, but only the lasso sets coefficients exactly to zero. The ridge solution $\widehat\beta_j = a_j / (1 + n\lambda)$ rescales the score by a factor strictly between zero and one, so it never reaches zero for a nonzero score. The lasso solution $\widehat\beta_j = S(a_j, \lambda)$ applies soft thresholding, which maps the entire interval $[-\lambda, \lambda]$ to zero. Geometrically, the $\ell_1$ ball has corners on the coordinate axes, and the contour of the quadratic loss is more likely to first touch a corner than a smooth point, producing an exact zero. If we replaced the $\ell_1$ penalty with an $\ell_q$ penalty for some $q \in (1, 2)$, would the resulting estimator still produce exact zeros, or does the sparsity property disappear as soon as $q > 1$?