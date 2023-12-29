```ad-Definition
title:Definition: Fundamental domain
Consider a group $G$ acting on a simplicial complex $S$ via simplicial maps. A closed simplex $\Delta\subseteq S$ is a <u> fundamental domain</u> if every orbit intersects $S$ exactly once. Then, for each face $\sigma$ of $\Delta$ we can associate $G_\sigma$ the subgroup of $G$ which stabelizes $\sigma$. Then, for any subface $\tau\subseteq \sigma$ we have $G_\sigma\subseteq G_\tau$.

```


```ad-Definition
title:Definition: Simplex of Groups and Fundamental Group

For a simplex $\Delta$, we may assign groups $G_\sigma$ to each face and embeddings $\phi_{\tau\sigma}G_\sigma\to G_\tau$ such that $\phi_{\eta\tau}\circ \phi_{\tau\sigma} = \phi_{\eta\sigma}$. This structure is called a <u>group simplex</u>.

The <u>fundamental group</u> of this simplex of groups is given by $\pi(\Delta)={\Large{*}}_{\sigma\subseteq \Delta} G_\sigma/\langle \phi_{\tau\sigma}(g)=h|\ \tau\subseteq \sigma\subseteq\Delta,\ g\in G_\sigma,\ h\in G_\tau\rangle$

```

```ad-Definition
title:Definition: Developable Simplex of Groups

A simplex of groups is Developable iff there is a group $G$ acting on a simplicial complex whose fundamental domain has the same structure of subgroups as the grup simplex.

```

```ad-Proposition
A group simplex is developable iff the natural maps $G_\sigma\to \pi(\Delta)$ are injective.

```
__Proof__: If $\Delta$ is developable, then let $G$ and $S$ witness that. Then, $G_\sigma \inj G\inj \pi(\Delta)$.
If the natural maps are injective, then let $\tilde{K} = \Delta\times \pi(\Delta)/ \sim$ where $(x,q) \sim (x,h)$ if $x\in \sigma$ and $q = hg$ for $g\in G_\sigma$. Then, $\pi(\Delta)$ acts by right multiplication $g(x,q) = (x,qx)$ works.

```ad-Definition
title:Definition: Local Development
The local development of a simplex of groups $\Delta$ at a vertex $v$ is the simplicial complex given by $\Delta \times G_{v}/ \sim$ where $(x,g)\sim (x,h)$ if $x\in \sigma$ where $v\in\sigma$ and $g = hq$ for some $q\in \Image \phi_{v\sigma}$.

```

```ad-Theorem
title:Theorem: Bridson Haeflinger Theorem
Let $\Delta$ be a simplex of groups wher $\Delta$ came with a peicewise euclidean metric. Then, if the local developments are $\CAT(0)$. Then $\Delta$ is developable (and $\tilde K$ is $\CAT(0)$).


```
