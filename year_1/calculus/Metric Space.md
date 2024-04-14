A metric space is set together with a notion of *distance* between it's elements. For example, the set $\mathbb{R}$ is a metric space, and we measure the distance between $x,y \in \mathbb{R}$ with $|y-x|$.
![[Pasted image 20240121163018.png|400]]

# Formal Definition
A ***metric space*** is the pair of objects $(X, d)$, consisting of the nonempty [[Set Theory|set]] $X$ and a [[Mathematical Functions|function]] $d: X^2 \to \mathbb{R}$, provided that for all $x,y \in X$, they follow these axioms:
$$
\begin{align}
\text{The Identity of Indiscernibles:} &&& d(x,y) = 0 \iff x = y \\
\text{Symmetry} &&& d(x,y) = d(y,x) \\
\text{Triangle Inequality} &&& \forall z \in X ( \ d(x,z) \leq d(x,y) + d(y,z) \ )
\end{align}
$$
The function $d$ is also called the ***metric*** or ***distance function*** on $X$; the set $X$ is called the ***underlying set***.

## Metric Subspace
If $(X,d)$ is a *metric space*, and $S \subset X$, then we can restrict $d$ to $S$ and obtain $(S, d)$, also a *metric space*. We say that $(S,d)$ is a ***metric subspace*** of $(X,d)$.

# Examples
## Discrete Spaces
For any nonempty set $X$, and for all $x,y \in X$, define $$d(x,y) = \begin{cases} 0 & x=y \\ 1 & x \ne y \end{cases}$$
Then $(X,d)$ is called a ***discrete space***, and $d$ is a ***discrete metric***. All distinct points are equally close to each other.

## Real Coordinate Spaces
Given some [[Vector Space#Coordinate Vector Space|real coordinate space]] $\mathbb{R}^n$ ($n \in \mathbb{N}$), we can use can equip it with the [dot product](https://en.wikipedia.org/wiki/Dot_product#Coordinate_definition) (with respect to the [[Basis of Vector Space#Standard Basis|standard basis]]), and then induce the ***Euclidean [[Normed Vector Space|norm]]*** $\lvert \lvert x \rvert \rvert = \sqrt{ x \cdot x}$, and use it to define $d$ for all $x,y \in \mathbb{R}^n$: $$d(x,y) = \lvert \lvert y-x \rvert  \rvert = \sqrt{ \sum_{i=1}^n (y_{i}-x_{i})^2 }$$Then $\mathbb{R}^n$ becomes a [[Inner Product Space#Euclidean Vector Space|Euclidean vector space]] - and *also* metric space, with $d$ being the ***Euclidean metric*** for $\mathbb{R}^n$. It is important because it is the standard metric on $\mathbb{R}^n$, so it is assumed unless explicitly stated otherwise. In fact the *metric* $(x,y) \mapsto |y-x|$ for $\mathbb{R}$ is just a special case where $n = 1$. This is because $\sqrt{ (y-x)^2 } = |y-x|$.
