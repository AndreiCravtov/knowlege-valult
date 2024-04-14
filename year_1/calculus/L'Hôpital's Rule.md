L'Hôpital's rule is a theorem that helps evaluate limits of an indeterminate form, using derivatives.

# Formal Definition
Let there be $f,g: (a,b) \to \mathbb{R}$ such that the [[Differentiation of Real Functions|derivatives]] $f',g': (a,b) \to \mathbb{R}$ are [[Continuity|continuous]] in $(a,b)$. If for some $c \in (a,b)$, $f(c)=g(c)=0$, and $g'(c) \neq 0$, then:
$$
\lim_{ x \to c } \frac{f(x)}{g(x)} = \frac{f'(c)}{g'(c)} = \lim_{ x \to c } \frac{f'(x)}{g'(x)}
$$

## Proof
We can simply manipulate the expression as such:
$$
\begin{gathered}
& \lim_{ x \to c } \frac{f(x)}{g(x)} = \lim_{ x \to c } \frac{f(x) - f(c)}{g(x) - g(c)} = \lim_{ x \to c } \frac{\left( \frac{f(x) - f(c)}{x-c} \right)}{\left( \frac{g(x) - g(c)}{x-c} \right)} \\
= & \frac{\lim_{ x \to c } \left( \frac{f(x) - f(c)}{x-c} \right)}{ \lim_{ x \to c } \left( \frac{g(x) - g(c)}{x-c} \right)} = \frac{f'(c)}{g'(c)} = \lim_{ x \to c } \frac{f'(x)}{g'(x)} \\
\end{gathered}
$$
To arrive at L'Hôpital's rule