# Formal Definition
Let $U \subseteq \mathbb{R}^n$ be an [[Open Set|open set]] and $f: U \to \mathbb{R}$ be a function. Fix some point $\pmb {a} = (a_{1},\dots,a_{n}) \in U$. If $f$ is [[Partial Derivative|partially differentiable]] at $\pmb a$ with respect to every component, then we can define the ***gradient*** of $f$ at $\pmb a$ as:
$$\nabla f(\pmb a) = \left( \dfrac{\partial f}{\partial x_{1}}(\pmb a), \dots, \dfrac{\partial f}{\partial x_{n}}(\pmb a) \right)$$
The function that maps every point $\pmb a$ to the ***gradient*** of $\nabla f(\pmb a)$, is called the ***gradient*** of $f$; denoted as $\nabla f$. The ***gradient*** is the generalisation of *slope*, or *steepness*, to $n$-dimensions. Therefore, it gives you the direction of the greatest growth of the function $f$.

## Intuition
With $n=1$, the ***gradient*** can be visualised as a tangent line:
![[Pasted image 20231129171651.png|350]]
With $n=2$, the ***gradient*** can be visualised as a tangent plane:
![[Pasted image 20240311042158.png]]
With $n\geq 3$, visualising the ***gradient*** is hard, the concept remains the same.

## Critical Point
Just like with [[Differentiation of Real Functions#Critical Points of Real Functions|regular differentiation]], we can have ***critical points***. We call $\pmb a$ a ***critical point*** if $\nabla f(\pmb a)=\pmb 0$ or *undefined*.
For instance with function $f(x,y)=x^2 + y^2$, we have $\nabla f(0, 0) = (0,0)$, hence $(0,0)$ is a critical point.
![[Pasted image 20240317000209.png|400]]
