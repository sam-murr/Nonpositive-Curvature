```ad-Definition
title:Definition: Submersion
A <u>submersion</u> $f:\R^k\to\R^{k-n}$ differentiable such that for all $x$, $f(x) = 0$ implies $D_xf$ has full rank. Then, $X = \{x\in\R^k: f(x) = 0\}$ is an<u> $n$ dimensional differentiable manifold</u> with <u>tangent space</u> at point $p$ is $T_pX = \ker D_p f$.
```
```ad-Example
- $f:\R^{n+1}\to \R$ via $f(x) = \inner x x -1$. This results in a differentiable manifold structure on $\sph^n = f^{-1}(\{0\})$. Note that $D_xf(p) = \inner x p$, so the tangent space is $x^\perp$.
- $f:\R^{n+1}\to \R$ via $f(x) = \pr x x +1$. This results in a differentiable manifold structure on $\HP^n \subseteq f^{-1}(\{0\})$. Note that $D_xf(p) = \pr x p$, so the tangent space is $x^\perp$ with repsect to $\pr \cdot\cdot$.
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
```ad-Example
title:Example: Riemannian Metrics on $\sph^n$ and $\HP^n$
- For $\sph^n$, recall tangent space of a point $x$ is $x^\perp$, so we can just restrict the usual inner product on $\R^{n+1}$ $\inner \cdot \cdot$ to $x^\perp$.
- For $\HP^n$, recall tangent space of a point $x$ is $x^\perp$ with respect to  $\pr \cdot \cdot$, so we can just restrict the minkowski linear form on $\R^{n+1}$ $\pr \cdot \cdot$ to $x^\perp$, and it will be positive definite since $x\in\HP^n$

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

```ad-Definition
title:Definition: The $\exp$ map
We can define the map $\exp_x:T_xM_\kappa^2 \to\HP^2$ such that the origin $0$ gets mapped to $x$, any other point $v\in\R^2$ gets mapped to the point at distance $||v||$ from $x$ in direction $\frac{v}{||v||}$ (here and below the norm $||\cdot||$ it taken with respect to the riemannian metric on $T_xM_\kappa^2$ given by the restriction of the linear form $\pr\cdot\cdot$). Formally:
$$
\exp_{x}(v)= x\cosh(||v||) + \frac{v}{||v||}\sinh(||v||) 
$$
Which is the endpoint of the [[Geometry of Hyperbolic Space#^34b463|hyperbolic arc]] starting at $x$ in direction $v$ of length $||v||$. In the case where $e_z = (0,0,1)$, then the tangent space is just the subspace $\R^2\subseteq \R^3$, and the riemannian metric corrisponds to the usual inner product on $\R^2$, and the map looks like:
$$
\exp_{e_z }(v)= (0,0,1)\cosh(||v||) + \frac{v}{||v||}\sinh(||v||) 
$$
Let $u_\theta = (\cos(\theta),\sin(\theta))$ and $v_\theta = (-\sin(\theta),\cos(\theta))$, then we can parameterize $\R^2\subseteq \R^3$ with polar coordinates $(r,\theta)\mapsto ru_\theta$. Then \exp_{e_z }(v) this map becomes:
$$
\exp_{e_z}(ru_\theta)= (0,0,\cosh(r)) + (u_\theta\sinh(r),0)
$$
```

^82c0c0

```ad-Proposition
The metric $d_{-1}$ on $\HP^2$ agrees with the riemannian length metric $d'$ when taking the natural riemannian metric on $\HP^2$.
```

__Proof__: 
Pull back the natural remannian metric on $\HP^2$ to riemannian metric  $\inner \cdot\cdot_p$ on $\R^2$ via the $\exp_{e_z}$ map. Then:
```ad-Lemma
The riemannian metric at point $ru_\theta$ with respect to basis vectors (of the tangent space) $u_\theta$ and $v_\theta$ is given by:
$$
\begin{bmatrix}
1 &0\\
0 & (\frac{\sinh(r)}{r})^2
\end{bmatrix}
$$

```
__Proof__:

