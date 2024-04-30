#linear-algebra #matrix

An $m \times n$ ***matrix*** is rectangular grid arranged in $m$ <u>rows</u> and $n$ <u>columns</u>, and values in that grid are called <u>elements</u> or <u>entries</u>.
$$\Large
\textcolor{Green}{\begin{matrix} \\ 1 \\ 2 \\ \vdots \\ m\end{matrix}}
\begin{gathered}
\textcolor{Red}{\begin{matrix}1 && 2 && \dots && n \end{matrix}} \\
\begin{bmatrix}
a_{\textcolor{Green}{1}\textcolor{Red}{1}} & a_{\textcolor{Green}{1}\textcolor{Red}{2}} & \dots & a_{\textcolor{Green}{1}\textcolor{Red}{n}} \\
a_{\textcolor{Green}{2}\textcolor{Red}{1}} & a_{\textcolor{Green}{2}\textcolor{Red}{2}} & \dots & a_{\textcolor{Green}{2}\textcolor{Red}{n}} \\
\vdots & \vdots & \ddots & \vdots \\
a_{\textcolor{Green}{m}\textcolor{Red}{1}} & a_{\textcolor{Green}{m}\textcolor{Red}{2}} & \dots & a_{\textcolor{Green}{m}\textcolor{Red}{n}} \\
\end{bmatrix}
\end{gathered}
$$
For $m \times n$ ***matrix*** $\mathbf{M}$, the <u>entry</u> in the $i$-th <u>row</u> and $j$-th *column* is denoted by $\sub{\mathbf{M}}{i,j}$, $\mathbf{M}[i,j]$ or $\mathbf{M}(i,j)$ - alternatively with lowercase $\sub{a}{i,j}$. The [[#Row and Column Vectors|row vector]] corresponding to the $i$-th <u>row</u> is denoted by $\sub{\mathbf{M}}{i,\star}$ or $\mathbf{M}[i,\star]$, and the [[#Row and Column Vectors|column vector]] corresponding to the $j$-th <u>column</u> is denoted by $\sub{\mathbf{M}}{\star,j}$ or $\mathbf{M}[\star,j]$. Most commonly, ***matrices*** contain values from algebraic structures like [[Field|fields]] or [[Ring|rings]], but really could be any mathematical object.

# Formal Definition
For some $m,n > 0$, define $I =  \{ 1,2, \dots, m \}$ and $J = \{ 1,2, \dots, n \}$. Thus, an $m \times n$ ***matrix*** is an [[Indexed Family|indexed family]] $\mathbf{M}: I \times J \to S$ with $m$ <u>rows</u> and $n$ <u>columns</u>, and its <u>entries</u> from set $S$. The $i$-th row and $j$-th column is denoted by by $\sub{\mathbf{M}}{i,j}$, $\mathbf{M}[i,j]$, or $\mathbf{M}(i,j)$ - with $\mathbf{M}(i,j)$ being the interpretation of $\mathbf{M}$ as a [[Mathematical Functions|function]]; alternatively with lowercase $\sub{a}{i,j}$.

The [[#Row and Column Vectors|row vector]] corresponding to the $i$-th <u>row</u> is denoted by $\sub{\mathbf{M}}{i,\star}$ or $\mathbf{M}[i,\star]$, and the [[#Row and Column Vectors|column vector]] corresponding to the $j$-th <u>column</u> is denoted by $\sub{\mathbf{M}}{\star,j}$ or $\mathbf{M}[\star,j]$. The set of all $m \times n$ ***matrices*** with <u>entries</u> from set $S$ is denoted by $S^{m \times n}$ or $\sub{\mathcal{M}}{m \times n}(S)$.

This definition is the most general possible definition, and the vast majority of the time, there are additional requirements.

# Zero Matrix and Identity Matrix
Let $S$ be *some algebraic structure* equipped with ***addition*** *(e.g. an [[Group#Additive group|additive group]])*, thus there will be some <u>additive identity</u> $0 \in S$. The $m \times n$ <u>matrix</u> whose <u>entries</u> are *all* $0$ is called the ***zero matrix*** $\sub{\mathbf{0}}{m,n}$, and it is the ***additive identity*** of [[#Addition and Subtraction|matrix addition]]. Therefore the set of <u>matrices</u> $S^{m \times n}$ equipped with [[#Addition and Subtraction|matrix addition]], forms a [[Group#Additive group|group]] called an ***additive matrix group***.

Suppose $S$ is *also* equipped with ***multiplication*** *(e.g. a [[Ring|ring]] or [[Field|field]])*, thus there will be some <u>multiplicative identity</u> $1 \in S$. The ***identity matrix*** $\sub{\mathbf{I}}{n}$ of <u>order</u> $n$, is the $n \times n$ <u>matrix</u> who's are $0$ except for the [[#Main Diagonal|main diagonal entries]] which are all $1$. The ***identity matrix*** $\sub{\mathbf{I}}{n}$ is the ***neutral element*** of [[Matrix#Matrix Multiplication|matrix multiplication]], and therfore for any <u>matrix</u> $\mathbf{A} \in S^{m \times n}$ we have
$$\large \sub{\mathbf{I}}{m} \mathbf{A} = \mathbf{A} \sub{\mathbf{I}}{n} = \mathbf{A}$$
If we only consider the set of <u>matrices</u> $S^{n \times n}$, equipping it with <u>matrix multiplication</u> forms a [[Ring|ring]], *with $\sub{\mathbf{I}}{n}$ as the [[Ring#Formal Definition|multiplicative identity]]*, called a [matrix ring](https://en.wikipedia.org/wiki/Matrix_ring).

# Row and Column Vectors
A ***column vector*** $\mathbf{x}$ with $m$ elements, is a $m \times 1$ <u>matrix</u> consisting of a single <u>column</u> of $m$ entries. Similarly, a ***row vector*** $\mathbf{a}$ with $n$ elements, is a $1 \times n$ <u>matrix</u> consisting of a single <u>row</u> of $n$ entries. Their general forms are 
$$\large
\mathbf{x} = \begin{bmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{m}
\end{bmatrix} \ \ \ \
\mathbf{a} =\begin{bmatrix}
a_{1} & a_{2} & \dots & a_{n}
\end{bmatrix}
$$
Hence, $\mathbf{x}^\mathrm{T}$ is a ***row vector*** and $\mathbf{a}^\mathrm{T}$ is a ***column vector***. The set of <u>rows</u> and <u>columns</u> of some $m \times n$ matrix can be interpreted as $m$ lots of ***row vectors*** with $n$ elements, and $n$ lots of ***column vectors*** with $m$ elements - respectively.

Over a [[Field|field]] $F$, the set of ***column vectors*** $F^{m \times 1}$ is [[Homomorphism (algebraic)#Isomorphism|isomorphic]] to the [[Vector Space#Coordinate Vector Space|coordinate vector space]] $F^m$. Likewise, the set of ***row vectors*** $F^{1 \times n}$ is [[Homomorphism (algebraic)#Isomorphism|isomorphic]] to the [[Vector Space#Coordinate Vector Space|coordinate vector space]] $F^n$. This *(rather obvious)* duality is used to construct and analyse [[Transformation Matrix#Row and Column Spaces|row and column spaces]].

# Matrix Operations
## General Operations
### Transpose
The ***transpose*** of an $m\times n$ matrix $\mathbf{A}$ is the $n \times m$ matrix $\mathbf{A}^{\mathrm{T}}$ formed by turning <u>rows</u> in to <u>columns</u> and vice versa:
$$\large \sub{(\mathbf{A}^\mathrm{T})}{i,j} = \sub{\mathbf{A}}{j,i}$$
The ***transpose*** of ***transpose*** is the original matrix, i.e. $(\mathbf{A}^{\mathrm{T}})^{\mathrm{T}} = A$. The ***transpose*** is compatible with [[#Scalar Multiplication|scalar multiplication]], [[#Addition and Subtraction|addition, and subtraction]], as expressed by $(c\mathbf{A})^{\mathrm{T}} = (c\mathbf{A})^{\mathrm{T}}$, $(\mathbf{A} + \mathbf{B})^\mathrm{T} = \mathbf{A}^\mathrm{T} + \mathbf{B}^\mathrm{T}$ and $(\mathbf{A} - \mathbf{B})^\mathrm{T} = \mathbf{A}^\mathrm{T} - \mathbf{B}^\mathrm{T}$.

### Augmentation
The ***augmented matrix*** $(\mathbf{A}|\mathbf{B})$ is the $m \times (\alpha + \beta)$ <u>matrix</u> that results from ***concatenating*** the <u>columns</u> of $m \times \alpha$ <u>matrix</u> $\mathbf{A}$ with the <u>columns</u> of $m \times \beta$ <u>matrix</u> $\mathbf{B}$. The <u>columns</u> aren't *actually* separated, but ***augmented matrices*** are most commonly denoted as
$$\large
(\mathbf{A}|\mathbf{B}) = \left[\begin{array}{cccc|cccc}  
a_{11} & a_{12} & \dots & a_{1 \alpha} & b_{11} & b_{12} & \dots & b_{1 \beta} \\
a_{21} & a_{22} & \dots & a_{2 \alpha} & b_{21} & b_{22} & \dots & b_{2 \beta} \\
\vdots & \vdots & \ddots & \vdots & \vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \dots & a_{m \alpha} & b_{m1} & b_{m2} & \dots & b_{m \beta} \\
\end{array}\right]
$$
This is usually done for the purpose of performing the same [[Elementary Row and Column Operations|row operations]] on the ***augmented matrix*** $(\mathbf{A}|\mathbf{B})$ as is done on the original one $\mathbf{A}$ when solving a system of linear equations by [[Gaussian Elimination|Gaussian elimination]].

### Submatrix
A ***submatrix*** of a <u>matrix</u> is the <u>matrix</u> obtained by deleting any collection of rows and/or columns. For example, from the following $3\times 4$ <u>matrix</u>, we can construct a $2 \times 3$ ***submatrix*** by removing <u>row</u> $3$ and <u>column</u> $2$
$$\large
\begin{bmatrix}
1 & \textcolor{Red}{2} & 3 & 4 \\
5 & \textcolor{Red}{6} & 7 & 8 \\
\textcolor{Red}{3} & \textcolor{Red}{10} & \textcolor{Red}{11} & \textcolor{Red}{12}
\end{bmatrix} \to
\begin{bmatrix}
1 & 3 & 4 \\
5 & 7 & 8
\end{bmatrix}
$$
For example, the [[Minor (matrix)|minors]] and [[Minor (matrix)#Cofactor of a Matrix|cofactors]] of a matrix are found by computing the [[Square Matrix (algebraic)#Determinant|determinant]] of certain ***submatrices***.

## Algebraic Operations
### Addition and Subtraction
Let $S$ be *some algebraic structure* equipped with ***addition*** *(e.g. an [[Group#Additive group|additive group]])*. For all $m \times n$ <u>matrices</u> over $S$, we can define ***matrix addition*** $(+): S^{m \times n} \to S^{m \times n}$ <u>entrywise</u>, as
$$\large \sub{(\mathbf{A} + \mathbf{B})}{i,j} = \sub{\mathbf{A}}{i,j} + \sub{\mathbf{B}}{i,j}$$
for any two matrices $\mathbf{A},\mathbf{B}$. If $S$ is also equipped with ***additive inverses***, then for all $m \times n$ <u>matrices</u> over $S$, we can define ***matrix subtraction*** $(-): S^{m \times n} \to S^{m \times n}$ <u>entrywise</u>, as
$$\large \sub{(\mathbf{A} - \mathbf{B})}{i,j} = \sub{\mathbf{A}}{i,j} - \sub{\mathbf{B}}{i,j}$$
for any two matrices $\mathbf{A},\mathbf{B}$.

### Scalar Multiplication
For some <u>scalar</u> $c$, $m \times n$ <u>matrix</u> $\mathbf{A}$ and <u>entries</u> supporting ***scalar multiplication*** with it, the ***product*** $c \mathbf{A}$ is the $m \times n$ <u>matrix</u> computed by ***multiplying*** every <u>entry</u> of $\mathbf{A}$ by $c$
$$\large \sub{(c\mathbf{A})}{i,j} = c \cdot \sub{\mathbf{A}}{i,j}$$

### Matrix Multiplication
For <u>entries</u> supporting <u>addition</u> and <u>scalar multiplication</u>, and for $m \times n$ <u>matrix</u> $\mathbf{A}$ and $n \times p$ <u>matrix</u> $\mathbf{B}$, their ***matrix multiplication*** is the $m \times p$ <u>matrix</u> $\mathbf{A} \mathbf{B}$. The <u>entries</u> of $\mathbf{A} \mathbf{B}$ are given by the [dot product](https://en.wikipedia.org/wiki/Dot_product#Coordinate_definition) of the corresponding <u>row</u> of $\mathbf{A}$ and <u>column</u> of $\mathbf{B}$
$$\large
\sub{(\mathbf{A} \mathbf{B})}{i,j} 
= \sub{\mathbf{A}}{i,\star} \cdot \sub{\mathbf{B}}{\star,j} 
= \sum_{k=1}^n \sub{a}{i,k} \sub{b}{k,j}
= \sub{a}{i,1} \sub{b}{1,j} + \sub{a}{i,2} \sub{b}{2,j} + \dots + \sub{a}{i,n} \sub{b}{n,j}
$$
***Matrix multiplication*** satisfies:
- ***Associativity:*** $(\mathbf{A} \mathbf{B}) \mathbf{C} = \mathbf{A} (\mathbf{B} \mathbf{C})$
- ***Left Distributivity:*** $\mathbf{C}(\mathbf{A} + \mathbf{B}) = \mathbf{C}\mathbf{A} + \mathbf{C}\mathbf{B}$
- ***Right Distributivity:*** $(\mathbf{A} + \mathbf{B})\mathbf{C} = \mathbf{A}\mathbf{C} + \mathbf{B}\mathbf{C}$
However its <u>not necessarily</u> $\mathbf{A}\mathbf{B} = \mathbf{B}\mathbf{A}$, i.e. not ***commutative***.

# Properties
## Main Diagonal
For an $m \times n$ ***matrix*** $\mathbf{A}$, the <u>entries</u> $\sub{\mathbf{A}}{i,i}$ ($1 \leq i \leq n$) are called the ***main diagonal*** of $\mathbf{A}$. They lie on the imaginary line which runs *diagonally* from the <u>top left corner</u> down.
$$\large
\begin{bmatrix}
\textcolor{Red}{a_{11}} & a_{12} & \dots & a_{1n} \\
a_{21} & \textcolor{Red}{a_{22}} & \dots & a_{2n} \\
\vdots & \vdots & \textcolor{Red}{\ddots} & \vdots \\
a_{n1} & a_{n2} & \dots & \textcolor{Red}{a_{nn}} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn} \\
\end{bmatrix} \ \ \ \
\begin{bmatrix}
\textcolor{Red}{a_{11}} & a_{12} & \dots & a_{1m} & \dots & a_{1n} \\
a_{21} & \textcolor{Red}{a_{22}} & \dots & a_{2m} & \dots & a_{2n} \\
\vdots & \vdots & \textcolor{Red}{\ddots} & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \dots & \textcolor{Red}{a_{mm}} & \dots & a_{mn} \\
\end{bmatrix}
$$
It could look like the <u>left</u> or <u>right</u> visualisation, depending on if $m>m$ or $m<n$.

## Representing Linear Transformations
For any $m \times n$ <u>matrix</u> $\mathbf{A}$ over [[Field|field]] $F$ we can define the [[Linear Map|linear map]] $\sub{\mathcal{T}}{\mathbf{A}}: F^n \to F^m$ from [[Vector Space#Coordinate Vector Space|coordinate vector spaces]] $F^n$ to $F^m$ as
$$\large
\sub{\mathcal{T}}{\mathbf{A}}(\vec{x}) = \mathbf{A} \vec{x}
$$
where we *interpret* the <u>vectors</u> $\vec{x} \in F^n$ as [[Matrix#Row and Column Vectors|column vectors]] and thus apply [[#Matrix Multiplication|matrix multiplication]]. The [[Transformation Matrix|transformation matrix]] of $\sub{\mathcal{T}}{\mathbf{A}}$ is $\mathbf{A}$, and $\sub{\mathcal{T}}{\mathbf{A}}$ is the ***transformation*** that $\mathbf{A}$ ***represents***. The *correspondence* between such <u>matrices</u> and <u>linear maps</u> is therefore ***unique*** - one determines the other.

If we *instead* have a <u>linear map</u> $\varphi: F^n \to F^m$ we can calculate its ***transformation matrix*** $\sub{\mathbf{T}}{\varphi} \in F^{m \times n}$ by using the [[Basis of Vector Space#Standard Basis|standard basis]] $E_{n} = (\mathbf{e}_{1}, \dots, \mathbf{e}_{n})$ to define $\sub{\mathbf{T}}{\varphi}$ point-wise, column-wise, or in total - for $1 \leq i \leq m$ and $1\leq j \leq n$
$$\large
\begin{align}
\sub{\mathbf{T}}{\varphi}[i,j] \ \ = \ \ \varphi(\mathbf{e}_{j})_{i} &&
\sub{\mathbf{T}}{\varphi}[\star,j] \ \ = \ \ \varphi(\mathbf{e}_{j}) &&
\sub{\mathbf{T}}{\varphi} = [\varphi(\mathbf{e}_{1}),\dots,\varphi(\mathbf{e}_{n})]
\end{align}
$$
where $\varphi(\mathbf{e}_{j})_{i}$ is the $i$-th component of $\varphi(\mathbf{e}_{j}) \in F^m$. Each column of $\large \sub{\mathbf{T}}{\varphi}$ represents *where* each <u>basis vector</u> in $E_{n}$ is mapped to, under $\varphi$.

We can - [[Vector Space#Coordinate Representation of Linear Maps|by picking bases]] - use matrices to [[Transformation Matrix|represent any linear map]] not just between $F^n$ and $F^m$.

## Matrix Rank
#todo
rank definitions:
[dimension] of the [vector space](https://en.wikipedia.org/wiki/Vector_space "Vector space") generated (or [spanned](https://en.wikipedia.org/wiki/Linear_span "Linear span")) by its columns. (The **column rank** of A is the [dimension](https://en.wikipedia.org/wiki/Dimension_(linear_algebra) "Dimension (linear algebra)") of the [column space](https://en.wikipedia.org/wiki/Column_space "Column space") of A, while the **row rank** of A is the dimension of the [row space](https://en.wikipedia.org/wiki/Row_space "Row space") of A.)
maximal number of [linearly independent](https://en.wikipedia.org/wiki/Linearly_independent) columns of A
identical to the dimension of the vector space spanned by its rows
a measure of the "[nondegenerateness](https://en.wikipedia.org/wiki/Degenerate_form "Degenerate form")" of the [system of linear equations](https://en.wikipedia.org/wiki/System_of_linear_equations "System of linear equations") and [linear transformation](https://en.wikipedia.org/wiki/Linear_transformation "Linear transformation") encoded by A.

$\mathrm{rank}(A) \ or \  \mathrm{rk}(A)$

A matrix is said to have **full rank** if its rank equals the largest possible for a matrix of the same dimensions, which is the lesser of the number of rows and columns
A matrix is said to be **rank-deficient** if it does not have full rank.
The **rank deficiency** of a matrix is the difference between the lesser of the number of rows and columns, and the rank.

..
The rank of a [linear map](https://en.wikipedia.org/wiki/Linear_map "Linear map") or operator Φ![{\displaystyle \Phi }](https://wikimedia.org/api/rest_v1/media/math/render/svg/aed80a2011a3912b028ba32a52dfa57165455f24) is defined as the dimension of its [image](https://en.wikipedia.org/wiki/Image_(mathematics) "Image (mathematics)"):[[5]](https://en.wikipedia.org/wiki/Rank_(linear_algebra)#cite_note-6)[[6]](https://en.wikipedia.org/wiki/Rank_(linear_algebra)#cite_note-7)[[7]](https://en.wikipedia.org/wiki/Rank_(linear_algebra)#cite_note-8)[[8]](https://en.wikipedia.org/wiki/Rank_(linear_algebra)#cite_note-9)

rank⁡(Φ):=dim⁡(img⁡(Φ))

![{\displaystyle \operatorname {rank} (\Phi ):=\dim(\operatorname {img} (\Phi ))}](https://wikimedia.org/api/rest_v1/media/math/render/svg/990037eac62b307fbe458dd6c310c14cd1c28412)

where dim![{\displaystyle \dim }](https://wikimedia.org/api/rest_v1/media/math/render/svg/66115c83c4bb19068adb45849f0f596647c18f2e) is the dimension of a vector space, and img![{\displaystyle \operatorname {img} }](https://wikimedia.org/api/rest_v1/media/math/render/svg/01a70438fbe53caf48e8d69a30dea74a86c9d38b) is the image of a map.
...
<--Rank from row echelon forms

~~
rank = dimension of image
Given the matrix 𝐴![{\displaystyle A}](https://wikimedia.org/api/rest_v1/media/math/render/svg/7daff47fa58cdfd29dc333def748ff5fa4c923e3), there is an associated [linear mapping](https://en.wikipedia.org/wiki/Linear_mapping "Linear mapping")

𝑓:𝐹𝑛→𝐹𝑚

![{\displaystyle f:F^{n}\to F^{m}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/f7da3da06774be21a2d52dc94131694e5f0196de)

defined by

𝑓(𝑥)=𝐴𝑥.

![{\displaystyle f(x)=Ax.}](https://wikimedia.org/api/rest_v1/media/math/render/svg/7d502b2884080511e480d76e22817571de3ca833)

The rank of 𝐴![{\displaystyle A}](https://wikimedia.org/api/rest_v1/media/math/render/svg/7daff47fa58cdfd29dc333def748ff5fa4c923e3) is the dimension of the image of 𝑓![{\displaystyle f}](https://wikimedia.org/api/rest_v1/media/math/render/svg/132e57acb643253e7810ee9702d9581f159a1c61). This definition has the advantage that it can be applied to any linear map without need for a specific matrix.

---











The **column rank** of A is the [dimension](https://en.wikipedia.org/wiki/Dimension_(linear_algebra) "Dimension (linear algebra)") of the [column space](https://en.wikipedia.org/wiki/Column_space "Column space") of A, while the **row rank** of A is the dimension of the [row space](https://en.wikipedia.org/wiki/Row_space "Row space") of A.

A fundamental result in linear algebra is that the column rank and the row rank are always equal. (Three proofs of this result are given in [§ Proofs that column rank = row rank](https://en.wikipedia.org/wiki/Rank_(linear_algebra)#Proofs_that_column_rank_=_row_rank), below.) This number (i.e., the number of linearly independent rows or columns) is simply called the **rank** of A.

A matrix is said to have **full rank** if its rank equals the largest possible for a matrix of the same dimensions, which is the lesser of the number of rows and columns. A matrix is said to be **rank-deficient** if it does not have full rank. The **rank deficiency** of a matrix is the difference between the lesser of the number of rows and columns, and the rank.

The rank of a [linear map](https://en.wikipedia.org/wiki/Linear_map "Linear map") or operator Φ![{\displaystyle \Phi }](https://wikimedia.org/api/rest_v1/media/math/render/svg/aed80a2011a3912b028ba32a52dfa57165455f24) is defined as the dimension of its image

rank⁡(Φ):=dim⁡(img⁡(Φ))

![{\displaystyle \operatorname {rank} (\Phi ):=\dim(\operatorname {img} (\Phi ))}](https://wikimedia.org/api/rest_v1/media/math/render/svg/990037eac62b307fbe458dd6c310c14cd1c28412)

where dim![{\displaystyle \dim }](https://wikimedia.org/api/rest_v1/media/math/render/svg/66115c83c4bb19068adb45849f0f596647c18f2e) is the dimension of a vector space, and img![{\displaystyle \operatorname {img} }](https://wikimedia.org/api/rest_v1/media/math/render/svg/01a70438fbe53caf48e8d69a30dea74a86c9d38b) is the image of a map.

