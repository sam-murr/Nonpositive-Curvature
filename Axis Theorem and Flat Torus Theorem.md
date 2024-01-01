
```ad-Definition
title: Displacement Function and Hyperbolic Isometries
Let $g$ be an isometry of metric space $X$. The <u>displacement function</u> of $g$ is $d_g:X\to\R$ via $d_g(x)= d(x,gx)$. The <u>translation length</u> of $g$ is $|g| = \inf_{x\in X}d_g(x))$. The set of $x\in X$ witnessing this is called the <u>minset</u> $\Min(g)=\{x\in X: d_g(x)=|g|\}$.
-  If $|g| = 0$ and $\Min(g)\neq\emptyset$, then $g$ is called <u>elliptic</u>.
- If $|g| > 0$ and $\Min(g)\neq\emptyset$, then $g$ is called <u>hyperbolic</u>.
- If  $\Min(g)=\emptyset$, then $g$ is called <u>parabolic</u>.

Hyperbolic and elliptic isometries are called <u>semi-simple</u>
```

^hypisom

```ad-Example
In $\HP^2$, rotations are elliptic, compositions of two inversions which are perpendicular to the same line is hyperbolic, and the composition of two inversions.
```

```ad-Lemma
If $X$ is convex, then $\Min(g)$ is convex.
```
__Proof__: Let $x,y\in \Min(g)$ and let $c$ be a geodesic from $x$ to $y$. Then $gc$ is a geodesic from $gx$ to $gy$. Then by convexity $d(c(t),gc(t))\leq (1-t)d(x,gx)+td(y,gy) = |g|$. $\square$

```ad-Theorem
title:Theorem: Axis Theorem
Let $g$ be an isometry of a $\CAT(0)$ space $X$, then $g$ is hyperbolic iff there exists a geodesic line $c$ such that $g$ acts by translation along $c$ (ie $gc(t)= c(t+a)$).
```

^axisthm

__Proof__: ($\Rightarrow$) Let $x\in\Min(g)$, then take geodesic $c_1$ from $x$ to $g\cdot x$. Let $c_2  = gc_1$ be geodesic from $gx$ to $g^2 x$. If $c_2\cup c_1$ is a geodesic from $x$ to $g^2x$, then we can repeat this to get a geodesic line translated by $|g|$. Let $m$ be midpoint of $c_1$, then $gm$ is the midpoint of $c_2$. Note $m\in\Min(g)$,  $c_1\rest[\frac 12, 1]\cup c_2\rest[0,\frac 12]$ is a geodesic since it has length $|g|$. So $c_2\cup c_1$ is a local geodesic, so it is geodesic. 

($\Leftarrow$) Since the axis is a convex complete set, we can [[Projection to a Convex Set|project]] any point $x$ to $c$ to get $\pi(x)$. Then, since $g$ is an isometry, $\pi(gx) = g\pi(x)$, so $d(x,gx)\geq d(\pi(x),\pi(gx))= d(\pi(x),g\pi(x))=a$. $\square$

```ad-Theorem
title:Theorem: Decomposition Theorem
Let $g$ be a hyperbolic isometry on a $\CAT(0)$ metric space $X$, then $\Min(g)$ is of the form $Y\times \R$ where $Y$ is a $\CAT(0)$ metric space $g$ acts on $\Min(g)$ via $(t,x)\mapsto (t+a,r)$.
```

^decompositionthm

__Proof__:
```ad-Lemma
title:Lemma: Flat Triangle Lemma
Let $pqq'$ be a geodesic triangle in $\CAT(0)$ space. If the alexandrov angle at $p$ equals the angle at $\bar{p}$ in the $0$ comparison triangle $\bar{p}\bar{q}\bar{q}'$ then there is an isometry from the convex hull of $pqq'$ to the convex hull of $\bar{p}\bar{q}\bar{q}'$.
```
^flattri

