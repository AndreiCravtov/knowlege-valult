A coordinate vector is a representation of a [[Vector Space|vector]] as a list of numbers, which describes the coordinate in terms of a particular [[Basis of Vector Space#Ordered Basis|ordered basis]]. If we are dealing with [[Vector Space#Coordinate Vector Space|coordinate vector spaces]] under their [[Basis of Vector Space#Standard Basis|standard basis]], then any *vector* **is it's own** *coordinate vector*.

# Formal Definition
Let $V$ be a [[Vector Space|vector space]] over $F$, and let $\mathcal{B} = \{ \pmb{\hat{b}}_{1}, \pmb{\hat{b}}_{2}, \dots, \pmb{\hat{b}}_{n} \}$ be it's [[Basis of Vector Space#Ordered Basis|ordered basis]]. This means that for every $\pmb v \in V$, there exists some $\alpha_{1},\alpha_{2},\dots,\alpha_{n}\in F$ so that: $$\pmb v = \alpha_{1}\pmb{\hat{b}}_{1} + \alpha_{2}\pmb{\hat{b}}_{2} + \dots + \alpha_{n}\pmb{\hat{b}}_{n}$$So the ***coordinate vector*** of $\pmb v$ relative to $\mathcal{B}$ is the $n$-tuple: $$[\pmb v]_{\mathcal{B}} = (\alpha_{1},\alpha_{2},\dots,\alpha_{n})$$where each of the $\alpha_{1},\alpha_{2},\dots,\alpha_{n})$ are called the ***coordinates*** of $\pmb v$. We can also represent them as [[Row and Column Vectors|row or column vectors]] if we want, so 
$$
\begin{align}
&[\pmb v]_{\mathcal{B}} = \begin{bmatrix} \alpha_{1} \\ \vdots \\ \alpha_{n} \end{bmatrix} \\
\text{And} \ \ & [\pmb v]_{\mathcal{B}}^T = \begin{bmatrix} \alpha_{1} \ \ \alpha_{2} \ \ \dots \ \ \alpha_{n} \end{bmatrix}
\end{align}
$$
Where $[\pmb v]_{\mathcal{B}}^T$ is the [[Transpose|transpose]] of the [[Matrix|matrix]] $[\pmb v]_{\mathcal{B}}$.