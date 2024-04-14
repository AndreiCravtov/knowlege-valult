A ***Taylor Series*** expansion of an [[Smoothness|infinitely differentiable]] function, is the [[Series#Partial sums|infinite sum]] created from the [[Taylor's Theorem#Taylor Polynomial|Taylor polynomial]]. A tailor series is a [[Power Series|power series]] of the form $$\large T(x) = \sum^\infty_{k=0} \frac{f^{(k)}(c)}{k!} (k-c)^k$$
# Formal Definition
Let $f: \mathbb{R} \to \mathbb{R}$ be a function such that $f$ is [[Smoothness|infinitely differentiable]] at $c \in \mathbb{R}$. This means that for any $n \in \mathbb{N}$, we can apply [[Taylor's Theorem|Taylor's theorem]]
$$\large f(x) = \sum^{n}_{k=0} \frac{f^{(k)}(c)}{k!}(x-c)^k + R_{n}(x)$$
We can then take the [[Convergence of Sequences#Convergence to a Limit|limit at infinity]] on both sides of this equality, getting the following result
$$
\begin{align}
\begin{aligned}
\\ \iff \\ \\ \\
\end{aligned} \ \
\begin{aligned}
\lim_{ n \to \infty } f(x) &= \lim_{ n \to \infty } \left[ \sum^{n}_{k=0} \frac{f^{(k)}(c)}{k!}(x-c)^k + R_{n}(x) \right] \\
f(x) &= \lim_{ n \to \infty } \left[ \sum^{n}_{k=0} \frac{f^{(k)}(c)}{k!}(x-c)^k \right] + \lim_{ n \to \infty } R_{n}(x) \\
&= \sum^{\infty}_{k=0} \frac{f^{(k)}(c)}{k!}(x-c)^k + \lim_{ n \to \infty } R_{n}(x) \\
&= T(x) + R(x) 
\end{aligned} \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \
\end{align}
$$
where the $\large T(x)= \sum^{\infty}_{k=0} \frac{f^{(k)}(c)}{k!}(x-c)^k$ is called the ***Taylor Series*** expansion of $f$. Since $T(x)$ is a  [[Power Series|power series]], it only converges within the [[Power Series#Radius of Convergence|radius of convergence]]. Therefore, whenever $x$ is within the [[Power Series#Radius of Convergence|radius of convergence]] and $R(x) = 0$, we get
$$
\begin{align}
f(x) &= T(x) + R(x) = T(x) + 0 \\
&= \sum^{\infty}_{k=0} \frac{f^{(k)}(c)}{k!}(x-c)^k \\
&= f(c) + f'(c)(x-c) + \frac{f''(c)}{2!}(x-c)^2 + \dots + \frac{f^{(n)}(c)}{n!}(x-c)^n + \dots
\end{align}
$$
meaning that $f$ is *entirely* described by the [[Series#Partial sums|infinite sum]] of polynomial terms. Whenever this happens, we say that $f$ is [[Analytic Function|analytic]] at $c$. If $f$ is ***analytic*** at every $c \in \mathbb{R}$, then we say that $f$ is a [[Analytic Function|real analytic function]].

# Multivariate Taylor Series
Let $f: \mathbb{R}^n \to \mathbb{R}$ be a function such that ***all*** $n$-th order [[Partial Derivative#Mixed Partial Derivatives|partial derivatives]] of $f$ exist, and are [[Continuity|continuous]] functions, for *every* $n \in \mathbb{N}$. This allows us to apply [[Taylor's Theorem#Multivariate Taylor's Theorem|multivariate Taylor's theorem]] for *any* $n$, and *any* $\pmb c \in \mathbb{R}^n$
$$\large f(\pmb x) = {\sum_{|\alpha| \leq k} \frac{D^\alpha f(\pmb c)}{\alpha!}(\pmb x - \pmb c)^\alpha} \ + \ R_{k}(\pmb x)$$
We can then take the [[Convergence of Sequences#Convergence to a Limit|limit at infinity]] on both sides of this equality, getting the following result
$$
\begin{align}
\begin{aligned}
\\ \iff \\ \\ \\
\end{aligned} \ \
\begin{aligned}
\lim_{ k \to \infty } f(x) &= \lim_{ k \to \infty } \left[ {\sum_{|\alpha| \leq k} \frac{D^\alpha f(\pmb c)}{\alpha!}(\pmb x - \pmb c)^\alpha} \ + \ R_{k}(\pmb x) \right] \\
f(x) &= \lim_{ k \to \infty } \left[ {\sum_{|\alpha| \leq k} \frac{D^\alpha f(\pmb c)}{\alpha!}(\pmb x - \pmb c)^\alpha} \right] + \lim_{ k \to \infty } R_{k}(\pmb x) \\
&= {\sum_{|\alpha| < \infty} \frac{D^\alpha f(\pmb c)}{\alpha!}(\pmb x - \pmb c)^\alpha} + \lim_{ k \to \infty } R_{k}(\pmb x) \\
&= T(\pmb x) + R(\pmb x) 
\end{aligned} \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \
\end{align}
$$
where the $\large T(\pmb x)= {\sum_{|\alpha| < \infty} \frac{D^\alpha f(\pmb c)}{\alpha!}(\pmb x - \pmb c)^\alpha}$ is called the ***Taylor Series*** expansion of $f$. Therefore whenever $T(\pmb x)$ exists, and $R(\pmb x) = 0$, we conclude that $f(\pmb x) = T(\pmb x)$, like so
$$
\large
\begin{align}
f(\pmb x) &= T(\pmb x) + R(\pmb x) = T(\pmb x) + 0 \\
&= {\sum_{|\alpha| < \infty} \frac{D^\alpha f(\pmb c)}{\alpha!}(\pmb x - \pmb c)^\alpha}
= {\sum_{\alpha \in \mathbb{N}^n} \frac{D^\alpha f(\pmb c)}{\alpha!}(\pmb x - \pmb c)^\alpha} \\
&= {\sum_{\alpha_{1}=0}^\infty \dots \sum_{\alpha_{n}=0}^\infty { \frac{(x_{1} - c_{1})^{\alpha_{1}} \dots (x_{n} - c_{n})^{\alpha_{n}}}{\alpha_{1}!  \dots \alpha_{n}!} \cdot \dfrac{\partial^{\alpha_{1} + \dots + \alpha_{n}}f}{\partial x_{1}^{\alpha_{1}}\dots\partial x_{n}^{\alpha_{n}}}(c_{1}, \dots, c_{n}) }} \\
\end{align}
$$
Whenever this happens, we say that $f$ is [[Analytic Function|analytic]] at $\pmb c$. If $f$ is ***analytic*** at every $\pmb c \in \mathbb{R}$, then we say that $f$ is an [[Analytic Function|analytic function of several real variables]].
