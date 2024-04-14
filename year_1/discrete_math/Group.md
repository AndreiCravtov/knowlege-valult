A group is a [[Set Theory|set]] equipped with an operation that is: associative, has an identity element, and every element has an inverse element. Many mathematical objects can be through of as groups, like [[Real Numbers|real numbers]], [[Vector Space|vector spaces]], [[Field|fields]], and so on.

# Formal Definition
A ***group*** is a nonempty set $G$ equipped with some operation $(\cdot):G^2\to G$ that satisfies the following axioms:
$$
\begin{align}
\text{Associativity:} &&& \forall a,b,c \in G \bigg[ (a \cdot b) \cdot c = a \cdot (b \cdot c) \bigg] \\
\text{Identity element:} &&& \exists e \in G, \forall a \in G \bigg[ e \cdot a = a = a \cdot e \bigg] &&& \\
\text{Inverse element:} &&& \forall a \in G, \exists a^{-1} \in G \bigg[ a \cdot a^{-1} = e = a^{-1} \cdot a \bigg] &&& \\
\end{align}
$$

The **identity element** a of group $G$ is denoted as $e$. The **inverse element** of $a \in G$ is denoted as $a^{-1}$.

# Properties
## Abelian group
An **Abelian group**, or **commutative group**, is a group $G$ who's operation also obeys *commutativity*. What this means is that we have $a \cdot b = b \cdot a$ for any $a,b \in G$.

## Additive group
An **additive group** is a group who's operation can be thought of as addition, and therefore is denoted with $+$ symbol. For example, we can say for additive group $G$, that $a+a^{-1} = e$ for any $a,b \in G$. 