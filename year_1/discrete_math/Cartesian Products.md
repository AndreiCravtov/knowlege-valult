#set-theory

The ***Cartesian product*** of two [[Set Theory|sets]] $A$ and $B$, denoted $A \times B$, is the set of all [[Ordered Pair|ordered pairs]] $\opair{a}{b}$ where $a \in A$ and $b \in B$, written as
$$\large A \times B \ \ \triangleq \ \ \{ \ \opair{a}{b} \ | \ a \in A \wedge b \in B \ \}$$
visualised as
$$\large
\begin{matrix}
\opair{a_{1}}{b_{1}} & \dots & \opair{a_{1}}{b_{m}}  \\
\vdots & \ddots & \vdots \\
\opair{a_{n}}{b_{1}} & \dots & \opair{a_{n}}{b_{m}}
\end{matrix}
$$
If you're taking the ***Cartesian product*** of $A \times A$ then you can use the shorthand $A^2$


# Formal Definition
Formally, elements [[Naive Set Theory#Solution|have to be selected]] from some other set. Using the [Kuratowski](https://en.wikipedia.org/wiki/Kazimierz_Kuratowski) definition of [[Ordered Pair|ordered pairs]], i.e. $\opair{a}{b} = \{ \{ a \}, \{ a, b \} \}$, we thus can select elements from $\wp\wp A \cup B$ (all of which are [[Ordered Pair|ordered pairs]]) to define the ***Cartesian product***
$$\large A \times B \ \ \triangleq \ \ \{ \ \opair{a}{b} \in \wp\wp A \cup B \ | \ a \in A \wedge b \in B \ \}$$
where $\wp A$ is the [[Power Sets|power set]] of $A$.

# Properties
The ***Cartesian product*** is not commutative, so $A \times B \not= B \times A$.

The [[Cardinality of Sets|cardinality]] of $A \times B$, for some finite sets $A$ and $B$, is $|A\times B|=|A| \times |B|$.
# $n$-ary product
Just as [[Tuple|tuples]] are the *extrapolation* of [[Ordered Pair|ordered pairs]], so is the $n$***-ary product*** is the *extrapolation* of the ***Cartesian product***.
1. Let $A_{1},\dots,A_{n}$ be arbitrary sets. The $n$***-ary product*** is written as $A_{1}\times \dots \times A_{n}$, or $\times^{n}_{i=1}A_{i}$, defined as $\{ \ \langle a_{1},\dots, a_{n} \rangle \ | \ i \in \mathbb{N} \ ( 1 \leq i \leq n \implies a_{i} \in A_{i} ) \ \}$.
3. The $n$-ary product of $A$ is written as $A^n$.

## Weak equivalence
Even though the $\times$ operation is not commutative, there is however still some clear correspondence between $A \times B \times C$, $(A \times B) \times C$ and $A \times (B \times C)$.