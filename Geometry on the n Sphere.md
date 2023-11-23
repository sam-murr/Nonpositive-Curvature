```ad-Definition
Define [[Metric Space|metric]] $d_1$ on the $n$ sphere $\sph^n$ via:
$$
d_1(x,y) = \arccos(\langle x,y \rangle )
$$
When it is clear from the context we write $d$ instead of $d_1$.
```
This clearly satisfies property $1$ of being a metric, property $2$ follows from the [[Cauchy Schwarz Inequality]]. We will show triangle inequality later.

```ad-Definition
title:Definition: Great Circle and Creat Arcs
A great circle $S$ is the intersection of a 2 dimensional subspace of $\R^{n+1}$ with $\sph^n$. The great circle containing (non-antipodal) points $x, y\in\sph^n$ is parameterized by: $$P = \{\cos(\theta) x + \sin(\theta)\frac{( y - \inner{ x} { y} x)}{|| y - \inner{ x} { y} x||}): \theta \in [0,2\pi]\}$$

The <u>minimal great arc</u> $a:[0,d( x,  y)]\to \sph^n$ between (non-antipodal) points $x,y \in\sph^n$ with $x$ and $y$ is
$$a(\theta) = \cos(\theta) x + \sin(\theta)\frac{( y - \inner{ x} { y} x)}{|| y - \inner{ x} { y} x||}$$

The <u>minimal great arc</u> $a:[0,d( x,  y)]\to \sph^n$ between antipodal points $x,y \in\sph^n$ with $x$ and $y$ is
$$a(\theta) = \cos(\theta) x + \sin(\theta) u$$
Where $u \in \sph^n$ any unit vector orthogonal to $ x$.

In either case, let <u>the direction of the minimal arc</u> $a$ be the unit orthogonal component added to $\cos(\theta) x$ in the definition of $a$, ie either $\frac{( y - \inner{ x} { y} x)}{|| y - \inner{ x} { y} x||}$ or $ u$ in the non-antipodal and antipodal cases.
```

```ad-Proposition
The minimal great arc between points $x,y \in\sph^n$ is a geodesic path from $x$ to $y$.
```
__Proof__: First, note that $a(d( x,\ y)) =  y$. If $ x$ and $ y$ not antipodal, then:
$$
\begin{align}
a(d( x, y)) &= \cos(d( x, y)) x + \sin(d( x, y))\frac{( y - \inner{ x} { y} x)}{|| y - \inner{ x} { y} x||}\\
&= \inner{ x} { y} x + \sqrt{1-\inner { x}{ y}^2}\frac{( y - \inner{ x} { y} x)}{\sqrt{1 - \inner{ x} { y}^2}}\\
&=  y
\end{align}
$$
If $ x$ and $ y$ not antipodal, then $a(d(x,  y)) = a(\pi) = - x = y$.


Moreover, since $x$ and $y- \inner{ x} { y}x$  (or $ u$ in the antipodal case) are orthogonal, for any $\alpha, \beta\in [0,d(x,y)]$ we have:
$$
\begin{align}
\inner{a(\alpha)}{a(\beta)} &= \cos(\alpha)\cos(\beta) + \sin(\alpha)\sin(\beta)\\
&= \cos(\alpha - \beta)
\end{align}
$$
So $d(a(\alpha),a(\beta)) = |\alpha - \beta|$. $\square$

```ad-Definition
title:Definition: Angles between Arcs
Let $x,y,z\in \sph^n$ and $a_z$, $a_y$ be minimal great arcs with directions $u$ and $v$ from $x$ to $z$ and $y$ respectively. The angle $\gamma$ between $a_z$ and $a_y$ is $d(u,v) = \arccos(\inner{u}{v})$.
```
![[angle between arcs.png]]
```ad-Theorem
title: Theorem: Spherical Law of Cosines
Let $x,y,z\in\sph^n$, $c = d(x,z)$, $b = d(x,y)$, $a= d(y,z)$. Fix minimal great arcs $a_{xz}$ and $a_{xy}$ from $x$ to $z$ and $y$ with directions $u$ and $v$. Let $\gamma$ be the angle between these great arcs. Then:
$$
\cos(a) = \cos(b)\cos(c)+\sin(b)\sin(c)\cos(\gamma)
$$
```
![[Spherical law of cosines.png]]
__Proof__:
$$
\begin{align}
\cos(a) &= \inner{z}{y}\\
&= \inner{\cos(c)x+\sin(c)u}{\cos(b)x+\sin(b)v}\\
&= \cos(c)\cos(b)\inner{x}{x}+\cos(c)\sin(b)\inner{x}{u} + \cos(b)\sin(c)\inner{x}{v}+\sin(c)\sin(b)\inner{u}{v}\\
&= \cos(c)\cos(b)+\sin(c)\sin(b)\inner{u}{v}\\
&= \cos(c)\cos(b)+\sin(c)\sin(b)\cos(\gamma)\\
\end{align}
$$
$\square$
```ad-Proposition
The triangle inequality holds for $d$.
```
__Proof__: Let $x,y,z\in\sph^n$, , $c = d(x,z)$, $b = d(x,y)$, $a= d(y,z)$. Fix minimal great arcs $a_{xz}$ and $a_{xy}$ from $x$ to $z$ and $y$ with directions $u$ and $v$. Let $\gamma$ be the angle between these great arcs. We know $\arccos$ has range $[0,\pi]$, over which $\sin$ is positive and $\cos \gamma$ is strictly decreasing. 

