The inverse square [[Series|series]] is the summation of reciprocal squares, so it is defined as $\sum^\infty_{i=1} \frac{1}{i^2} = 1 +\frac{1}{4} + \frac{1}{9}+\dots$.

# Determining convergence
We begin by studying a different series. This series is $$T= \sum^\infty_{i=1} \frac{1}{i(i+1)}$$
Using partial fractions, we have
$$
\frac{1}{i(i+1)} = \frac{1}{i}-\frac{1}{i+1}
$$
therefore we can define the partial sum $T_{n}$ as
$$
\begin{gathered}
T_{n} = & \sum^n_{i=1} \left( \frac{1}{i}-\frac{1}{i+1} \right) \\
= & 1 - \frac{1}{2} \\
& +\frac{1}{2} -\frac{1}{3} \\
& \vdots \\
& + \frac{1}{n} - \frac{1}{n+1} \\
= & 1 - \frac{1}{n+1}
\end{gathered}
$$
From this, we can see that $\lim_{ n \to \infty } T_{n} = 1$, therefore $T \ \text{converges to 1}$. 
Then we notice that $$\frac{1}{i(i+1)}< \frac{1}{i^2} < \frac{1}{i(i-1)} \ \ \ \ \text{(for} \ i \geq 2 \text{)}$$
So expand them into the series
$$\frac{1}{2 \cdot 3} + \frac{1}{3 \cdot 4} + \frac{1}{4 \cdot 5} + \dots + \frac{1}{n(n+1)} < \sum^n_{i=2} \frac{1}{i^2} < \frac{1}{1 \cdot 2} + \frac{1}{2 \cdot 3} + \frac{1}{3 \cdot 4} + \dots + \frac{1}{n(n-1)}$$
Which can be rewritten as
$$
\begin{gathered}
\left( \sum^n_{i=1} \frac{1}{i(i+1)} \right) -\frac{1}{2}< \sum^n_{i=2} \frac{1}{i^2} < \sum^{n-1}_{i=1} \frac{1}{i(i+1)} \\ \\
\text{Now we add} \ 1 \ \text{on all sides} \\ \\
\frac{1}{2} + \sum^n_{i=1} \frac{1}{i(i+1)} < \sum^n_{i=1} \frac{1}{i^2} < 1 + \sum^{n-1}_{i=1} \frac{1}{i(i+1)} \\ \\
\text{And we use the result for} \ T_{n} \ \text{to get} \\ \\
\frac{3}{2}-\frac{1}{n+1} < \sum^n_{i=1} \frac{1}{i^2} < 2 - \frac{1}{n} \ \ \ \ \text{(for} \ n\geq 2 \text{)}
\end{gathered}
$$

Since $S_{n} = \sum^n_{i=1} \frac{1}{i^2}$ is an increasing sequence, and is shown to be bounded above, we can use the [[Monotone Convergence Theorem|monotone convergence theorem]] to deduce that it converges to a real limit which is $\leq 2$. Thus the inverse square series converges.

## Actual value to which it converges
The series converges to $\sum^\infty_{i=1} \frac{1}{i^2} = \frac{\pi^2}{6}$

## Generalising to inverse polynomials
For all $c \in R \ \text{such that \ c > 0}$, $\sum^\infty_{n=1} \frac{1}{n^c}$ converges.