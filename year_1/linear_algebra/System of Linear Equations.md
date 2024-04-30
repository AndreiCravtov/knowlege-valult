#linear-algebra

A ***system of linear equations*** is a collection of one of more ***linear equations*** involving the same ***unknowns***. For example,
$$\Large
\begin{cases}
3x + 2y - z = 1 \\
2x - 2y + 4z = -2 \\
-x + \frac{1}{2}y - z = 0
\end{cases}
$$
is a system of *three* equations with ***unknowns*** $x,y,z$. Solutions to a ***linear system*** is a collection of values that, *when substituted  for the unknowns*, <u>simultaneously</u> satisfy the equations in the system. In the example above, one solution would be $(x,y,z) = (1,-2,-2)$.

Many problems can be <u>formulated</u> as ***systems of linear equations***, and we can interpret such systems as various algebraic structures - giving us more flexibility and tools for solving such problems.

# General Form
A general system of $m$ linear equations with $n$ <u>unknowns</u> is written as
$$\large
\begin{cases}
a_{11}x_{1} + a_{12}x_{2} + \dots + a_{1n}x_{n} = b_{1} \\
a_{21}x_{1} + a_{22}x_{2} + \dots + a_{2n}x_{n} = b_{2} \\
\vdots \\
a_{m1}x_{1} + a_{m2}x_{2} + \dots + a_{mn}x_{n} = b_{m}
\end{cases}
$$
with <u>unknowns</u> $x_{1},x_{2},\dots,x_{n}$, coefficients $a_{11}, a_{12},\dots,a_{mn}$, and constant terms $b_{1}, b_{2}, \dots, b_{m}$. The equations most often involve [[Real Numbers|reals]] or [[Complex Numbers|complex numbers]] - but could in theory be elements of any abstract algebraic structure.

