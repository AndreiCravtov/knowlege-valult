The set $B$ of a [[Vector Space|vector space]] $V$ is called a ***basis*** of $V$, if every vector in $V$ can be uniquely written as a [[Vector Space#Linear Combination|linear combination]] of elements of $\mathcal{B}$. The coefficients of this linear combination are referred to as [[Coordinate Vector|coordinates]] of that vector with respect to $\mathcal{B}$. The elements of $\mathcal{B}$ are called ***basis vectors***.

# Formal Definition
A ***basis*** $\mathcal{B}$ of [[Vector Space|vector space]] $V$ over $F$, is a subset $\mathcal{B} \subseteq V$ which [[Linear Span|spans]] $V$, and the all the ***basis vectors*** are [[Vector Space#Linear Independence|linearly independent]]. Those two conditions can be explicitly stated as:

**linear independence:** for every [[Cardinality of Sets#Finite Sets|finite]] subset $\{ \pmb{v_{1}},\pmb{v_{2}},\dots,\pmb{v_{n}} \} \subseteq \mathcal{B}$, if $a_{1}\pmb{v_{1}} + a_{2}\pmb{v_{2}} + \dots + a_{n}\pmb{v_{n}} = \pmb 0$, then $a_{1} = \dots = a_{n} = 0$, for any $a_{1},a_{2},\dots,a_{n} \in F$.

**spanning property:** for all $\pmb v \in V$, there exist some $\pmb{v_{1}},\pmb{v_{2}},\dots,\pmb{v_{n}} \in \mathcal{B}$ and $a_{1},a_{2},\dots,a_{n} \in F$, such that $\pmb v = a_{1}\pmb{v_{1}} + a_{2}\pmb{v_{2}} + \dots + a_{n}\pmb{v_{n}}$.

## Ordered Basis
An ***ordered basis***, also called a ***frame***, is a *basis* $\mathcal{B}$ paired with an ordering of it's *basis vectors*. This is done by [[Indexed Family|indexing]] the *basis vectors*, usually by putting them in an $n$-tuple or defining a [[Sequences|sequence]]. Ordering is very important when discussing things like [[Coordinate Vector|coordinate vectors]].

# Properties
## Existence
Every single vector space $V$ has at least one **basis**. This statement is [equivalent to the choice axiom](https://en.wikipedia.org/wiki/Basis_(linear_algebra)#Proof_that_every_vector_space_has_a_basis).

# Examples
## Orthonormal Basis
An ***orthonormal basis*** $\mathcal{B}$ for a [[Hilbert Space#Finite Dimensional Inner Product Space|finite-dimensional inner product space]] $V$, is a **basis** who's **basis vectors** are ***orthonormal***, i.e. they are all unit vectors and orthogonal to each-other. This means that for every $\pmb {b_{a}}, \pmb {b_{a}} \in \mathcal{B}$, we have:
- $\lvert \lvert \pmb{b_{a}} \rvert \rvert = 1$.
- $\langle \pmb{b_{a}},\pmb{b_{a}}\rangle = 1$.
- $\langle \pmb{b_{a}},\pmb{b_{b}}\rangle = 0$ if $\pmb{b_{a}} \ne \pmb{b_{b}}$.

Because $\mathcal{B} = \{ \pmb {b_{1}}, \pmb {b_{2}}, \dots, \pmb {b_{n}} \}$ is a basis, it means that for every $\pmb v \in V$, there exist some unique scalars $v_{1}, v_{2},\dots,v_{n}$ for which: $$\pmb v = v_{1} \pmb{b_{1}} + v_{2} \pmb{b_{2}} + \dots + v_{n} \pmb{b_{n}}$$From this, we can write $\pmb v$ *purely* in terms of **itself** and the basis vectors:
$$
\begin{align}
&& \pmb v &= \sum_{i=1}^n v_{i} \pmb{b_{i}} = \sum_{i=1}^n v_{i} \langle \pmb{b_{i}}, \pmb{b_{i}} \rangle \pmb{b_{i}} = \sum_{i=1}^n \sum_{j=1}^n v_{j} \langle \pmb{b_{j}}, \pmb{b_{i}} \rangle \pmb{b_{i}} \\
&&&= \sum_{i=1}^n \langle \sum_{j=1}^n v_{j} \pmb{b_{j}}, \pmb{b_{i}} \rangle \pmb{b_{i}} = \sum_{i=1}^n \langle \pmb v, \pmb{b_{i}} \rangle \pmb{b_{i}} \\ \\
&\therefore & \pmb v &= \langle \pmb v, \pmb{b_{1}} \rangle \pmb{b_{1}} + \langle \pmb v, \pmb{b_{2}} \rangle \pmb{b_{2}} + \dots + \langle \pmb v, \pmb{b_{n}} \rangle \pmb{b_{n}}
\end{align}
$$
therefore the corresponding [[Coordinate Vector|coordinate vector]] is $$[\pmb v]_{\mathcal{B}} = \bigg(\langle \pmb{b_{1}}, \pmb v \rangle, \langle \pmb{b_{2}}, \pmb v \rangle, \dots, \langle \pmb{b_{n}}, \pmb v \rangle \bigg)$$We can now write $\langle \pmb u, \pmb v \rangle$ as:
$$
\begin{align}
&&\langle \pmb u, \pmb v \rangle &= \bigg\langle \sum_{i=1}^n \langle \pmb u, \pmb{b_{i}} \rangle \pmb{b_{i}}, \ \pmb v \bigg\rangle
= \sum_{i=1}^n \langle \pmb u, \pmb{b_{i}} \rangle \langle \pmb{b_{i}}, \ \pmb v \rangle \\
&&&= \sum_{i=1}^n \langle \pmb u, \pmb{b_{i}} \rangle \overline{\langle \pmb u, \pmb{b_{i}} \rangle} \\
&\therefore & \langle \pmb u, \pmb v \rangle &= [\pmb u]_{\mathcal{B}} \cdot [\pmb v]_{\mathcal{B}}
\end{align}
$$
Which means that under an *orthonormal basis*, $\langle \pmb u, \pmb v \rangle$ can be written as the [dot product](https://en.wikipedia.org/wiki/Dot_product#Coordinate_definition) (for *real* vector spaces) or [complex dot product](https://en.wikipedia.org/wiki/Dot_product#Complex_vectors) (for *complex* vector spaces) of their [[Coordinate Vector|coordinate vectors]].

## Standard Basis
The ***standard basis*** $\mathcal{B}$ for a [[Vector Space#Coordinate Vector Space|coordinate space]] $\mathbb{F}^n$, is a **basis** consisting of $n$ elements, where all the components are $0$, except for one of them, which is $1$, so it would be:
$$
\begin{align}
\kern .4em
    \underbrace{
      \kern-.4em
      \left.
      \left.
        \begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0\end{pmatrix} \\
        \begin{pmatrix} 0 \\ 1 \\ \vdots \\ 0\end{pmatrix} \\ \dots \\
        \begin{pmatrix} 0 \\ 0 \\ \vdots \\ 1\end{pmatrix}
      \right.    
      \right\} n
      \Rule{0em}{0em}{3.1em}
      \kern -1.9em
    }_{\textstyle n}
\kern 4.5em
\end{align}
$$
When $\mathbb{F}^n = \mathbb{R}^n$ or $\mathbb{F}^n = \mathbb{C}^n$, then it can be equipped with the [dot product](https://en.wikipedia.org/wiki/Dot_product#Coordinate_definition) or [complex dot product](https://en.wikipedia.org/wiki/Dot_product#Complex_vectors), making it an [[Inner Product Space|inner product space]], and making $\mathcal{B}$ an [[#Orthonormal Basis]].