A well known and common example of [[Series|series]], that is based on the [geometric sequence](https://en.wikipedia.org/wiki/Geometric_progression). The geometric sequence is defined as $(a_{n})_{n \geq 0} = ar^{n}$ (where $a,r$ are constants), so the geometric series is defined as $\sum^\infty_{i=0}ar^{i} = a+ar+ar^2+ar^3+\dots$.

# Determining convergence
We can begin by defining the [[Series#Partial sums|partial sum]] of the series: $$G_{n} = \sum_{i=0}^{n-1} ar^{i} =\sum_{i=0}^{n} ar^{i-1}$$
Then we can reason like so: 
$$
\begin{gathered}
G_{n} = a + ar + ar^2 + \dots + ar^{n-2} + ar^{n-1} \\
rG_{n} = ar + ar^2 + ar^3 + \dots + ar^{n-1} + ar^{n} \\
G_{n}-rG_{n} = G_{n}(1-r) = a - ar^n = a(1-r^n) \\
\vdots \\
G_{n} = \frac{a(1-r^n)}{1-r}
\end{gathered}
$$
And now that we have obtained the partial sum, we can take it's limit to determine the convergence of geometric series.
$$
\begin{gathered}
\lim_{ n \to \infty } G_{n} = \lim_{ n \to \infty }  \frac{a(1-r^n)}{1-r}= \frac{a(1 -\lim_{ n \to \infty } (r^n))}{1-r} \\ \\
\text{We can see that:} \ G_{n} \ \text{converges} \iff \lim_{ n \to \infty }  r^n \ \text{converges} \\
\text{Which only happens if} \ |r|<1 \\ \\
|r| < 1 \iff \lim_{ n \to \infty } G_{n} = \frac{a}{1-r}
\end{gathered}
$$
Therefore for $|r|<1$ the geometric series converges to $\sum^\infty_{i=1}ar^{i-1} = \frac{a}{1-r}$, and for $|r|\geq 1$ it diverges.

## Other forms
For the geometric series of the form $\sum^\infty_{i=1} x^i$, it converges to $\frac{x}{1-x}$ if and only if $|x|<1$, and diverges if and only if $|x|\geq 1$.