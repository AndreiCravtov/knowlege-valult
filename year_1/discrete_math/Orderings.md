Orderings are [[Relations on Sets|binary relations]] with special properties. They generally capture the idea of an object being "bigger" than another. For example, for $\mathbb{N}$ the relation $\leq$ is an order relation.

# Formal Definitions
Let $R$ be a binary relation on $A$. Here are the types of order

## Preorder
Preorder (also quasiorder) is the general case of [[Equivalence Relations|equivalence relations]] and [[Partial Order|partial orders]]. Preorders must be both [[Relations on Sets#Reflexive|reflexive]] and [[Relations on Sets#Transitive|transitive]]. A preorder is defined as: $$R \ \text{is a preorder} \triangleq R \ \text{is reflexive} \ \wedge \ R \ \text{is transitive}$$
A preorder with [[Relations on Sets#Symmetric|symmetry]] is an equivalence relation. A preorder with [[Relations on Sets#Anti-symmetric|anti-symmetry]] is a partial order. The identity relation is both a partial order, and an equivalence relation.

## Partial Order
A [[Partial Order|partial order]] relation is an [[Relations on Sets#Anti-symmetric|anti-symmetric]] [[#Preorder|preorder]].

## Strict Partial Order
A strict partial order is an [[Relations on Sets#Irreflexive|irreflexive]] and [[Relations on Sets#Transitive|transitive]] relation. It is defined as: $$R \ \text{is a strict partial order} \triangleq R \ \text{is irreflexive} \ \wedge \ R \ \text{is transitive}$$
Despite intuition, strict partial orders are not a [[Partial Order|partial orders]]. It is intuitively understood as the generalisation of the $<$ relation. Partial orders are written as $<$, and strict partial orders on set $A$ is written as $(A,<)$ or $<_{A}$ .

A strict partial order $(A,<)$, can be expanded to a [[Partial Order|partial order]] $(A,\leq)$ by $\leq_{A} = <_{A} \cup \ Id_{A}$. The inverse is true, a strict partial order $(A,<)$ can be defined in-terms of a [[Partial Order|partial order]] $(A,\leq)$ like $a <_{A} b = a <_{A} b \wedge a \ne_{A} B$.

## Total Order
A total order is a [[Partial Order|partial order]] with an additional property that all elements are related to each other.  It is defined as: $$R \ \text{is a total order} \triangleq R \ \text{is a partial order} \ \wedge \ \forall a,b \in A (aRb \vee bRa)$$

## Orders on the product set $A \times B$
For two partially ordered sets $(A,\le_{A})$ and $(B,\leq_{B})$, there exist the:
$$
\begin{gathered}
Product \ order: & \langle a_{1}, b_{1} \rangle \leq_{P} \langle a_{2}, b_{2} \rangle \triangleq (a_{1} \leq_{A} a_{2}) \wedge (b_{1} \leq_{B} b_{2}) \\
Lexicographical \ order: & \langle a_{1}, b_{1} \rangle \leq_{L} \langle a_{2}, b_{2} \rangle \triangleq (a_{1} \leq_{A} a_{2}) \vee (a_{1} =_{A} a_{2} \wedge b_{1} \leq_{B} b_{2})
\end{gathered}
$$
If $\leq_{B}, \leq_{B}$ are total orders, then $(A\times B, \leq_{L})$ is a total order. Product orders are a subset of the lexicographical orders, so $a\leq_{P}b \implies a\leq_{L}b$. 

### Visualisation
The left diagram represents the set $\{ \langle r_{1},r_{2} \rangle \in \mathbb{R}^2  | \langle r_{1},r_{2}\rangle \leq_{P} \langle 10,5 \rangle \}$, and the set $\{ \langle r_{1},r_{2} \rangle \in \mathbb{R}^2  | \langle r_{1},r_{2}\rangle \leq_{L} \langle 10,5 \rangle \}$ is represented on the right:
![[Pasted image 20231104211256.png|800]]

### Full Lexicographic Order
For any total order $(A, \leq_{A})$ where $A$ is finite, let $A^* \triangleq \{ \epsilon \} \cup A \cup A^2 \cup A^3 \cup \dots$, the set of all finite sequences made from the elements of $A$ as ordered by $\leq_{A}$. $\{ \epsilon \}$ denotes an empty sequence. The full lexicographic order, $\leq_{F}$, on $A*$ is defined by this: $$a \leq_{F} b \triangleq (u=\epsilon) \vee (u=xu' \wedge v=yv' \wedge (x <_{A} y \vee (x=y \wedge u' \leq_{F} v')))$$
Where $x,y$ are the first terms of $u,v$, and $u',v'$ are the rest of the terms, respectively.

i.e. The full lexicographic order gives the ordering for words in a dictionary, using the total order on characters that is defined by the alphabet