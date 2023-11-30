```ad-Definition
title:Definition: The Klein Model of the Hyperbolic Plane
Consider the projection of $\HP^2\subseteq\R^{3}$ to the unit disc $\D^2$ where $x\in\HP^2$ gets mapped to the unique $y\in\D^2$ in the interior of the disc such that $(y_1,y_2, 1)$ is on the line from $0$ to $x$.

The <u>cross ratio</u> of four colinear points $x,y,w,z\in\D^n$ is:
$$
(x,y\ ;\ w,z) = \frac{\overline{wy}\ \overline{xz}}{\overline{wx}\ \overline{yz}}
$$

For points $x,y\in\D^2$ in the interior, let $l$ be the line connecting them and let $x_\infty$, $y_\infty$ on $l\cap\partial \D^2$ such that going along $l$ in the $x$ to $y$ direction the order of points you encounter is $x_\infty$, $x$, $y$, $y_\infty$. Then, define the distance $d$ from $x$ to $y$ as:
$$
d(x,y) = \frac{1}{2}\log(x,y\ ;\ x_\infty,y_\infty)
$$

```
![[Klein Model.png]]
![[Klein Model 2.png]]
```ad-Proposition
The projection $\phi:\HP^2\to\D^2$ with the above metric is a isometry from $d_{-1}$ to $d$
```
__Proof__: Take $x,y\in \HP$ We will reduce this to the case when $x = (0,0,1)$ and $y = (\sinh(r),0,\cosh(r))$, which is the point at distance $r$ on the hyperbolic arc starting at $x$ in the $e_1$ direction. Then, $\phi(x) = (0,0)$, $\phi(y) = (\frac{\sinh(r)}{\cosh(r)},0)$. In the above figure, we find a simplified equation for the distance assuming $x = (0,0)$. We then have:
$$
\begin{align}
d(\phi(y),\phi(x)) &= \frac{1}{2}\ln(\frac{1 + \frac{\sinh(r)}{\cosh(r)}}{1 - \frac{\sinh(r)}{\cosh(r)}})\\
&= \frac{1}{2}\ln(\frac{e^r}{e^{-r}})\\
&= r\\
\end{align}
$$
It suffices now to prove that hyperbolic reflections fix the cross ratio, since we can map any pair of points on the hyperbolic plane to  $(0,0,1)$ and $(\sinh(r),0,\cosh(r))$ for some $r$ via reflections.

```ad-Lemma
Let $x_\infty,x,y,y_\infty$ be colinear points, and $z$ be some point not on that line, then the cross ratio $(x,y;\ x_\infty,y_\infty)$ is determined by the angles between the lines from $z$ to $x_\infty,x,y,y_\infty$. Specifically, if $\alpha$, $\beta$, $\gamma$ defined as in the figure, then we have:
$$
\frac{\sin(\alpha+\beta)\sin(\beta+\gamma)}{\sin(\alpha)\sin(\gamma)}
$$

```

^ee4e56

![[Cross Ratio.png]]
__Proof__:
Adding extra labels to the diagram, we have:

![[Cross Ratio 2.png| center |500]]

