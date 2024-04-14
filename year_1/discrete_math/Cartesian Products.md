The Cartesian product of $A$ and $B$ is written as $A \times B$. The resulting set from this operation is defined as follows:
1. An *ordered pair* of elements $a \in A$ and $b \in B$ is written as $\langle a,b \rangle$.
2. $A \times B$ is the set of all possible ordered pairs of all the elements in set $A$ and $B$. The formal definition is $$A \times B \triangleq \{ \ \langle a, b \rangle \ | \ a \in A \ \wedge \ b \in B \ \}$$
***NOTE:** $A^2$ is shorthand for $A \times A$.*
3. Equality on elements of $A \times B$ is defined as: $$\begin{gathered}
=_{A \times B} \ \triangleq \ \{ \ \langle p_{1}, p_{2} \rangle \in (A \times B)^2 \ |\  \exists a,c \in A \ \ \ b, d \in B ( \ p_{1} = \langle a,b \rangle \ \wedge \ p_{2} = \langle c,d \rangle \ \wedge \ a =_{A} c \ \wedge \ b =_{B} d \ ) \ \} \\ \\
\text{or} \\ \\

=_{A \times B} \ \triangleq \ \{ \ \langle \langle a, b \rangle, \langle c, d \rangle \rangle \in (A \times B)^2 \ | \ a =_{A} c \ \wedge \ b =_{B} d \ \} \\ \\
\text{or} \\ \\

\langle a, b \rangle =_{A \times B} \langle c, d \rangle \ \triangleq \ a =_{A} c \ \wedge \ b =_{B} d

\end{gathered}$$

# Visualisation
A way to visualise $A \times B$ is 
$$
\begin{gathered}

\begin{gathered}[c]
\langle a_{1}, b_{1} \rangle
\end{gathered}

\begin{gathered}[c]
& \dots &
\end{gathered}

\begin{gathered}[c]
\langle a_{1}, b_{m} \rangle
\end{gathered} \\

\begin{gathered}[c]
\vdots &&&
\end{gathered}

\begin{gathered}[c]
\ddots &&&
\end{gathered}

\begin{gathered}[c]
\vdots
\end{gathered} \\

\begin{gathered}[c]
\langle a_{n}, b_{1} \rangle
\end{gathered}

\begin{gathered}[c]
& \dots &
\end{gathered}

\begin{gathered}[c]
\langle a_{n}, b_{m} \rangle
\end{gathered}

\end{gathered}
$$
# Properties
## Non-commutative
The $\times$ operation is not commutative, so $A \times B \not= B \times A$.

## Cardinality
The [[Cardinality of Sets|cardinality]] of $A \times B$, for some finite sets $A$ and $B$, is $|A\times B|=|A| \times |B|$.
# $n$-ary product
The $n$-ary product is the extrapolation of the Cartesian product from a binary operator to an $n$-ary operator, but keeping the same principle.
1. For any $n>1$, the $n$-tuple is an *ordered sequence* is $\langle a_{1},\dots, a_{n} \rangle$ of $n$ objects.
2. Let $A_{1},\dots,A_{n}$ be arbitrary sets. The $n$-ary product is written as $A_{1}\times \dots \times A_{n}$, or $\times^{n}_{i=1}A_{i}$, defined as $\{ \ \langle a_{1},\dots, a_{n} \rangle \ | \ i \in \mathbb{N} \ ( 1 \leq i \leq n \implies a_{i} \in A_{i} ) \ \}$.
3. The $n$-ary product of $A$ is written as $A^n$.

## Weak equivalence
Even though the $\times$ operation is not commutative, there is however still some clear correspondence between $A \times B \times C$, $(A \times B) \times C$ and $A \times (B \times C)$.