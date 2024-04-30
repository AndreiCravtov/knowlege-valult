#linear-algebra 

A ***multilinear map*** is a [[Mathematical Functions#Multivariate Function Syntax|multivariate function]] from and to [[Vector Space|vector spaces]] *(over the same [[Field|field]])* that is also [[Linear Map|linear]] ***separately*** in each variable. A ***multilinear map*** with $k$ variables is called a ***$k$-linear map***.

# Formal Definition
Let $V_{1},\dots,V_{n}$ and $W$ be [[Vector Space|vector spaces]] over [[Field|field]] $F$, and the [[Mathematical Functions#Multivariate Function Syntax|function]] $f: V_{1} \times \dots \times V_{n} \to W$. If *(for each of it's variables)* you fix <u>all but one</u> variable and the result is a [[Linear Map|linear map]], then $f$ is a ***multilinear map***. More formally, for every $1 \leq i \leq n$ we have
$$\large
\begin{left}
\ \ \ \ \forall (c_{1}, \dots, c_{n}) \in V_{1} \times \dots \times V_{n}: \ \ \ \ \ \ \ \
V_{i} \to W; \ \mathbf{v}_{i} \mapsto f(c_{1},\dots, \mathbf{v}_{i},\dots,c_{n}) \
\text{is linear}
\end{left}
$$
One way to visualise this is to imagine [perpendicular](https://en.wikipedia.org/wiki/Perpendicular#Lines_in_three_dimensions) <u>vectors</u> - its like when one of these vectors is scaled by some factor while the other remains unchanged. A ***multilinear map*** with $k$ variables is called a ***$k$-linear map***, and if $W=F$ then it is a $k$[[Linear, Bilinear, and Multilinear Forms|-linear form]],

# Special Types of Multilinear Maps
## Linear Map
The most trivial case of <u>multilinear maps</u> are [[Linear Map|linear maps]] or $1$<u>-linear maps</u>. When the [[Mathematical Functions#Domains, co-domains, ranges|domain]] of the <u>linear map</u> is its [[Field|field]] of scalars, then you get a well-studied <u>special case</u> called a [[Linear, Bilinear, and Multilinear Forms|linear form]].

## Bilinear Map
A $2$<u>-linear map</u> $B: V \times W \to X$ *(with $V,W,X$ over [[Field|field]] $F$)* is most often called a ***bilinear map***, and satisfies *(by definition)* the following properties for every $\lambda \in F$ and $\mathbf{v}, \mathbf{v}' \in V$ and $\mathbf{w}, \mathbf{w}' \in W$ 
$$\large
\begin{align}
\textbf{Scalar multiplication:} && B(\lambda \mathbf{v}, \mathbf{w}) = B(\mathbf{v}, \lambda \mathbf{w}) &= \lambda B(\mathbf{v}, \mathbf{w}) \\ 
\textbf{Left vector addition:} && B(\mathbf{v} + \mathbf{v}', \mathbf{w}) &= B(\mathbf{v}, \mathbf{w}) + B(\mathbf{v}', \mathbf{w}) \\ 
\textbf{Right vector addition:} && B(\mathbf{v}, \mathbf{w} + \mathbf{w}') &= B(\mathbf{v}, \mathbf{w}) + B(\mathbf{v}', \mathbf{w}')
\end{align} \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \
$$
If $\mathbf{v} = \mathbf{0}_{V}$ or $\mathbf{w} = \mathbf{0}_{W}$ then $B(\mathbf{v},\mathbf{w}) = \mathbf{0}_{X}$. When $V=W$ and $X=F$, then you get a well-studied <u>special case</u> called a [[Linear, Bilinear, and Multilinear Forms|bilinear form]].

### Symmetric Bilinear Map
When $V=W$ and $B(\mathbf{v},\mathbf{w}) = B(\mathbf{w},\mathbf{v})$ for all $\mathbf{v}, \mathbf{w} \in V$, then we call $B$ a ***symmetric bilinear map***.