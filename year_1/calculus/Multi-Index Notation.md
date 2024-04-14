***Multi-index notation*** is compact notation for component-wise expressions.

# Formal Definition
If $\alpha, \beta \in \mathbb{N}^n$ are $n$-tuples, then they are called a ***multi-index***. We can now define basic ***multi-index operations***:
- **Sum and difference:** $\large \alpha \pm \beta \triangleq (\alpha_{1} \pm \beta_{1},\alpha_{2} \pm \beta_{2},\dots,\alpha_{n} \pm \beta_{n})$
- **Absolute value:** $\large |\alpha| \triangleq \alpha_{1} + \alpha_{2} + \dots + \alpha_{n}$
- **Factorial:** $\large \alpha! \triangleq \alpha_{1}! \alpha_{2}! \dots \alpha_{n}!$
- **Power:** for any $\large \pmb x \in \mathbb{R}^n$, $\large \pmb x^\alpha \triangleq x_{1}^{\alpha_{1}} x_{2}^{\alpha_{2}} \dots x_{n}^{\alpha_{n}}$

## Higher-order partial derivative
You can also use ***multi-index notation*** to compactly represent [[Partial Derivative#Mixed Partial Derivatives|higher-order partial derivatives]], like so
$$\large D^{\alpha} f \triangleq \dfrac{\partial^{|\alpha|}f}{\partial x_{1}^{\alpha_{1}}\partial x_{2}^{\alpha_{2}}\dots\partial x_{n}^{\alpha_{n}}}$$
If we know that all $|\alpha|$-th order partial derivatives are [[Continuity|continuous]], then we can use [[Partial Derivative#Schwarz's Theorem|Schwarz's theorem]] to [[Partial Derivative#Schwarz's Theorem|ignore the order]] of *these* partial derivatives; $D^{\alpha}f$ becomes equal to *every possible* such partial derivative - *simultaneously*.

## Sigma-Summation
In a normal sigma-summation, we can write $\sum_{k=n}^N f(k)$ to represent the summation of $f(k)$, for every $k$ in the range $n\leq k \leq N$
$$\large \sum^N_{k=n}f(k) = f(n) + f(n+1) + \dots + f(N - 1) + f(N)$$
Similarly, we can write $\large \sum_{|\alpha|=k}f(\alpha)$ to represent the summation of $f(\alpha)$, for every $\alpha \in \mathbb{N}^n$ such that $|\alpha| = k$. This is the ***multi-index sigma-summation***. When we construct the set of such multi-indexes $\large {\mathbb{N}^n}_{|\alpha| = k} = \{ \ \alpha \in \mathbb{N}^n \ : \ |\alpha| = k \ \}$, we find it's [[Cardinality of Sets|cardinality]] to be $\large {k + n - 1 \choose n - 1}$, meaning there are exactly $\large {k + n - 1 \choose n - 1}$ such $\alpha$ for which $|\alpha| = k$. This is because we can model the problem as [distributing](https://brilliant.org/wiki/identical-objects-into-distinct-bins/) $k$ [identical objects into](https://brilliant.org/wiki/identical-objects-into-distinct-bins/) $n$ [distinct bins](https://brilliant.org/wiki/identical-objects-into-distinct-bins/).

We can also extend this notation to range over every $\alpha \in \mathbb{N}^n$ such that  $|\alpha| \leq k$, or such that $|\alpha| \geq k$, like so
$$\large
\begin{align}
\sum_{|\alpha| \leq k}f(\alpha) &= \sum_{i=0}^k \sum_{|\alpha| = i}f(\alpha)
= \sum_{|\alpha| = 0}f(\alpha) + \sum_{|\alpha| = 1}f(\alpha) +  \dots + \sum_{|\alpha| = k}f(\alpha) \\
\\
\sum_{|\alpha| \geq k}f(\alpha) &= \sum_{i=k}^{\infty} \sum_{|\alpha| = i}f(\alpha)
= \sum_{|\alpha| = k}f(\alpha) + \sum_{|\alpha| = k+1}f(\alpha) +  \dots \\
\end{align}
$$
And even treat $\large \sum_{|\alpha| \leq k}f(\alpha)$ as [[Series#Partial sums|partial sum]], and [[Convergence of Sequences#Convergence to a Limit|take the limit]] of $k$ at $\infty$ to create an infinite sum, like so
$$
\large
\begin{align}
\lim_{ k \to \infty } \large \sum_{|\alpha| \leq k}f(\alpha) &&=&&&
\lim_{ k \to \infty } \sum_{i=0}^k \sum_{|\alpha| = i}f(\alpha)
= \sum_{i=0}^{\infty} \sum_{|\alpha| = i}f(\alpha) \\
&&=&&& \sum_{|\alpha| \geq 0}f(\alpha)
= \large \sum_{|\alpha| < \infty}f(\alpha) \\
&&=&&& \large \sum_{\alpha \in \mathbb{N}^n}f(\alpha)
= \sum_{\alpha_{1}=0}^\infty \dots \sum_{\alpha_{n}=0}^\infty f(\alpha) \\
&&=&&& \sum_{|\alpha| = 0}f(\alpha) + \sum_{|\alpha| = 1}f(\alpha) +  \dots
\end{align} 
$$

