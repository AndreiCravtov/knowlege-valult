The set $B$ of a [[Vector Space|vector space]] $V$ is called a ***basis*** of $V$, if every vector in $V$ can be uniquely written as a [[Vector Space#Linear Combination|linear combination]] of elements of $B$. The *(usually [[#Ordered Basis and Coordinate Vectors|ordered]])* coefficients of this linear combination are known as the ***coordinates*** of that vector relative to basis $B$. The <u>vectors</u> in $B$ are called ***basis vectors***, and can be *intuitively* understood as units *(including rather odd units, such as "apples", "bananas", "kilograms" or "seconds")*

# Formal Definition
A ***basis*** $B$ of [[Vector Space|vector space]] $V$ over $F$, is a subset $B \subseteq V$ which [[Linear Span|spans]] $V$, and the all the ***basis vectors*** are [[Vector Space#Linear Independence|linearly independent]]. Those two conditions can be explicitly stated as:
- ***Linear independence:*** for every [[Cardinality of Sets#Finite Sets|finite]] subset $\{ \mathbf{b}_{1}, \mathbf{b}_{2},\dots, \mathbf{b}_{n} \} \subseteq B$ and coefficients $\alpha_{1},\alpha_{2}, \dots, \alpha_{n} \in F$, we have $\alpha_{1}\mathbf{b}_{1} + \alpha_{2}\mathbf{b}_{2} + \dots + \alpha_{n}\mathbf{b}_{n} = \mathbf{0} \implies \alpha_{1},\alpha_{2},\dots,\alpha_{n} = 0$
- ***Spanning property:*** for every $\mathbf{v} \in V$ there exist some $\mathbf{b}_{1}, \mathbf{b}_{2},\dots, \mathbf{b}_{n} \subseteq B$ and $\alpha_{1}, \alpha_{2}, \dots, \alpha_{n} \in F$, such that $\mathbf{v} = \alpha_{1}\mathbf{b}_{1} + \alpha_{2}\mathbf{b}_{2} + \dots + \alpha_{n}\mathbf{b}_{n}$
The scalars $\alpha_{1}, \alpha_{2}, \dots, \alpha_{n} \in F$ for which $\mathbf{v} = \alpha_{1}\mathbf{b}_{1} + \alpha_{2}\mathbf{b}_{2} + \dots + \alpha_{n}\mathbf{b}_{n}$ are known as the ***coordinates*** of $\mathbf{v}$ relative to basis $B$.

# Ordered Basis and Coordinate Vectors
Let [[Vector Space|vector space]] $V$ over [[Field|field]] $F$ have some <u>basis</u> $B$. When you pair ***basis*** $B$ with an ordering of it's <u>basis vectors</u>, you get whats called an ***ordered basis*** *(or frame)* of $V$. This is done by [[Indexed Family|indexing]] the ***basis vectors*** - usually by putting them in an $n$-tuple or defining a [[Sequences|sequence]].

When $V$ is [[Vector Space#Dimension of Vector Space|finite-dimensional]] and has ***ordered basis*** $B = (\mathbf{b}_{1}, \mathbf{b}_{2},\dots, \mathbf{b}_{n})$, then every <u>vector</u> $\mathbf{v} \in V$ has <u>unique</u> ***coordinates*** $\alpha_{1},\alpha_{2},\dots,\alpha_{n}\in F$ relative to $B$ - the scalars $\alpha_{1}, \alpha_{2}, \dots, \alpha_{n} \in F$ for which $\mathbf{v} = \alpha_{1}\mathbf{b}_{1} + \alpha_{2}\mathbf{b}_{2} + \dots + \alpha_{n}\mathbf{b}_{n}$. Thus, the ***coordinate vector*** of $\mathbf{v}$ relative to $B$, is the $n$-tuple $[\mathbf{v}]_{B} = (\alpha_{1},\alpha_{2},\dots,\alpha_{n}) \in F^n$. It can be interpreted as a <u>vector</u> of [[Vector Space#Coordinate Vector Space|coordinate space]] $F^n$ that encodes the ***coordinates*** of $\mathbf{v}$ relative to $B$. You can also represent the ***coordinate vector*** of $\mathbf{v}$ (relative to $B$) as either a [[Matrix#Row and Column Vectors|row vector]] or [[Matrix#Row and Column Vectors|column vector]]
$$
\begin{align}
[\mathbf{v}]_{B} = \begin{bmatrix} \alpha_{1} \\ \vdots \\ \alpha_{n} \end{bmatrix}
&&{[\mathbf{v}]_{B}}^{\mathrm{T}} = \begin{bmatrix} \alpha_{1} \ \ \alpha_{2} \ \ \dots \ \ \alpha_{n} \end{bmatrix}
\end{align}
$$
where ${[\mathbf{v}]_{B}}^{\mathrm{T}}$ is the [[Matrix#Transpose|transpose]] of $[\mathbf{v}]_{B}$. For any $\mathbf{v} \in F^n$ *(relative to [[#Standard Basis|standard basis]] $E$)* we have $[\mathbf{v}]_{E} = \mathbf{v}$; this is *precisely* why $F^n$ is called the <u>canonical</u> $n$-dimensional <u>vector space</u> over <u>field</u> $F$.

## Change-of-Basis Map
Every [[Vector Space|vector space]] $V$ over [[Field|field]] $F$ will have its [[Linear Map#Identity Map|identity map]] $I: V \to V$. So for two [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|ordered bases]] $B = (\mathbf{b}_{1}, \mathbf{b}_{2}, \dots, \mathbf{b}_{n})$, $D = (\mathbf{d}_{1}, \mathbf{d}_{2},\dots, \mathbf{d}_{n})$ of $V$, the [[#Coordinate Representation of Linear Maps|coordinate representations]] $I_{DB}$ and $I_{BD}$ are called ***change of basis maps***. They can turn the [[#Coordinate Vector|coordinate vector]] $[\mathbf{v}]_{B}$ into $[\mathbf{v}]_{D}$ and vice versa, for any $\mathbf{v} \in V$; from this its *pretty obvious* that $I_{DB} = (I_{DB})^{-1}$.

Under the ***change of basis map***, notice how $I_{DB}([\mathbf{v}]_{B}) = \mathbf{v}_{D}$ looks like the $B$ in the super script gets *"cancelled"* leaving behind $D$. While this may serve as a memory aid, no <u>actual cancellation</u> operation is taking place.

Consider two vector spaces $V,W$ over field $F$, with <u>ordered bases</u> $B$ and $D$ - respectively. Hence, for any <u>linear map</u> $\varphi: V \to W$ we can find its <u>coordinate representation</u> $\varphi_{DB}: V_{B} \to W_{D}$ relative to $B,D$. Suppose you define new ordered bases $\tilde{B}$ and $\tilde{D}$ of $V$ and $W$ respectively, and now you want to turn $\varphi_{DB}$ into $\varphi_{\tilde{B}\tilde{D}}$. Using [[Vector Space#Composing Coordinate Representations of Linear Maps|composition properties of coordinate representations]] we can write
$$\large 
\varphi_{\tilde{B}\tilde{D}} 
= I_{\tilde{B}B} \circ \varphi_{BD} \circ I_{D\tilde{D}}
$$
Notice how all change-of-basis maps are [[Linear Map#Linear Automorphism|automorphisms]] on $F^n$.

# Properties
## Existence
Every single vector space $V$ has at least one **basis**. This statement is [equivalent to the choice axiom](https://en.wikipedia.org/wiki/Basis_(linear_algebra)#Proof_that_every_vector_space_has_a_basis).

# Examples
## Orthogonal Basis
[[Vector Space#Orthogonal Vectors and Functions|orthogonal]] #todo 
https://en.wikipedia.org/wiki/Orthogonal_basis#In_functional_analysis
not done yet

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
therefore the corresponding [[#Ordered Basis and Coordinate Vectors|coordinate vector]] is $$[\pmb v]_{\mathcal{B}} = \bigg(\langle \pmb{b_{1}}, \pmb v \rangle, \langle \pmb{b_{2}}, \pmb v \rangle, \dots, \langle \pmb{b_{n}}, \pmb v \rangle \bigg)$$We can now write $\langle \pmb u, \pmb v \rangle$ as:
$$
\begin{align}
&&\langle \pmb u, \pmb v \rangle &= \bigg\langle \sum_{i=1}^n \langle \pmb u, \pmb{b_{i}} \rangle \pmb{b_{i}}, \ \pmb v \bigg\rangle
= \sum_{i=1}^n \langle \pmb u, \pmb{b_{i}} \rangle \langle \pmb{b_{i}}, \ \pmb v \rangle \\
&&&= \sum_{i=1}^n \langle \pmb u, \pmb{b_{i}} \rangle \overline{\langle \pmb u, \pmb{b_{i}} \rangle} \\
&\therefore & \langle \pmb u, \pmb v \rangle &= [\pmb u]_{\mathcal{B}} \cdot [\pmb v]_{\mathcal{B}}
\end{align}
$$
Which means that under an *orthonormal basis*, $\langle \pmb u, \pmb v \rangle$ can be written as the [dot product](https://en.wikipedia.org/wiki/Dot_product#Coordinate_definition) (for *real* vector spaces) or [complex dot product](https://en.wikipedia.org/wiki/Dot_product#Complex_vectors) (for *complex* vector spaces) of their [[#Ordered Basis and Coordinate Vectors|coordinate vector]].

## Standard Basis
The ***standard basis*** $E = (\mathbf{e}_{1}, \mathbf{e}_{2}, \dots, \mathbf{e}_{n})$ of [[Vector Space#Coordinate Vector Space|coordinate vector space]] $F^n$ is the [[#Ordered Basis and Coordinate Vectors|ordered basis]] where the components of each $\mathbf{e}_{i}$ are $0$ except the diagonal ones *(from top-left to bottom-right)* which are $1$
$$
n\left\{ \ \
\mathbf{e}_{1} = \begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0\end{pmatrix}, \ \\
\mathbf{e}_{2} = \begin{pmatrix} 0 \\ 1 \\ \vdots \\ 0\end{pmatrix}, \ \\ \dots, \ \ \\
\mathbf{e}_{n} = \begin{pmatrix} 0 \\ 0 \\ \vdots \\ 1\end{pmatrix}
\right.
$$
When $F^n = \mathbb{R}^n$ or $F^n = \mathbb{C}^n$, then it can be equipped with the [dot product](https://en.wikipedia.org/wiki/Dot_product#Coordinate_definition) or [complex dot product](https://en.wikipedia.org/wiki/Dot_product#Complex_vectors), making it an [[Inner Product Space|inner product space]], and making $E$ an [[#Orthonormal Basis|orthonormal basis]].