By the sine law we have:
$$
\begin{align}
||x-x_\infty|| &= a\frac{\sin(\alpha)}{\sin(\eta)} & ||y-x_\infty|| &= a\frac{\sin(\alpha+\beta)}{\sin(\eta)} & ||y-y_\infty|| &= b\frac{\sin(\gamma)}{\sin(\delta)} & ||x-y_\infty|| &= b\frac{\sin(\beta+\gamma)}{\sin(\delta)}
\end{align}
$$
$$
\begin{align}
(x,y;\ x_\infty, y_\infty) = &\frac{ ||y-x_\infty||||x-y_\infty||}{||x-x_\infty||||y-y_\infty||}\\
= &\frac{\sin(\eta)}{a\sin(\alpha)}\frac{a\sin(\alpha+\beta)}{\sin(\eta)}\frac{b\sin(\beta+\gamma)}{\sin(\delta)}\frac{\sin(\delta)}{b\sin(\gamma)}\\
=&\frac{\sin(\alpha+\beta)\sin(\beta+\gamma)}{\sin(\alpha)\sin(\gamma)}
\end{align}
$$
$\square$ (Lemma)
```ad-Lemma
The image of hyperplanes in the hyperbolic plane $\HP^2$ under $\phi$ are lines in klein model $\D^2$ and vice versa.
```
__Proof__: By [[Geometry of Hyperbolic Space#^bd160e|this proposition]] we know that hyperplanes in $\HP^2$ are exactly the intersection of a linear subspace $S$ of $\R^3$ and $\HP$. Then that for any point $x\in S\cap\HP$, $\phi(x) = \frac{1}{x_2}x \in \D^2\cap S$, so the image of $S\cap\HP$ under $\phi$ is the line $\D^2\cap S$. Similarly, a line $L$ in $\D^2$ is the intersection of $\D^2$ with he subspace $\span(L,0)$. $\square$ (Lemma)

We can then think of the Klein model $\D^2$ as sitting in the plane $z = 1$, and hyperplanes of $\HP^2$ correspond to lines in $\R^2$ intersecting $\D^2$.

```ad-Definition
The pole of a line $S$ in $\D^2$ is the point $p$ at the intersection of the two tangent lines where $S$ meets the boundary of $\D^2$. If $S$ is a diameter of $\D^2$, then say the pole is the point at infinity.
```
![[Pole of Hyperplane.png]]
```ad-Lemma
Let $H,S$ be linear subspaces of $\R^3$ that correspond to hyperplanes in $\HP^2$. When $p$, the pole of $S$, is finite, hyperplanes are orthogonal (ie the normal vectors are orthogonal wrt the [[Geometry of Hyperbolic Space|minkowski bilinear form]]) iff $H$ passes through the pole of $S$. If $p$ is infinite, $H$ is orthogonal iff it is parallel (in the euclidean sense) to the tangent lines from the boundary of $S\cap\D^2$.

```
__Proof__:
Let $u$ and $v$ be unit vectors such that $u^\perp = H$ and $v^\perp = S$. Note that since $u^\perp$ and $v^\perp$ intersect $\HP^2$, $\pr u u,\pr v v > 0$. Let $q$ and $t$ be where $S$ intersects $\D^2$.

The line tangent to $\D^2$ at $q$ is the intersection of the plane $z=1$ with the linear subspace $Q$ which intersects the [[Geometry of Hyperbolic Space|light cone]] at $q$, but never enters the interior of the light cone (ie always has $\pr x x\geq 0$ for all $x\in Q$). Specifically, $Q = \span(q,v)$, since $q\in Q$, and for all $aq+bv\in Q$, $\pr {aq+bv}{aq+bv} = a^2\pr q q + 2ab\pr q v + b^2 \pr v v = b^2\pr v v\geq 0$, since $q\in v^\perp$ and also is in the light cone. Similarly define $T = \span(t,v)$. Then, $T\cap Q = \span(v)$, since  $\span(v)\subseteq T\cap Q$ and $T$ and $Q$ are not equal (since $t$ and $q$ are independent, and if $t = aq+bv$, $0=\pr tv = a\pr qv + b\pr vv$ implies $b = 0$). 

Then if $\span(v)$ intersects $z=1$, that intersection is $p$, and otherwise $p$ is infinity. $H$  is perpendicular to $S$ iff $\span(v)\subseteq H$. If $p$ is not infinity, this is equivalent to $H$ intersecting $p$.

If $p$ is infinity, then the $z$ coordinate of $v$ is $0$. Then the tangent lines at $t$ and $q$ can be parameterized as $t+rv$ and  $q+rv$ for $r\in \R$. $H$ is then parallel to these lines if the intersection $H$ and $z = 1$ can be similarly parameterized $h_0 + rv$ for some $h_0 \in H\cap\{(x,y,z):z = 1\}$ , in which case $v\in H$.
$\square$ (Lemma)


We'll continue the proof of the proposition following Antoines proof:
![[Antoines Proof.png]]
Suppose you have a reflection over a hyperplane whose pole is not $\infty$. We know that [[Hyperplanes and Reflections#^5458a9|reflections]] send hyperplanes to hyperplanes, and they fix the light cone and orthogonal hyperplanes. Therefore, taking a reflection of colinear points $x$,$y$, $x_\infty$, $y_\infty$ with the latter two on the boundary of $\D^2$ will result in colinear points $x'$,$y'$, $x'_\infty$, $y'_\infty$ again with the latter two on the boundary of $\D^2$. Moreover, the reflected point will be on the same line from $p$ to the original point, since these lines are the orthogonal hyperplanes. Using the [[The Klein Model of the Hyperbolic Plane#^ee4e56|first lemma]] we proved, this means that the cross ratio of the reflected points is the same as the original points.

![[Antoines Proof 2.png]]
If you have a reflection over a hyperplane whose pole is $\infty$, then the normal vector of that hyperplane has $0$ z component, so the reflection across the hyperplane using the minkowski bilinear form is the same as the normal euclidean inner product, so the distances and the cross ratio is preserved. $\square$
