Series are just the summation of all the terms of a [[Sequences|sequence]]. So for some sequence $(a_{n})_{n\geq 1}$, the corresponding series would be $a_{1}+a_{2}+a_{3}+\dots= \sum_{n=1}^\infty a_{n}$.

# Formal Definitions
## Summand
For some series $\sum_{n=1}^\infty a_{n} = a_{1}+a_{2}+a_{3}+\dots$, the **summands** are the individual terms being added, so $a_{1}, a_{2}, a_{3}$ are the summands. Notice that the summands are nothing but the terms of the [[Sequences|sequence]] that the series is based on.

## Partial sums
A partial sum of a series of the form $\sum_{n=1}^\infty a_{n}$ is called $S_{n}$ (for $n\geq 1$), defined as: $$S_{n} = \sum_{i=1}^n a_{i}$$This means you can take any [[Sequences|sequence]] and turn it into a partial sum, then turn it into a series: $$(a_{n})_{n\geq 1} \ \ \mapsto \ \ \left(\sum_{i=1}^n a_{i} \right)_{n\geq 1} \ \ \mapsto \ \ \sum^\infty_{i=1}a_{i} = \lim_{ n \to \infty } \sum_{i=1}^n a_{i} $$
And thinking of it like this is useful because:
- We can define infinite sums as the limit of a partial sum
- The limit behaviour of the [[#Summand|summands]] $a_{n}$ can help determine if the series diverges

## Convergence and Divergence of Series
The definition of convergence and divergence are different from that of [[Sequences|sequences]], namely that convergence to infinity is considered to be divergence. Therefore the definition of convergence is 
$$
\sum^\infty_{i=1} a_{i} \ \text{converges to} \ L \in \mathbb{R} \triangleq \lim_{ n \to \infty } S_{n} = L \ \ \ \ \ \ \ \ \ \ \ \ \text{(where } S_{n} = \sum_{i=1}^n a_{i} \text{)}
$$
And for anything else, it diverges. So if for example it converges to infinity or doesn't converge at all.

## Unconditional Convergence of Series
The notion of *unconditional convergence* is a more strong condition than simple [[#Convergence and Divergence of Series|convergence]]. It says that swapping the terms of the series has no effect on the number which the series converges to.

The way to say this mathematically is, for all [[Mathematical Functions#Bijective Functions|bijections]] $\pi: \mathbb{N} \to \mathbb{N}$ $$\sum^\infty_{i=1}a_{i} \ \text{is unconditionally convergent} \iff \text{for all bijections}, \ \pi:\mathbb{N}\to \mathbb{N}, \ \sum^\infty_{i=1}a_{i} \ \text{and} \sum^\infty_{i=1}a_{\pi(i)} \ \text{converge to the same limit}$$

For example, the series $1 - \frac{1}{2} + \frac{1}{3} -\frac{1}{4}+\dots = \ln 2$ is **not** unconditionally convergent, since one of it's permutations, $1+\frac{1}{3}-\frac{1}{2}+\frac{1}{5}-\frac{1}{7}-\frac{1}{7}+\dots=\frac{3}{2}\ln2$, converges to a different number.

Because it is a stronger condition than convergence, we have $$\sum^\infty_{i=1}a_{i} \ \text{is unconditionally convergent} \implies \sum^\infty_{i=1}a_{i} \ \text{is convergent}$$

## Absolute Convergence of Series
We say that $$\sum^\infty_{i=1} a_{i} \ \text{is absolutely convergent} \iff \sum^\infty_{i=1} |a_{i}| \ \text{is convergent}$$
This is a useful definition because for series in [[Real Numbers|real numbers]] or in [[Vector Space|finite-dimensional real vector spaces]], a series being **absolutely convergent** is equivalent to being [[#Unconditional Convergence of Series|unconditionally convergent]].

# Properties
There are a few useful results to keep in mind with series.

## Applying properties of sequences
Defining convergence in such a way allows us to use properties of [[Sequences|sequences]] for analysing series.
- For instance, we can use [[Monotone Convergence Theorem|fundamental axiom of analysis]] to determine that for an increasing series (i.e. $S_{1} \leq S_{2} \leq S_{3} \leq \dots$) which is bounded above, it also converges (i.e. has a limit in the real numbers).

## Convergence properties
There are a few interesting things about the conditions of convergence for series
- $\sum^\infty_{i=1} a_{i} \ \text{converges} \implies (a_{n})_{n\geq 1} \ \text{converges to} \ 0$, which means that if the [[Sequences|sequence]], that the series is based on, does not converge to $0$, then neither will the series.
- $\sum^\infty_{i=1} a_{i} \ \text{converges} \iff \sum^\infty_{i=100} a_{i} \ \text{converges} \iff \sum^\infty_{i=N} a_{i} \ \text{converges}$ for some $N \in \mathbb{N}$, which means that the convergence of a series is determined by the behaviour of it's tail, and not any initial finite part. 
