```ad-Definition
title:Definition: $\CAT(\kappa)$ Space
Let $(M,d)$ be a metric space. Let $x,y,z\in M$ and $l_{xy}$, $l_{yz}$, and $l_{zx}$ be geodesics (with lengths $a,b,c$ resp) forming a geodesic triangle $\Delta xyz$. Define the perimeter of $\Delta$ to be $a+b+c$

Take $\Delta' = x'y'z'$ to be the corrisponding [[Model Spaces|comparison triangle]] in $M^2_\kappa$ with geodesics  $l_{x'y'}$, $l_{y'z'}$, and $l_{z'x'}$. For any point $p = l_{xy}(t)$ for some $t\in[0,a]$ on $l_{xy}$, let $p' = l_{x'y'}(t)$. Similarly define $p'$ for $p$ on $l_{yz}$ and $l_{zx}$. Say $p\in \Delta$ if $p$ is on one of $l_{xy}$, $l_{yz}$, and $l_{zx}$.

This geodesic triangle satisfies the <u>$\CAT(\kappa)$ inequality</u> if for all $p,q\in \Delta$ we have:
- $d(p,q)\leq d_\kappa(p',q')$

This is just saying that the geodesic triangle in $M$ is "thinner" than the comparison triangle. 

If $M$ is a $\diam(M_\kappa^2)$ [[Geodesic|geodesic]] metric space such that every triangle $\Delta$ with perimeter $<2\diam(M_\kappa^2)$ the $\CAT(\kappa)$ inequality holds, then, then $M$ is a <u>$\CAT(\kappa)$ space</u>
```
![[CAT(0) Space.png]]
<center> Above: An example of the CAT(0) inequality holding</center>


```ad-Proposition
Suppose $xyz$ geodesic triangle in $X$. The following are equivalent:
- $xyz$ satisfies the $\CAT(\kappa)$ inquality.
- For all $r\in [x,y]$, the distance between $r$ and $z$ is less than the distance between $z'$ and $r'$ in the $\kappa$ comparison triangle $x'y'z'$.
- The alexandrov angles are no greater than the angles of the $\kappa$ comparison triangles $x'y'z'$.
- Let $p,q$ on $xy$ and $xz$ respectively, then the angles in the $\kappa$ comparison triangles $\bar{\Delta}(xpq)$ are no larger than the angles in $\bar{\Delta}(xyz)$.
```
__Proof__: 1