The mean value theorem, or Lagrange theorem, is basically the idea that the line running between two endpoints of a differentiable function is parallel to the tangent of at least one point between those two endpoints
![[Pasted image 20231211135449.png|450]]

# Formal Definition
Let $f:[a,b] \to \mathbb{R}$ be [[Continuity|continuous]] in $[a,b]$, and [[Differentiation of Real Functions#Differentiable Functions|differentiable]] in $(a,b)$, such that $a<b$. Then the mean value theorem is stated as $$\exists c \in (a,b) \left[  \ \ f'(c) = \frac{f(b)-f(a)}{b-a} \ \  \right]$$
Or that, there exists some point $c \in (a,b)$ such that the gradient at that point is equal to the gradient of the line running through $(a,\ f(a))$ and $(b,\ f(b))$.

## Rolle's Theorem
Rolle's theorem is a special case of the mean value theorem, where an additional assumption is made. Namely, $f(a)=f(b)$, so $\frac{f(b)-f(a)}{b-a} = 0$. Therefore, the conclusion is that: $$\exists c \in (a,b) \left[  \ \ f'(c) = 0 \ \  \right]$$
Or that if the two points at $a$ and $b$ have then same value, then some stationary point must exist between $a$ and $b$.
![[Pasted image 20231211143424.png|500]]

The proof roughly follows these steps:
1. $f$ continuous in $[a,b]$ $\implies$ $f$ has maximum/minimum in $[a,b]$
2. $f$ has maximum/minimum in $[a,b]$ $\implies$ $f$ has maximum and minimum at $a$ and $b$ **OR** $f$ has maximum/minimum in $(a,b)$
3. $f$ has maximum and minimum at $a$ and $b$ $\implies$ $f$ is a horizontal line, so $f'(x)=0$ for any $x \in[a,b]$
4. For any $c \in (a,b)$: $f(c)$ is a maximum or minimum $\implies$ $f'(c)=0$
5. $f$ has maximum or minimum in $(a,b)$ $\implies$ For some $c \in (a,b)$, $f'(c)=0$

## Proof of Mean Value Theorem
We can use [[#Rolle's Theorem|Rolle's theorem]] by defining a second function: $$g(x)=f(x)-rx$$Where $r$ is some constant. Since $f$ is [[Continuity|continuous]] in $[a,b]$, and [[Differentiation of Real Functions#Differentiable Functions|differentiable]] in $(a,b)$, so is $g$. Choose $r = \frac{f(b)-f(a)}{b-a}$, thus: 
$$
\begin{gathered}
r = \frac{f(b)-f(a)}{b-a} & \iff & \\
r(b-a) = f(b)-f(a) & \iff & \\
f(a)-ra = f(b)-rb & \iff & g(a) = g(b) \\
\end{gathered}
$$
Thus we can apply [[#Rolle's Theorem|Rolle's theorem]] and deduce that for some $c \in (a,b)$, we have $g'(c)=0$. We know that $g'(x) = f'(x) - r$, hence we reason as such:
$$
\begin{gathered}
g'(c)=0 & \iff & \\
f'(c) - r=0 & \iff & \\
f'(c) - \frac{f(b)-f(a)}{b-a} = 0 & \iff & f'(c) = \frac{f(b)-f(a)}{b-a} \\
\end{gathered}
$$
Which concludes the proof for the - more general - median value theorem, using the - less general - Rolle's theorem.