## Interpreting as Vectors
One extremely helpful *interpretation* is that each <u>unknowns</u> $x_{1},x_{2},\dots,x_{n}$ is a weight for [[Matrix#Row and Column Vectors|column vector]] in [[Vector Space#Linear Combination|linear combination]]
$$\large
x_{1} \begin{bmatrix}
a_{11} \\
a_{21} \\
\vdots \\
a_{m1}
\end{bmatrix} +
x_{2} \begin{bmatrix}
a_{12} \\
a_{22} \\
\vdots \\
a_{m2}
\end{bmatrix} + 
\dots +
x_{n} \begin{bmatrix}
a_{1n} \\
a_{2n} \\
\vdots \\
a_{mn}
\end{bmatrix} =
\begin{bmatrix}
b_{1} \\
b_{2} \\
\vdots \\
b_{m}
\end{bmatrix}
$$
Since the set of all <u>column vectors</u> with $m$ entries forms an $m$-dimensional [[Vector Space#Coordinate Vector Space|coordinate vector space]] $\mathbb{F}^n$, we can utilise the associated language and theory to help us.

For example, the set of left-hand side <u>column vectors</u> $A \subseteq \mathbb{F}^n$ define the [[Linear Span|linear span]] $span(A)$; the ***system of linear equations*** will have a [[#Solution Set|solution]] only if the right-hand side <u>column vector</u> $\mathbf{b}$ is within $span(A)$. Further, if we can establish the [[Vector Space#Linear Independence|linear independence]] of vectors $\mathbf{a} \in A$, then $A$ is *also* a [[Basis of Vector Space|basis]] of $\mathbb{F}^n$ and any solution is unique.

Even if $A$ is not itself a <u>basis</u>, $span(A)$ will always have a <u>basis</u> of <u>linearly independent</u> vectors that do guarantee exactly one expression; the number of vectors in that basis *(its [[Vector Space#Dimension of Vector Space|dimension]])* will be $\leq m,n$. This is important because if we have _m_ independent vectors a solution is guaranteed regardless of the right-hand side, and otherwise not guaranteed.

## Interpreting as Matrix Equation
Building from the [[#Interpreting as Vectors|vector equasion]], it is equivalent to a [[Matrix|matrix]] equation of the form $\mathbf{M}_{A} \mathbf{x} = \mathbf{b}$, where $\mathbf{M}_{A}$ is an $m \times n$ <u>matrix</u> of coefficients, $\mathbf{x}$ is a [[Matrix#Row and Column Vectors|column vector]] with $n$ entries, and $\mathbf{b}$ is a <u>column vector</u> with $m$ entries
$$\large
\begin{gathered}
A = \begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn} \\
\end{bmatrix}, &&
\mathbf{x} =\begin{bmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{bmatrix}, &&
\mathbf{b} =\begin{bmatrix}
b_{1} \\
b_{2} \\
\vdots \\
b_{m}
\end{bmatrix}
\end{gathered}
$$
The number of basis vectors in a [[Basis of Vector Space|basis]] *(its [[Vector Space#Dimension of Vector Space|dimension]])* of [[Linear Span|linear span]] $span(A)$, can now be expressed as the [[Matrix#Rank|rank]] of <u>matrix</u> $\mathbf{M}_{A}$. In fact, we could interpret $\mathbf{M}_{A}$ as a [[Transformation Matrix|transformation matrix]] of some [[Linear Map|linear map]] - opening up an even richer level of analysis.

# Solution Set
A solution of a ***linear system*** is the set of values that, *when substituted for the unknowns*, <u>simultaneously</u> satisfy the equations in the system; the set of all solutions is the ***solution set***. 

A ***linear system*** *definitely* behaves in <u>only three</u> ways:
1. The system has _infinitely many solutions_.
2. The system has one _unique solution_.
3. The system has _no solution_.

But generally, ***linear systems*** *(almost)* always behave like this:
- A ***linear system*** with fewer <u>equations</u> than <u>unknowns</u> has ***infinitely*** many solutions, but it may also have ***no*** solution; these are called [underdetermined systems](https://en.wikipedia.org/wiki/Underdetermined_system "Underdetermined system"). The [[#Dimension of Solution Space|dimension of the solution set]] is, in general, equal to $n-m$, where $n$ is the number of variables and $m$ is the number of equations.
- A system with the same number of <u>equations</u> and <u>unknowns</u> has a one ***unique*** solution.
- In general, a system with more <u>equations</u> than *unknowns* has no solution. Such a system is also known as an [overdetermined system](https://en.wikipedia.org/wiki/Overdetermined_system "Overdetermined system").

A system of linear equations behave differently from the general case if the equations are [[#Independence|independent]], or if it is [[#Consistency|inconsistent]] and has no more equations than unknowns.

## Geometric Interpretation
For a system involving <u>two</u> variables $x,y$, each equation determines a line on a 2D plane, with the solution being a point at which those lines intersect. For <u>three</u> variables, each equation determines a plane in 3D space, and the points of intersection are solutions.
![[Pasted image 20240425152053.png|300]] ![[Pasted image 20240425152225.png|300]]
This can be *generalised* to more variables and higher dimensions. The following pictures illustrate the trichotomy in the case of two variables:
![[Pasted image 20240426082016.png|200]] ![[Pasted image 20240426082028.png|200]]  ![[Pasted image 20240426082053.png|200]]
The first <u>system</u> has ***infinitely*** many <u>solutions</u>, namely all of the points on the blue line. The second system has a <u>single unique solution</u>, namely the intersection of the two lines. The third system has <u>no solutions</u>, since the three lines share no common point.

It must be kept in mind that the pictures above show only the most common case (the general case). It is possible for a <u>system</u> of two equations and two <u>unknowns</u> to have <u>no solution</u> (if the two lines are parallel), or for a <u>system</u> of three <u>equations</u> and two <u>unknowns</u> to be solvable (if the three lines intersect at a single point).

# Properties
## Independence
The <u>equations</u> of a <u>linear system</u> are ***independent*** if none of the <u>equations</u> can be derived algebraically from the others, i.e. each <u>equation</u> contains new information about the <u>unknowns</u>, and removing any of the equations increases the size of the [[#Solution Set|solution set]].

The [[#Interpreting as Matrix Equation|matrix]] that represents a <u>linear system</u> could be interpreted as the [[Transformation Matrix|transformation matrix]] of some [[Linear Map|linear map]] $\varphi$; the ***independence*** if the <u>linear system</u> is equivalent to the [[Vector Space#Linear Independence|linear independence]] of $\varphi$.

## Consistency
A <u>linear system</u> is ***inconsistent*** if it has no <u>solution</u>, and otherwise, it is said to be ***consistent***. When the system is ***inconsistent***, it is possible to derive a <u>contradiction</u> from the equations, that may always be rewritten as $0 = 1$. In general, ***inconsistencies*** occur if the <u>system</u> is [[#Independence|dependent]] and and the <u>constant terms</u> do not satisfy the dependence relation. An [[#Independence|independent system]] is always consistent.

## Equivalence
Two <u>linear systems</u> using the same set of <u>variables</u> are ***equivalent*** if each of the equations in the *second system* can be derived algebraically from the equations in the *first system*, and vice versa. Two systems are equivalent if either both are [[#Consistency|inconsistent]] or each equation of each of them is a <u>linear combination</u> of the equations of the other one. It follows that two <u>linear systems</u> are equivalent if and only if they have the same [[#Solution Set|solution set]].

# Solution Space
We can interpret any ***nonempty*** <u>solution set</u> as either a [[Linear Subspace|linear subspace]] *(for [[#Linear Solution Space of Homogeneous Systems|homogeneous systems]])* or [[Affine Space#Affine Subspaces|affine subspace]] *(for [[#Affine Solution Space of Nonhomogeneous Systems|nonhomogeneous systems]])* which we call the ***solution space***. Given that any [[Affine Space#Vector Spaces as Affine Spaces|vector space is an affine space]] over itself, and lacking further context, ***solution spaces*** should be assumed to be [[Affine Space#Affine Subspaces|affine subspaces]].

## Linear Solution Space of Homogeneous Systems
A *system of linear equations* is ***homogeneous*** if all of the constant terms are ***zero***
$$\large
\begin{cases}
a_{11}x_{1} + a_{12}x_{2} + \dots + a_{1n}x_{n} = 0 \\
a_{21}x_{1} + a_{22}x_{2} + \dots + a_{2n}x_{n} = 0 \\
\vdots \\
a_{m1}x_{1} + a_{m2}x_{2} + \dots + a_{mn}x_{n} = 0
\end{cases}
$$
A ***homogeneous system*** is equivalent to a [[Matrix|matrix]] equation of the form $\mathbf{M}_{A} \mathbf{x} = \mathbf{0}$ where $\mathbf{M}_{A}$ is an $m \times n$ <u>matrix</u> of coefficients, $\mathbf{x}$ is a [[Matrix#Row and Column Vectors|column vector]] with $n$ entries, and $\mathbf{0}$ is the [[Vector Space#Formal Definition|zero vecrtor]] with $m$ entries.

Every ***homogeneous system*** has *at least* <u>one</u> solution, known as the <u>zero</u> *(or trivial)* solution; every <u>unknown</u> is assigned to $0$ and that satisfies the <u>equations</u> in the *system*. If [[Matrix|matrix]] $\mathbf{M}_{A}$ is [[Square Matrix (algebraic)#Invertible Matrix|non-singular]] *($\det(\mathbf{M}_{A}) \neq 0$)*, then there is only ***one*** solution. If *matrix* $\mathbf{M}_{A}$ is <u>singular</u>, then the [[#Solution Set|solution set]] is ***infinite***.

The <u>matrix</u> $\mathbf{M}_{A}$ can [[Transformation Matrix|represent]] some [[Linear Map|linear map]], and thus the <u>solution set</u> of a ***homogeneous system*** is the [[Linear Map#Kernel, Image and Rank–Nullity Theorem|null space]] of that <u>linear map</u>. As a result, all <u>solution set</u> are [[Linear Subspace|linear subspaces]] of the overall [[Vector Space|vector space]] - called the ***solution space***.

## Affine Solution Space of Nonhomogeneous Systems
A ***honhomogeneous system*** is any system that *isn't* [[#Linear Solution Space of Homogeneous Systems|homogeneous]], i.e. $\mathbf{M}_{A} \mathbf{x} = \mathbf{b}$ where $\mathbf{b} \neq \mathbf{0}$. There is a close relationship between the <u>solution set</u> of ***honhomogeneous system*** $\mathbf{M}_{A} \mathbf{x} = \mathbf{b}$ and <u>solution set</u> of the corresponding ***homogeneous system*** $\mathbf{M}_{A} \mathbf{x} = \mathbf{0}$.

In particular, if $\mathbf{p}$ is a solution to $\mathbf{M}_{A} \mathbf{x} = \mathbf{b}$, then the entire <u>solution set</u> $S_{\mathbf{b}}$ can be expressed in terms of the [[#Linear Solution Space of Homogeneous Systems|solution space]] $S_{\mathbf{0}}$ of $\mathbf{M}_{A} \mathbf{x} = \mathbf{0}$
$$\large S_{\mathbf{b}} \ = \ \mathbf{p} + S_{\mathbf{0}} \ = \ \{ \ \mathbf{p} + \mathbf{v} \ | \ \mathbf{v} \in S_{\mathbf{0}} \ \}$$
Any [[Affine Space#Vector Spaces as Affine Spaces|vector space is an affine space]] over itself, hence so is the [[#Interpreting as Vectors|overall vector space]] $\mathbb{F}^n$. As such, <u>solution set</u> $S_{\mathbf{b}}$ is [[Affine Space#Affine Subspaces|affine subspace]] of $\mathbb{F}^n$ that <u>passes through</u> $\mathbf{p}$ with <u>direction</u> $S_{\mathbf{b}}$ - i.e. the <u>affine subspace</u> $\mathbf{p} + S_{\mathbf{0}}$, and is called the ***solution space***.

Unlike for [[#Linear Solution Space of Homogeneous Systems|homogeneous systems]] which are always [[Linear Subspace|linear subspaces]], ***honhomogeneous systems*** are only <u>affine subspaces</u> if they are non-empty.

## Properties of Solution Spaces
The ***solution space*** $S_{\mathbf{b}}$ of a <u>system of linear equations</u> $\mathbf{M}_{A} \mathbf{x} = \mathbf{b}$ inherits the *associated language and properties* of [[Linear Subspace|linear]] and [[Affine Space#Affine Subspaces|affine]] spaces. As [[#Affine Solution Space of Nonhomogeneous Systems|mentioned previously]] we can write $S_{\mathbf{b}} = \mathbf{p} + S_{\mathbf{0}}$, where $\mathbf{p}$ is a particular solution of <u>system</u> $\mathbf{M}_{A} \mathbf{x} = \mathbf{b}$ and $S_{\mathbf{0}}$ the [[#Linear Solution Space of Homogeneous Systems|solution space]] of $\mathbf{M}_{A} \mathbf{x} = \mathbf{0}$.

### Dimension of Solution Space
The ***dimension of solution space*** $S_{\mathbf{b}}$ is the [[Vector Space#Dimension of Vector Space|dimension of linear subspace]] $S_{\mathbf{0}}$. This is because its [[Affine Space#Affine Subspaces|associated vector space]] is $S_{\mathbf{0}}$, and the [[Affine Space#Dimension of Affine Space|dimension of affine spaces]] *(such as $S_{\mathbf{b}}$)* are the [[Vector Space#Dimension of Vector Space|dimension of their associated vector space]].

### Basis of Solution Space
#todo

