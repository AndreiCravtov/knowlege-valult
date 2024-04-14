Power series are a family of infinite [[Series|series]], where each of those series is actually the [[Taylor Series|Taylor series expansion]] of a [[Smoothness|infinitely differentiable]] function. They are of the form $\sum^\infty_{i=0} a_{i}(x-c)^i$, where $(a_{n})_{n\geq 0}$ is some sequence, $c \in \mathbb{R}$ is a constant, and $x \in \mathbb{R}$ is a variable.
Fun fact, if we set $a_{n} = a, c=0$ - for some constant $a \in \mathbb{R}$, then the power series becomes a [[Geometric Series|geometric series]], thus power series as a generalisation of [[Geometric Series|geometric series]].

# Formal Definition
For some sequence $(a_{n})_{n\geq 0}$, constant $c \in \mathbb{R}$ , and variable $x \in \mathbb{R}$, a power series is defined as
$$P(x) = \sum^\infty_{k=0} a_{k}(x-c)^k$$
# Radius of Convergence
Just by inspection, we can see that $P(x)$ is [[Convergence of Sequences|convergent]] for at least some values of $x$ (i.e. $x=c$). For other values of $x$ it might [[Convergence of Sequences#Divergence|diverge]]. The values of $x$ for which $P(x)$ converges/diverges are captured by the **radius of convergence** $0\leq r \leq \infty$, which can be defined using the [[Limit Superior and Limit Inferior|limit superior]] as: $$r^{-1} = \limsup_{ n \to \infty } |a_{n}|^{\frac{1}{n}}$$
Once we have $r$, we know that $P(x)$ *converges* when $|x-c| < r$, and *diverges* when $|x-c| > r$.

## Proof
Keeping the definition of $r^{-1} = \limsup_{ n \to \infty } |a_{n}|^{\frac{1}{n}}$ in mind, we apply [[Convergence Tests for Series#The $n { text{th}}$-root test for convergence|n'th root test]] to $P(x)$:
$$
\begin{gathered}
\limsup_{ n \to \infty } |a_{n}(x-c)^n|^{1/n} \ = \ |x-c|\limsup_{ n \to \infty } |a_{n}|^{1/n} \ = \ r^{-1}|x-c| \\
\\ \text{and} \\ \\
r^{-1}|x-c| < 1 \iff |x-c| < r\\
r^{-1}|x-c| > 1 \iff |x-c| > r
\end{gathered}
$$
Hence, according to the [[Convergence Tests for Series#The $n { text{th}}$-root test for convergence|n'th root test]], when
1. $|x-c| < r$ then $P(x)$ converges absolutely
2. $|x-c| > r$ then $P(x)$ diverges
Which proves the properties of the [[#Radius of Convergence|radius of convergence]] $r$, as described above.

**NOTE:** since $r$ can take on values of $0$ and $\infty$, then we use the convention $r=0 \iff r^{-1}=\infty$ and $r=\infty \iff r^{-1}=0$.

## Ratio Test for Radius of Convergence
We can apply the [[Convergence Tests for Series#Limit Absolute Value Ratio Test|limit absolute value ratio test]] on $P(x)$ to arrive at the conclusion that for the radius of convergence $r$, or power series $P(x)$, we have: $$\lim_{ n \to \infty } \left| \frac{a_{n+1}}{a_{n}} \right| = l \ \ \in \ \mathbb{R} \implies r=l^{-1}$$

# Operations on Power Series
Two power series, $P_{1}(x) = \sum^\infty_{i=0} a_{i}(x-c)^i$ and $P_{2}(x) = \sum^\infty_{i=0} b_{i}(x-c)^i$ have [[#Radius of Convergence|radii of convergence]] of $r_{1}$ and $r_{2}$ respectively.

## Adding and Subtracting
We can add and subtract like this: $$P_{3}(x) = P_{1}(x) \pm P_{2}(x) = \sum^\infty_{i=0} (a_{i} + b_{i})(x-c)^i$$
Where the resulting series, $P_{3}(x)$, will have a radius of convergence $r_{3}\geq \min \{ r_{1}, r_{2} \}$.

## Multiplication
If $|x| < \min \{ r_{1}, r_{2} \}$, we can multiply like this:
$$P_{3}(x) = P_{1}(x)P_{2}(x) = \sum^\infty_{n=0} \left( \sum^n_{i=0} a_{i}b_{n-1} \right)(x-c)^n$$
Where the sequence $(m_{n})_{n\geq 0} = \sum^n_{i=0} a_{i}b_{n-1}$ is known as the [convolution](https://en.wikipedia.org/wiki/Convolution) of sequences $a_{n}$ and $b_{n}$.

## Integration and Differentiation
Within the [[#Radius of Convergence|radius of convergence]], a power series is [[Continuity|continuous]] and can be [[Differentiation of Real Functions|differentiated]] and [[Riemann Integral|integrated]]. So for some power series $P(x) = \sum^\infty_{n=0} a_{n}(x-c)^n$ that has a convergence radius $r$, we can say that $P(x)$ converges for all $x$ where $|x-c| < r$, and as such the derivative is: $$P'(x) = \sum^{\infty}_{n=0} a_{n+1} (n+1) (x-c)^n$$
Similarly, the integral is: $$\int_{c}^x P(y) \, dy = \sum^{\infty}_{n=0} \frac{a_{n} (x-c)^{n+1}}{n+1}$$

## Solving Ordinary Differential Equations 
We can use integration and differentiation of power series to solve certain differential equations by rewriting all terms as their power series equivalent, and then matching coefficients to get a recurrence relation, which is resolved to give the final answer. [Here](https://www.youtube.com/watch?v=LjV_yHafIj8) is an example