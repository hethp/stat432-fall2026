---
id: w11-heta2-scaling-distance
title: "How does feature scaling alter cluster distance?"
author: "Heta Patel (heta2)"
---

Consider three individuals measured on Age (years) and Annual Income (dollars):
- Person $A$: $(30, 50000)$
- Person $B$: $(31, 50050)$
- Person $C$: $(60, 50000)$

Using Euclidean distance in raw units:

$$
d(A, B) = \sqrt{(31 - 30)^2 + (50050 - 50000)^2} = \sqrt{1 + 2500} \approx 50.01
$$

$$
d(A, C) = \sqrt{(60 - 30)^2 + (50000 - 50000)^2} = \sqrt{900 + 0} = 30.00
$$

Here, Person $A$ (age 30) is deemed closer to Person $C$ (age 60, a 30-year difference) than to Person $B$ (age 31, a 1-year difference), simply because income has a larger numerical scale. If income is instead measured in thousands of dollars, $d(A, B) \approx 1.00$ while $d(A, C) = 30.00$, reversing the nearest neighbor.

How does standardizing each feature to unit variance prevent clustering algorithms from being dominated by arbitrary unit choices, and in what practical setting might an analyst deliberately choose not to standardize variables before clustering?
