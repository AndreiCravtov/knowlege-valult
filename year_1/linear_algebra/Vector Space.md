A **vector space** is a [[Set Theory|set]] whose elements (called vectors) can be *added* and *scaled* by scalars. These scalars can be elements of any [[Field|field]], but its most commonly the [[Real Numbers|real numbers]].
![[Pasted image 20240121171146.png]]

# Formal Definition
A ***vector space*** over [[Field|field]] $F$ is a nonempty set $V$, equipped with *vector addition* $(+):V^2 \to V$, and *scalar multiplication* $(\cdot \cdot): F \times V \to V$, such that these [[Mathematical Functions|functions]] satisfy the following axioms for every $\pmb u,\pmb v, \pmb w \in V$, and $a,b \in F$:
$$
\begin{align}
\text{Associativity:} &&& \pmb u + (\pmb v + \pmb w) = (\pmb u+\pmb v)+\pmb w \\
\text{Commutativity:} &&& \pmb u + \pmb v = \pmb v + \pmb u \\
\text{Vector addition identity element:} &&& \exists \pmb 0 \in V [ \ \pmb v + \pmb 0 = \pmb v \ ] \\
\text{Inverse element:} &&& \exists \pmb{-v} \in V [\ \pmb v + \pmb {-v} = \pmb 0 \ ] \\
\text{Field and scalar multiplication composability:} &&& a(b \pmb v) = (ab) \pmb v \\ 
\text{Saclar multiplication identity element:} &&& 1 \pmb v = \pmb v, \ \text{where} \ 1 \ \text{is the multiplicative identity in} \ F \text{.} \\
\text{Distributivity:} &&& \begin{aligned}
& a(\pmb u + \pmb v) = a \pmb u + a \pmb v \\
& (a + b) \pmb v = a \pmb v + b \pmb v
\end{aligned}
\end{align}
$$
The elements of $V$ are called ***vectors**,* and the elements of $F$ are called ***scalars***. Every *vector space* is an [[Group#Additive group|additive]] [[Group#Abelian group|Abelian group]], because *vector addition* satisfies the [[Group#Formal Definition|group axioms]] and is *commutative*.

When the scalar [[Field|field]] is the [[Real Numbers|real numbers]], then the vector space is called a ***real vector space***; likewise for [[Complex Numbers|complex numbers]] it is called a ***complex vector space***. Those are the two most common cases.

# Properties
## Dimension of Vector Space
The dimension of a vector space $V$, is the [[Cardinality of Sets|cardinality]] of a [[Basis of Vector Space|basis]] of $V$.

## Linear Combination
$V$ is a vector space over field $F$. Given some vectors $\pmb{v_{1}},\pmb{v_{2}},\dots,\pmb{v_{n}} \in V$ and scalars $a_{1},a_{2},\dots,a_{n} \in F$, their ***linear combination*** is: $a_{1}\pmb{v_{1}} + a_{2}\pmb{v_{2}} + \dots + a_{n}\pmb{v_{n}}$. A ***trivial*** linear combination is one where all the scalar coefficients $a_{1},a_{2},\dots,a_{n} \in F$ are $0$.

## Linear Independence
$V$ is a vector space over field $F$. The vectors $\pmb{v_{1}},\pmb{v_{2}},\dots,\pmb{v_{n}} \in V$ are ***linearly independent*** if for all $a_{1},a_{2},\dots,a_{n} \in F$, $a_{1}\pmb{v_{1}} + a_{2}\pmb{v_{2}} + \dots + a_{n}\pmb{v_{n}} = \pmb 0$ is a [[#Linear Combination|trivial linear combination]], i.e. all the scalar coefficients $a_{1},a_{2},\dots,a_{n} \in F$ are $0$.

If there exists some $a_{1},a_{2},\dots,a_{n} \in F$, where $a_{1}\pmb{v_{1}} + a_{2}\pmb{v_{2}} + \dots + a_{n}\pmb{v_{n}} = \pmb 0$ is not a [[#Linear Combination|trivial linear combination]], then we say that $\pmb{v_{1}},\pmb{v_{2}},\dots,\pmb{v_{n}} \in V$ are ***linearly dependent***. The reason they are called *dependent*, is because at least one of those scalars is nonzero (i.e. $a_{1} \ne 0$). This means that at least one of those vectors can be expressed in terms of the other vectors, i.e. $$\pmb{v_{1}} = \frac{-a_{2}}{a_{1}}\pmb{v_{2}} + \dots + \frac{-a_{n}}{a_{1}}\pmb{v_{n}}$$and therefore the value of that one vector, depends on the value of the other vectors.

### Linearly Independent Sets
Given some set $B \subseteq V$, its called ***linearly independent*** if every [[Cardinality of Sets#Finite Sets|finite]] subset $\{ \pmb{v_{1}},\pmb{v_{2}},\dots,\pmb{v_{n}} \} \subseteq B$ is also *linearly independent*.

# Examples
## Coordinate Vector Space
The simplest way to construct a *vector space* $V$ over [[Field|field]] $F$, is the field $F$ itself. It is already equipped with addition and multiplication, which become the *vector addition* and *scalar multiplication* - respectively.

You can generalise this property using $n$-tuples, i.e. ***coordinates***. For some $n \in \mathbb{N}$, any set $\mathbb{F}^n$ is a **vector space** over the [[Field|field]] $\mathbb{F}$, called a ***coordinate vector space***. Each element (*vector*) of $\mathbb{F}^n$ is an $n$-tuple (*coordinate*), who's components are elements of $\mathbb{F}$. Once you have this structure, you can define *vector addition* and *scalar multiplication* as such: 
$$
\begin{align}
\text{For any} \ a \in F \ \text{and} \ (u_{1}, u_{2},& \dots, u_{n}) , (v_{1}, v_{2}, \dots, v_{n}) \in F^n \\ \\
(u_{1}, u_{2}, \dots, u_{n}) + (v_{1}, v_{2}, \dots, v_{n}) &= (u_{1} + v_{1}, u_{2} + v_{2}, \dots, u_{n} + v_{n}) \\
a(u_{1}, u_{2}, \dots, u_{n}) &= (au_{1}, au_{2}, \dots, au_{n})
\end{align}
$$

The most common kind of *coordinate vector space* is that of $\mathbb{R}^n$, which is often called a [real coordinate space](https://en.wikipedia.org/wiki/Real_coordinate_space).