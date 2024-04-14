Taylor's theorem is one that defines a differentiable function a summation of polynomial terms. The last term is often impossible to compute, so it heuristics are used to approximate it. This is why Taylor's theorem is used as a way to approximate functions.
![[Pasted image 20231213143955.png|500]]

# Formal Definition
Let $f: \mathbb{R} \to \mathbb{R}$ be a function such that $f$ is $n$-times [[Differentiation of Real Functions#Higher Order Derivatives|differentiable]] at $c \in \mathbb{R}$. Then, then there exists a function $h_{n}: \mathbb{R} \to \mathbb{R}$ such that
$$
\large
\begin{align}
\lim_{ x \to a } h_{n}(x) &= 0, \ \text{and}  \\
f(x) &=  f(c) + f'(c)(x-c) + \frac{f''(c)}{2!}(x-c)^2 + \dots + \frac{f^{(n)}(c)}{n!}(x-c)^n + h_{n}(x)(x-c)^n \\
&= \sum_{k=0}^n \frac{f^{(k)}(c)}{k!}(x-c)^k + h_{n}(x)(x-c)^n \\
&= T_{n}(x) + R_{n}(x)
\end{align}
$$
where $\large T_{n}(x) = \sum_{k=0}^n \frac{f^{(k)}(c)}{k!}(x-c)^k$ is called the ***Taylor polynomial***. The function $R_{n}$ is called the ***remainder*** or ***error term***. The specific formula of $\large R_{n}(x) = h_{n}(x)(x-c)^n$ is called the ***Peano form*** of the remainder.

## Lagrange Form of the Remainder
If $[a,b]$ is a *closed interval* on which $f^{(n)}$ is [[Continuity|continuous]], and $f$ is $n + 1$-times [[Differentiation of Real Functions#Higher Order Derivatives|differentiable]] on $(a,b) = I$, and $c \in I$, then
$$\large
R_{n}(x) = \frac{f^{(n+1)}(\xi )}{(n+1)!}(x-c)^{n+1}
$$
for some $\xi$ between $x$ and $c$. This explicit formula for $R_{n}$ is called the ***Lagrange form*** of the remainder. Therefore we can write
$$\large
\begin{align}
\lim_{ x \to a } h_{n}(x) &= 0, \ \text{and}  \\
f(x) &=  f(c) + f'(c)(x-c) + \frac{f''(c)}{2!}(x-c)^2 + \dots + \frac{f^{(n)}(c)}{n!}(x-c)^n + \frac{f^{(n+1)}(\xi )}{(n+1)!}(x-c)^{n+1} \\
&= \sum_{k=0}^n \frac{f^{(k)}(c)}{k!}(x-c)^k + \frac{f^{(n+1)}(\xi )}{(n+1)!}(x-c)^{n+1}
\end{align}
$$
In practice, the number $\xi$ is not calculated, but rather estimated using techniques from mathematical optimisation or real analysis.

# Multivariate Taylor's Theorem
Let $f: \mathbb{R}^n \to \mathbb{R}$ be a function such that ***all*** $k+1$-th order [[Partial Derivative#Mixed Partial Derivatives|partial derivatives]] of $f$ exist, and are [[Continuity|continuous]] functions; we can use [[Multi-Index Notation|multi-index notation]] because we can [[Partial Derivative#Schwarz's Theorem|interchange the order]] of *these* partial derivatives. For all $\pmb c \in \mathbb{R}^n$ we have
$$
\large
\begin{align}
f(\pmb x) &= {\sum_{|\alpha| \leq k} \frac{D^\alpha f(\pmb c)}{\alpha!}(\pmb x - \pmb c)^\alpha} \ + \ {\sum_{|\alpha| = k+1} \frac{D^\alpha f(\pmb \xi)}{\alpha!}(\pmb x - \pmb c)^\alpha} \\
&= T_{k}(\pmb x) + R_{k}(\pmb x)
\end{align}
$$
for some $\pmb \xi$ on the line segment between $\pmb x$ and $\pmb c$. The function $\large T_{k}(\pmb x) = {\sum_{|\alpha| \leq k} \frac{D^\alpha f(\pmb c)}{\alpha!}(\pmb x - \pmb c)^\alpha}$ is called the ***Taylor polynomial***, and $\large R_{k}(\pmb x) = {\sum_{|\alpha| = k+1} \frac{D^\alpha f(\pmb \xi)}{\alpha!}(\pmb x - \pmb c)^\alpha}$ is called the ***remainder*** or ***error term***. This explicit formula for $R_{k}$ is the multivariate extension of the ***Lagrange form***.

## Two-variable second-order expansion
The second order ***Taylor polynomial*** of analytic function $f: \mathbb{R}^2 \to \mathbb{R}$, about the point $(x_{0},y_{0}) \in \mathbb{R}^2$, is
$$
\large
\begin{align}
f(x,y)
&&= \ & T_{2}(x,y) = {\sum_{k_{x} + y_{x} \leq 2} \frac{(x - x_{0})^{k_{x}}(y - y_{0})^{k_{y}}}{k_{x}!k_{y}!} \cdot \dfrac{\partial^{k_{x} + k_{y}}f}{\partial x^{k_{x}} \partial y_{k_{y}}}(x_{0},y_{0})}
\\
&&= \ & f(x_{0},y_{0}) + (x - x_{0}) \dfrac{\partial f}{\partial x}(x_{0},y_{0}) + (y - y_{0}) \dfrac{\partial f}{\partial y}(x_{0},y_{0} ) \\
&&&+ \frac{1}{2} \left[
(x - x_{0})^2 \dfrac{\partial^2 f}{\partial x^2}(x_{0},y_{0})
+ 2(x - x_{0})(y - y_{0}) \dfrac{\partial^2 f}{\partial x \partial y}(x_{0},y_{0})
+ (y - y_{0})^2 \dfrac{\partial^2 f}{\partial y^2}(x_{0},y_{0})
\right]
\end{align}
$$


