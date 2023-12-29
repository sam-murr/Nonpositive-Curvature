```ad-Definition
title:Definition: Minkowski Bilinear From
For $x,y\in\R^n$, define the <u>minkowski bilinear form</u> as:
$$
\pr x y = \sum_{i=1}^n x_iy_i\ -\ x_{n+1}y_{n+1}
$$
The <u>light cone</u> is defined to be $\{x: (x,x) = 0\}$
The <u>n hyperboloid</u>, $\HP^n$ is defined to be $\{x: (x,x) = -1,\ x_{n+1}>0\}$
```
```ad-Definition
title:Definition: Hyperbolic Metric
For $x,y\in\HP^n$, define: $$d_{-1}(x,y) = \cosh^{-1}(-(x,y))$$
(ie the unique positive number $\theta$ such that $\cosh(\theta) = -(x,y)$). In order to show this is well defined, we must prove $(x,y)\leq -1$ for all $x,y\in\HP^n$, as the domain of $\cosh^{-1}$ is $[1,\infty)$. When the context is clear, we write $d$ for $d_{-1}$.
```
![[Hyperbolic Plane.png]]
```ad-Proposition
$d$ is well defined and satisfies properties 1 and 2 of a [[Metric Space|metric]].
```

^ee256e

__Proof__: For any $x,y\in\HP^n$, we have that $\sum_{i=1}^n x_i^2\ -\ x_{n+1}^2 = -1$ (0), so $x_{n+1},y_{n+1} \geq 1$ (1). We (using [[Cauchy Schwarz Inequality]]) have that $(\sum_{i=1}^n x_iy_i)^2\leq \sum_{i=1}^n x_i^2\sum_{i=1}^n y_i^2$ (2) and $2x_{n+1}y_{n+1}\leq x_{n+1}^2+y_{n+1}^2$ (3) with equality in both iff $x = y$. Then:
$$
\begin{align}
-2x_{n+1}y_{n+1}&\geq -x_{n+1}^2-y_{n+1}^2&&{(3)}\\
x_{n+1}^2y_{n+1}^2-2x_{n+1}y_{n+1}+1&\geq x_{n+1}^2y_{n+1}^2-x_{n+1}^2-y_{n+1}^2+1\\
(x_{n+1}y_{n+1}-1)^2&\geq (x_{n+1}^2-1)(y_{n+1}^2-1)\\
(x_{n+1}y_{n+1}-1)&\geq \sqrt{(x_{n+1}^2-1)(y_{n+1}^2-1)}&&{(1)}\\
-1&\geq \sqrt{(x_{n+1}^2-1)(y_{n+1}^2-1)}-x_{n+1}y_{n+1}\\
-1&\geq \sqrt{(\sum_{i=1}^n x_i^2)(\sum_{i=1}^n y_i^2)}-x_{n+1}y_{n+1}&&(0)\\
-1&\geq \sum_{i=1}^n x_iy_i-x_{n+1}y_{n+1}&&(2)\\
-1&\geq (x,y)\\
\end{align}
$$
With equality iff $x = y$, since the inequality is introduced in $(2)$ and $(3)$. This shows $d$ is well defined.Since $\cosh(\theta) = 0$ iff $\theta = 0$, this proves property $2$ of a [[Basic Topology/Metric Spaces/Metric Space|metric]]. Property 1 follows from the definition. $\square$


```ad-Definition
title:Definition: Hyperbolic Arc
A hyperbolic line starting at $x$ in direction $u$ is the curve $l:\R\to\HP^n$ via:
$$
l(t) = x\cosh(t)+u\sinh(t)
$$
Where $x\in\HP^n$ and $(x,u)=0$, $(u,u) = 1$.

A hyperbolic segment of length $a$ starting at $x$ in direction $u$ is the curve $l\rest [0,a]$

The hyperbolic segment between points $x,y\in\HP^n$, $x\neq y$, is the hyperbolic segment of length $d(x,y)$ starting at $x$ in direction $u_{xy} = \frac{y+(x,y)x}{\sqrt{(y+(x,y)x,y+(x,y)x)}}$
```

