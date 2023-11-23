```ad-Lemma
title: Lemma: Minkowski Bilinear Form is Positive Definite on $v^\perp$
If $v\in\R^{n+1}$, $\pr v v < 0$, then $\pr \cdot\cdot$ is positive definite on $v^\perp =\{u\in\R^{n+1}: \pr u v = 0\}$
```
__Proof__:
Take $u\in v^\perp$. Since $\pr v v \neq 0$, $u$ and $v$ are linearly independent so span a 2d subspace $V$. If $\pr u u< 0$, then $\pr \cdot\cdot$ is negative definite on $V$, however $V$ must intersect $\R^{n}$ (the first $n$ coordinates), over which $\pr \cdot\cdot$ is positive definite, which is a contradiction. $\square$