
![[Convex Subspace]]
```ad-Definition
title:Definition: $M^n_\kappa$ Simplex
A set of points $v_0,\dots, v_n$ in $M_\kappa^n$ is in <u>General Position</u> if they are not contained in a subspace isometric to $M^{n-1}_\kappa$ (in particular, a hyperplane)

A <u>$M^n_\kappa$ Simplex</u> is the [[Convex Subspace|convex hull]] of $n+1$ <u>vertices</u>  $S = \{v_0,\dots, v_n\}\subseteq M_\kappa^n$ that are in general position and contained in an open ball with radius $\leq \frac{1}{2}\diam(M_\kappa^n)$

A <u>face</u> of a simplex is the convex hull of some $T\subseteq S$. Note this is a $|T|-1$ simplex in the isometric copy of $M^{|T|-1}_\kappa$ spanned by $T$.
```


```ad-Definition
title:Definition: $\kappa$ Simplicial Complex
A $\kappa$ simplicial complex is a quotient of the disjoint union over $\lambda \in I$ of $M^{n_\lambda}_\kappa$ simplices $S_\lambda$ under an equivalence relation $\sim$ where $\sim$ identifies faces of simplices. Specifically, if $X = \bigsqcup_{\lambda\in I} S_\lambda /\sim$, $p:\bigsqcup_{\lambda\in I} S_\lambda\to X$ quotient map, and $p_\lambda = p\rest S_\lambda$, then:
- Each $S_\lambda$ embeds into $X$ via $p_\lambda$
- If $p_\lambda(S_\lambda)\cap p_\gamma(S_\gamma)\neq \emptyset$, then both $T_\lambda = p^{-1}_\lambda(p_\gamma(S_\gamma))$, $T_\gamma = p^{-1}_\gamma(p_\lambda(S_\lambda))$ are faces of their respective simplices and there exists an isometry $h_{\lambda\gamma}: T_\lambda \to T_\gamma$ such that $p_\gamma\rest T_\gamma = p_\lambda\rest T_\gamma\circ h_{\lambda\gamma}$.

The set of isometry classes of simplices and their faces in $X$ is called $\Shapes(X)$.

If $X$ is a $0$ simplicial complex (resp 1,-1), it is called piecewise euclidean(resp spherical, hyperbolic).
```

```ad-Definition
title:Definition: The Intrinsic Pseudometric
Let $X = \bigsqcup_{\lambda\in I} S_\lambda /\sim$ be a $\kappa$ simplicial complex. A <u>string</u> in $X$ between points $x$ and $y$ is a set of points $\Sigma = x_0,\dots, x_{m-1}$ along with a sequence of simplices $S_{\gamma_{i}}$ such that $x_0 = x$, $x_{m-1} = y$, and for all $i$ $x_{i+1}$ is in the same simplex $S_{\gamma_{i}}$ as $x_i$. We can then define the length of a string as:
$$
\len(\Sigma) = d_{\lambda_0}(x_0,x_1) + \dots + d_{\lambda_{m-2}}(x_{m-2},x_{m-1})
$$
Where $d_{\lambda_i}(x_i,x_{i+1})$ is the distance between $x_i$ and $x_{i+1}$ in $S_{\gamma_{i}}$. We can then define the <u>intrinsic pseudometric</u> $d$:
$$
d(x,y) = \inf\{\len(\Sigma): \Sigma \text{ is a string from }x\text{ to }y\}
$$
If there is no such string, then $d(x,y) = \infty$
```
```ad-note
This definition is clearly a pseudometric, as the reverse of a string is still a string and concatinating strings adds their length.
```

```ad-Definition
For $x\in X = \bigsqcup_{\lambda\in I} S_\lambda /\sim$, define $\eps(x)$ to be:
$$
\eps(x) = \inf\{d_{S}(x,T): T\text{ is a face of a simplex } S\text{ containing }x\text{ but }T \text{ does not contain $x$}\}
$$
```
```ad-Proposition
If $x,y\in X$ with $d(x,y) < \eps(x)$, then any simplex $S$ containing $y$ contains $x$, and $d(x,y) = d_S(x,y)$.
```
__Proof__: Let $\Sigma = x_0\dots x_m$ be a string from $x$ to $y$ with $\len(\Sigma) < \eps(x)$. Because of this, $d(x_0,x_1) <\eps(x)$, so $x_1$ is in the interior of some face of a simplex containing $x$. Then, since $x_2$ shares a simplex with $x_1$, it shares a simplex $S$ with $x_0$, since $x_1$ is in a face containing $x$. Moreover, it must be in the interior of that simplex. Therefore, $d(x,x_2) = d_S(x,x_2)\leq d_S(x,x_1)+d_S(x_1,x_2)$. This means $\Sigma' = x_0x_2\dots x_m$ is a chain with strictly smaller length. Continue until you get a two length chain, this will show $y$ is in the interior of a face containing $x$, which proves the two desired properties. $\square$.

```ad-Corollary
If for all $x\in X$, $\eps(x) > 0$, then it is a metric space with the induced pseudometric. 
```

```ad-Theorem
title: Bridson Theorem
If $\Shapes(X)$ has finitley many isometry classes, then $X$ is a complete geodesic space.
```
__Proof__: Note that $\eps(x) > 0$ for all $x$, since taking $T$ to be the simplex/face containing $x$ on its interior


(Proof of completeness) Let $x_n$ be Cauchy. Let $S_n$ be a simplex containing $x_n$ and by finiteness assume all the $S_n$ are isometric to some simplex $S$ via $f_n:S_n\to S$. Then, $f_n(x_n)$ has a convergent subsequence, since $S$ is compact, so say it converges to $y$. Let $T$ be the face of $S$ containing $y$ in the interior.

Let $\eps_0 <\eps(y)$ and  $\eps_0 < d(y,j(y))$ where $j$ is any isometry of $T$ which preserves vertices and does not fix $y$ (Note there are only finitely many such $j$ since the position of each point is determined by its distance to the vertices). Let $y_n = f^{-1}_n(y)$

Then, let $N$ big enough so that $d(x_n,x_N)<\frac{\eps_0}{3}$, $d(f_n(x_n),y)<\frac{\eps_0}{3}$ for all $n\geq N$. This means:
$$
d(y_N,y_n)\leq d(x_n,y_n)+d(x_n,x_N)+d(x_N,y_N) <\eps_0
$$
This means that if $d(y_N,y_n)<\eps_0$, so $d(y,f_N\circ f_n(y))<\eps_0$, since $f_N\circ f_n$ is an isometry of $S$, $y = f_N\circ f_n(y)$, so $y_N = y_n$, so $x_n\to y_N$. $\square$

```ad-missing
Somewhere we should use the fact that $d(y_N,y_n)<\eps(y)$ to show $y_N$ and $y_n$ are in the same simplex $S_n$, not sure how.
```

