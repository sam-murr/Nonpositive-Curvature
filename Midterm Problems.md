```ad-Exercise
title:Exercise 1
Consider the metric on $\R^n$ via:
$$
d(x,y) = \sqrt[3]{|x_1-y_1|^3+\dots+|x_n-y_n|^3}
$$
Is this metric space geodesic? For which points are the geodesics unique?
```
__Proof__:
Straight lines are geodesics. Take $u,v\in\R^n$, $l(t):[0,d(u,v)]\to \R^n$ via $l(t) = u(1-\frac{t}{d(u,v)}) + v\frac{t}{d(u,v)}$. Then:
$$
\begin{align}
d(l(t),l(t')) &= \sqrt[3]{|\frac{1}{d(u,v)}(t-t')(u_1-v_1)|^3+\dots+|(\frac{1}{d(u,v)}t-t')(u_n-v_n)|^3}\\
&= \frac{1}{d(u,v)}|(t-t')|\sqrt[3]{|(u_1-v_1)|^3+\dots+|(u_n-v_n)|^3}\\
&= |t-t'|
\end{align}
$$
