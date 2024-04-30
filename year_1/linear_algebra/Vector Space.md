#linear-algebra

A **vector space** is a [[Set Theory|set]] whose elements (called vectors) can be *added* and *scaled* by scalars. These scalars can be elements of any [[Field|field]], but its most commonly the [[Real Numbers|real numbers]].
![[Pasted image 20240121171146.png]]

# Formal Definition
A ***vector space*** over [[Field|field]] $F$ is a nonempty set $V$, equipped with *vector addition* $(+):V \times V \to V$, and *scalar multiplication* $(\cdot): F \times V \to V$, such that these [[Mathematical Functions|functions]] satisfy the following axioms for every $\pmb u,\pmb v, \pmb w \in V$, and $a,b \in F$:
$$
\begin{align}
\text{Associativity:} &&& \mathbf{u} + (\mathbf v + \mathbf w) = (\mathbf u+ \mathbf v)+ \mathbf w \\
\text{Commutativity:} &&& \mathbf u + \mathbf v = \mathbf v + \mathbf u \\
\text{Vector addition identity element:} &&& \exists \mathbf 0 \in V [ \ \mathbf v + \mathbf 0 = \mathbf v \ ] \\
\text{Inverse element:} &&& \exists \mathbf{-v} \in V [\ \mathbf v + \mathbf {-v} = \mathbf 0 \ ] \\
\text{Field and scalar multiplication composability:} &&& a(b \mathbf v) = (ab) \mathbf v \\ 
\text{Saclar multiplication identity element:} &&& 1 \mathbf v = \mathbf v, \ \text{where} \ 1 \ \text{is the multiplicative identity in} \ F \text{.} \\
\text{Distributivity:} &&& \begin{aligned}
& a(\mathbf u + \mathbf v) = a \mathbf u + a \mathbf v \\
& (a + b) \mathbf v = a \mathbf v + b \mathbf v
\end{aligned}
\end{align}
$$
The elements of $V$ are called ***vectors**,* and the elements of $F$ are called ***scalars***. Every *vector space* is an [[Group#Additive group|additive]] [[Group#Abelian group|Abelian group]], because *vector addition* satisfies the [[Group#Formal Definition|group axioms]] and is *commutative*.

When the scalar [[Field|field]] is the [[Real Numbers|real numbers]], then the vector space is called a ***real vector space***; likewise for [[Complex Numbers|complex numbers]] it is called a ***complex vector space***. Those are the two most common cases.

# Properties
## Dimension of Vector Space
The dimension of a vector space $V$, denoted by $\dim(V)$, is the [[Cardinality of Sets|cardinality]] of a [[Basis of Vector Space|basis]] of $V$.

## Linear Combination
$V$ is a vector space over field $F$. Given some vectors $\mathbf{v}_{1}, \mathbf{v}_{2},\dots, \mathbf{v}_{n} \in V$ and scalars $\alpha_{1},\alpha_{2},\dots,\alpha_{n} \in F$, their ***linear combination*** is: $\alpha_{1} \mathbf{v}_{1} + \alpha_{2} \mathbf{v}_{2} + \dots + \alpha_{n} \mathbf{v}_{n}$. A ***trivial*** linear combination is one where all the scalar coefficients $\alpha_{1},\alpha_{2},\dots,\alpha_{n} \in F$ are $0$.

## Linear Independence
$V$ is a vector space over field $F$. The vectors $\mathbf{v}_{1}, \mathbf{v}_{2},\dots, \mathbf{v}_{n} \in V$ are ***linearly independent*** if for all $\alpha_{1}, \alpha_{2}, \dots, \alpha_{n} \in F$, $\alpha_{1} \mathbf{v}_{1} + \alpha_{2} \mathbf{v}_{2} + \dots + \alpha_{n} \mathbf{v}_{n} = \mathbf0$ is a [[#Linear Combination|trivial linear combination]], i.e. the scalar coefficients $\alpha_{1},\alpha_{2},\dots,\alpha_{n} \in F$ are always $0$.

If there exists some $\alpha_{1},\alpha_{2},\dots,\alpha_{n} \in F$, where $a_{1} \mathbf{v}_{1} + a_{2} \mathbf{v}_{2} + \dots + a_{n} \mathbf{v}_{n} = \mathbf0$ is <u>not</u> a [[#Linear Combination|trivial linear combination]], then we say that $\mathbf{v}_{1}, \mathbf{v}_{2},\dots, \mathbf{v}_{n} \in V$ are ***linearly dependent***. The reason they are called <u>dependent</u>, is because at least one of those scalars is nonzero (e.g. $\alpha_{1} \ne 0$). This means that at least one of those vectors can be expressed in terms of the other vectors, i.e. $$\mathbf{v}_{1} = \frac{-\alpha_{2}}{\alpha_{1}}\mathbf{v}_{2} + \dots + \frac{-\alpha_{n}}{\alpha_{1}}\mathbf{v}_{n}$$and therefore the value of that one vector, depends on the value of the other vectors.

### Linearly Independent Sets
Given some set $B \subseteq V$, its called ***linearly independent*** if every [[Cardinality of Sets#Finite Sets|finite]] subset $\{ \mathbf{v}_{1}, \mathbf{v}_{2},\dots, \mathbf{v}_{n} \} \subseteq B$ is also *linearly independent*.

## Orthogonal Vectors and Functions
***Orthogonality*** is the generalisation of [perpendicularity](https://en.wikipedia.org/wiki/Perpendicularity "Perpendicularity") for <u>vector spaces</u> and [[Linear, Bilinear, and Multilinear Forms#Bilinear Form - Symmetric, Skew-Symmetric, Alternating, Reflexive|bilinear forms]]. Consider <u>vector space</u> $V$ over [[Field|field]] $F$ and equipped with <u>bilinear form</u> $B: V \times V \to F$. When $B$ is [[Linear, Bilinear, and Multilinear Forms#Bilinear Form - Symmetric, Skew-Symmetric, Alternating, Reflexive|reflexive]], then the <u>vectors</u> $\mathbf{u}, \mathbf{v} \in V$ for which $B(\mathbf{u}, \mathbf{v}) = 0$, are called ***orthogonal vectors*** and denoted by $\mathbf{u} \perp \mathbf{v}$.

When $B$ is ***not reflexive***, then we must distinguish ***left-orthogonal*** and ***right-orthogonal***: for <u>vectors</u> $\mathbf{u}, \mathbf{v} \in V$ such that $B(\mathbf{u}, \mathbf{v}) = 0$, $\mathbf{u}$ is ***left-orthogonal*** to $\mathbf{v}$ *and* $\mathbf{v}$ is ***left-orthogonal*** to $\mathbf{u}$.

If $V$ is *also* a [[Function Space|function space]], then all <u>vectors</u> are <u>functions</u> thus it can be called ***orthogonal functions*** rather than ***orthogonal vectors***.

## Endomorphism Algebra of a Vector Space: $\mathrm{End}(V)$
Consider the [[Function Space#Space of Linear Transformations $ mathcal{L}(V,W)$,$ mathrm{Hom}(V,W)$|space of linear transformations]] $\mathcal{L}(V,V)$ for some [[Vector Space|vector space]] $V$ over [[Field|field]] $F$. Every [[Linear Map|linear maps]] in $\mathcal{L}(V,V)$ is a [[Linear Map#Linear Endomorphism|linear endomorphism]], so we instead write $\mathrm{End}(V)$. Every $\varphi \in \mathrm{End}(V)$ is of the form $\varphi: V \to V$, which allows for arbitrary [[Mathematical Functions#Function Composition|composition]] $(\circ)$ of [[Mathematical Functions|functions]] in $\mathrm{End}(V)$.

This *induces* a natural [[Algebra (over a field)#Associative Algebra|associative algebra]] over <u>field</u> $F$ - called the ***endomorphism algebra*** $\mathrm{End}(V)$ of <u>vector space</u> $V$. This algebra uses $(\circ)$ as <u>multiplication</u>, [[Linear Map#Zero Map|zero map]] $0_{V}: V \to V$ as the <u>additive identity</u>, and [[Linear Map#Identity Map|identity map]] $I_{V}: V \to V$ as the <u>multiplicative identity</u>. It has the following properties for every $\varphi,\psi, f \in \mathrm{End}(V)$ and $\alpha,\beta \in F$:
$$\large
\begin{align}
\textbf{Scalar compatibility:} &&& \alpha \varphi \circ \beta \psi = (\alpha \beta)(\varphi \circ \psi) \\
\textbf{Additive identity:} &&& \varphi + 0_{V} = 0_{V} + \varphi = \varphi \\
\textbf{Multiplicative identity:} &&& \varphi \circ I_{V} = I_{V} \circ \varphi = \varphi \\
\textbf{Distributivity:} &&& \begin{aligned}
& (\varphi + \psi) \circ f = \varphi \circ f + \psi \circ f \\
& f \circ (\varphi + \psi) = f \circ \varphi + f \circ \psi
\end{aligned} \\
\textbf{Associativity:} &&& (\varphi \circ \psi) \circ f =  \varphi \circ (\psi \circ f)
\end{align}
$$
This <u>algebra</u> extends the *flexibility* of algebraic manipulations to all <u>linear endomorphisms</u>.

## General Linear Group of a Vector Space: $\operatorname{GL}(V)$,$\mathrm{Aut}(V)$
We can take any [[#Endomorphism Algebra of a Vector Space $ mathrm{End}(V)$|endomorphism algebra]] $\operatorname{End}(V)$ of [[Vector Space|vector space]] $V$ over [[Field|field]] $F$ and select the subset $\mathrm{Aut}(V) \subseteq \mathrm{End}(V)$ of [[Mathematical Functions#Bijective Functions|bijections]] within it. This subset *(of all [[Linear Map#Linear Automorphism|automorphisms]] on $V$)* <u>breaks</u> the $(+)$ operator so $\mathrm{Aut}(V)$ is reduced to a [[Group|multiplicative group]] under $(\circ)$ with [[Linear Map#Identity Map|identity map]] $I_{V}: V \to V$ as the <u>multiplicative identity</u>. It is called the ***general linear group*** $\operatorname{GL}(V)$ of $V$. By [[Transformation Matrix#Relating General Linear Groups of Vector Spaces and Matrices $ operatorname{GL}(V)$,$ operatorname{GL}_{n}(F)$|relating general linear groups to matrices]], we open the door for applying very useful algorithms like [[Gaussian Elimination|Gaussian elimination]] onto arbitrary <u>vector spaces</u>.

One way you can visualise as the group of all possible ways to rigidly transform a space around the origin $\mathbf{0}_{V}$, without tearing, gluing, or otherwise losing parts of the space, ensuring that every transformation is perfectly reversible.

# Standard Coordinate Representation
Let $V$ be a [[#Dimension of Vector Space|finite-dimensional]] <u>vector space</u> over [[Field|field]] $F$. By selecting an [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|ordered basis]] $B = (\mathbf{b}_{1}, \mathbf{b}_{2}, \dots, \mathbf{b}_{n})$, we can obtain the [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|coordinate vector]] $[\mathbf{v}]_{B} \in F^n$ relative to <u>basis</u> $B$, for each vector $\mathbf{v} \in V$. The complete set of all such <u>coordinate vectors</u> is the ***standard coordinate representation*** of <u>vector space</u> $V$ relative to <u>basis</u> $B$, and it is denoted by $V_{B}$
$$\large V_{B} \  \triangleq \ \ \{ \ [\mathbf{v}]_{B} \ |\ \mathbf{v} \in V \ \}$$
Notice that $V_{B}$ is *essentially* just [[#Coordinate Vector Space|coordinate vector space]] $F^n$, but *renamed* to reflect the *connection* to <u>vector space</u> $V$ and <u>basis</u> $B$. This is *precisely* why $F^n$ *(relative to [[Basis of Vector Space#Standard Basis|standard basis]] $E$)* is called the <u>canonical</u> $n$-dimensional <u>vector space</u> over <u>field</u> $F$.

We know that [[Linear Map#Correspondence with Ordered Basis|ordered bases define isomorphisms]] so $V \cong_{EB} F^n$ is the <u>unique isomorphism</u> defined by $B$ and $E$, and is the one that *connects* $V$ and $V_{B}$. We define the application of $V \cong_{EB} F^n$ ***left-to-right*** as $\sub{\eta}{\overset{EB}{\longleftarrow}}: V \to F^n$, and ***right-to-left*** as $\sub{\eta}{\overset{BE}{\longleftarrow}}: F^n \to V$
$$\large
\begin{align}
\sub{\eta}{\overset{EB}{\longleftarrow}}(\mathbf{v}) \ \ &\triangleq \ \ [\mathbf{v}]_{B} = (\alpha_{1}, \dots, \alpha_{n}) \\
\sub{\eta}{\overset{BE}{\longleftarrow}}(\alpha_{1}, \dots, \alpha_{n}) \ \ &\triangleq \ \ \alpha_{1} \mathbf{b}_{1} + \alpha_{2} \mathbf{b}_{2} + \dots + \alpha_{n} \mathbf{b}_{n} = \mathbf{v}
\end{align}
$$
These <u>isomorphisms</u> *mechanise* the correspondence between <u>vectors</u> $\mathbf{v} \in V$ and $[\mathbf{v}]_{B} \in V_{B}$. The $\eta$-notation is inspired by [natural transformations](https://en.wikipedia.org/wiki/Natural_transformation) but there doesn't exist any *standard* notation for this correspondence.

## Coordinate Representation of Linear Maps
Just like $V$, let $W$ be a ***another*** [[#Dimension of Vector Space|finite-dimensional]] <u>vector space</u> over [[Field|field]] $F$, and let $D = (\mathbf{d}_{1}, \mathbf{d}_{2},\dots, \mathbf{d}_{m})$ be an [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|ordered basis]] of $W$. We can now describe the ***standard coordinate representation*** $\varphi_{DB}: V_{B} \to W_{D}$ for all [[Linear Map|linear maps]] $\varphi: V \to W$.

The first thing to note is that $W$ is $m$-dimensional, so to avoid confusion we clarify $V \cong_{\sub{E}{n}B} F^n$ and $W \cong_{\sub{E}{m}B} F^m$ where $E_{n},E_{m}$ are the [[Basis of Vector Space#Standard Basis|standard bases]] of dimensions $n,m$ respectively. With respect to $\sub{\eta}{\overset{\sub{E}{n}B}{\longleftarrow}}: V \to F^n$, $\sub{\eta}{\overset{B\sub{E}{n}}{\longleftarrow}}: F^n \to V$, $\sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}}: W \to F^m$, $\sub{\eta}{\overset{D\sub{E}{m}}{\longleftarrow}}: F^m \to W$ the definition of $\varphi_{DB}: V_{B} \to W_{D}$ is
$$\large
\varphi_{DB} \left( [\mathbf{v}]_{B} \right) \ \ \ \ \triangleq \ \ \ \ 
\sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}} \circ \varphi \circ \sub{\eta}{\overset{B\sub{E}{n}}{\longleftarrow}}\left( [\mathbf{v}]_{B} \right) \
= \ \sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}}\left( \varphi\left( \sub{\eta}{\overset{B\sub{E}{n}}{\longleftarrow}}\left( [\mathbf{v}]_{B} \right) \right) \right) 
$$
Conceptually $\varphi_{DB}$ is a <u>linear map</u> that *emulates* (on [[#Coordinate Vector Space|coordinate spaces]] $F^n$ into $F^m$) the behaviour of $\varphi$ on <u>vector spaces</u> $V$ into $W$. If you had $\mathbf{v} \in V$ and $\mathbf{w} \in W$ for which $\varphi(\mathbf{v})=\mathbf{w}$, then you would also have $\varphi_{DB}([\mathbf{v}]_{B}) = [\mathbf{w}]_{D}$. For clarity, we can <u>expand</u> it explicitly: for every $1\leq j \leq n$ we have <u>basis vector</u> $\mathbf{b}_{j} \in B$ getting mapped to $\varphi(\mathbf{b}_{j}) = \alpha_{1j} \mathbf{d}_{1} + \dots + \alpha_{mj} \mathbf{d}_{m} = \sum_{i=1}^m a_{ij} \mathbf{d}_i$. With this, we can expand $\varphi_{DB}: V_{B} \to W_{D}$ by using the [[Basis of Vector Space#Standard Basis|standard basis]] $\sub{E}{m} = (\mathbf{e}_{1},\dots,\mathbf{e}_{m})$ of $F^n$
$$\large 
\begin{align}
\varphi_{DB}(v_{1}, \dots, v_{n})
&= \sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}}\left( \varphi\left( \sub{\eta}{\overset{B\sub{E}{n}}{\longleftarrow}}\left( v_{1}, \dots, v_{n} \right) \right) \right)
= \sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}}\left( \varphi(v_{1} \mathbf{b}_{1} + \dots + v_{n} \mathbf{b}_{n}) \right) \\ 
&= \sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}} \left( v_{1} \varphi(\mathbf{b}_{1}) + \dots + v_{n} \varphi(\mathbf{b}_{n}) \right)
= v_{1} \cdot \sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}}(\varphi(\mathbf{b}_{1})) + \dots + v_{n} \cdot \sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}}(\varphi(\mathbf{b}_{n})) \\
&= \sum_{j=1}^n v_{j} \cdot \sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}}(\varphi(\mathbf{b}_{j}))
= \sum_{j=1}^n v_{j} \cdot \sub{\eta}{\overset{\sub{E}{m}D}{\longleftarrow}} \left( \sum_{i=1}^m a_{ij} \mathbf{d}_i \right)
= \sum_{j=1}^n v_{j} \sum_{i=1}^m a_{ij} \mathbf{e}_i \\
&= \sum_{j=1}^n \sum_{i=1}^m v_{j} a_{ij} \mathbf{e}_i \\
\end{align}
$$
Another way to think about it is in terms of [[Linear Map#Correspondence with Ordered Basis|ordered bases defining unique isomorphisms]]
1. ***One*** <u>ordered basis</u> $B$ [[Linear Map#Correspondence with Ordered Basis|defines the isomorphism]] $V \cong_{EB} F^n$, a ***second*** <u>ordered basis</u> $D$ defines $W \cong_{\sub{E}{m}B} F^m$
2. Together, they define ***two more*** [[Linear Map#Linear Isomorphism|linear isomorphisms]] $\mathcal{L}(V,W) \cong_{DB} \mathcal{L}(F^n, F^m)$ and $\mathcal{L}(W,V) \cong_{BD} \mathcal{L}(F^m, F^n)$
where $\mathcal{L}(V,W) \cong_{DB} \mathcal{L}(F^n, F^m)$ and $\mathcal{L}(W,V) \cong_{BD} \mathcal{L}(F^m, F^n)$ are [[Function Space#Space of Linear Transformations $ mathcal{L}(V,W)$,$ mathrm{Hom}(V,W)$|spaces of linear transformations]] from $V$ and $W$ *into* $F^n$ and $F^m$.

## Composing Coordinate Representations of Linear Maps
Notice also that *because* [[Linear Map#Composition of Linear Maps|linear maps are composable]], so are these [[#Coordinate Representation of Linear Maps|coordinate representations]]. If you have <u>vector spaces</u> $V,W,X$ *(over the same [[Field|field]])*, [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|ordered bases]] $B,C,D$, and [[Linear Map|linear maps]] $\phi:V\to W,\psi:W \to X$ - respectively, then you would have
$$\large (\psi \circ \phi)_{DB} = \psi_{DC} \circ \phi_{CB}$$
so you get this *(very convenient)* [[Relations on Sets#Transitive|transitivity]]-like property of the subscript notation.

# Examples
## Coordinate Vector Space
For some $n > 0$ and [[Field|field]] $F$, the set of [[Tuple|tuples]] $F^n$ is called the ***coordinate vector space*** $F^n$ over <u>field</u> $F$ with $\dim(F^n)=n$; when $n=1$ it is just <u>field</u> $F$ as a <u>vector space</u> over itself. Each vector $\mathbf{v} \in F^n$ is called a ***coordinate*** and is an $n$-tuple who's components are in $F$.

Each ***coordinate vector space*** $F^n$ is <u>by default</u> relative to [[Basis of Vector Space#Standard Basis|standard basis]] $E = (\mathbf{e}_{1}, \mathbf{e}_{2}, \dots, \mathbf{e}_{n})$ - all manipulations on $F^n$ naturally behave as if you had explicitly specified them relative to <u>standard basis</u> $E$.

The ***canonical*** $n$-dimensional <u>vector space</u> over <u>field</u> $F$ - ***is*** $F^n$ *(relative to <u>standard basis</u> $E$)*. This is because all other such <u>vector spaces</u> are [[Linear Map#Linear Isomorphism|isomorphic]] to it. The most common kind of ***coordinate vector space*** is that of $\mathbb{R}^n$, which is often called a [real coordinate space](https://en.wikipedia.org/wiki/Real_coordinate_space).
