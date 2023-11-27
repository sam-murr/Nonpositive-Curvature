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

```ad-Lemma

```
