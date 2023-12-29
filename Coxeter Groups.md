```ad-Definition
title:Definition: Coxeter and Cosine Matrix, the Coxeter Group
A Coxeter matrix $M = [m_{ij}]$ is an $n\times n$ symmetric integer matrix with $1$s in the diagonal and all other enteries $\geq 2$. We also allow enteries with value $\infty$.

The associated cosine matrix $C$ is given by $C = [c_{ij}]$, where $c_{ij} = -\cos{\frac{\pi}{m_{ij}}}$ ($-1$ if $m_{ij}$ is $\infty$)

The Coxeter group $W$ associated with $M$ is the group with $n$ generators $s_{1},\dots,s_n$ and relators $(s_is_j)^{m_{ij}} = 1$.
```
```ad-Definition
title: Definition: Tits Representation
Note that $C$ gives a bilinear form $\pr\cdot\cdot$ on $\R^n$. For each unit vector $e_i$, let $\rho_i$ be the isometry given by reflecting around $e_i$ ($v\mapsto v-2(v,e_i)e_i$). The representation of $W$ given by $s_i\to\rho_i$ is the <u>Tits Representation</u>
```
```ad-Proposition
This is a valid representation
```
__Proof__: It suffices to show $\rho_i\rho_j$ has order $m_{ij}$. Let $V = \span(e_i,e_j)$, then $C$ restricted to $V$ is:
$$
C' = \begin{bmatrix}
1&-\cos{\frac{\pi}{m_{ij}}}\\
-\cos{\frac{\pi}{m_{ij}}}&1
\end{bmatrix}
$$

If $m_{ij} =\infty$, then its:
$$
\begin{bmatrix}
1&-1\\
-1&1
\end{bmatrix}
$$
Letting $x = e_i+e_j$, then $x\in V^\perp$ invariant under $\rho_i$ and $\rho_j$. Then, $\rho_i\rho_j(e_i) = \rho_i(e_i+2e_j) = x + \rho_i(e_j) = 2x+e_i$. This means $(\rho_i\rho_j)^m(e_i)\neq e_i$ for all $m$, so $\rho_i\rho_j$ has infinite order.

If $m_{ij} \neq \infty$ then $C'$ is positive definite, so after a coordinate change $(V,\pr \cdot\cdot) = (\R^2,\inner\cdot\cdot)$. Then, $e_i$ and $e_j$ get sent to vectors with angle $\arccos(\pr {e_j} {e_i}) = \arccos(-\cos(\frac\pi{m_{{ij}}}))= \pi-\frac\pi{m_{{ij}}}$, so the lines $l_i = \span(e_i)^\perp$ and $l_j = \span(e_j)^\perp$ have angle $\frac\pi{m_{{ij}}}$ between them. $\rho_i\rho_j$ then becomes reflecting across $l_j$ then across $l_i$, resulting in a rotation  of angle $\frac{2\pi}{m_{{ij}}}$, which has order $m_{ij}$. Then since $\pr \cdot\cdot$ nondegenerate on $V$, we have  $\R^n = V\oplus V^\perp$ and $\rho_i$, $\rho_j$ acts trivially on $V^\perp$, so this shows  $\rho_i\rho_j$ has order $m_{ij}$. $\square$

```ad-Definition
title:Definition: Coxeter Complex and Cayley Graph
Start with a $n-1$ dimensional simplex $\Delta$ with $n$ vertices. Associate to each $n-2$ dimensional face $f_i$ a generator $s_i$. Label lower dimensional faces with the labels of the $n-2$ dimensional faces which contain them.

Consider the simplicial complex given by $X= \Delta\times W/\sim$, where $(x,p)\sim(x,q)$ if $x$ is in $n-2$ dim face labeled with $f_i$ and $q = p s_i$.

The Cayley graph is the duel graph of this complex: the vertices are $n-1$ simplices, and you attach an edge if they share a $n-2$ face.
```
![[Coxeter 1.png]]
Above is the coxeter complex for coxeter group with matrix:
$$
\begin{bmatrix}
1&2&3\\
2&1&4\\
3&4&1
\end{bmatrix}
$$
Below is the complex along with the Cayley graph:
![[Coxeter 2.png]]
```ad-Remark
Note that if $m_{ij}=\infty$, then things get kinda weird (the face at the intersection of $f_i$ and $f_j$ is adjacent to $\infty$ many cells)

```

```ad-Definition
title: Definition: Davis Complex
Let $W$ be a infinite order coxeter group, and let the <u>Davis Complex</u> $\Sigma$ be the subcomplex of the barycentric subdivision of the coxeter complex $X$ spanned by vertices which are in faces labeled by $T$ where $W_T$ is finite.

If $W$ is finite, then let $\Sigma$ be the $0$ cone over $X$.

We can equip each of 
```

```ad-Proposition
This is $\CAT(0)$.
```