__Proof__: We will first show that for all $r$ in geodesic $qq'$, $d(p,r) = d(\bar{p},\bar{r})$. Let $\alpha = \angle_p qq'$ be the alexandrov angle at $p$.
![[Axis 1.png]]
We see that the sum of the alexandrov angles $\angle_pqr$ and $\angle_pqr$ is at least $\angle_p qq'$, so using the [[Alexandrov Lemma|alexandrov lemma]] on geodesic triangles $pqr$ and $prq'$ we have that:
$$
\begin{align}
\angle_pqq' &\leq \angle_pqr + \angle_pqr\\
&\leq \angle_{\bar{p}}^0\bar{q}\bar{r} + \angle_{\bar{p}}^0\bar{q}'\bar{r}&\text{By $\CAT(0)$ ineq}\\ 
&\leq \angle_{\bar{p}}^0\bar{q}\bar{q}'&\text{By Alexandrov lemma}\\
&= \angle_pqq'&\text{By assumption}
\end{align}
$$
So by the equality clause of the Alexandrov lemma, since $\angle_{\bar{p}}^0\bar{q}\bar{q}' = \angle_{\bar{p}}^0\bar{q}\bar{r} + \angle_{\bar{p}}^0\bar{q}'\bar{r}$, we have $d(p,r) = d(\bar p,\bar r)$. This proves our first claim. We'll now show that the map from the triangle $\bar{p}\bar{q}\bar{q}'$ to the convex hull of $pqq'$ given by $x\mapsto x'$ where $x'$ is the unique point at distance $d(\bar{p},x)$ along the geodesic $pr$ where $r$ is the unique point on $qq'$ such that  $\bar p \bar r$ is contains x.  This map is continuous by convexity. Let $x,y4 in the convex hull of  $pqq'$,  and let $r, r'$ as below. Note by what we just proved $\bar p\bar q \bar r$, $\bar p\bar r \bar r'$ ,and  $\bar p\bar r' \bar q'$ are comparison triangles for $pqr$, $prr'$, and $pr'q'$. So in particular, $d(x',y')\leq d(x,y)$. It suffices to show the reverse inequality.

![[Axis 2.png]]

 By $\CAT 0$ inequality, $\angle_{\bar p}\bar q \bar r$, $\angle_{\bar p}\bar r \bar r'$ ,and  $\angle_{\bar p}\bar r' \bar q'$ are greater than or equal to $\angle_{p}q r$, $\angle_{ p}r  r'$ ,and  $\angle_{ p} r'  q'$ respectively. since $\angle_{\bar p}\bar q \bar r+\angle_{\bar p}\bar r \bar r'+\angle_{\bar p}\bar r' \bar q' = \angle_{\bar p}\bar q \bar q' = \angle_{ p} q  q' = \angle_{p}q r+\angle_{ p}r  r'+\angle_{ p} r'  q'$, we then have equality  $\angle_{\bar p}\bar r \bar r'=\angle_{ p} r  r'$. Then if $d(x',y') < d(x,y)$, the comparison triangle for $px'y'$ would have a strictly smaller angle at $p$ than $\angle_{ p} r  r'$ contradicting $\CAT(0)$. $\square$ (lemma)
```ad-Corollary
title:Lemma: Flat Quadrangle lemma
Let $pp'qq'$ be a geodesic quadrangle in $\CAT(0)$ space. If the inner alexandrov angles sum to $\geq 2\pi$, then the sum to exactly $2\pi$ and the is an isometry from the convex hull of the vertices to a convex hull of the quadrangle in $\R^2$ with corrisponding angles and side lengths.
```
^flatquad

__Proof__:  exercise $\square$

