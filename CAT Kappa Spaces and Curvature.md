```ad-Definition
title:Definition: $\CAT(\kappa)$ Space
Let $(M,d)$ be a metric space. Let $x,y,z\in M$ and $l_{xy}$, $l_{yz}$, and $l_{zx}$ be geodesics (with lengths $a,b,c$ resp) forming a geodesic triangle $\Delta xyz$. Define the perimeter of $\Delta$ to be $a+b+c$

Take $\Delta' = x'y'z'$ to be the corrisponding [[Model Spaces|comparison triangle]] in $M^2_\kappa$ with geodesics  $l_{x'y'}$, $l_{y'z'}$, and $l_{z'x'}$. For any point $p = l_{xy}(t)$ for some $t\in[0,a]$ on $l_{xy}$, let $p' = l_{x'y'}(t)$. Similarly define $p'$ for $p$ on $l_{yz}$ and $l_{zx}$. Say $p\in \Delta$ if $p$ is on one of $l_{xy}$, $l_{yz}$, and $l_{zx}$.

This geodesic triangle satisfies the <u>$\CAT(\kappa)$ inequality</u> if for all $p,q\in \Delta$ we have:
- $d(p,q)\leq d_\kappa(p',q')$

This is just saying that the geodesic triangle in $M$ is "thinner" than the comparison triangle. 

If $M$ is a $\diam(M_\kappa^2)$ [[Geodesic|geodesic]] metric space such that every triangle $\Delta$ with perimeter $<2\diam(M_\kappa^2)$ the $\CAT(\kappa)$ inequality holds, then, then $M$ is a <u>$\CAT(\kappa)$ space</u>
```

```ad-Definition
title:Definition: Spaces with Curvature $\leq \kappa$
Let $(M,d)$ be a metric space. If $(M,d)$ is locally a $\CAT(\kappa)$ (at every point there is a small enough open ball that is $\CAT(\kappa)$ with the induced metric), then it has curvature $\leq \kappa$.
