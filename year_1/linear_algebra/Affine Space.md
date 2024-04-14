Conceptually, an affine space is what is left of a [[Vector Space|vector space]] when you forget which point is the origin. Vector spaces contain a **zero vector** (which acts as an origin). However, by pairing a vector space together with an *independent* set of points (while treating vectors as translations between those points) we lose the sense of what the origin should be; the **zero vector** becomes just another translation between points, rather than the origin.

# Formal Definition
Given some [[Vector Space|vector space]] $\vec{A}$, the ***affine space*** $A$, is a nonempty set $A$ equipped with a [[Group Action#Free Group Action|free]] and [[Group Action#Transitive Group Action|transitive]] [[Group Action|group action]] $(+)$ of $\vec{A}$ on $A$.

Explicitly, what these mean is that $(+): A \times \vec{A} \to A$ has the following properties:
- **Right identity:** $\forall a \in A, a + \pmb 0 = a$, where $\pmb 0$ is the zero vector in $\vec{A}$.
- **Associativity:** $\forall \pmb u, \pmb v \in \vec{A}, \forall a \in A, (a + \pmb u) + v = a + (\pmb u + \pmb v)$.
- **Free and transitive action:** For every $a \in A$, the mapping $\vec{A} \to A: \pmb v \to a + \pmb v$ is a [[Mathematical Functions#Bijective Functions|bijection]].
The above criteria describe $(+)$ as a [[Group Action#Right Group Action|right group action]], but since all [[Vector Space#Formal Definition|vector spaces]] are a [[Group#Additive group|additive]] [[Group#Abelian group|Abelian groups]], it means that [[Group Action#Formal Definition|it does't matter if it is right or left action]].

Elements of $A$ are called **points**. Elements of $\vec{A}$ are called **translations**. $\vec{A}$ is said to be the **associated vector space** of $A$. The properties of $(+)$ are such that for every $a,b \in A$, there exists exactly one $\pmb v \in \vec{A}$ such that $a + \pmb v = b$. The translation $\pmb v$ is denoted as $\overrightarrow{ab}$.

# Properties
## Dimension of Affine Space
The **dimension** of the affine space $A$ is the [[Vector Space#Dimension of Vector Space|dimension]] of it's associated vector space $\vec{A}$.