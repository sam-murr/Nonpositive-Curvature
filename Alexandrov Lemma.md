![[Classes/Metric Spaces with Nonpositive Curvature/Figures/Alexandrov Lemma.png]]
In the above picture, imagine the four green lines are bars and the vertices are hinges connecting them. If we were to push the $z$ vertex away from $x$ (in the case of the picture, along the geodesic ray from $x$ containing $z$) until the $yz$ and $zy'$ bars formed a straight line, then the angle of the hinges at $x$, $y$, and $y'$ would increase.

We can formalize this as follows:

```ad-Lemma
title: Lemma: Alexandrov Lemma
Let $x,y,y',z \in M_\kappa^2$ with $d(x,y) + d(y,z) + d(z,y') + d(y',z) < 2\diam(M_\kappa^2)$. Suppose that $y$ and $y'$ lie on opposite sides of the line $xy$. Let $\Delta$ be the triangle $xyz$ and $\Delta' = xy'z$. Let $\alpha, \beta, \gamma$ and $\alpha', \beta', \gamma'$ be the angles of $\Delta$ and $\Delta'$ resp. If $\gamma+\gamma' \geq \pi$ then we have:
- $d(x,y)$, $d(x,y')$, and $d(y,z) + d(z,y')$ satisfies the triangle inequality.
- Let $\bar{\Delta} = \bar{x}\bar{y}\bar{y}'$ be the $\kappa$ comparison triangle associated with these lengths. Let $\bar{\alpha}, \bar{\beta}, \bar{\beta}'$ be the angles of $\bar{\Delta}$ and $\bar{z}$ be the point on $\bar{y}\bar{y}'$ with $d(\bar{y},\bar{z}) = d(y,z)$. Then, $\bar{\alpha} \leq \alpha +\alpha'$, $\bar{\beta}'\geq \beta'$, $\bar{\beta}\geq \beta$, and $d(\bar{x},\bar{z})\geq d(x,z)$. Moreover, if any of these inequalities are strict, then they all are.

```
__Proof__: Let $\tilde{y}'$ (this y' tilde, not y' bar) be the unique point with distance $d(z,y')$ from $z$ with $z$ on the geodesic $y\tilde{y}'$:
![[Classes/Metric Spaces with Nonpositive Curvature/Figures/Alexandrov Lemma 2.png]]
Let $\tilde{\gamma}'$ be the angle between $xz$ and $z\tilde{y}'$. Note that $\gamma+\tilde{\gamma}' = \pi$, so since $\gamma+\gamma'\geq \pi$ we have that $\gamma'\geq\tilde{\gamma}'$  This means by the law of cosines applied at vertex $z$ we have that $d(x,\tilde{y}')\leq d(x,y')$, so:
$$d(x,y')+d(x,y)\geq d(x,\tilde{y}')+d(x,y) \geq d(y,\tilde{y}') = d(y,z) + d(z,y')$$
This proves the first part. Take $\bar{\Delta}$ to be the comparison triangle in the statement of the second part (this time in the figure we fix $\bar{x} = x$ and $\bar{y} =y$):
![[Alexandrov Lemma 3.png]]
We know $d(x,\bar{y}') = d(x,y') \geq d(x,\tilde{y}')$, so by law of cosines $\bar{\beta}\geq \beta$. Also, by the triangle inequality, $d(y,y')\leq d(z,y)+d(z,y') = d(y\bar{y}')$, so by law of cosines applied at $x$ again we have $\bar{\alpha} \geq \alpha+\alpha'$. Since $\bar{\beta}\geq\beta$, by the law of cosines applied at $y$ we then have $d(x,z)\leq d(x,\bar{z})$.


Moreover, we have $\gamma+\gamma' = \pi$ iff $d(x,y') = d(x,\tilde{y}')$ iff  $d(y,y')= d(z,y)+d(z,y')$ iff  $d(x,z)\leq d(x,\bar{z})$, so  if any of the previous inequalities are equalities, then they all are. If we were to do this construction with the roles of $y$ and $y'$ reversed, we'd get $\beta'\leq \bar{\beta}'$ again with equality iff all other inequalities are equalities. $\square$

