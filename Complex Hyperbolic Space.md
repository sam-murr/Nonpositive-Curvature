```ad-Definition
title:Definition: Extended Minkowski Bilinear Form and Complex Hyperbolic Space
We may extend the [[Geometry of Hyperbolic Space|minkowski bilinear form]] on $\R^{n+1}$ to $\C^{n+1}$ via:
$$
\pr x y = \sum_{i=0}^{n-1}\bar{x}_iy_{i} - \bar{x}_{n}y_{n}
$$
Previously, we defined [[Geometry of Hyperbolic Space|real hyperbolic space]] by the upper sheet of the surface defined by $(x,y) = -1$. We could have instead identified points in the hyperbolic space with lines through the origin intersecting that surface (ie the image of the interior of the ligth cone $\pr x x < 0$ under the projective map).


Similarly, we will define <u>complex hyperbolic space</u> $\C H^n$ as the set of $[x]$ in complex projective space (ie identfying one dimensional linear subspaces of $\C^{n+1})$ such that $(x,x) < 0$.
```

```ad-Proposition
title:Proposition: General Minkowski Bilinear Form Lemma
For any $x\in \C^{n+1}$ with $\pr x x <0$, $\pr \cdot \cdot$ is positive definite on $x^\perp$
```
__Proof__: This is the same as the $\R^{n+1}$  [[Minkowski Bilinear Form Lemma|proof]], since $\pr \cdot \cdot$ is positive definite on the copy of $\C^{n}$ in $\C^{n+1}$ with last coordinate $0$. $\square$


```ad-Lemma
title: Lemma: Reverse Schwartz Inequality
If $x,y\in \C^{n+1}$ with $\pr x x <0$ and  $\pr y y <0$:
$$
\pr x y \pr y x \geq \pr x x \pr y y
$$
With equality when $x = r y$ for some $r\in \C$.
```

__Proof__: If $x = ry$, then both sides are just $||r||^2\pr x x^2$. By the previous proposition, we know that since $\pr y y <0$, $\pr x y\neq 0$. Let $\lambda = \frac{-\pr x x}{\pr x y}$, then $x+\lambda y = x^\perp$ so we have:
$$
\begin{align}
0 < &\pr {x+\lambda y}{x+\lambda y} \\
=&\pr {x+\lambda y}{x} +\pr {x+\lambda y}{\lambda y} \\
=&\pr {x}{\lambda y}+\pr{\lambda y}{\lambda y}\\
=&\frac{-\pr x x}{\pr x y}\pr {x}{ y}+\frac{\pr x x\pr x x}{\pr x y\pr y x}\pr{y}{y}\\
=&-\pr x x+\frac{\pr x x\pr x x}{\pr x y\pr y x}\pr{y}{y}\\
1>&\frac{\pr x x}{\pr x y\pr y x}\pr{y}{y}\\
\pr x y\pr y x>&\pr x x\pr{y}{y}\\
\end{align}
$$
Note the inequality flipped because we divide by $\pr x x < 0$. $\square$



```ad-Definition
title:Definition: Metric on Complex Hyperbolic Space
For $[x], [y]\in \C H^n$, define the distance $d([x],[y])$ to be the unique nonegative real $d\in\R$ with:
$$
\cosh^2d = \frac{\pr x y \pr y x}{\pr x x \pr y y}
$$
```
```ad-Proposition
This defines a metric on $\C H^n$
```
__Proof__: Since the expression is symmetric and $\frac{\pr x y \pr y x}{\pr x x \pr y y} \geq 1$ with equality iff $x = y$, this definition satisfies the first two properties of a [[Classes/Metric Spaces with Nonpositive Curvature/Copied Notes for GIT/Metric Space|metric]]. The triangle inequality follows from a version of the law of cosines for $\C H^n$. $\square$