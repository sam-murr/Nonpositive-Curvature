```ad-Definition
title:Definiton: Convex Space and Locally Convex Space
In the following definition, we will linearly reparametrize geodesics to have domain $[0,1]$.

A metric space $(X,d)$ is convex if it is [[Geodesic|geodesic]] and for all geodesics $c_1,c_2:[0,1]\to X$ and $t\in[0,1]$:
$$
d(c_1(t),c_2(t))\leq (1-t)d(c_1(0),c_2(0))+td(c_1(1),c_2(1))
$$
Specifically, the function $t\mapsto d(c_1(t),c_2(t))$ is [[Convex Function|convex]].

$(X,d)$ is locally convex if for each $x$ there is an open ball around $x$ which is convex.
```
![[Convex Space.png]]
```ad-Example
The above figure shows $\R^n$ is convex, which implies $\CAT(0)$ spaces are convex.
```
