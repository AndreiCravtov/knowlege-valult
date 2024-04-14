Cauchy sequences are [[Sequences|sequences]] where the terms are arbitrarily close to each-other. This concept requires that the sequence is of the form $a_{n}:\mathbb{N} \to X$, where $X$ is a [[Metric Space|metric space]], since the definition requires a notion of *distance*. If the Cauchy sequence is over a [[#Complete Metric Spaces|complete metric space]] (such as the [[Real Numbers|reals]]), then that sequence [[Convergence of Sequences#Convergence to a Limit|converges]] to a limit within the metric space.

# Formal definition
If $(X,d)$ is a [[Metric Space|metric space]], and $a_{n}: \mathbb{N} \to X$ is a [[Sequences|sequence]], then $a_{n}$ is said to be ***Cauchy*** if the following statement holds: $$\forall \varepsilon \in \mathbb{R^+}, \exists N \in \mathbb{N}, \forall m,n\geq N: \ \ d(a_{m}, a_{n})<\varepsilon$$
This means that: to prove that $a_n$ is *Cauchy*, we must show that for any arbitrary $\varepsilon$ that you can pick, some $N$ can be found where all terms past $a_{N}$ are within $\varepsilon$ of each other.

Most commonly, $X = \mathbb{R}$, so $d(a_{m}, a_{n}) = |a_{n} - a_{m}|$.

# Proving Cauchy sequences
All [[Real Numbers|real]] Cauchy sequences can be proven to be [[Convergence of Sequences|convergent]], and all *real* sequences that converge to a limit can be proven to be Cauchy. $$a_{n} \ \text{converges to limit} \ l \iff a_{n} \ \text{is Cauchy}$$
To prove the $\implies$ step, we first begin with supposing that the sequence $a_{n}$ is convergent to the limit $l$. Therefore, if $n\geq N$ then we have $|a_{n}-l|< \frac{\varepsilon}{2}$, by definition. Now suppose we have $n,m \geq N$. Using the [[Absolute value#Properties with real numbers|triangle inequality]], we see that:
$$
\begin{gathered}
|a_{n}-a_{m}| = |a_{n}-a_{m}+l - l| = |(a_{n}-l)+(l-a_{m})|\\
|a_{n}-a_{m}| \leq |a_{n}-l| + |a_{m}-l| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \\
|a_{n}-a_{m}| < \varepsilon
\end{gathered}
$$
So the converging sequence has been shown to be Cauchy.

## Example: $a_{n} = \frac{1}{n}$
We start with the absolute values we must prove, and expand what it means: 
$$
\begin{gathered}
|a_{n}-a_{m}| \\
|\frac{1}{n} - \frac{1}{m}|\\
|\frac{1}{n} + (- \frac{1}{m} )|
\end{gathered}
$$
And then using the [[Absolute value#Properties with real numbers|triangle inequality]] lemma, we have that:
$$
\begin{gathered}
|\frac{1}{n} + \left( - \frac{1}{m}  \right)| \leq |\frac{1}{n}| + |-\frac{1}{m}| \\
|a_{n}-a_{m}| \leq \frac{1}{n} + \frac{1}{m} \\
\end{gathered}
$$
Now we choose any $N$ such that $N > \frac{2}{\varepsilon}$, so we have $\varepsilon > \frac{2}{N}$. Since $m,n \geq N$, then $\frac{1}{m}, \frac{1}{n} \leq \frac{1}{N}$. So we put it all together. 
$$
\begin{gathered}
|a_{n}-a_{m}| \leq \frac{1}{n}+\frac{1}{m} \leq \frac{1}{N} + \frac{1}{N} = \frac{2}{N} < \varepsilon \\
|a_{n}-a_{m}| < \varepsilon
\end{gathered}
$$
# Complete Metric Spaces
A [[Metric Space|metric space]] $(X,d)$ is ***complete*** if every *Cauchy sequence* of points in $X$, converges to a [[Convergence of Sequences#Convergence to a Limit|limit]] also in $X$. For example, $\mathbb{Q}$ is **not** complete, because some *Cauchy sequences* in $\mathbb{Q}$ converge to a limit in $\mathbb{R}$.