__Proof__: ([[Axis Theorem and Flat Torus Theorem#^decompositionthm|decomposition theorem]]): WLOG let $X = \Min(g)$ since $\Min(g)$ is convex. Take $x\in X$, then by the [[Axis Theorem and Flat Torus Theorem#^axisthm|axis theorem]] let $c_x$ be the geodesic axis through x and let $c_x(0) = x$. $c_x$ is convex, so we can call the projection to $c_x$ via $\pi_x$. Let $Y = \pi_x^{-1}(\{x\})$, then we can define the map $\phi:Y\times \R\to X$ via $(y,t)\mapsto c_y(t)$. 

 Note for any $x,z\in X$, the map $t\mapsto d(c_x(t),c_z(t))$ is periodic since $d(c_x(t),c_z(t)) = d(c_x(t+|g|),c_z(t+|g|))$, so by convexity it is constant.

$\phi$ is then a surjection: for any $z\in X$, if $c_x(t) = \pi_x(z)$, then $x = c_x(0) = \pi_x(c_z(-t))$, so $\phi(c_z(-t),t) = z$. A similar argument shows that $\pi_x(y) = c_x(t)$ then $\pi_y(c_x(t)) = y$, and moreover if $y\in Y$ then $\pi_x(c_y(r)) = c_x(r)$ and $\pi_y(c_x(r)) = c_y(r)$ 

We will show that $d(\phi(0,r),\phi(y,t)) = \sqrt{d(z,y)^2+(t-r)^2}$. Consider the rectangle $c_x(r),c_x(t), c_y(r), c_y(t)$. Note that by our proposition about [[Projection to a Convex Set|projections]] we have that each of the angles in the quadrangle is $\geq \pi/2$, so their sum is at least $2\pi$. By the [[Axis Theorem and Flat Torus Theorem#^flatquad|flat quadrangle lemma]], each of these angles are exactly $\pi/2$ and the rectangle is isometric to the rectangle in $\R^2$ with side lengths $d(x,y)$ and $|r-t|$. This means that the diagonal from $c_x(r)$ to $c_y(t)$ has length  $\sqrt{d(z,y)^2+(t-r)^2}$ as desired.
![[Axis 3.png]]

We just need to prove that the map $\phi$ is independent of what point $x$ in $Y$ you pick to be the base point, ie if $x'\in Y$, then if $Y' = \pi^{-1}_{x'}(\{x'\})$ and $\phi':Y'\times \R \to X$ ,then is $\phi = \phi'$. It suffices to show that $Y' = Y$, in particular, if $\pi_x(y)=\pi_x(z) = x$, then is $\pi_z(y) = z$.

Suppose $\pi_(y) = c_y(\eps)$. Let $a = d(x,y)$, $a' = d(c_y(\eps),z)$, and $a'' = d(x,z)$. Let $A = a+a'+a''$. Then, for any $s$ and $t$, we have: 
$$
\begin{align}
d(c_x(s),c_y(s+t)) &= \sqrt{a^2+t^2} & d(c_z(s),c_x(s+t)) &= \sqrt{a''^2+t^2} & d(c_y(s),c_x(s+t)) &= \sqrt{a'^2+(t-\eps)^2}
\end{align}
$$
![[Axis 4.png]]
Consider the following applications of the triangle inequality:
$$
\begin{align}
d(c_x(0),c_x(As+\eps)) &= d(c_x(0),c_y(as)) + d(c_y(as),c_z((a+a')s+\eps)) + d(c_z((a+a')s+\eps),c_x(As+\eps))\\
 &= \sqrt{a^2+as^2} + \sqrt{a'^2 + a'^2s^2} + \sqrt{a''^2+a''^2s^2}\\
 &= A\sqrt{s^2+1}\\
As+\eps&\leq A\sqrt{s^2+1}\\
\eps&\leq A(\sqrt{s^2+1}-s)\\
\end{align}
$$
As  $s\to \infty$, $\sqrt{s^2+1}-s\to 0$, so $\eps = 0$. For any $x,z\in Y$, we can take $y'$ to be a point on the geodesic $x$, $z$ and let $y = \pi_{y'}(x)$. The above analysis then shows that $d(y,z)\leq d(y',z)$ and $d(y,x)\leq d(y',x)$, so the the path $[xy][yz]$ is a geodesic, so $y=y'$. This shows that $Y$ is convex, so it is $\CAT(0)$. $\square$



```ad-Theorem
title:Theorem: Flat Torus Theorem
If $G$ is a torsion free abeleian group of rank $n$ acting properly by semisimple isometries on complete $\CAT(0)$ space $X$, then $\Min(G) = \cap_{g\in G} \Min(g)$ is nonempty and splits as $Y\times \R^n$ where $G$ acts trivially on $\CAT(0)$ space $Y$ and by translations on $\R^n$. Moreover, $\R^n/G$ is an $n$ torus.
```
__Proof__: We will induct on the rank of $G$. Since the $G$ acts by [[Axis Theorem and Flat Torus Theorem#^hypisom|semi-simple]] isometries is [[Actions on CAT 0 Spaces|proper]], it is [[Axis Theorem and Flat Torus Theorem#^hypisom|hyperbolic]]. So if $n = 1$, this is just the [[Axis Theorem and Flat Torus Theorem#^decompositionthm| decomposition theorem]]. 

```ad-Lemma
title:Lemma: Splitting Lemma
Let $g$ be a hyperbolic isometry on $\CAT(0)$ space and let $f$ be isometery which commutes with $g$, then $\Min(g)=Y\times \R$ is invariant under $f$, and $f$ splits into $(f',f'')$, where $f'$ is an isometry of $Y$ and $f''$ is a translation of $\R$.
```
__Proof__:(lemma)  Firstly, note that $d_g(x) = d(x,g\cdot x) = d(f\cdot x,fg\cdot x)=d((f\cdot x),fgf^{-1}\cdot (f\cdot x)) = d_{fgf^{-1}}(f(x))$, so $|g|=|fgf^{-1}|$ and $f\cdot\Min(g) = \Min(fgf^{-1})$. Since $f$ and $g$ commute, $f\cdot\Min(g) = \Min(g)$. Moreover, $g$ axes are sent to $g$ axes by $f$ (since the axis from $x$ to $g(x)$ is sent to the axis from $f(x)$ to $g(f(x))$).

Fix some $x\in Y$, associate $Y$ and $\R$ with subsets $Y\times\{0\}$ and $\{x\}\times\R$. Below we will write $(y,t)$ as $y+t$ for $y\in Y$ and $t\in\R$.

We will show that $f' = \pi_{Y}\circ f$ and  $f'' = \pi_{\R}\circ f$. We have $f = (f',f'')$, so it just suffices to show they are isometries. Let $x,y\in Y$, then $d(x,y) = d(f(x),f(y)) = d(x'+t'+y'+r')\geq d(x',y') = d(f'(x),f'(y))$. Since $f$ sends axes to axes, $f^{-1}(x') = x+t''$ and $f^{-1}(y') = y+r''$, so $d(x',y') = d(f^{-1}(x'),f^{-1}(y'))=d(x+t'',y+r'')\geq d(x,y)$, so $d(x,y) = d(x',y')$. $f''$ will also be an isometry, since $|t-r|=d(x+t,x+r) = d(f(x+t),f(x+r)) = d(x'+t',x'+r') = |t'-r'|$.  Since $f$ commutes with $g$, we know that $f'$ cannot be a reflection, so it must be a translation of $\R$. 
$\square$ (lemma)

Now suppose $n>1$, $G = \langle g_1,\dots,g_n\rangle\cong\Z^n$ where the $g_i$ are the usual generators. By the decomposition theorem, $\Min(g_1) = Y_1\times \R$. Let $N$ be subgroup of $G$ fixing $Y_1$.

```ad-Claim
$N = \langle g_1 \rangle$

```
__Proof__:(claim) Since $N$ fixes  $Y_1$,  $N$ then acts properly on $\{y\}\times \R$ for any $y\in Y_1$. Fix a $y$, then  $N$  acts properly on $\R$ by semi-simple (thus hyperbolic) isometries, ie by translations. For any $f\in N$, let $t_f$ be such that $f\cdot r = r+t_f$ for all $r\in\R$. WLOG take $|g_1| = t_{g_1}$. Note that if $f,h\in N$ then $t_{fh} = t_{f}+t_{h}$, and moreover by properness and the fact $N$ is torsion free if $t_{fh} = 0$ then $f = h$ (otherwise, $\{(fh)^n\}$ would be an infinite set fixing $0$)

Let $f\in N$, take $S=\{n|g_1| + mt: n,m\in \N, n|g_1| + mt>0\}$ and $l = \inf S$. $l > 0$ by properness. Also if $S$ is closed under taking differences, so $l$ is witnessed by some element $c = n_0|g_1|+m_0t$ and we have that $kc=|g_1|$ and $jc=t$ for integer $k,j$. Let $h = n_0g_1+m_0f$, then $kh = g_1$ and $jh = f$. Since $g_1$ is not a proper power of another element, $h = g_1$, so $f = jg_1$.
$\square$ (claim) 

$H = \gen{g_2,\dots,g_{n}}\cong G/N$ acts on $Y_1$: let $f\in G$, $f=(f',f'')$ as in the splitting lemma, then $(f+N)\cdot y = f'(y)$. Let $r\in\R$ such that $f''$ is translation by $r$, then: $$d_f((y,t)) = \sqrt{d(y,f'(y))^2+d(t,f''(t))^2}=\sqrt{d_{f+N}(y)^2+r^2}$$
So $|f|=|f+N|$ and $\Min(f) = \Min(f+N)\times \R$ (so $\Min(H)\times\R=\Min(G)$). In particular, $G/N$ acts by semi-simple isometries. In order to apply the induction hypothesis, we just need to show the action is proper.

Let $B = B_\eps(y)\subseteq Y$ be a ball, then by properness $S = \{g\in G: g\cdot B\times[0,|g_1|]\cap B\times[0,|g_1|]\neq \emptyset\}$ is finite. If $\bar{f}=f+N \in H$ with $\bar{f}\cdot B\cap B$, then there is $y$, $y'\in B$ with $y' = f'(y)$. Then, there is some multiple of $g_1$ such that $f''(y)+n|g_1|\in[0,|g_1|]$, so $f+ng_1\in S$. Therefore there must be finitely many such $\bar{f}$. 

By induction, $\Min(H) = Y\times \R^{n-1}$ where $Y$ is fixed by $H$ and  $H$ acts by translations on $\R^{n+1}$. Then, $\Min(G) = Y\times \R^{n}$, where $Y$ is 