The idea of *convergence* as it applies to [[Sequences|sequences]] is that as $n$ approaches infinity, $a_{n}$ approaches some value. Sequences are a *kind* of [[Mathematical Functions|function]], therefore if $a_{n}: \mathbb{N} \to X$ (where $X$ is a [[Metric Space|metric space]]) then we can use [[Limit of a Function|limits]] to define what it means for a sequence to *converge*. 

# Formal definition
Consider the [[Metric Space|metric space]] $(X,d)$ and [[Sequences|sequence]] $a_{n}:\mathbb{N} \to A$, where $A \subseteq X$.

## Convergence to a Limit
For some limit $L \in X$, we say that $a_{n}$ ***converges to*** $L$, if we have the [[Limit of a Function#Finite Limit at Infinity|limit]] $\lim_{ n \to \infty } a_{n} = L$. For **sequences**, it is customary to work with this definition: $$\forall \varepsilon >0, \exists N \in \mathbb{N}, \forall n \in \mathbb{N}: \ \ n>N \implies d(a_{n},L)<\varepsilon$$but this definition is [[Limit of a Function#Infinite Limit at a Point|equivalent to all the others]]. We can denote that $a_{n}$ converges to $L$ with: $$\lim_{ n \to \infty } a_{n} = L \ \ \text{or} \ \ (a_{n})_{n \geq 0} \to L $$
We can visualise this definition with an example sequence, $a_{n}=\frac{1}{n}$:
```desmos-graph
left=-1; right=11;
top=1.1; bottom=-0.1;
---
(2, 0.75) | hidden | black | label: `a_n=\frac{1}_{n}`
n = 15
N = [1,2,...n]
a(x) = 1/x | hidden
(N, a(N))

(-0.2, 0.2) | hidden | red | label: `\varepsilon`
(5, -0.04) | hidden | blue | label: `N`
y=0.2 | x>0
x=5 | y>0
```
Given that value of $\varepsilon$ we found $N$ where all values of $a_n$ for $n>N$ are less than $\varepsilon$ distance from $0$ (the *limit* of the example sequence). This exact proof must be supplied for each and every possible $\varepsilon$. Only then can that sequence be said to converge to $0$.

## Convergence to Infinity
When $X=\mathbb{R}$, we can say that $a_{n}$ ***converges to*** $\pm \infty$, if we have a [[Limit of a Function#Infinite Limit at Infinity|limit]] $\lim_{ n \to \infty } a_{n} = \pm \infty$. For **sequences**, it is customary to work with *these* definitions:  $$
\begin{align}
&\lim_{ n \to \infty } a_{n} = \infty &&\iff&& \forall r \in \mathbb{R}, \exists N \in \mathbb{N}, \forall x \in A: \ \ x>N \implies f(x)>r \\
&\lim_{ n \to \infty } a_{n} = -\infty &&\iff&& \forall r \in \mathbb{R}, \exists N \in \mathbb{N}, \forall x \in A: \ \ x>N \implies f(x)<r
\end{align}
$$but those are [[Limit of a Function#Infinite Limit at Infinity|equivalent to all the others]]. We can denote that $a_{n}$ converges to $L$ with: $$\lim_{ n \to \infty } a_{n} = \pm \infty \ \ \text{or} \ \ (a_{n})_{n \geq 0} \to \pm \infty $$

## Divergence
When $X=\mathbb{R}$, we say that $a_{n}$ ***converges***, if it [[#Convergence to a Limit|converges to some limit]] or [[#Convergence to Infinity|infinity]]. We say that $a_{n}$ ***diverges***, if it *does not converge*.

# Proving convergence
In order to prove convergence for a sequence $a_{n}: \mathbb{N} \to \mathbb{R}$ and some limit $L$, we must take an arbitrary $\varepsilon$ and then derive an $N$ from it. In effect, we want some function of the type  $f: \mathbb{R^+} \to \mathbb{N}$ that takes the $\varepsilon$ as input and produces some $N$ as output. When constructing such a function, we must prove that it will always produce values that meet the definition of what it means to converge to limit $L$.

## Example: $a_{n} = \frac{1}{n}$
We start with an arbitrary $\varepsilon$, and we take its reciprocal (it seems like the intuitive step to take given that the sequence is a reciprocal).
So we have $\frac{1}{\varepsilon}$. The value $\frac{1}{\varepsilon}$ is not always whole, but we need it to be whole, so we will apply the $ceil$ operator to it. We choose $N$ as the result of that, so $N = \lceil \frac{1}{\varepsilon} \rceil$.
Now we put the steps together, remembering that $a_{n} = \frac{1}{n}$ and $L=0$
$$
\begin{gathered}
n > N = \lceil \frac{1}{\varepsilon} \rceil > \frac{1}{\varepsilon} \\ \\
n > \frac{1}{\varepsilon} \\
|\frac{1}{n}| < \varepsilon \\
|\frac{1}{n} - 0| < \varepsilon \\ \\
|a_{n} - L| < \varepsilon
\end{gathered}
$$
And just like that we ended up proving that $a_{n} = \frac{1}{n}$ tends towards $0$

# Composing the Limits of Sequences
We can apply the [[Limit of a Function#Limit Composition Theorem|limit composition theorem]] directly to convergence of [[Sequences|sequences]]. Consider the [[Sequences|sequences]] $a_{n}:\mathbb{N}\to A$ and $b_{n}:\mathbb{N}\to B$ (where $A, B \subseteq \mathbb{R}$), and numbers $\lambda,a,b \in \mathbb{R}$. By applying [[Limit of a Function#Examples|these results]], we get the following:
$$
\begin{aligned}
1: \ & \lim_{ n \to \infty } a_{n} = a &&\iff&& \lim_{ n \to \infty } \lambda a_{n} &&= \lambda \lim_{ n \to \infty } a_{n} &&= \lambda a \\
2: \ & \lim_{ n \to \infty } a_{n} = a, \ \lim_{ n \to \infty } b_{n} = b &&\iff&& \lim_{ n \to \infty } a_{n} + b_{n} &&= \lim_{ n \to \infty } a_{b} + \lim_{ n \to \infty } b_{n} &&= a+b \\
3: \ & \lim_{ n \to \infty } a_{n} = a, \ \lim_{ n \to \infty } b_{n} = b &&\iff&& \lim_{ n \to \infty } a_{n} - b_{n} &&= \lim_{ n \to \infty } a_{n} - \lim_{ n \to \infty } b_{n} &&= a-b \\
4: \ & \lim_{ n \to \infty } a_{n} = a, \ \lim_{ n \to \infty } b_{n} = b &&\iff&& \lim_{ n \to \infty } a_{n}b_{n} &&= \lim_{ n \to \infty } a_{n} \lim_{ n \to \infty } b_{n} &&= ab \\
5: \ & \lim_{ n \to \infty } a_{n} = a, \ \lim_{ n \to \infty } b_{n} = b \neq 0 &&\iff&& \lim_{ n \to \infty } \frac{a_{n}}{b_{n}} &&= \frac{\lim_{ n \to \infty } a_{n}}{\lim_{ n \to \infty } b_{n}} &&= \frac{a}{b}
\end{aligned}
$$
