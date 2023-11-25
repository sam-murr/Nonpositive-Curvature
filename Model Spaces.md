```ad-Definition
title:Definition: $\kappa$ Model Space
For $\kappa\in\R$, define the $\kappa$ model space $M_\kappa^n$ to be the metric space:
- $\R^n$ equipped with the [[Geometry of Euclidean Space|metric]] $d_0$ when $\kappa = 0$
- $\sph^n$ equipped with the [[Geometry on the n Sphere|metric]] $d_\kappa = \frac{1}{\sqrt{|\kappa|}}d_1$ when $\kappa > 0$
- $\HP^n$ equipped with the [[Geometry of Hyperbolic Space|metric]] $d_\kappa = \frac{1}{\sqrt{|\kappa|}}d_{-1}$ when $\kappa < 0$

If $\kappa >0$, then set $\diam(M_\kappa^n) = \frac{1}{\sqrt{|\kappa|}}\pi$. Otherwise, let $\diam(M_\kappa^n) = \infty$
```
```ad-Proposition
title:Proposition: Law of Cosines
let $x,y,z \in M_\kappa^n$ be a geodesic triangle in $M_\kappa^n$ with $d(x,y) = a$, $d(y,z) = b$, and $d(z,x) = c$, and $\gamma$ is the angle $\angle xyz$ (defined in $\sph^n$, $\R^n$, and $\HP^n$ depending on $\kappa$), we then have:
- If $\kappa > 0$:
	$$
	\cos(\sqrt{k} c) = \cos(\sqrt{k} a)\cos(\sqrt{k} b) + \sin(\sqrt{k} a)\sin(\sqrt{k} b)\cos(\gamma)
	$$
- If $\kappa = 0$:
$$
c^2 = a^2+b^2 - 2ab\cos(\gamma)
$$
- If $\kappa < 0$:
	$$
	\cosh(\sqrt{k} c) = \cosh(\sqrt{k} a)\cosh(\sqrt{k} b) - \sinh(\sqrt{k} a)\sinh(\sqrt{k} b)\cos(\gamma)
	$$
```
__Proof__: This follows from the law of cosines in [[Geometry of Euclidean Space|euclidean]], [[Geometry of the n Sphere|spherical]], and [[Geometry of Hyperbolic Space|hyperbolic]] space.
```ad-Definition
title:Definition: $\kappa$ Comparison Triangles
Let $x,y,z\in M$ some metric space $(M,d)$ with $d(x,y) = a$, $d(z,y) = b$, and $d(z,x) = c$ such that $a+b+c\leq 2\diam(M_\kappa^2)$. Then, let $x',y',z'\in M_\kappa^2$ with $d(x',y') = a$, $d(z',y') = b$, and $d(z',x') = c$. Such a triangle $x'y'z'$ is called a  <u>$\kappa$ Comparison Triangle</u>. This triangle is unqiue up to [[Hyperplanes and Reflections#^d21a1e|isometry]].
```

```ad-Proposition
title:Proposition: Comparison Triangles Exist
Let $a,b,c\in\R^+$ satisfying the triangle inquality and $a+b+c\leq 2\diam(M_\kappa^2)$. Then, there exists $x',y',z'\in M_\kappa^2$ with $d(x',y') = a$, $d(z',y') = b$, and $d(z',x') = c$.
```
__Proof__: WLOG, take $a\leq b\leq c$. Suppose that $\kappa > 0$, but the same trick will work with arbitrary $\kappa$. Take $\gamma$ such that:
$$
	\cos(\sqrt{k} c) = \cos(\sqrt{k} a)\cos(\sqrt{k} b) + \sin(\sqrt{k} a)\sin(\sqrt{k} b)\cos(\gamma)
$$
Such a $\gamma$ exists, since $\cos(\gamma)$ is decreasing on $[0,\pi]$, so  $\cos(\sqrt{k} a)\cos(\sqrt{k} b)+\sin(\sqrt{k} a)\sin(\sqrt{k} b)\cos(\gamma)$ goes from $\cos(\sqrt{k}(b-a))$ to $\cos(\sqrt{k}(a+b))$. Since $b-a \leq c \leq a+b$, this range includes $\cos(\sqrt{k}(c))$.

We also have that $2c \leq a+b+c \leq 2\diam(M_\kappa^2)$, so $a,b,c\leq \diam(M_\kappa^2)$. 

Take any $y'$ in $M_\kappa^n$, fix unit $u,v\in y'^\perp$ with the angle between $u$ and $v$ equal to $\gamma$. Let $x'$ be the endpoint of the spherical arc starting at $y'$ in direction $u$ with length $a$.  Let $z'$ be the endpoint of the spherical arc starting at $y'$ in direction $v$ with length $b$. Note these are geodesics since $a,b\leq \diam(M_\kappa^2)$. Then, taking any geodesic from $x'$ to $z'$, we get that this is a geodesic triangle, so by the law of cosines $d(x',z')=c$. $\square$


```ad-Definition
title:Definition: $\kappa$ Comparison Angles
Let $x,y,z\in M$ some metric space, define the <u>$\kappa$ comparison angle</u> $\overline{\angle_y}(x,z)$ as the angle $\angle x'y'z'$ of the corrisponding comparison triangle in $M_\kappa^2$.

We can also define the angle of two curves $c_0$, $c_1$ with starting point $y$ as:
$$
\angle(c_0,c_1) = \inf_\eps\sup_{t_0,t_1\in (0,\eps)}\overline{\angle_y}(c_0(t_0),c_1(t_1))
$$
``` 



