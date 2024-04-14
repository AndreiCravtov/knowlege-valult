A well known example of [[Series|series]], that is based on the [harmonic sequence](https://en.wikipedia.org/wiki/Harmonic_progression_(mathematics)). The harmonic sequence is defined as $(a_{n})_{n\geq 1} = \frac{1}{n}$, so the harmonic series is defined as $\sum^\infty_{i=1} \frac{1}{i} = 1+\frac{1}{2} + \frac{1}{3}+\dots$.

# Determining divergence
The harmonic series is given by $$S = \sum^\infty_{i=1} \frac{1}{i} = 1 + \frac{1}{2} + \frac{1}{3}+\dots$$
Even though the summands $\frac{1}{i}$ converge to $0$, the series itself still diverges. We can see this by grouping the terms like so 
$$
\begin{gathered}
S = & 1 + \frac{1}{2}  \\
& + \frac{1}{3} + \frac{1}{4} > \frac{1}{4} + \frac{1}{4} \\
& + \frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8} > \frac{1}{8} + \frac{1}{8} + \frac{1}{8} + \frac{1}{8} \\
& \vdots \\
S = & 1 + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \dots > 1 + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \dots
\end{gathered}
$$
Clearly the sequence of $1 + \frac{1}{2} + \frac{1}{2} +\frac{1}{2} +\dots$ diverges, since it's summands converge to $\frac{1}{2}$ instead of $0$, and since the harmonic series is larger than it, it itself is also divergent.