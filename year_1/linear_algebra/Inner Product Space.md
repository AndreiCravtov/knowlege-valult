An ***inner product space*** is a [[Real Numbers|real]] or [[Complex Numbers|complex]] [[Vector Space|vector space]], together with a [[Mathematical Functions|function]] called the ***inner product***. The *inner product* is used to define intuitive geometric notions, such as lengths, angles, and orthogonality of vectors.

# Formal Definition
$F$ is a [[Field|field]] that is either $\mathbb{R}$ or $\mathbb{C}$. Given a [[Vector Space|vector space]] $V$ over $F$, it becomes an ***inner product space*** when equipped with a function $\langle \cdot , \cdot \rangle: V^2 \to F$, called the ***inner product***, such that it satisfies these three properties for all $\pmb u, \pmb v, \pmb w \in V$ and $a,b \in F$:
- **Conjugate symmetry:** $\langle \pmb u, \pmb v\rangle = \overline{\langle \pmb v , \pmb u \rangle}$. If $F = \mathbb{R}$, then *conjugate symmetry* is just *symmetry*.
- **Linearity in the first argument:** $\langle a \pmb u + b \pmb v, \pmb w \rangle = a \langle \pmb u, \pmb w \rangle + b \langle \pmb v, \pmb w \rangle$.
- **Positive-definiteness:** $\pmb v \ne \pmb 0 \implies \langle \pmb v, \pmb v \rangle > 0$.
In the above $\overline{a}$ is the [[Complex Numbers|complex conjugate]] of scalar $a$, and $\pmb 0 \in V$ is the zero vector.

The following basic properties follow almost immediately from the definition of inner product:
 - $\langle \pmb 0, \pmb v \rangle = \langle \pmb v, \pmb 0 \rangle = 0$.
 - $\langle \pmb v, \pmb v \rangle \geq 0$ and it is [[Real Numbers|real]].
 - $\langle \pmb v, \pmb v \rangle = 0 \iff \pmb v = \pmb 0$.
 - $\langle \pmb u , a \pmb v + b \pmb w \rangle = \overline{a} \langle \pmb u, \pmb v \rangle + \overline {b} \langle \pmb u, \pmb w \rangle$.
 - $\langle \pmb u + \pmb v, \pmb u + \pmb v \rangle = \langle \pmb u, \pmb u \rangle + 2Re(\langle \pmb u, \pmb v \rangle) + \langle \pmb v, \pmb v \rangle$, where $Re$ denotes the [[Complex Numbers|real part]] of it's argument.
	 - If $F = \mathbb{R}$, then this becomes $\langle \pmb u + \pmb v, \pmb u + \pmb v \rangle = \langle \pmb u, \pmb u \rangle + 2\langle \pmb u, \pmb v \rangle + \langle \pmb v, \pmb v \rangle$.

Every inner product space induces a [[Normed Vector Space|norm]], called its ***canonical Norm***, that is defined by $$\lvert \lvert \pmb v \rvert \rvert = \sqrt{ \langle \pmb v, \pmb v \rangle }$$With this norm, every inner product space becomes a [[Normed Vector Space|Normed vector space]]. Using this *Norm*, the [[Normed Vector Space#Induced Metric|Norm induced metric]] induces the formula for a [[Metric Space|metric]] $$d(\pmb u, \pmb v) = \sqrt{ \langle \pmb v - \pmb u, \pmb v - \pmb u \rangle }$$With this, every *inner product space* can also be a [[Metric Space|metric space]].

# Examples
## Hilbert Space
![[Hilbert Space#Formal Definition]]

## Euclidean Vector Space
The ***Euclidean vector space*** $\overrightarrow{E}$, is a *real* [[Hilbert Space#Finite Dimensional Inner Product Space|finite-dimensional inner product space]]. It is is common to write the inner product of $\overrightarrow{E}$ as $\pmb u \cdot \pmb v$, because the study of every $\overrightarrow{E}$ can be reduced to the study of the study of of $\mathbb{R}^n$ under the [dot product](https://en.wikipedia.org/wiki/Dot_product#Coordinate_definition). The [[Normed Vector Space|norm]] induced by this inner product , is referred to as the ***Euclidean norm***; the [[Normed Vector Space#Induced Metric|induced metric]] of the *Euclidean norm* is called the ***Euclidean metric***.