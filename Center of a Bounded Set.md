```ad-Definition
title:Definition: Radius of Bounded Set
Let $B\subseteq X$ be a bounded set in metric space $X$, then the <u>radius</u> of $B$ is:
$$\text{rad}(B) = \inf_{x\in B,\ r\in \R}\{r:\bar{B}_r(x)\supseteq B\}$$
$x\in B$ is the <u>center</u> of $B$ if $\bar{B}_{\text{rad}(B)}(x)\supseteq B$
```
```ad-Proposition
title:Proposition: Centers exist and are unique
Let $B\subseteq X$ be a bounded subset of complete $\CAT{(0)}$ space $X$ then there exists a unique center $c$ of $B$.
```
__Proof__: Let $r=\text{rad}(B)$ and $r_n\to r$ and $x_n$ with $\bar{B}_{r_n}(x_n)\supseteq B$. We will show $x_n$ is Cauchy. Otherwise, there exists some $\eps$ and subsequence of $x_n$ (wlog the entire sequence) with $d(x_n,x_{n+1})\geq 2\eps$. Take $n$ large enough so that $r_n^2<r_n^2-\eps^2$. Then take any $y\in B$.
![[Center 1.png]]
Let $m$ be the midpoint of the comparison triangle $y'x_n'x_{n+1}'$. Then by the law of cosines:
$$
\begin{align}
d(y',x_n')^2 &= d(x_n',m)^2+d(y',m)^2 -2d(x_n',m)d(y',m)\cos(\theta)\\
&\geq d(x_n',m)^2+d(y',m)^2\\
d(y',m)^2 &\leq d(y',x_n')^2-d(x_n',m)^2\\
& \leq r_n^2-\frac{d(x_n',x_{n+1}'')}{2}^2\\
& \leq r_n^2-\eps^2\\
& <r^2\\
\end{align}
$$
This means $d(y',m)<r$. So the point corresponding to $m$ in the geodesic $x_{n}x_{n+1}$  had distance $< r$ for all $y\in B$, contradicting the definition of $r$. $\square$

```ad-Corollary
Let $G$ be a group of isometrys on $\CAT(0)$ space $X$ with bounded orbit. Then there exists $x\in X$ fixed by $G$.
```
__Proof__: Take any $x\in X$, then $G\cdot x$ is a bounded set invariant under $G$. The center of $G\cdot x$ is invariant under $G$, since $G\cdot x$ is. $\square$