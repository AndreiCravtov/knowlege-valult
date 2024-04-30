#linear-algebra #matrix 

# Representing Linear Transformations
As [[Matrix#Representing Linear Transformations|discussed here]], we can use [[Matrix|matrices]] over field $F$ represent [[Linear Map|linear transformations]] between [[Vector Space#Coordinate Vector Space|coordinate spaces]]. Namely, for any $m \times n$ <u>matrix</u> $\mathbf{A}$ over [[Field|field]] $F$ we define the ***transformation that it represents*** as $\sub{\mathcal{T}}{\mathbf{A}}: F^n \to F^m; \ \vec{x} \mapsto \mathbf{A} \vec{x}$. Conversely, for any [[Linear Map|linear map]] $\varphi: F^n \to F^m$ we can calculate its ***transformation matrix*** $\sub{\mathbf{T}}{\varphi} \in F^{m \times n}$ by using the [[Basis of Vector Space#Standard Basis|standard basis]] $E_{n} = (\mathbf{e}_{1}, \dots, \mathbf{e}_{n})$ to define $\sub{\mathbf{T}}{\varphi}$ point-wise, column-wise, or in total - for $1 \leq i \leq m$ and $1\leq j \leq n$
$$\large
\begin{align}
\sub{\mathbf{T}}{\varphi}[i,j] \ \ = \ \ \varphi(\mathbf{e}_{j})_{i} &&
\sub{\mathbf{T}}{\varphi}[\star,j] \ \ = \ \ \varphi(\mathbf{e}_{j}) &&
\sub{\mathbf{T}}{\varphi} = [\varphi(\mathbf{e}_{1}),\dots,\varphi(\mathbf{e}_{n})]
\end{align}
$$
where $\varphi(\mathbf{e}_{j})_{i}$ is the $i$-th component of $\varphi(\mathbf{e}_{j}) \in F^m$. Each column of $\large \sub{\mathbf{T}}{\varphi}$ represents *where* each <u>basis vector</u> in $E_{n}$ is mapped to, under $\varphi$.

We can extend this to ***all*** [[Vector Space|vector spaces]] and <u>linear transformations</u> between them, by picking [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|ordered bases]] and finding the [[Vector Space#Coordinate Representation of Linear Maps|coordinate representation of those linear transformations]]. Consider two vector spaces $V,W$ over field $F$, with <u>ordered bases</u> $B = (\mathbf{b}_{1}, \mathbf{b}_{2},\dots, \mathbf{b}_{b})$ and $D = (\mathbf{d}_{1}, \mathbf{d}_{2},\dots, \mathbf{d}_{m})$ - respectively. Hence, for any <u>linear map</u> $\varphi: V \to W$ we can find its <u>coordinate representation</u> $\varphi_{DB}: V_{B} \to W_{D}$ relative to $B,D$. Recall that $V_{B},W_{D}$ are just $F^n,F^m$ but [[Vector Space#Standard Coordinate Representation|renamed to explicitly reflect the connection]], so that means $\varphi_{DB}$ should have a ***transformation matrix*** associated with it. Namely, it is $\varphi$'s ***transformation matrix*** $[\varphi]_{DB} \in F^{m \times n}$ relative to $B,D$.

More explicitly: for $1\leq j \leq n$ *each* <u>basis vector</u> $\mathbf{b}_{j} \in B$ is mapped to $\varphi(\mathbf{b}_{j}) = \alpha_{1j} \mathbf{d}_{1} + \dots + \alpha_{mj} \mathbf{d}_{m} = \sum_{i=1}^m a_{ij} \mathbf{d}_i$, and its [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|coordinate vector]] relative to $D$ is thus $(\alpha_{1j}, \dots, \alpha_{mj}) \in W_{D}$. With this, we can define $\varphi_{DB}: V_{B} \to W_{D}$ by using the [[Basis of Vector Space#Standard Basis|standard basis]] $\sub{E}{m} = (\mathbf{e}_{1},\dots,\mathbf{e}_{m})$ of $F^n$
$$\large 
\varphi_{DB}(v_{1}, \dots, v_{n})
= v_1 \left(\sum_{i=1}^m a_{i1} \mathbf{e}_i \right) + \dots + v_n \left(\sum_{i=1}^m a_{in} \mathbf{e}_i \right)
= \sum_{j=1}^n \sum_{i=1}^m v_{j} a_{ij} \mathbf{e}_i
$$
which allows us to demonstrate how $[\varphi]_{DB}$ can be computed point-wise, column-wise, or in total - for $1 \leq i \leq m$ and $1\leq j \leq n$
$$\large
\begin{align}
[\varphi]_{DB}(i,j) \ \ = \ \ a_{ij} &&
[\varphi]_{DB}(\star,j) \ \ = \ \ [\alpha_{1j}, \dots, \alpha_{mj}]^{\mathrm{T}} &&
[\varphi]_{DB}= 
\begin{bmatrix}
\begin{bmatrix} \alpha_{11} \\ \vdots \\ \alpha_{m1} \end{bmatrix}
,\dots,
\begin{bmatrix} \alpha_{1n} \\ \vdots \\ \alpha_{mn} \end{bmatrix}
\end{bmatrix}
\end{align}
$$

# Composing Transformation Matrices
Just how you can [[Vector Space#Composing Coordinate Representations of Linear Maps|compose the coordinate representations of linear maps]], so are their [[#Representing Linear Transformations|transformation matrices]]. If you have [[Vector Space|vector space]] $V,W,X$ *(over the same [[Field|field]])*, [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|ordered bases]] $B,C,D$, and [[Linear Map|linear maps]] $\varphi:V\to W,\psi:W \to X$ - respectively, then you would have
$$\large (\psi \circ \varphi)_{DB} = \psi_{DC} \circ \varphi_{CB}$$
so you get this *(very convenient)* [[Relations on Sets#Transitive|transitivity]]-like property of the subscript notation. Its the same for their ***transformation matrices*** $[\varphi]_{CB} \in F^{m \times n}$ and $[\psi]_{DC} \in F^{m \times n}$, i.e. $[\psi \circ \varphi]_{DB} = [\psi]_{DC} \cdot [\varphi]_{CB}$ where [[Mathematical Functions#Function Composition|composition]] corresponds to [[Matrix#Matrix Multiplication|matrix multiplication]].


# Change-of-Basis Matrix
Every [[Vector Space|vector space]] $V$ over [[Field|field]] $F$ will have its [[Linear Map#Identity Map|identity map]] $I: V \to V$. So for two [[Basis of Vector Space#Ordered Basis and Coordinate Vectors|ordered bases]] $B = (\mathbf{b}_{1}, \mathbf{b}_{2}, \dots, \mathbf{b}_{n})$, $D = (\mathbf{d}_{1}, \mathbf{d}_{2},\dots, \mathbf{d}_{n})$ of $V$, the [[#Coordinate Representation of Linear Maps|coordinate representations]] $I_{DB}$ and $I_{BD}$ are called [[Basis of Vector Space#Change-of-Basis Map|change-of-basis maps]] and turn [[#Coordinate Vector|coordinate vectors]] $[\mathbf{v}]_{B}$ into $[\mathbf{v}]_{D}$ and vice versa. As always, we can represent those as [[#Representing Linear Transformations|transformation matrices]] $[I]_{DB},[I]_{BD} \in F^{n \times n}$ called ***change-of-basis matrices***
$$\large
\begin{align}
[I]_{DB} &= [[\mathbf{b}_{1}]_{D}, \dots, [\mathbf{b}_{n}]_{D}] \\
[I]_{BD} &= [[\mathbf{d}_{1}]_{B}, \dots, [\mathbf{d}_{n}]_{B}]
\end{align}
$$
and so you can do $[\mathbf{v}]_{D} = [I]_{DB} [\mathbf{v}]_{B}$. From this its *pretty obvious* that $I_{DB} = (I_{DB})^{-1}$ and hence $[I]_{DB}[I]_{BD} = [I]_{BD}[I]_{DB} = \mathbf{I}_{n}$ where $\mathbf{I}_{n}$ is the [[Matrix#Zero Matrix and Identity Matrix|identity matrix]]. Notice how all ***change-of-basis*** maps are [[Invertible Matrix|invertible matrices]] on $F^{n \times n}$.

Consider two vector spaces $V,W$ over field $F$, with <u>ordered bases</u> $B$ and $D$ - respectively. Hence, for any <u>linear map</u> $\varphi: V \to W$ we can find its [[Transformation Matrix#Representing Linear Transformations|transformation matrix]] $[\varphi]_{DB}$ relative to $B,D$. Suppose you define new ordered bases $\tilde{B}$ and $\tilde{D}$ of $V$ and $W$ respectively, and now you want to turn $[\varphi]_{DB}$ into $[\varphi]_{\tilde{B}\tilde{D}}$. Using [[#Composing Transformation Matrices|composition of transformation matrices]] we can write
$$\large 
[\varphi]_{\tilde{B}\tilde{D}} 
= [I]_{\tilde{B}B} \cdot [\varphi]_{BD} \cdot [I]_{D\tilde{D}}
$$
![[Pasted image 20240430151543.png]]

## Change-of-Basis Matrix for Coordinate Vector Spaces
In the particular case of finding a transformation ***change-of-basis*** within $F^n$, there is an *easy* shortcut. You are given two <u>ordered bases</u> on <u>vector space</u> $F^n$
$$\large
\begin{align}
A = \left(
\begin{bmatrix} a_{11} \\ \vdots \\ a_{n1} \end{bmatrix}
,\dots,
\begin{bmatrix} a_{1n} \\ \vdots \\ a_{nn} \end{bmatrix}
\right) &&
B = \left(
\begin{bmatrix} b_{11} \\ \vdots \\ b_{n1} \end{bmatrix}
,\dots,
\begin{bmatrix} b_{1n} \\ \vdots \\ b_{nn} \end{bmatrix}
\right)
\end{align}
$$
well, guess what - those are not <u>bases</u>, but ***coordinate representations*** of those <u>bases</u>, relative to standard basis $E$, so instead what you have is $A = ([\mathbf{a}_{1}]_{E}, \dots, [\mathbf{a}_n]_{E})$ and $B = ([\mathbf{b}_{1}]_{E}, \dots, [\mathbf{b}_n]_{E})$ ***which by the definition above*** forms $[I]_{EB}$ and $[I]_{EA}$. Then, simply compute 
$$\large [I]_{BA} = ([I]_{EB})^{-1} \cdot [I]_{EA}$$
which is derived by using [[#Composing Transformation Matrices|composition of transformation matrices]] and $I_{BE} = (I_{EB})^{-1}$.

## Relating General Linear Groups of Vector Spaces and Matrices: $\operatorname{GL}(V)$,$\operatorname{GL}_{n}(F)$
#todo



## ranks correspondence
![[Pasted image 20240430121821.png]]



# Row and Column Spaces
The column or image space of A is defined to be ImA := ImfA. The kernel or null space of A is defined to be kerA := ker fA
For A = [a1 ,...,an] we obtain Im(fA) = {Ax : x ∈ R n } = {x1a1 + ... + xnan : x1 ,..., xn ∈ R} ⊂ R m , (1.75) i.e., ImA = ImfA is the span of the columns of A. Therefore, the column (image) space of A is a subspace of Rm, where m is the “height” of the matrix. • The kernel/null space kerA = ker(fA) is a subspace of Rn , where n is the “width” of the matrix, and is the set of all solutions x to the linear homogeneous equation system Ax = 0.




the image/span of liner map matrix thing. 


Matrices and matrix multiplication reveal their essential features when related to _linear transformations_, also known as _linear maps_. A real _m_-by-_n_ matrix **A** gives rise to a linear transformation **R**_n_ → **R**_m_ mapping each vector **x** in **R**_n_ to the (matrix) product **Ax**, which is a vector in **R**_m_. Conversely, each linear transformation _f_: **R**_n_ → **R**_m_ arises from a unique _m_-by-_n_ matrix **A**: explicitly, the (_i_, _j_)-entry of **A** is the _i_th coordinate of _f_(**e**_j_), where **e**_j_ = (0,...,0,1,0,...,0) is the [unit vector](https://en.wikipedia.org/wiki/Unit_vector "Unit vector") with 1 in the _j_th position and 0 elsewhere. The matrix **A** is said to represent the linear map _f_, and **A** is called the _transformation matrix_ of _f_.

For example, the 2×2 matrix

𝐴=[𝑎𝑐𝑏𝑑]![{\displaystyle \mathbf {A} ={\begin{bmatrix}a&c\\b&d\end{bmatrix}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/0996c87b9d5163ae1a5e132fd08eb0abced82042)

can be viewed as the transform of the [unit square](https://en.wikipedia.org/wiki/Unit_square "Unit square") into a [parallelogram](https://en.wikipedia.org/wiki/Parallelogram "Parallelogram") with vertices at (0, 0), (_a_, _b_), (_a_ + _c_, _b_ + _d_), and (_c_, _d_). The parallelogram pictured at the right is obtained by multiplying **A** with each of the column vectors [00],[10],[11]![{\displaystyle {\begin{bmatrix}0\\0\end{bmatrix}},{\begin{bmatrix}1\\0\end{bmatrix}},{\begin{bmatrix}1\\1\end{bmatrix}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ee78c2dd87473db52d51e244cefb9172eea1bb58), and [01]![{\displaystyle {\begin{bmatrix}0\\1\end{bmatrix}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/2b48db099856bd05394c31adef4678aa9a6f9bee) in turn. These vectors define the vertices of the unit square.

The following table shows several 2×2 real matrices with the associated linear maps of **R**2. The blue original is mapped to the green grid and shapes. The origin (0,0) is marked with a black point.

Under the [1-to-1 correspondence](https://en.wikipedia.org/wiki/Bijection "Bijection") between matrices and linear maps, matrix multiplication corresponds to [composition](https://en.wikipedia.org/wiki/Function_composition "Function composition") of maps:[[23]](https://en.wikipedia.org/wiki/Matrix_(mathematics)#cite_note-23) if a _k_-by-_m_ matrix **B** represents another linear map _g_: **R**_m_ → **R**_k_, then the composition _g_ ∘ _f_ is represented by **BA** since

(_g_ ∘ _f_)(**x**) = _g_(_f_(**x**)) = _g_(**Ax**) = **B**(**Ax**) = (**BA**)**x**.

The last equality follows from the above-mentioned associativity of matrix multiplication.

The [rank of a matrix](https://en.wikipedia.org/wiki/Rank_of_a_matrix "Rank of a matrix") **A** is the maximum number of [linearly independent](https://en.wikipedia.org/wiki/Linear_independence "Linear independence") row vectors of the matrix, which is the same as the maximum number of linearly independent column vectors.[[24]](https://en.wikipedia.org/wiki/Matrix_(mathematics)#cite_note-24) Equivalently it is the [dimension](https://en.wikipedia.org/wiki/Hamel_dimension "Hamel dimension") of the [image](https://en.wikipedia.org/wiki/Image_(mathematics) "Image (mathematics)") of the linear map represented by **A**.[[25]](https://en.wikipedia.org/wiki/Matrix_(mathematics)#cite_note-25) The [rank–nullity theorem](https://en.wikipedia.org/wiki/Rank%E2%80%93nullity_theorem "Rank–nullity theorem") states that the dimension of the [kernel](https://en.wikipedia.org/wiki/Kernel_(matrix) "Kernel (matrix)") of a matrix plus the rank equals the number of columns of the matrix.[[26]](https://en.wikipedia.org/wiki/Matrix_(mathematics)#cite_note-26)