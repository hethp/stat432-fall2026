---
id: w09-heta2-kernel-trick-example
title: "How does the kernel trick avoid explicit feature mapping?"
author: "Heta Patel (heta2)"
---

Consider two observations in $\mathbb{R}^2$: $\mathbf{a} = (1, 2)$ and $\mathbf{b} = (3, 1)$. A degree-2 polynomial kernel is $K(\mathbf{a}, \mathbf{b}) = (1 + \mathbf{a}^\mathsf{T} \mathbf{b})^2$. Compute $K(\mathbf{a}, \mathbf{b})$ directly from this formula. Then write out the expanded feature map $\phi(\mathbf{x})$ that includes all monomials up to degree 2, compute $\phi(\mathbf{a})$ and $\phi(\mathbf{b})$, and verify that $\phi(\mathbf{a})^\mathsf{T} \phi(\mathbf{b})$ gives the same value. Why is the kernel formula cheaper, and at what dimension $p$ would this computational savings start to matter in practice?
