# Definition
If $f: \mathbb{N} \to \mathbb{R}$ is a [[Sequences|sequence]] and $M \subseteq \mathbb{N}$, then the restriction $f: M \to \mathbb{R}$ is called a *subsequence* of $f$. The notation for a sequence is usually like like this: $a_{n}$ where $a$ is the name of the sequence and $n$ is the indexing variable. The notation of the subsequence of $a_{n}$ would be $a_{n_{i}}$ where the name of the subsequence is $a_{n}$ and the indexing variable is $i$. The values $n_{i}$ should be increasing positive integers such that $n_{1}<n_{2}<n_{3}<\dots$ where $M = \{ n_{i} : i\geq 1 \}$. This means that $n_{i} \geq i$ is true by definition.

## Example usage
For example take the sequence $a_{n} = \frac{1}{n}$ (for all $n\geq 1$). Lets say we want a subsequence using only odd numbers. Then $M = \{ 1, 3, 5, 7, \dots \} \subseteq \mathbb{R}$. Thus $n_{1}=1<n_{2}=3<n_{3}=5<n_{4}=7, \dots$ and $a_{n_{1}}=1, a_{n_{2}}=\frac{1}{3}, a_{n_{3}} = \frac{1}{5}, a_{n_{4}}=\frac{1}{7},\dots$ and so on.

# Shortcut Representation
A convenient notation to represent a subsequence would be to write $a_{f(i)}$ where $f(i)$ is some function of type $f: \mathbb{N} \to \mathbb{N}$.

## Example usage
For example, given the sequence $a_{n} = \frac{1}{n}$ (for all $n\geq 1$), a subsequence of only odd numbers would be $a_{2i-1}$ thus given that $i\geq 1$, we get $i=1 \to a_{1}, \ i=2 \to a_{3}, \ i=3 \to a_{5}, \ i=4 \to a_{7}$ and so on.

# Properties
## Convergence
Given some sequence $(a_{n})_{n\geq 1}$ which[[Convergence of Sequences|converges to some limit]], then any subsequence $(a_{n_{i}})_{i\geq 1}$ also converges to that limit.

### Proof
Given that $\lim_{ n \to \infty } a_{n} = L$, where $L \in \mathbb{R}$, and given some arbitrary subsequence $(a_{n_{i}})_{i\geq 1}$, then for all $\varepsilon>0$ there exists $N \in \mathbb{N}$ such that for all $n>N$ we have $|a_{n}-L|<\varepsilon$, by the definition of limit. Note that by definition we always have that $n_{i} \geq i$ therefore: 
$$
\begin{gathered}
n \geq n_{i} \geq i > N \\
\text{so} \\
i > N
\end{gathered}
$$
thus we have $|a_{n_{i}-L}|<\varepsilon$ as the arbitrary $\varepsilon$ remains the same, the selected $N$ remains the same for which the indexing variable is more than it, and the result of the inequality, too, remains the same as the actual values of the subsequence are the same as the ones in the sequence.

The proof for convergence to $\pm \infty$ would be similar.  