#linear-algebra

A *linear subspace* is [[Vector Space|vector space]] that is a subset of some *larger* vector space.

# Formal Definition
Given some [[Vector Space|vector space]] $V$ over a [[Field|field]] $F$, we call $W \subseteq V$ a ***linear subspace*** if, under the operations of $V$, $W$ is a vector space over $F$.

Every vector space $V$ is equipped with two **trivial subspaces**: $\{ \pmb 0 \} \subseteq V$ and $V \subseteq V$.

# Properties
## Orthogonal Compliment
Let $V$ be a [[Vector Space|vector space]] over [[Field|field]] $F$ equipped with [[Linear, Bilinear, and Multilinear Forms#Bilinear Form - Symmetric, Skew-Symmetric, Alternating, Reflexive|bilinear form]] $B: V \times V \to F$. If $B$ is <u>not</u> [[Linear, Bilinear, and Multilinear Forms#Bilinear Form - Symmetric, Skew-Symmetric, Alternating, Reflexive|reflexive]] we have to distinguish between [[Vector Space#Orthogonal Vectors and Functions|left-orthogonal/right-orthogonal]] cases. Then for any [[Linear Subspace|linear subspace]] $W \subseteq V$, define the ***left-orthogonal compliment*** $W^\perp$ to be
$$\large
W^\perp \ \ \triangleq \ \ \{ \ \mathbf{v} \in V \ | \ \mathbf{w} \in W \wedge B(\mathbf{v}, \mathbf{w}) = 0 \ \} 
$$
There is a corresponding definition of ***right-orthogonal complement***. If $B$ is [[Linear, Bilinear, and Multilinear Forms#Bilinear Form - Symmetric, Skew-Symmetric, Alternating, Reflexive|reflexive]] then we ***left*** and ***right*** agree.

Here are some key properties of $W$ and $W^\perp$:
- $W^\perp$ is a <u>linear subspace</u> of $V$
- $X \subseteq Y \implies X^\perp \supseteq Y^\perp$
- $W \subseteq (W^\perp)^\perp$
- If $B$ is [[Linear, Bilinear, and Multilinear Forms#Degenerate Bilinear Form|non-degenerate]] and $V$ is [[Vector Space#Dimension of Vector Space|finite dimensional]], then $\dim(W) + \dim(W^\perp) = \dim(V)$

