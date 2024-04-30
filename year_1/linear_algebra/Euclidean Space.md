***Euclidean spaces*** are mathematical objects intended to represent physical space. They have the intuitive notion of ***points*** in space, as-well as ***translations*** between these points. The most common types are the 2D and 3D spaces, representing a flat sheet of paper and our physical world, respectively.

There is essentially *only one* **Euclidean space** for each dimension $n$, and it is called the [[#Standard Euclidean Space|standard Euclidean space]]. All other *Euclidean spaces* (of the same dimension) are isomorphic to it. We represent this *Euclidean space* of dimension $n$ as $\mathbb{E}^n$. 

# Formal Definition
A ***Euclidean space*** (also called ***Euclidean affine space***), is an [[Affine Space|affine space]] space $E$ - who's associated vector space $\overrightarrow{E}$ is a [[Inner Product Space#Euclidean Vector Space|Euclidean vector space]]. Because $E$ is an affine space, that means for any $P,Q \in E$ there exists a unique $\vec{v} \in \overrightarrow{E}$ for which $P + \vec{v} = Q$. This $\vec{v}$ is denoted as $\overrightarrow{PQ}$.  As with any affine space, the dimension of $E$ is the [[Vector Space#Dimension of Vector Space|dimension of]] $\overrightarrow{E}$.


The Euclidean space $E$ inherits $\overrightarrow{E}\text{ 's}$ [[Inner Product Space|inner product]], and it's *canonical* induced [[Normed Vector Space|Norm]] $$\lvert \lvert \vec{x} \rvert  \rvert = \sqrt{ \vec{x} \cdot \vec{x} }$$and using it, we can define the ***Euclidean [[Metric Space|metric]]*** on $E$ as such$$d(P,Q) = \lvert \lvert \overrightarrow{PQ} \rvert  \rvert$$making every $E$ also becomes a [[Metric Space|metric space]].

## Orthogonality
We define $\vec{u}$ and $\vec{v}$ to be orthogonal when $\vec{u} \cdot \vec{v} = 0$; for two line segments $AB$ and $BC$ which share a point $B \in E$, they form a *right angle* if $\overrightarrow{AB} \cdot \overrightarrow{BC} = 0$. If $AB$ and $BC$ form a *right angle*, then we can derive the *Pythagorean theorem*:
$$
\begin{align}
\lvert AC \rvert^2 &= \lvert \lvert \overrightarrow{AC} \rvert  \rvert^2 = \overrightarrow{AC} \cdot \overrightarrow{AC} 
= (\overrightarrow{AB} + \overrightarrow{BC}) \cdot (\overrightarrow{AB} + \overrightarrow{BC}) \\ 
&= \overrightarrow{AB} \cdot \overrightarrow{AB} + \overrightarrow{BC} \cdot \overrightarrow{BC} - 2\overrightarrow{AB} \cdot \overrightarrow{BC} \\
&= \overrightarrow{AB} \cdot \overrightarrow{AB} + \overrightarrow{BC} \cdot \overrightarrow{BC}
= \lvert \lvert \overrightarrow{AB} \rvert  \rvert^2 + \lvert \lvert \overrightarrow{BC} \rvert  \rvert^2 \\
&= \lvert AB \rvert^2 + \lvert BC \rvert^2
\end{align}
$$

## Cartesian Coordinates
Every [[Inner Product Space#Euclidean Vector Space|Euclidean vector space]] $\overrightarrow{E}$ has has some [[Basis of Vector Space#Orthonormal Basis|orthonormal basis]] $\mathcal{B} = \{ \pmb{\hat{e}}_{1}, \pmb{\hat{e}}_{n}, \dots, \pmb{\hat{e}}_{n} \}$, and together with some point $O \in E$, we can create a ***Cartesian frame*** $(O, \pmb{\hat{e}}_{1}, \pmb{\hat{e}}_{n}, \dots, \pmb{\hat{e}}_{n})$ - where $O$ represents the ***origin***, with which we can define the ***Cartesian coordinates*** for *vectors* and *points* as follows:
 - *Cartesian coordinates* of any $\vec{v} \in \overrightarrow{E}$ is just the [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|coordinate vector]] $[\vec{v}]_{\mathcal{B}}$.
 - *Cartesian coordinates* of any $P \in E$ is just the [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|coordinate vector]] $[\overrightarrow{OP}]_{\mathcal{B}}$.

# Examples
## Euclidean Vector Spaces
For any [[Vector Space|vector space]], the *vector addition* acts [[Group Action#Free Group Action|freely]] and [[Group Action#Transitive Group Action|transitively]] on the vector space itself. Thus any [[Inner Product Space#Euclidean Vector Space|Euclidean vector space]] $\overrightarrow{E}$ can be viewed as a *Euclidean affine space* that has itself as the associated vector space. The standard origin $O \in \overrightarrow{E}$ that is used for [[#Cartesian Coordinates|Cartesian frames]] is the **zero vector** of $\overrightarrow{E}$ - so this means $O = \pmb {\vec{0}}$.

### Standard Euclidean Space
The *real* [[Vector Space#Coordinate Vector Space|coordinate space]] $\mathbb{R}^n$, equipped with the [dot product](https://en.wikipedia.org/wiki/Dot_product#Coordinate_definition) (with respect to the [[Basis of Vector Space#Standard Basis|standard basis]]), is a [[#Euclidean Vector Spaces]], and therefore it can also be a *Euclidean affine space* - called the ***standard Euclidean space***. The standard origin $O \in \mathbb{R}^n$ is the **zero vector** of $\mathbb{R}^n$ $$O = \underbrace{(0, 0, \dots, 0)}_{n}$$meaning that the *point* $P \in \mathbb{R}^n$ equals to the *translation vector* $\overrightarrow{OP} \in\mathbb{R}^n$; this makes calculations incredibly convenient. It is ***standard*** because every other *Euclidean affine space* is *isomorphic* to it. Meaning that for ***any*** *Euclidean affine space* $E$, we can pick a [[#Cartesian Coordinates|Cartesian frame]] of $E$, and it will define an isomorphism to $\mathbb{R}^n$. We write $\mathbb{E}^n$ to represent the ***standard Euclidean space*** $\mathbb{R}^n$.