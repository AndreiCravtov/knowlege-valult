

A <u>square matrix</u> $\mathbf{A} \in F^{n \times n}$ is called an ***invertable matrix*** if there exists a <u>square matrix</u> $\mathbf{A}^{-1} \in F^{n \times n}$ for which
$$\large \mathbf{A} \mathbf{A}^{-1} = \mathbf{A}^{-1} \mathbf{A} = \sub{\mathbf{I}}{n}$$
where $\mathbf{A}^{-1} \in F^{n \times n}$ is called the ***multiplicative inverse*** of $\mathbf{A} \in F^{n \times n}$. The set of all ***invertable matrices*** of $n$, equipped with <u>matrix multiplication</u> $(\cdot)$, forms a [[Group|multiplicative group]] who's [[Ring#Formal Definition|multiplicative identity]] is $\sub{\mathbf{I}}{n}$ and is called the [[General Linear Group|general linear group]] $\sub{GL}{n}(F)$.



## Invertible Matrix Theorem
The ***invertible matrix theorem*** states that the following statements *(as they apply to $\mathbf{A} \in F^{n \times n}$)* are equivalent
- $\mathbf{A}$ is ***inverible*** under [[Matrix#Matrix Multiplication|matrix multiplication]], i.e. there exists a $\mathbf{A}^{-1} \in F^{n \times n}$ for which $\mathbf{A} \mathbf{A}^{-1} = \mathbf{A}^{-1} \mathbf{A} = \sub{\mathbf{I}}{n}$
- The [[Linear Map|linear map]] that $\mathbf{A}$ [[Transformation Matrix|represents]] is either [[Mathematical Functions#Function Inverses|left or right invertible]]
- $\mathbf{A}^{\mathrm{T}}$ is ***inverible*** if you can it into $\sub{\mathbf{I}}{n}$ by a sequence of [[Elementary Row and Column Operations|elementary row and column operations]]
- $\mathbf{A}^{\mathrm{T}}$ has $n$ [[Row Echelon Form#Pivot Position|pivot positions]]
- $\mathbf{A}^{\mathrm{T}}$ has full rank, i.e. $rank(\mathbf{A}) = n$


- **A** has full [rank](https://en.wikipedia.org/wiki/Rank_(linear_algebra) "Rank (linear algebra)"): rank **A** = _n_.
- **A** has a trivial [kernel](https://en.wikipedia.org/wiki/Kernel_(linear_algebra) "Kernel (linear algebra)"): ker(**A**) = {**0**}.
- The linear transformation mapping **x** to **Ax** is bijective; that is, the equation **Ax** = **b** has exactly one solution for each **b** in Kn. (Here, "bijective" can equivalently be replaced with "[injective](https://en.wikipedia.org/wiki/Injective "Injective")" or "[surjective](https://en.wikipedia.org/wiki/Surjective "Surjective")")
- The columns of **A** form a [basis](https://en.wikipedia.org/wiki/Basis_of_a_vector_space "Basis of a vector space") of Kn. (In this statement, "basis" can equivalently be replaced with either "linearly independent set" or "spanning set")
- The rows of **A** form a basis of Kn. (Similarly, here, "basis" can equivalently be replaced with either "linearly independent set" or "spanning set")
- The [determinant](https://en.wikipedia.org/wiki/Determinant "Determinant") of **A** is nonzero: det **A** ≠ 0. (In general, a square matrix over a [commutative ring](https://en.wikipedia.org/wiki/Commutative_ring "Commutative ring") is invertible if and only if its determinant is a [unit](https://en.wikipedia.org/wiki/Unit_(ring_theory) "Unit (ring theory)") (i.e. multiplicatively invertible element) of that ring.
- The number 0 is not an [eigenvalue](https://en.wikipedia.org/wiki/Eigenvalue "Eigenvalue") of **A**. (More generally, a number 𝜆![{\displaystyle \lambda }](https://wikimedia.org/api/rest_v1/media/math/render/svg/b43d0ea3c9c025af1be9128e62a18fa74bedda2a) is an eigenvalue of **A** iff the matrix 𝐴−𝜆𝐼![{\displaystyle \mathbf {A} -\lambda \mathbf {I} }](https://wikimedia.org/api/rest_v1/media/math/render/svg/29a7c87b40de792974d3929d9d1f470e0671caa4) is singular, where **I** is the identity matrix.)
- The matrix **A** can be expressed as a finite product of [elementary matrices](https://en.wikipedia.org/wiki/Elementary_matrix "Elementary matrix").




## General Linear Group of Invertible Matrices: $\operatorname{GL}_{n}(F)$
#todio
https://en.wikipedia.org/wiki/General_linear_group#General_linear_group_of_a_vector_space