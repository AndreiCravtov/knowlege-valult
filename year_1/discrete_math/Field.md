A field is a set on which addition, subtraction, multiplication, and division are defined, and behave as the corresponding operations on [[Rational Numbers|rational]] and [[Real Numbers|real]] numbers do.

# Formal Definition
A field is is a [[Set Theory|set]] $F$ equipped with *addition* $(+): F^2 \to F$, and *multiplication* $(\cdot): F^2 \to F$, such that these [[Mathematical Functions|functions]] satisfy the following axioms for all $a,b,c \in F$:
$$
\begin{align}
\text{Associativity:} &&& \begin{aligned}
&a + (b + c) = (a + b) + c \\
&a \cdot (b \cdot c) = (a \cdot b) \cdot c
\end{aligned} \\ \\
\text{Commutativity:} &&& \begin{aligned}
&a + b = b + a \\
&a \cdot b = b \cdot a
\end{aligned} \\ \\
\text{Identity elements:} &&& \begin{aligned}
&\exists 0 \in F \bigg[ a + 0 = a \bigg] \\
&\exists 1 \in F \bigg[ a \cdot 1 = a \bigg]
\end{aligned} \\ \\
\text{Inverse elements:} &&& \begin{aligned}
&\exists {-a} \in F \bigg[ a + {-a} = 0 \bigg] \\
&\text{If} \ a \ne 0, \ \exists {a^{-1}} \in F \bigg[ a \cdot a^{-1} = 1 \bigg]
\end{aligned} \\ \\
\text{Distributivity:} &&& a \cdot (b + c) = (a \cdot b) + (a \cdot c)
\end{align}
$$
The **multiplicative identity** and **additive identity** of field $F$ are denoted as $1$ and $0$ respectively. The **multiplicative inverse** and **additive inverse** of element $a \in F$ are denoted as $a^{-1}$ and ${-a}$ respectively.

## Subfield
A subfield $K$ of field $L$, is a subset $K \subseteq L$ that is a field with respect to the field operations of $L$. For example, $\mathbb{R}$ is a subfield of $\mathbb{C}$.