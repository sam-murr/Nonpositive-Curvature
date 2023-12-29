Below, we will usually usually linearly reparametrize geodesics to have domain $[0,1]$.
![[Curvature]]
![[Convex Space]]


```ad-Theorem
title:Cartan Hadamard Theorem (part 1)
Let $X$ be a simply connected complete geodesic metric space with [[Curvature|curvature]] $\leq \kappa \leq 0$. Then it is $\CAT(\kappa)$.
```

^thmpt1

```ad-Theorem
title:Cartan Hadamard Theorem (part 2)
Let $X$ be a simply connected complete geodesic metric space which is locally convex. Then it is convex.
```

^thmpt2

__Proof__: Will start by proving part 2. Starred lemmas are not proven in class, will likely not be on exam.
```ad-Lemma
title:Lemma 1 *
If we have two local geodesics $c'$, $c''$ such that $t\mapsto d(c'(t),c''(t))$ is locally convex, then $t\mapsto d(c'(t),c''(t))$ is convex.
```

^lemma1

![[Cartan Hadamard 1.png]]
__Proof__ :It suffices to show that if $f(t) = d(c'(t),c''(t))$ is convex on $[0,b]$ and $[a,1]$ for $a < b$, then it is convex on $[0,1]$. Suppose $q\in(a,b)$, then we have:
$$
\begin{align}
f(q)&\leq(1-\frac{q-a}{1-a})f(a) + (\frac{q-a}{1-a})f(1)\\
&\leq(1-\frac{q-a}{1-a})(1-\frac{a}{q})f(0)+(1-\frac{q-a}{1-a})\frac{a}{q}f(q) + (\frac{q-a}{1-a})f(1)\\
(1-(1-\frac{q-a}{1-a})\frac{a}{q})f(q)&\leq(1-\frac{q-a}{1-a})(1-\frac{a}{q})f(0)+ (\frac{q-a}{1-a})f(1)\\
f(q)&\leq\frac{(1-\frac{q-a}{1-a})(1-\frac{a}{q})}{(1-(1-\frac{q-a}{1-a})\frac{a}{q})}f(0)+ \frac{\frac{q-a}{1-a}}{(1-(1-\frac{q-a}{1-a})\frac{a}{q})}f(1)\\
&=(1-q)f(0)+ qf(1)
\end{align}
$$
A similar thing works for $q\geq b$ and $q\leq a$. $\square$ (lemma)
```ad-Lemma
title:Lemma 2
Let $X$ be complete and locally convex, let $c:[0,1]\to X$ be a [[Geodesic|local geodesic]] from $x$ to $y$. Suppose $\eps$ is small enough so that for all $t\in[0,1$], $B_{2\eps}(c(t))$ is convex. Then, taking $x'$ and $y'$ less than $\eps$ from $x$ and $y$ resp. we have that there is a unique local geodesic $c':[0,1]\to X$ from $x'$ to $y'$ such that $d(c'(t),c(t))<\eps$ for all $t$.
```

^lemma2

__Proof__: If $c'$ exists, then it is unique, since if $c'(0) = c''(0)$ and $c'(1) = c''(1)$, then $t\mapsto d(c'(t),c''(t))$ is locally convex, so  it is convex, so $d(c'(t),c''(t)) = 0$ for all $t$.

To show existence, we will use "induction on the real numbers". Specifically, let the proposition $P(A)$ stand for for all $a,b\in[0,1]$, $b-a<A$, $x',y'\in X$ with $d(c(a),x'),\ d(c(b),y')<\eps$ then there is a local geodesic $c':[a,b]\to X$ with $c'(a) = x'$ and $c'(b)=y'$.

The base case is $A<\frac{\eps}{\len(c)}$, which is true by local convexity ($b-a<\frac{\eps}{\len(c)}$ implies $d(c(a),c(b))<\eps$, so $x'$ and $y'$ are both in $B_{2\eps}(c(a))$).

We will now show that if it is true for $A$, then it is true for $\frac{3}{2}A$.
Suppose below that $a_0,a_1,a_2,a_3\in[0,1]$ with $a_{i+1}-a_i < \frac{A}{2}$. Let $p_0 = a_1$, $2_0 = a_2$. Take $d(c(a_0),x'),\ d(c(a_3),y')<\eps$. By the induction hypothesis, there is local geodesic $g_0$ from $x'$ to $q_0$ and $l_0$ from $y'$ to $p_0$. Let $p_1$ and $q_1$ be the point halfway along each of the respective geodesics. 
![[Cartan Hadamard 2.png]]
By (local) convexity of function $t\mapsto d(g_0(t),c(\frac{a_2-a_0}t+a_0))$ (here we are rescaling $c\rest[0,a_2]$ to have unit interval domain), we have that $p_1$ and $q_1$ are less than $\frac{\eps}{2}<\eps$ away from $c(a_1)$ and  $c(a_2)$ respectively. Then, we can apply $P(A)$ again to get $g_1$, $l_1$ from $x'$ to $q_1$ and $y'$ to $p_1$:
![[Cartan Hadamard 3.png]]
Similarly define $p_2$ and $q_2$ to be the halfway points of $g_1$, $l_1$. By convexity now applied to $g_1$ and $g_0$ (who have the same right endpoint and left endpoints are $<\eps/2$ apart), we get that $d(p_2,p_1)<\frac{\eps}{4}$, and similarly for $q_1$ and $q_2$. Moreover, the distance between $g_0(t)$ and $g_1(t)$ is bounded by $\eps/2$. 

If we continue this process of making $g_n$ and $l_n$ go from $x'$ to $q_n$ and  $y'$ to $p_n$, and define $p_{n+1}$ and $q_{n+1}$ to be the midpoints, we get that $d(g_{n-1}(t),g_n(t))\leq \frac{\eps}{2^n}$ (same for $l_n$). Therefore $g_n$ and $l_n$ converge pointwise to local geodesics $g$ and $l$. 

$g(\frac{1}{2}) = \lim_n p_n = p$, $g(1) = \lim_n q_n = q$, and $g(\frac{1}{2}) = \lim_n p_n = p$, $g(1) = \lim_n q_n = q$. Since $d(c(a_1),p) < \sum_n 2^{-n}\eps = \eps$ and $d(c(a_2),q) < \sum_n 2^{-n}\eps = \eps$, by $P(A)$ there is unique local geodesic from $p$ to $q$, meaning that $g\rest[\frac12,1] = l\rest[0,\frac12]$. This means we can glue together $g$ and $l$ in the usual way to get a local geodesic from $x'$ to $y'$. Moreover, by convexity of $g$ and $l$ and the fact that $d(c(a_1),p) < \eps$ and $d(c(a_2),q) < \eps$ the resulting geodesic will be within $\eps$ of $c$. $\square$ (lemma)

```ad-Lemma
title:Lemma 3 *
Let $f:X'\to X$ be a [[Classes/Metric Spaces with Nonpositive Curvature/Copied Notes for GIT/Isometry|local isometry]] with $X'$ complete metric space and $X$ locally convex geodesic metric space. Then, $f$ is a covering map.
```

^lemma3

__Proof__: First, note that local isometry implies $X'$ is complete locally convex.


Take a point $x\in X$ and $x'\in f^{-1}(\{x\})$ and $c:[0,a]\to X$ geodesic from $x$ to some $y$, then we can define a unique lifting $c':[0,a]\to X$ local geodesic from $x'$ to unique $y'$ with $f \circ c' = c$. This is certainly true for $a<\eps'$, where $\eps'$ witnesses local convexity around $x'$. Suppose $c'$ has been defined on $[0,b)$ for $b\leq a$. Then, by completeness, there is a unique value $c'(b) = \lim_{r\to b}c'(r)$, and $c(b) = f(c'(b))$. Moreover, around $c'(b)$ there is some $\eps_b$ ball which is isometric to the ball around $c(b)$, so we may extend $c'$ to agree with the local geodesic $c$ in this ball. So $c'$ exists. The same argument shows uniqueness.

