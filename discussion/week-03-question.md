---
id: w03-heta2-ridge-stability-predictions
title: "Ridge stabilizes coefficients but not fits"
author: "Heta Patel (heta2)"
---

Ridge regression can dramatically stabilize individual coefficient estimates for nearly collinear predictors without much changing the fitted values, because the difference direction has a tiny singular value and carries little predictive information. But if the true coefficients along that pair are unequal (say $\beta_1 = 3$, $\beta_2 = 0$), ridge shrinks them toward each other and introduces large individual bias. Does this coefficient bias necessarily hurt prediction accuracy, or can the fitted values $\mathbf{X}\widehat{\boldsymbol\beta}_\lambda$ remain nearly unbiased? How does the answer depend on the smallest singular value relative to $\sqrt{n\lambda}$?
