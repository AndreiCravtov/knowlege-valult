#linear-algebra 

A ***function space*** is a [[Vector Space|vector space]] who's <u>vectors</u> are *all* [[Mathematical Functions|functions]] from $X$ into $Y$ - for some [[Set Theory|sets]] $X$ and $Y$ called its <u>fixed points</u>. Most often it is the set of ***all*** such functions, and $Y$ is *also* a <u>vector space</u> *(while $X$ is any set)* because there is a [[#Natural Function Space Structure|natural structure]] given by point-wise <u>vector addition</u> and <u>scalar multiplication</u>; unless *explicitly* specified otherwise [[#Natural Function Space Structure|natural structure]] is assumed for <u>vector space</u> [[Mathematical Functions#Domains, co-domains, ranges|co-domains]].

# Formal Definition
For any [[Set Theory|sets]] $X,Y$ and [[Field|field]] $F$, some set of functions from $X$ to $Y$ - $\pmb{f}_{X \to Y}$ - can be equipped with $(+):\pmb{f}_{X \to Y} \times \pmb{f}_{X \to Y} \to \pmb{f}_{X \to Y}$ and $(\cdot): F \times \pmb{f}_{X \to Y} \to \pmb{f}_{X \to Y}$ such that the satisfy the [[#Formal Definition|vector space axioms]], making $\pmb{f}_{X \to Y}$ a <u>vector space</u> over $F$ called a ***function space***.

By imposing <u>additional structure</u> on $\pmb{f}_{X \to Y}$, you are essentially defining a [[Linear Subspace|linear subspace]] of $\pmb{f}_{X \to Y}$. For instance, the set of [[Mathematical Functions#Bijective Functions|bijective functions]] $X \leftrightarrow Y$ from $X$ to $Y$ *(such that they still obey the <u>vector space axioms</u>)* is a ***function subspace*** of the [[Mathematical Functions#Function type notation|set of all functions]] $Y^X$ *(from $X$ to $Y$)*.

Most of the time $Y$ is a [[Vector Space|vector space]] so, unless *explicitly* specified otherwise, the [[#Natural Function Space Structure|natural vector space structure]] is <u>assumed</u> for ***function space*** $Y^X$.

# Natural Function Space Structure
For some [[Vector Space|vector space]] $V$ over $F$, we can pick ***any*** set $X$ to define the [[Mathematical Functions#Function type notation|set of all functions]] $V^X$ *(from $X$ to $V$)* which induces the ***natural*** <u>vector space structure</u> $(+):V^X \times V^X \to V^X$ and $(\cdot): F \times V^X \to V^X$ defined ***point-wise*** as: for every $f,g: X \to V$, and $\lambda \in F$, and $x \in X$ we have
$$\large
\begin{align}
(f + g)(x) &= f(x) + g(x) \\
(\lambda \cdot f)(x) &= \lambda \cdot f(x) 
\end{align}
$$
creating the <u>function space</u> $V^X$ over $F$ ***with natural function space structure*** - the <u>assumed</u> structure unless *explicitly* specified otherwise.

***NOTE:*** this only works for the set of ***all*** functions, subsets of functions might not have enough structure to satisfy the vector space axioms.

# Common Types of Function Space
Although the [[#Natural Function Space Structure|above]] template is <u>powerful</u> and <u>flexible</u>, it is nice to explicitly notate some useful types of functions.

## Space of Linear Transformations: $\mathcal{L}(V,W)$,$\mathrm{Hom}(V,W)$
The set $\mathcal{L}(V,W)$ or $\mathrm{Hom}(V,W)$, of ***all*** [[Linear Map|linear maps]] *(or [[Homomorphism (algebraic)|homomorphisms]])* between [[Vector Space|vector spaces]] $V$ and $W$ *(over some [[Field|field]] $F$)* is a [[Linear Subspace|linear subspace]] of the <u>function space</u> of every [[Mathematical Functions|map]] from $V$ into $W$. 

If $V$ and $W$ are [[Vector Space#Dimension of Vector Space|finite dimensional]] then so is $\mathcal{L}(V,W)$, namely $\dim \mathcal{L}(V,W) = \dim V \cdot \dim W$. When $W=F$, i.e. [[Linear, Bilinear, and Multilinear Forms|linear forms]], we get the the <u>function space</u> $\mathrm{Hom}(V,F)$ - from $V$ into $F$, called $V$'s [[Dual Space (algebraic)|dual space]] $V^*$.

### Endomorphism Algebra: $\mathrm{End}(V)$
When we specifically have $\mathcal{L}(V,V)$, then every $\varphi \in \mathcal{L}(V,V)$ is a [[Linear Map#Linear Endomorphism|linear endomorphism]]. This enables us to use [[Mathematical Functions#Function Composition|function composition]] to add [[Vector Space#Endomorphism Algebra of a Vector Space $ mathrm{End}(V)$|add more structure to it naturally]] with the result being called the ***endomorphism algebra*** $\mathrm{End}(V)$ on $V$.

## Space of $k$-Linear Transformations: $\mathcal{L}(V_{1},\dots,V_{k};W)$
The set $\mathcal{L}(V_{1},\dots,V_{k};W)$ of all [[Bilinear and Multilinear Maps|multilinear maps]] with $k$ variables, from [[Vector Space|vector spaces]] $V_{1},\dots,V_{k}$ into $W$ *(over some [[Field|field]] $F$)* is a [[Linear Subspace|linear subspace]] of the <u>function space</u> of every [[Mathematical Functions#Multivariate Function Syntax|multivariate map]] from $V_{1},\dots,V_{k}$ into $W$. 

If $V_{1},\dots,V_{k}$ and $W$ are [[Vector Space#Dimension of Vector Space|finite dimensional]] then so is $\mathcal{L}(V_{1},\dots,V_{k};W)$, namely $\dim \mathcal{L}(V_{1},\dots,V_{k};W) = {\large \prod_{i=1}^k} \dim V_i \cdot \dim W$. 

When $V = V_{1} = V_{2} = \dots = V_{k}$ and $W=F$, i.e. $k$[[Linear, Bilinear, and Multilinear Forms|-linear forms]], the <u>dimension</u> of this space is $(\dim V)^k$.

### Vector Space of (covariant) $k$-Tensors: $\mathcal{T}^k(V)$, $\mathcal{L}^k(V)$
When $V = V_{1} = V_{2} = \dots = V_{k}$ and $W=F$, i.e. $k$[[Linear, Bilinear, and Multilinear Forms|-linear forms]], ***and also*** $F=\mathbb{R}$, then a $k$[[Linear, Bilinear, and Multilinear Forms|-linear form]] on $V$ is called a ***(covariant) $k$-tensor*** and $\mathcal{L}(V^n;\mathbb{R})$ is called the [[Vector Space|vector space]] of such ***$k$-tensors***, denoted by $\mathcal{T}^k(V)$ or $\mathcal{L}^k(V)$.