This shows that $f$ is surjective.


Take $x\in X$ and let $\eps$ small enough so that $B_\eps(x)$ is locally convex,  take $x'\in f^{-1}\{x\}$, then let $\phi_{x'}:B_\eps(x)\to f^{-1}B_\eps(x)$ where $\phi(y)$ is the unique $y'$ that is the endpoint of the lift at $x'$ of the geodesic $c$ from $x$ to $y$. This is well defined, since $B_\eps(x)$ is uniquely geodesic. We also have $f\circ \phi_x = \Id_{B_\eps(x)}$.


For all $y'\in f^{-1}B_\eps(x)$, there exists some $x'$ with $y'\in \phi_{x'}(B_{\eps}(x))$. Let $y= f(y')$, then let $c$ be the geodesic from $y$ to $x$, lift that to $c'$, then $c'(1) = x'$ works. $\phi_{x'}$ is an open map, since $f$ is a local isometry.

Take $\eps'$ small enough so that $f\rest B_{\eps'}(c'(t))$ is an isometry for every $t$ and $\eps'$ satisfies the conditions for [[Cartan Hadamard Theorem#^lemma2|lemma 2]] with $c$ geodesic from $x$ to $y$. Then for every $z\in B_\eps(x)$ with $d(z,y)< \eps'$, we have by [[Cartan Hadamard Theorem#^lemma2|lemma 2]] that there is a unique local geodesic $g$ from $x$ to $z$ such that $d(c(t),g(t))< \eps'$ for all $t$. By convexity in $B_\eps(x)$ this is the geodesic from $x$ to $z$. Then, if $g'$ and $c'$ are the lifts of the geodesics, then a similar argument to the first paragraph shows that $d(c'(t),g'(t))< \eps'$, so $d(c'(t),g'(t))=d(c(t),g(t))$, so in particular  $d(\phi_{x'}(z),\phi_{x'}(y)) = d(z,y)$. This shows $\phi_{x'}$ is continuous.

It now suffices to show that for distinct $x',x''\in f^{-1}\{x\}$, $\Image \phi_{x'}\cap \Image \phi_{x''} = \emptyset$. Otherwise, there is $y'\in\phi_{x'}\cap \Image \phi_{x''}$, then there are two distinct lifts of the geodesic $c$ from $y$ to $x$, the one whose reverse is the local geodesic from $x'$ to $y'$, the other's reverse is the local geodesic from $x''$ to $y'$.  This contradicts uniqueness of lifts. $\square$

__Proof__: [[Cartan Hadamard Theorem#^thmpt2|(Thm pt 2) ]]
```ad-Definition
title: Definition: Space of Geodesics and the $\exp$ Map
Let $x\in X$, define $\tilde{X}$ to be the space of all local geodesics issuing from $x$ (along with the constant $x$ map $\tilde{x}$) with the $\sup$ metric $\tilde{d}$:
$$
\tilde{d}(c,c') = \sup_{t\in[0,1]} d(c(t),c'(t))
$$
Define the $\exp_x:\tilde{X}\to X$ via $c\mapsto c(1)$. (recall the $\exp_x$ [[Riemannian Geometry#^82c0c0|map]] from the tangent space at $x\in M_\kappa$ to $M_\kappa$, which does a similar thing)

```

```ad-Claim
title: Claim 1
$\tilde{X}$ is [[Null Homotopic|contractable]].
```
__Proof__: Define the [[Homotopy|homotopy]] $h:\tilde{X}\times[0,1]\to \tilde{X}$ via $h(c,r)(t) = c((1-r)t)$. This is a homotopy from the identity to the constant $\tilde{x}$ map. $\square$ (claim)

```ad-Claim
title: Claim 2
$\exp$ is a local isometry.
```
__Proof__: For all local geodesics $c$, let $c(1)=y$ and choose $\eps$ from [[Cartan Hadamard Theorem#^lemma2|lemma 2]], then $\exp\rest B_\eps(c)$ is an isometry to $B_\eps(y)$. Note that if $\tilde{d}(c,c')<\eps$, then $d(c(t),c'(t))<\eps$ for all $t$, so by local convexity and [[Cartan Hadamard Theorem#^lemma1|lemma 1]] we have that  $d(c(t),c'(t))\leq td(c(1),c'(1))$ which implies $\tilde{d}(c,c') =d(c(1),c'(1)) = d(\exp_x(c),\exp_x(c'))$. This shows $\exp$ is an isometric embedding on  $B_\eps(c)$. To show it is surjective, let $y'\in B_\eps(y)$, then by [[Cartan Hadamard Theorem#^lemma2|lemma 2]] there is a unique local geodesic $c'$ starting at $x$ ending at $y'$, so $\exp_x(c') = y'$. $\square$ (claim)

```ad-Claim
title: Claim 2
$\tilde{X}$ is complete.
```
__Proof__:
Let $c_n$ be a Cauchy sequence of local geodesics. Then $y_n = c_n(1)$ is cauchy, so by completeness of $X$ we have that $y_n\to y$ and $c_n(t)$ uniformly converges to some continuous function $c(t)$. We will show $c$ is a local geodesic. 

Let $\eps>0$ be small enough so that for all $t\in[0,1]$, $B_{4\eps}(c(t))$ is convex. In particular, this means that any local geodesic $c_n$ within $\eps$ of $c$ satisfies the conditions of [[Cartan Hadamard Theorem#^lemma2|lemma 2]].  Take $N$ big enough so that $d(y_N,y)< \eps/2$ and $\tilde{d}(c_n,c_m)<\eps/2$ for all $n,m\geq N$. Then by lemma 2 we have that for all $n\geq N$ there is a unique local geodesic $c'_n$ from $x$ to $y$ such that $\tilde{d}(c'_n,c_n) = d(y_n,y)<\eps/2$ (by convexity). Note that for all $n,m\geq M$, $c'_n = c'_m$ by uniqueness in lemma 2 (since $d(c'_n,c_n)<\eps/2$ and $d(c_n,c_m)<\eps/2$ implies $d(c'_n,c_m)<\eps$ ). Let $c'$ be this unique local geodesic.

Moreover, since $\tilde{d}(c_n,c') = d(y_n,y)\to 0$, the $c_n$ converge to $c'$ pointwise, so $c = c'$ is a local geodesic. $\square$




By [[Cartan Hadamard Theorem#^lemma3|lemma 3]] we then have that $\exp_x$ is a covering map. Since $X$ is simply connected, this means that $\exp_x$ is a homeomorphism. In particular, it is bijective, so for any point $y$ there is a unique local geodesic from $x$ to $y$, namely the geodesic.

Now take any two geodesics $c$ and $c'$, let $g$ and $g'$ connect $c(0), c'(0)$ and  $c(1), c'(1)$ respectively. Then, let $c_r$ be the geodesic from $g(t)$ to  $g'(t)$. Pick an $\eps$ small enough to satisfy the statement of  [[Cartan Hadamard Theorem#^lemma2|lemma 2]] for all $c_r$. Then, pick sequence $c_0,\dots, c_n$ with $c_0 = c$, $c_n = c'$, and the distance $d(c_i(0),c_{i+1}(0))$ and $d(c_i(1),c_{i+1}(1))$ is $< \eps$. 
![[Cartan Hadamard 4.png]]
By [[Cartan Hadamard Theorem#^lemma2|lemma 2]] , this means there is a unique local geodesic from $c_{i+1}(0)$ to $c_{i+1}(1)$ which is within $\eps$ of $c_i$. By what we proved above, this must be $c_{i+1}$, so in particular by local convexity $t\mapsto d(c_i(t),c_{i+1}(t))$ is convex. Then we have:
$$
\begin{align}
d(c_0(t),c_n(t)) & \leq \sum_{i} d(c_i(t),c_{i+1}(t))\\
& \leq \sum_{i} (1-t)d(c_i(0),c_{i+1}(0)) + td(c_i(1),c_{i+1}(1))\\
& = (1-t)\sum_{i}d(c_i(0),c_{i+1}(0)) + t \sum_{i}d(c_i(1),c_{i+1}(1)))\\
& = (1-t)d(c_0(t),c_n(0)) + td(c_0(1),c_n(1))
\end{align}
$$
(we have equality since the endpoints of the $c_i$s are on the geodesic $g$ and $g'$). $\square$ ([[Cartan Hadamard Theorem#^thmpt2|thm part 2]])

__Proof__: ([[Cartan Hadamard Theorem#^thmpt1|thm part 1]])
Note that since $\CAT(0)$ implies convex, curvature $\leq \kappa \leq 0$ implies locally convex. So $X$ is convex by [[Cartan Hadamard Theorem#^thmpt2|thm part 2]], so it is uniquely geodesic and geodesics vary continuousl (in $\tilde{X}$) with their endpoints. 



```ad-Lemma
title: Lemma 4 (Glueing Lemma)
Let $pq_1q_2$ be a geodesic triangle with $r$ on the geodesic $q_1$ to $q_2$. If the angles in the comparison triangles $p'q_1'r'$ and $p'q_2'r'$ are no smaller than the alexandrov angles of $pq_1r$ and $pq_2r$. Then, the angles on comparison triangle $p''q_1''q_2''$ are no smaller than the alexandrov angles of $pq_1q_2$.

```
![[Screenshot 2023-12-11 at 3.03.41 PM.png]]
__Proof__: This is a direct application of the  [[Alexandrov Lemma]]. $\square$ (lemma)

By the [[CAT Kappa Spaces and Curvature|equivalent characterizations]] of the $\CAT(\kappa)$ inequality, this means we can "glue together" two $\CAT(\kappa)$ triangles into a larger $\CAT(\kappa)$ triangle.

Consider a geodesic triangle $xyz$ in $X$, let $g$ be the geodesic connecting $x$ and $y$, for $s\in[0,1]$ let $c_s$ be the geodesic connecting $z$ and $g(s)$. Since geodesics vary continuously with their endpoints, the map $[0,1]^2\to X$ given by $(s,t)\mapsto c_s(t)$ is continuous. Therefore we can pick $\eps$ small enough so that $B_{2\eps}(c_s(t))$ is $\CAT(\kappa)$. Let $0 = s_0, s_1,\dots, s_n = 1$ divide $g$ into segments of length $<\eps$. Then, let $t^i_k$ divide each $c_{g(s_i)}$ into segments of length $<\eps$. Then the triangles $c_{g(s_i)}c_{g(s_{i+1})}$ subdivide $xyz$, and each of these triangles is within the $2\eps$ of a point in the image of $(s,t)\mapsto c_s(t)$ so the triangles are $\CAT{\kappa}$ .

![[Cartan Hadamard 6.png]]

We can then use the gluing lemma to glue together all the small triangles into one big $\CAT(\kappa)$ triangle. First, we glue together the long skinny triangles, in the order of the gradient starting from the top:

![[Cartan Hadamard 7.png]]
$\square$