^34b463

```ad-Proposition
Hyperbolic segments lie in $\HP^n$ and are geodesics.
```
__Proof__:
It suffices to show that a hyperbolic line starting at $x$ in the direction of $u$ is an isometric embedding from $\R$ into $\HP^n$.
$$
\begin{align}
(l(t),l(t)) &= \cosh^2(t)(x,x)+2\cosh(t)\sinh(t)(x,u)+\sinh^2(t)(u,u)\\
&= -\cosh^2(t)+\sinh^2(t)\\
&= -1
\end{align}
$$
Take $t_0,t_1\in\R$, $t_0\leq t_1$.
$$
\begin{align}
(l(t_0),l(t_1)) &= \cosh(t_1)\cosh(t_0)(x,x)+(\cosh(t_0)\sinh(t_1)+\sinh(t_0)\cosh(t_1))(x,u)+\sinh(t_0)\sinh(t_1)(u,u)\\
&= -\cosh(t_1)\cosh(t_0)+\sinh(t_0)\sinh(t_1)\\
&= \cosh(t_1-t_0)
\end{align}
$$
This means $d(l(t_0),l(t_1)) = t_1-t_0$. $\square$


```ad-Proposition
For $x,y\in\HP^n$, $u_{xy}$ is defined and the hyperbolic segment between points $x,y\in\HP^n$ is a geodesic.
```
In order to show that $u_{xy}$ is defined, we have to show $(y+(x,y)x,y+(x,y)x)> 0$. It suffices to show that  $(y+(x,y)x,y+(x,y)x) =0$ only when $x = y$,  and $\pr\cdot\cdot$ is positive definite on $x^\bot =\{y\in\R^{n+1}: \pr x y = 0\}$, since $(x,y+(x,y)x) = (x,y) + (x,y)(x,x) = 0$.