If $b+c > \pi$ then the triangle inequality is satisfied automatically.

Now suppose $b+c \leq \pi$. By the spherical law of cosines, we have that $\cos(a)\geq  \cos(b)\cos(c)-\sin(c)\sin(b) = \cos(c+b)$ with equality only when $\gamma = \pi$. Since $a, c+b \in [0,\pi]$ and $\cos$ strictly decreasing on this domain, then $a\leq c+b$ with equality only when $\gamma = \pi$. $\square$

```ad-Proposition
If there are two minimal great arcs between $x$ and $y$, then either the great arcs are the same or $x$ is antipodal to $y$
```
__Proof__: Let $a_{xy}$ and $a'_{xy}$ be the two minimal great arcs with directions $u$ and $v$ and angle $\gamma$. Let $d(x,y) = b$, and note $d(y,y)=0$. Applying the law of cosines to $x$, $y$, and $y$ with arcs $a_{xy}$ and $a'_{xy}$ gives $1 = \cos(b)^2+\sin(b)^2\cos(\gamma)$. rearranging gives $0 = \sin(b)^2(\cos(\gamma)-1)$, so either $b = 0$ or $\pi$ (corresponding to the trivial case and the antipodal case), or $\gamma = 0$ and the arcs are the same. $\square$
```ad-Proposition
Geodesics are exactly minimal great arcs. Moreover, if $d(z,y)<\pi$, then there is a unique geodesic from $z$ to $y$.
```
__Proof__: Let $l:[0,d(z,y)]\to X$ be any geodesic. Take some $x = l(c)$ for $c \in (0,d(z,y))$, and let  $c = d(x,z)$, $b = d(x,y)$, $a= d(y,z)$. Fix minimal great arcs $a_{xz}$ and $a_{xy}$  from $x$ to $z$ and $y$ with directions $u$ and $v$ respectively. 
Let $\gamma$ be the angle between these great arcs.

Since $l$ is a geodesic, we have $a = b+c$, so by above $\gamma = \pi$. This means $u = -v$, so $z = \cos(c)x - \sin(c)v$ and $y = \cos(b)x + \sin(b)v$. 




Let $g:[0,a]\to X$ be the arc starting at $z$ with length $a$ in the direction $q = \cos(c)v + \sin(c) x$. Note $q$ is orthogonal to $z$, since $\inner qz = \cos(c)\sin(c)-\cos(c)\sin(c)$. This is a geodesic from $z$ to $y$, and has $g(c) = x$:
$$
\begin{align}
g(c) &= \cos(c)z + \sin(c)q\\
&=  \cos^2(c)x - \cos(c)\sin(c)v+\sin(c)\cos(c)v + \sin^2(c)x\\
&=  x\\
g(a) &= \cos(a)z + \sin(a)q\\
&= \cos(a)\cos(c)x-\sin(c)\cos(a)v + \sin(a)\cos(c)v+\sin(a)\sin(c)x\\
&= \cos(a-c)x+\cos(a-c)v\\
&= \cos(b)x+\cos(b)v\\
&= y
\end{align}
$$

This is also true of every other point $x'=l(c')$, so every point on $l$ is on a minimal great arc from $z$ to $y$. By the above proposition, if $d(z,y)<\pi$, there is only one such arc, so every point on $l$ is on $g$. Since $l$ and $g$ are geodesics, it means $l(t)=g(t)$ for all $t\in[0,a]$. 

If $d(z,y)= \pi$, note that $b,c<\pi$, so $l\rest[0,c] = g\rest[0,c]$ is the unique geodesic from $z$ to $x$, and $l(t-c)\rest[c,a] = g(t-c)\rest[c,a]$ is the unique geodesic from $x$ to $y$, so $l = g$. $\square$