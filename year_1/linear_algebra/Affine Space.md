Conceptually, an affine space is what is left of a [[Vector Space|vector space]] when you forget which point is the origin. Vector spaces contain a **zero vector** (which acts as an origin). However, by pairing a vector space together with an *independent* set of points (while treating vectors as translations between those points) we lose the sense of what the origin should be; the **zero vector** becomes just another translation between points, rather than the origin.

# Formal Definition
Given some [[Vector Space|vector space]] $\vec{A}$, the ***affine space*** $A$ is a nonempty set of <u>points</u>, equipped with a [[Group Action#Free Group Action|free]] and [[Group Action#Transitive Group Action|transitive]] [[Group Action|action]] $(+)$ of [[Group#Additive group|additive group]] $\vec{A}$ on [[Set Theory|set]] $A$. $\vec{A}$ is called the <u>associated vector space</u> of $A$ and elements of $\vec{A}$ are called <u>translations</u>. The [[Field|field]] $F$ over which $\vec{A}$ is [[Vector Space#Formal Definition|defined]] is called the <u>ground field</u> of $A$.

That $(+)$ is a <u>free</u> and <u>transitive</u> <u>action</u> of $\vec{A}$ on $A$, means it is a [[Mathematical Functions|map]] $(+): A \times \vec{A} \to A$ for which
$$\large
\begin{align}
\text{Identity:} && \forall a \in A, \forall \mathbf{v}, \mathbf{w} \in \vec{A}&: \ \ a + \mathbf{0} = a \\
\text{Compatibility:} &&& \ \ \ \ \ \ \wedge \ a + (\mathbf{v} + \mathbf{w}) = (a + \mathbf{v}) + \mathbf{w} \\
\text{Free:} && \forall a \in A, \forall \mathbf{v} \in \vec{A}&: \ \ a + \mathbf{v} = a \implies \mathbf{v} = \mathbf{0} \\
\text{Transitive:} && \forall a,b \in A, \exists \mathbf{v} \in \vec{A}&: \ \ a + \mathbf{v} = b
\end{align}
$$
All together, this implies that for every point $a \in A$, the [[Mathematical Functions|map]] $\vec{A} \to A;\mathbf{v} \mapsto a + \mathbf{v}$ is [[Mathematical Functions#Bijective Functions|bijective]]. Further, it implies that for every $a,b \in A$ there exists <u>exactly one translation</u> $\mathbf{v} \in \vec{A}$ such that $a + \mathbf{v} = b$; this <u>unique translation</u> from $a$ to $b$ is denoted by $\overrightarrow{ab}$.

***NOTE:*** The above criteria describes $(+)$ as a [[Group Action#Right Group Action|right group action]], but it can be considered as [[Group Action#Formal Definition|either a right or left group action without distinction]], as all [[Vector Space#Formal Definition|vector spaces]] are [[Group#Abelian group|Abelian groups]], i.e. <u>vector addition</u> is commutative.

# Properties
## Dimension of Affine Space
The ***dimension*** of ***affine space*** $A$ is the [[Vector Space#Dimension of Vector Space|dimension]] of it's associated vector space $\vec{A}$.

## Vector Spaces as Affine Spaces
Every [[Vector Space|vector space]] $V$ may be considered as an ***affine space*** over itself, *denoted by $(V,V)$*, and every vector can be both a <u>point</u> and a <u>translation</u>. When considered as a point, the [[Vector Space#Formal Definition|zero vector]] is called the <u>origin</u>, denoted by $o$. Any [[Linear Subspace|linear subspace]] $S \subseteq V$ is thereby is also an [[Affine Space#Affine Subspaces and Parallelism|affine subspace]] $(S,S) \subseteq (V,V)$.

# Affine Map
Given two <u>affine spaces</u> $A,B$ *(with <u>associated vector spaces</u> $\vec{A}, \vec{B}$, and same <u>ground field</u>)*, an ***affine map*** *(or affine [[Homomorphism (algebraic)|homomorphism]])* from $A$ to $B$ is a [[Mathematical Functions|map]] $\varphi: A \to B$ such that its [[Linear Map|associated linear map]] $\vec{\varphi}: \vec{A} \to \vec{B}; \ \ \overrightarrow{ab} \mapsto \varphi(b) - \varphi(a)$ is *well defined*. 
This implies that for any point $a \in A$ and $\mathbf{v} \in \vec{A}$, we have
$$\large \varphi(a + \mathbf{v}) = \varphi(a) + \vec{\varphi}(\mathbf{v})$$
and as such, any ***affine map*** $\varphi$ is <u>completely defined</u> by a single point $a \in A$, its value $\varphi(a)$, and and <u>associated linear map</u> $\vec{\varphi}$.

## Affine Transformation
An ***affine transformation*** *(or affine [[Homomorphism (algebraic)#Endomorphism|endomorphism]])* of an <u>affine space</u> $A$, is an [[#Affine Map|affine map]] from an <u>affine space</u> to itself.

We can use some <u>translation</u> $\mathbf{v} \in \vec{A}$ to define the <u>translation map</u> $T_{\mathbf{v}}: A \to A; \ a \mapsto a + \mathbf{v}$, an ***affine transformation***. If can centre a [[Linear Map|linear map]] $\psi: \vec{A} \to \vec{A}$ by picking an <u>origin point</u> $o \in A$ and defining the ***affine transformation*** $\psi_{o}:A \to A; \ a \mapsto a + \psi\big(\overrightarrow{oa}\big)$. After picking an <u>origin point</u> $o \in A$, any <u>affine map</u> can be written uniquely as a combination of <u>translation maps</u> and $\psi_{o}$.

# Affine Subspaces
An ***affine subspace*** $B$ *(or flat, or linear variety)* of <u>affine space</u> $A$, is a subset $B \subseteq A$ such that the *set of vectors* $\vec{B}$
$$\large \vec{B} = \{ \ \overrightarrow{ab} \ | \ b \in B \ \}, \ \text{for some point}\ a \in A$$
qualifies as a [[Linear Subspace|linear subspace]] of $\vec{A}$ *(the <u>associated vector space</u> of $A$)*. This property *(independent of choice of $a$)* implies that $B$ is *itself* an <u>affine space</u> with <u>associated vector space</u> $\vec{B}$.

## Constructing Affine Subspaces
For some <u>affine space</u> $A$ (and <u>associated vector space</u> $\vec{A}$), we construct ***affine subspaces*** of $A$ by combining a <u>point</u> $a \in A$ with [[Linear Subspace|linear subspace]] $V \subseteq \vec{A}$ into the ***affine subspace*** $a + V$
$$\large a + V = \{ \ a + \mathbf{v} \ | \ \mathbf{v} \in V \ \}$$
The <u>direction</u> of $a + V$ is $V$ *(its <u>associated vector space</u>)*; $a + V$ is the <u>unique</u> ***affine subspace*** which <u>passes through</u> $a$ with <u>direction</u> $V$.

## Parallel Subspaces
If two ***affine subspaces*** have the *same* <u>direction</u>, or one of the <u>directions</u> is a [[Linear Subspace|linear subspace]] of the other, then they are are called parallel. For any ***affine subspace*** $S$ with <u>direction</u> $V$, every [[#Affine Transformation|translation map]] $T_{\mathbf{v}}: A \to A; \ a \mapsto a + \mathbf{v}$ will produce the [[Mathematical Functions#Image Sets|image affine subspace]] $T_{v}[S]$ that will be <u>parrallel</u> to $S$.

# Affine Combinations and Barycenter
Let $a_{1},\dots,a_{n} \in A$ be <u>points</u> from <u>affine space</u> $A$, let $\lambda_{1}, \dots, \lambda_{n} \in F$ be scalars from <u>ground field</u> $F$, and let $m = \lambda_{1} + \dots + \lambda_{n}$. When $m=1$, then there exists <u>exactly one point</u> $g \in A$ for which
$$\large
\forall o \in A: \ \ \lambda_{1}\overrightarrow{o a_{1}} + \dots + \lambda_{n}\overrightarrow{o a_{n}} = \overrightarrow{o g}
$$
That <u>unique point</u> $g$ is called the ***barycenter*** *(or centroid)* of the <u>points</u> $a_{1},\dots,a_{n}$ for the weights $\lambda_{1}, \dots, \lambda_{n}$. It is also called the ***affine combination*** of <u>points</u> $a_{1},\dots,a_{n}$ with <u>coefficients</u> $\lambda_{1}, \dots, \lambda_{n}$, which may be denoted by
$$\large g = \lambda_{1} a_{1} + \dots + \lambda_{n} a_{n}$$
For any other $m\neq 0$, the above result applied to the <u>normalised coefficients</u> $m^{-1}\lambda_{1} + \dots + m^{-1}\lambda_{n} = 1$.

## Balanced Sum
When $m=0$, then for any <u>points</u> $o_{L}, o_{R} \in A$, we have
$$\large
\lambda_{1}\overrightarrow{o_{L} a_{1}} + \dots + \lambda_{n}\overrightarrow{o_{L} a_{n}} = \lambda_{1}\overrightarrow{o_{R} b_{1}} + \dots + \lambda_{n}\overrightarrow{o_{L} b_{n}}
$$
Thus, this sum is independent of the choice of the origin, and the resulting <u>unique translation</u> may be denoted
$$\large \lambda_{1} a_{1} + \dots + \lambda_{n} a_{n} \in \vec{A}$$
The <u>translation</u> $\lambda_{1} a_{1} + \dots + \lambda_{n} a_{n}$ is sometimes called the ***balanced/zero-sum combination*** combination of <u>points</u> $a_{1},\dots,a_{n}$ with coefficients $\lambda_{1}, \dots, \lambda_{n}$. For example, setting $n=2, \lambda_{1} = 1, \lambda_{2} = -1$ yields the definition of the subtraction of points.

# Affine Span and Basis
For any nonempty subset $S \subseteq A$ of <u>affine space</u> $A$, the [[Cardinality of Sets|smallest]] [[#Affine Subspaces|affine subspace]] that contains $S$ is called the ***affine span*** of $S$, denoted by $span(S)$, and is equal to the intersection of all <u>affine subspaces</u> containing $S$. Thus we can deduce that the <u>direction</u> of $span(S)$ is the intersection of the <u>directions</u> of the <u>affine subspaces</u> that contain $S$

If $S$ is [[Cardinality of Sets#Finite Sets|finite]], then there's an equivalent definition of the ***affine span*** of $S$, namely: it is the set of all [[#Affine Combinations and Barycenter|affine combinations]] of <u>points</u> of $S$. More explicitly, for $S = \{ a_{1}, \dots, a_{n} \}$ and <u>ground field</u> $F$ we have 
$$\large
span(S) = \left\{ \ \lambda_{1} a_{1} + \dots + \lambda_{n} a_{n} \ | \ \lambda_{1}, \dots, \lambda_{n} \in F \ \wedge \ \lambda_{1} + \dots + \lambda_{n} = 1 \ \right\}
$$
As such, the <u>direction</u> of the ***affine span*** of $S$, is the [[Linear Span|linear span]] of the set $\{ \ \overrightarrow{ab} \ | \ a,b \in S \ \}$. By choosing a particular <u>origin point</u> $o \in S$, the <u>direction</u> of $span(S)$ is also the <u>linear span</u> of the set $\{ \ \overrightarrow{oa} \ | \ a \in S \ \}$. We say $span(S)$ was ***generated*** by $S$, and that $S$ is a ***generating set*** of $span(S)$.

The nonempty subset $S \subseteq A$ is said to be ***affinely independent*** *(or just independent)* if for every strict subset $X \subset S$ we have $span(X) \subset span(S)$. An ***affine basis*** (or ***barycentric frame***) of an <u>affine space</u> $A$ a ***generating set*** $S \subseteq A$ of $A$ which is also ***affinely independent***. Such a set $S$ is *also* called a ***minimal generating set***.

Recall that the [[#Dimension of Affine Space|dimension of an affine space]] $A$ is the [[Vector Space#Dimension of Vector Space|dimension]] of it's associated vector space $\vec{A}$. So if the dimension of $A$ is $n$, then the ***affine bases*** of $A$ will consist of $n+1$ elements.