```ad-Claim
For $x,y\in \HP^{n+1}$, $(y+(x,y)x,y+(x,y)x) = 0$ implies $x = y$
```
__Proof__(claim): 
$$
\begin{align}
(y+(x,y)x,y+(x,y)x) &= (y,y)+2(x,y)^2+(x,y)^2(x,x)\\
&= (x,y)^2-1\\
\end{align}
$$
This implies $(x,y)^2 = 1$, so since $d$ is well defined we have $(x,y) = -1$.  This gives $d(x,y) = 0$, so by [[Geometry of Hyperbolic Space#^ee256e|this proposition]] we have $x = y$. $\square$(claim)

```ad-Claim
For $x\in \HP^{n+1}$, $z\in x^\bot$, $(z,z)\geq 0$ with equality only when $z = 0$
```

^613ac9

__Proof__(claim): 
Suppose there exists $z\in x^\bot$, $z\neq 0$ and $(z,z) < 0$. Then, $S = \span(x,z)$ is a two dimensional subspace with $\pr \cdot\cdot$ negative definite on $S$, since:
$$
(rz+tx,rz+tx) = r^2(z,z)+t^2(x,x) < 0
$$
However, $S$ must intersect the $n$ dimensional subspace $P= \{x\in\R^{n+1}: x_{n+1} = 0\}$ nontrivially, contradicting the fact that $\pr \cdot\cdot$ restricts to a positive definite form on $P$. $\square$(claim)

Finally, we just have to show that if $l$ is the hyperbolic segment from $x$ to $y$, then $l(d(x,y)) = y$:
$$
\begin{align}
l(d(x,y)) &= \cosh(d(x,y))x + \sinh(d(x,y))\frac{y+(x,y)x}{\sqrt{\pr{y+\pr xy}{y+\pr xy}}}\\
&= -(x,y)x + \frac{\sinh(d(x,y))}{\sqrt{(x,y)^2-1}}(y+(x,y)x)\\
&= -(x,y)x + \frac{\sinh(d(x,y))}{\sqrt{\cosh(x,y)^2-1}}(y+(x,y)x)\\
&= -(x,y)x + \frac{\sinh(d(x,y))}{\sinh(d(x,y))}(y+(x,y)x)\\
&= y
\end{align}
$$
We're done. $\square$

```ad-Definition
title:Definition: Angle Between Arcs
The angle between two hyperbolic segments starting at $x$ in direction $u$ and $v$ is:
$$
\arccos(\pr uv)
$$
Recall from the [[Geometry of Hyperbolic Space#^613ac9|above claim]] that $\pr \cdot\cdot$ is an inner product on $x^\bot$, so for $u,v \in x^\bot$, $|\pr u v |\leq \frac 12\pr uu + \frac 12 \pr vv = 1$.
```
```ad-Theorem
title:Theorem: Hyperbolic Law of Cosines
Let $x,y,z\in\HP^n$, $c = d(x,z)$, $b = d(x,y)$, $a= d(y,z)$. Fix hyperbolic segments $l_{xz}$ and $l_{xy}$ from $x$ to $z$ and $y$ with directions $u_{xz}$ and $u_{xy}$. Let $\gamma$ be the angle between these hyperbolic segments. Then:
$$
\cosh(a) = \cosh(b)\cosh(c)-\sinh(b)\sinh(c)\cos(\gamma)

```

^6e1d46

__Proof__:
$$
\begin{align}
\cosh(a) &= -(y,z)\\
&= -(\cosh(d(x,y))x + \sinh(d(x,y))u_{xy}, \cosh(d(x,z))x + \sinh(d(x,z))u_{xz})\\
&= -\cosh(d(x,y))\cosh(d(x,z))(x,x) -\sinh(d(x,y))\sinh(d(x,z))(u_{xy},u_{xz})\\
&= \cosh(d(x,y))\cosh(d(x,z)) -\sinh(d(x,y))\sinh(d(x,z))\cos(\gamma)\\
&= \cosh(b)\cosh(c) -\sinh(b)\sinh(c)\cos(\gamma)
\end{align}
$$
$\square$
```ad-Proposition
The triangle inequality holds for $d$
```
__Proof__: Take all variables from the statement of the hyperbolic law of cosines. We want to show $a\leq b+c$. We have $b,c>0$ so $\sinh(b),\sinh(c)>0$. WLOG $b>c$. Therefore from the law of cosines $\cosh(a)$ has a minimum value:
$$\cosh(a)=\cosh(b)\cosh(c) -\sinh(b)\sinh(c) = \cosh(b-c)$$
at $\gamma = 0$ and maximum value:
$$\cosh(a)=\cosh(b)\cosh(c) + \sinh(b)\sinh(c) = \cosh(b+c)$$
at $\gamma = \pi$. Since $\cosh$ is increasing for positive values, we have $b-c \leq a \leq b+c$. $\square$
```ad-Proposition
There is a unique hyperbolic segments connecting $x$ and $y$ for $x\neq y$.
```

^67d194

__Proof__: Let $u,v$ be the two directions of the hyperbolic segments $l_u$ and $l_v$. Applying law of cosines to the triangle with sides $l_u,l_v$ we have:
$$
\begin{align}
\cosh(d(y,y))&= \cosh(d(y,x))\cosh(d(y,x)) -\sinh(d(y,x))\sinh(d(y,x))\cos(\gamma)\\
1&= \cosh(d(y,x))^2-\sinh(d(y,x))^2\cos(\gamma)\\
0&= \sinh(d(y,x))^2-\sinh(d(y,x))^2\cos(\gamma)\\
0&= \sinh(d(y,x))^2(1-\cos(\gamma))\\
1&= \cos(\gamma)\\
\end{align}
$$
Since $\gamma \in [0,\pi]$, $\gamma = 0$, so $u = v$. $\square$
```ad-Proposition
The unique geodesic from $z$ to $y$ is the hyperbolic segment from $z$ to $y$.
```
__Proof__: Take $g:[0,d(y,z)]\to \HP^n$ geodesic from $z$ to $y$. Let $x = g(c)$ for $c\in(0,d(y,x))$. Let $c = d(x,z)$, $b = d(x,y)$, $a= d(y,z)$. Fix hyperbolic segments $l_{xz}$ and $l_{xy}$ from $x$ to $z$ and $y$ with directions $u_{xz}$ and $u_{xy}$. Let $\gamma$ be the angle between these hyperbolic segments. By the law of cosines:
$$
\begin{align}
\cosh(a) &= \cosh(b)\cosh(c) -\sinh(b)\sinh(c)\cos(\gamma)\\
\cosh(c+b) &= \cosh(b)\cosh(c) -\sinh(b)\sinh(c)\cos(\gamma)\\
\cosh(b)\cosh(c) + \sinh(b)\sinh(c) &= \cosh(b)\cosh(c) -\sinh(b)\sinh(c)\cos(\gamma)\\
-1 &= \cos(\gamma)\\
\pi &= \gamma
\end{align}
$$
So $(u_{xz},u_{xy})= -1$. Again using the [[Geometry of Hyperbolic Space#^613ac9|claim]] that $\pr \cdot\cdot$ is positive definite on $x^\bot$, we have that $u_{xz}=-u_{xy}$.

. Let $w = -\sinh(c)x-\cosh(c)u_{xz}$. Then 
$$
\begin{align}
(z,w) &= (\cosh(c)x+\sinh(c)u_{xz},-\sinh(c)x-\cosh(c)u_{xz})\\
&= -\sinh(c)\cosh(c)(x,x)-\sinh(c)\cosh(c)(u_{xz},u_{xz})\\
&= 0\\
(w,w) &= \sinh(c)^2(x,x)+\cosh(c)^2(u_{xz},u_{xz})\\
&= 1\\
\end{align}
$$
Take $l_{zy}$ to be the hyperbolic segment starting at $z$ in the direction $w$ with length $a$. Then:
$$
\begin{align}
l_{zy}(c) &= \cosh(c)z+\sinh(c)w\\
&= \cosh(c)^2x+\sinh(c)\cosh(c)u_{xz}-\sinh(c)^2x-\cosh(c)\sinh(c)u_{xz}\\
&= x\\
l_{zy}(a) &= \cosh(a)z+\sinh(a)w\\
&= \cosh(a)\cosh(c)x+\sinh(c)\cosh(a)u_{xz}-\sinh(a)\sinh(c)x-\cosh(c)\sinh(a)u_{xz}\\
&= (\cosh(a)\cosh(c)-\sinh(a)\sinh(c))x+(\sinh(c)\cosh(a)-\cosh(c)\sinh(a))u_{xz}\\
&= \cosh(a-c)x-\sinh(a-c)u_{xz}\\
&= \cosh(b)x+\sinh(b)u_{xy}\\
&= y
\end{align}
$$
This proves every point $x$ on $g$ is on the [[Geometry of Hyperbolic Space#^67d194|unique]] hyperbolic segment $l_{zy}$ from $z$ to $y$, so $g = l_{zy}$. $\square$


```ad-Proposition
Hyperbolic lines are exactly the (non-empty) intersections of $\HP^n$ with two dimensional subspaces $S\subseteq \R^{n+1}$.
```

^bd160e

__Proof__: Let $l$ be a hyperbolic line at $x$ in direction $u$. Then $l\subseteq S = \span(x,u)$ by definition. Moreover, if $y\in S\cap \HP^n$, then we have:
$$
\begin{align}
\pr y y &= (rx + tu, rx + tu)\\
&= -r^2 + t^2\\
&= -1\\
1&= r^2 - t^2
\end{align}
$$
We'll first have to show that $r>0$. If not, then since $y_{n+1} = rx_{n+1}+tu_{n+1}>0$, we have $x_{n+1}<\frac{-tu_{n+1}}{r}$ where $tu_{n+1}> 0$.

Let $\theta$ be such that $\theta = \sinh^{-1}(t)$ ($\sinh$ is a bijection from $\R$ to $\R$). Then, $$





