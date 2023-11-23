


```ad-Definition
title:Definition: Hyperplane
A hyperplane in $\HP^n$ (resp. $\sph^n$) is the nonempty intersection of a hyperplane $V\subseteq \R^{n+1}$ with $\HP^n$ (resp. $\sph^n$). 
```

```ad-Proposition
For every hyperplane $V_H = V\cap \HP^n$, there exists a (unique up to sign) unit vector $v$ such that $V = v^\perp$ with respect to the [[Geometry of Hyperbolic Space|minkowski bilinear form]] $\pr\cdot\cdot$
```
__Proof__: First, we will show that $\span(V_H) = V$. Let $v\in V\cap\HP^n$, then $v^\perp = \{u\in\R^{n+1}: (u,v) = 0\}$ is a $n$ dimensional linear subspace of $\R^{n+1}$. Therefore,  it intersects $V$ in an $n-1$ dimensional subspace, so $\span(v,v^\perp\cap V) = V$. For any $z\in v^\perp$, if $\pr z z < 0$, then $\frac {1} {\sqrt{|\pr z z|}}z \in \HP^n$. Otherwise, if $\pr z z \geq 0$ then $\sqrt{1+(z,z)}v + z \in \HP^n$, as:
$$
\begin{align}
\pr {\sqrt{1+(z,z)}v + z} {\sqrt{1+(z,z)}v + z}& = (1+\pr z z)\pr v v + 2\sqrt{1+(z,z)}\pr v z + \pr z z\\
& = -1-\pr z z+  \pr z z\\
& = -1\\
\end{align}
$$
Take $v_1,\dots,v_n$ spanning $V$ in $\HP^n$. Then, $S = v_1^\perp\cap v_2^\perp\dots\cap v_n^\perp$ is at least a one dimensional subspace of $\R^{n}$. It is exactly one, since it intersects $V$ trivially (since $\pr \cdot\cdot$ is positive definite on $S$, and the norm of any vector in $V\cap S$ is 0). Therefore, there is a unique (up to sign) unit vector in $S$. $\square$
```ad-note
The same is true for $\sph^n$ with respect to the normal inner product.
```


```ad-Definition
title:Definition: Reflections Across Hyperplanes
For hyperplane $H$ subset of $\HP^n$ ($\sph^n$, $\R^n$ resp.). Define the reflection across $H$ as:
- In $\HP^n$: Let $u$ be unit with respect to $\pr \cdot\cdot$ with $u^\perp=H$. Then the reflection is:
 $$v\mapsto v - 2\pr u v u$$
- In $\sph^n$ or $\R^n$: Let $u$ be unit with respect to $\inner \cdot\cdot$ with $u^\perp=H$. Then the reflection is:
 $$v\mapsto v - 2\inner u v u$$
```
```ad-Proposition
Reflections are isometries
```
__Proof__:
For $x,y\in\HP^n$:
$$
\begin{align}
(x- 2\pr x u u,y- 2\pr u y u) &=(x,y)-4\pr x u\pr y u + 4\pr x u \pr u y\pr u u\\
&=(x,y)-4\pr x u\pr y u + 4\pr x u \pr y u\\
&=(x,y)\\
\end{align}
$$
The same holds in $\R^n$, $\sph^n$. $\square$
```ad-Proposition
Let $x,y\in \HP^n$ ($\sph^n$, $\R^n$ resp.), then there exists a reflection which maps $x\mapsto y$
```
__Proof__:
Consider $u = \frac{x-y}{\sqrt{|\pr{x-y}{x-y}|}}$. This is defined, since $(x-y,x-y) = -2 - 2(x,y) > 0$ for $x\neq y$.
Note, the hyperplane corresponding with $u$ is exactly the points $z$ which have $\pr x z = \pr y z$, which intersects $\HP^n$. Then:
$$
\begin{align}
&x- 2\frac{1}{\sqrt{|\pr{x-y}{x-y}|}}\pr x {x-y}\frac{x-y}{\sqrt{|\pr{x-y}{x-y}|}}\\
&=x- \frac{-2 -2\pr xy}{\pr{x-y}{x-y}} (x-y)\\
&=x- (x-y)\\
&=y\end{align}
$$
$\square$
```ad-Proposition
Let $x_1,x_2,\dots,x_k, y_1, y_2, \dots y_k\in \HP^n$ ($\sph^n$, $\R^n$ resp.) such that for all $i,j$, $d(x_i,x_j) = d(y_i,y_j)$. Then, there exists an isometry which maps $x_i\mapsto y_i$
```

^d21a1e

__Proof__: We will induct on $k$. For $k=1$, this is the previous proposition. Suppose it works for $k$ points. Then, take $\phi$ to be the isometry mapping $x_i\mapsto y_i$ for $i\leq k$, and let $\psi$ be the reflection which maps $\phi(x_{k+1})\mapsto y_{k+1}$. For $i\leq k$ we have $d(y_i,y_{k+1}) = d(x_i,x_{k+1}) = d(y_i, \phi(x_{k+1}))$, so $y_i$ is equidistant from $\phi(x_{k+1})$ and $y_{k+1}$, so it is fixed by $\psi$. This means $\psi\circ \phi$ is the desired isometry. $\square$