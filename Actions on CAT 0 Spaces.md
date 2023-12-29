```ad-Definition
Let $G$ act on metric space $X$ by isometrys.

- The action is <u>cocompact</u> if there exists compact $K\subseteq X$ with $G\cdot K = X$.
- The action is <u>free</u> if for all $g\in G$ with $g\neq1$, $gx\neq x$.
- The action is <u>metrically proper</u> if for all $x\in X$ with $r>0$ the set $\{g: B_r(x)\cap B_r(gx)\neq 0\}$ is finite.
```

```ad-Proposition
Let $X$ be a complete $\CAT(0)$ space and $G$ acts on $X$ properly and cocompactly, then $G$ has only finitely many conjugacy classes of finite subgroups.
```
__Proof__: Let $K\subseteq X$ witnessing cocompactness, and $H\leq G$ finite. Then by the corollary of [[Center of a Bounded Set|center existence]], there is an $x\in X$ fixed by $H$. Pick $f\in G$ with $fx\in K$, then $fHf^{-1}$ fixes $fx$, so $fHf^{-1}\subseteq \{g: K\cap g\cdot K\neq 0\}$, which is finite by properness. There are only finitly many subgroups in $\{g: K\cap g\cdot K\neq 0\}$, so there are only finitely many conjugacy classes of finite subgroups. $\square$