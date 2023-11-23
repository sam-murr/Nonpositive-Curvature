```ad-Definition
title:Definition: Submersion
A <u>submersion</u> $f:\R^k\to\R^{k-n}$ differentiable such that for all $x$, $f(x) = 0$ implies $D_xf$ has full rank. Then, $\{x\in\R^k: f(x) = 0\}$ is an<u> $n$ dimensional differentiable manifold</u> with <u>tangent space</u> at point $p$ is $\ker D_p f$.
```
```ad-Example
- $f:\R^{n+1}\to \R$ via $f(x) = \inner x x -1$. This results in a differentiable manifold structure on $\sph^n = f^{-1}(\{0\})$.
- $f:\R^{n+1}\to \R$ via $f(x) = \pr x x +1$. This results in a differentiable manifold structure on $\HP^n \subseteq f^{-1}(\{0\})$.
```
```ad-Definition
title:Definition: Riemannian Metric
A <u>Riemannian Metric</u> on a differentiable manifold $X$ is a continous choice of inner product $\inner \cdot\cdot _p$ on the tangent space of each point $p$.
```
```ad-Definition
title:Definition: Riemannian Length
Given a Riemannian metric</u> on a differentiable manifold $X$ and a piecewise differentiable path $c:[a,b]\to X$, the <u>Riemannian Length</u> of $c$ is:
$$
\len(c) = \int_a^b \sqrt{\inner{\dot{c}(t)}{\dot{c}(t)}_{c(t)}} dt
$$
We can then define the <u>global riemannian metric</u> $d':X^2\to \R$ via:
$$
d'(x,y) = \inf\{\len(c): c\text{ is a piecewise differentiable path from }x \text{ to }y\}
$$
```

```ad-Proposition
- $d'$ is a metric which generates the induced topology on the manifold $X$.
- If $X$ is connected and $d'$ is complete, then $(X,d')$ is geodesic.
```

```ad-Definition
title:Definition: Riemannian Angle
Let $c_0,c_1:[0,a]\to X$ be differentiable curves starting from a point $x$. The <u>Riemannian Angle</u> between $c_0$ and $c_1$ is:
$$
\angle(c_0,c_1) = \arccos{\frac{\inner {\dot{c}_0(0)}{\dot{c}_1(0)}_x}{\sqrt{\inner{\dot{c}_0(0)}{\dot{c}_0(0)}_x\inner{\dot{c}_1(0)}{\dot{c}_1(0)}_x}}}
$$
```

```ad-Proposition
The Riemannian angle is the same as the [[Alexanderov Angle]]
```
```ad-Proposition
For every $\kappa$, the global riemannian metric $d'$ on $M_\kappa^n$ (with the natural choice of riemannian metric $\inner \cdot\cdot _p$) is the same as $d_\kappa$.
```
