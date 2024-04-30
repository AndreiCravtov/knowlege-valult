#linear-algebra 

The *(algebraic)* ***square matrix*** of <u>order</u> $n$ is an $n \times n$ [[Matrix|matrix]] over some [[Field|field]]. It's distinguishing feature is that it has the same number of <u>rows</u> and <u>columns</u>. Any two ***square matrices*** of the same <u>order</u> can be [[Matrix#Addition and Subtraction - Zero Matrix and Additive Matrix Group|added]] and [[Matrix#Matrix Multiplication|multiplied]], and as such they are useful for developing rich *algebraic structures*.

# Main Diagonal and Antidiagonal
The ***main diagonal*** of ***square matrix*** $\mathbf{A}$ <u>order</u> $n$ is [[Matrix#Main Diagonal|just like all matrices]]: the <u>entries</u> $\sub{\mathbf{A}}{i,i}$ ($1 \leq i \leq n$)
$$\large
\begin{bmatrix}
\textcolor{Red}{a_{11}} & a_{12} & \dots & a_{1n} \\
a_{21} & \textcolor{Red}{a_{22}} & \dots & a_{2n} \\
\vdots & \vdots & \textcolor{Red}{\ddots} & \vdots \\
a_{n1} & a_{n2} & \dots & \textcolor{Red}{a_{nn}} \\
\end{bmatrix}
$$
But ***square matrices*** in particular can have ***antidiagonals*** or ***counterdiagonals***: the <u>entries</u> $\sub{\mathbf{A}}{i,j}$ ($1 \leq i,j \leq n$) for which $i + j = n - 1$
$$\large
\begin{bmatrix}
a_{11} & a_{12} & \dots & \textcolor{Green}{a_{1n}} \\
a_{21} & a_{22} & \textcolor{Green}{\dots} & a_{2n} \\
\vdots & \textcolor{Green}{\vdots} & \ddots & \vdots \\
\textcolor{Green}{a_{n1}} & a_{n2} & \dots & a_{nn} \\
\end{bmatrix}
$$
They lie on the imaginary line which runs from the <u>top right corner</u> to the <u>bottom left corner</u> of $\mathbf{A}$.




# Operations
## Trace
The ***trace*** of <u>square matrix</u> $\mathbf{A}$ <u>order</u> $n$ over [[Field|field]] $F$, is the sum of its [[#Main Diagonal and Antidiagonal|main diagonal]] elements. Namely, it is the [[Mathematical Functions|function]] $tr: F^{n \times n} \to F$ defined as
$$\large tr(\mathbf{A}) = \sum_{i=1}^n \sub{\mathbf{A}}{i,i}$$
While [[Matrix#Matrix Multiplication|matrix multiplication]] is <u>not</u> commutative, we always have $tr(\mathbf{A}\mathbf{B}) = tr(\mathbf{B \mathbf{A}})$ for any such <u>square matrices</u>. With respect to [[Matrix#Transpose|transpose]], we also always have $tr(\mathbf{A}) = tr(\mathbf{A}^{\mathrm{T}})$.

## Determinant
#todo

### Eigenvalues and Eigenvectors
#todo

# Induced Algebraic Structures
## Square Matrix Ring





#todo

