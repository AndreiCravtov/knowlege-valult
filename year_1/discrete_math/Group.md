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
## Subgroup
If $(G, *)$ is a <u>group</u>, then any subset $H \subseteq G$ that is *also* a <u>group</u> under $*$ is called a subgroup of $G$. Subgroups will therefore always share the same <u>identity element</u> as their ***overgroups***.

## Abelian group
An **Abelian group**, or **commutative group**, is a group $G$ who's operation also obeys *commutativity*. What this means is that we have $a \cdot b = b \cdot a$ for any $a,b \in G$.

## Opposite Group: $G^{\mathrm{op}}$
Let $(G,*)$ be a <u>group</u>. The opposite group $G^{\mathrm{op}}$ of $G$, is the same set of elements as $G$ but instead using $(\overset{\mathrm{op}}{*})$ instead of $(*)$ as its group operation: defined as $g \overset{\mathrm{op}}{*} h = h * g$ for any $g,h \in G$; if $G$ is [[#Abelian group|abelian]] then $G = G^{\mathrm{op}}$. Every $G$ is [naturally isomorphic](https://en.wikipedia.org/wiki/Naturally_isomorphic "Naturally isomorphic") to its $G^{\mathrm{op}}$ via $G \to G^{\mathrm{op}}; \ x \mapsto x^{-1}$.

## Group Homomorphism
[[Homomorphism (algebraic)|homomorphism]] on groups
![[Pasted image 20240430094817.png|800]]
#todo https://en.wikipedia.org/wiki/Group_homomorphism

# Common Types of Group
## Additive group
An **additive group** is a group who's operation can be thought of as addition, and therefore is denoted with $+$ symbol. For example, we can say for additive group $G$, that $a+a^{-1} = e$ for any $a,b \in G$.

## Symmetric Group of a Set: $\operatorname{Sym}(X)$
For any [[Cardinality of Sets|finite]] set $X$, the set of ***all*** [[Mathematical Functions#Bijective Functions|bijective functions]] from $X$ into itself - equipped with [[Mathematical Functions#Function Composition|function composition]] $(\circ)$ - forms the ***symmetric group*** $\operatorname{Sym}(X)$ on set $X$, with the [[Mathematical Functions#Identity Function|identity function]] $Id_{X}$ as the <u>group identity</u> element.
![[Pasted image 20240430094401.png]]
#todo https://en.wikipedia.org/wiki/Symmetric_group#