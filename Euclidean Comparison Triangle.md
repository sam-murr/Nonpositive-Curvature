```ad-Definition
title:Definition: Euclidean Comparison Triangle
Let $x,y,z$ be points in metric space $M$, take $b = d(x,y)$, $c = d(x,z)$, $a = d(z,y)$. Then $\Delta_0(x,y,z)$ the comparison triangle associated with $x,y,z$ is the triangle in $\R^2$ with $x' = (0,0)$, $y' = (0,b)$, and $z'$ such that $d(x',z') = c$, $d(y',z') = a$, and $z_1 \geq 0$. 

The comparison angle at $x$ is $\angle_x(x,y,z)$ is the angle $\angle y'x'z'$, ie the interior angle of $\Delta_0(x,y,z)$ at $x$.
```

```ad-Proposition
There is a unique comparison triangle for any $x,y,z \in M$.
```
__Proof__: Let $z' = c(\cos\theta,\sin\theta)$ for $\theta\in[0,\pi]$. Then there is a unique $\theta\in[0,\pi]$ such that $d(z',y') = a$, namely:
$$
\begin{align}
\arccos(\frac{b^2 + c^2-a^2}{2cb}) &=\theta
\end{align}
$$
Plugging this into the law of cosines gives $d(z',y') = a$. Also from the law of cosines we have it is unique. Note that $\theta$ is defined, since by the triangle inequality in $M$, we have (wlog taking $c \geq b$):
$$
\begin{align}
c-b\leq\ &a\ \leq c+b\\
(c-b)^2\leq\ &a^2\ \leq (c+b)^2\\
-2cb\leq\ &b^2 + c^2 - a^2\ \leq 2cb\\
-1\leq\ &\frac{b^2 + c^2 - a^2}{2cb} \leq 1\\
\end{align}
$$
$\square$