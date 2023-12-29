```ad-Definition
title:Definition: $\kappa$ Cone
For a metric space $(Y,d)$ and $\kappa\in\R$, define the <u> $\kappa$ cone</u> $C_\kappa Y = (Y\times [0,\diam(M_\kappa)])/\sim$ where $(y,t)\sim(y',t')$ if $t=t'=0$ or $t=t'>0$ and $y=y'$. The point $0 = [(y,0)]$ is called the <u>vertex of the cone</u>. Define a metric $d'$ on $C_\kappa Y$ is defined such that the $\kappa$ law of cosines is satisfied at $0$ (given that the distance from $0$ to $(y,t)$ is $t$ and the angle at $0$ between $(y,t)$ and $(y',t')$ is $\min(d(y,y'),\pi)$):
- $\kappa = 0$
$$
d'((y,t),(y',t'))^2 = t^2 +t'^2 - 2tt'\cos(\min(d(y,y'),\pi))
$$
- $\kappa < 0$
$$
\cosh(\sqrt{-\kappa}\ d'((y,t),(y',t'))) = \cosh(\sqrt{-\kappa}\ t)\cosh(\sqrt{-\kappa}\ t') - \sin(\sqrt{-\kappa}\ t)\sin(\sqrt{-\kappa}\ t')\cos(\min(d(y,y'),\pi))
$$
- $\kappa > 0$, then if $d(y,y')$
$$
\cos(\sqrt{\kappa}\ d'((y,t),(y',t'))) = \cos(\sqrt{-\kappa}\ t)\cos(\sqrt{\kappa}\ t') + \sin(\sqrt{\kappa}\ t)\sin(\sqrt{\kappa}\ t')\cos(\min(d(y,y'),\pi))
$$
```

```ad-Proposition
If $Y = \sph^{n-1}$, then $C_\kappa Y$ is isometric to $M_\kappa^n$ for $\kappa \leq 0$ and a closed ball of radius $\diam(M_\kappa^n)$ else.
```
```ad-Theorem
title: Berestovskii’s Theorem
If $C_\kappa Y$ is $\CAT(\kappa)$ iff $Y$ is $\CAT(1)$