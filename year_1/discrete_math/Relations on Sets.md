A relation is a way to capture a link between objects in two different [[Set Theory|sets]]. We that by putting these related objects into a tuple.
i.e. if we we to say that $\text{John} \ Loves \ \text{Mary}$, then the ordered pair $\langle \text{John}, \ \text{Mary}  \rangle$ is an element of the set $Loves$.

# Formal Definition
A *relation* $R$ between two sets $A$ and $B$ (from $A$ to $B$), is a subset of $A \times B$. So we say that $R \subseteq A \times B$. We can also say that $R$ is an element if the [[Power Sets|power set]] of $A\times B$, so $R \in \wp(A \times B)$, and thus the number of possible *relations* on $A\times B$ is $|\wp(A \times B)| = 2^{|A\times B|}$.
- Generally, we say that or $R$ has the type $A \times B$.
- If $A=B$, then $A \times B = A^2$, so we say $R$ is a *binary relation* on $A$.
The shorthand for writing $\langle a,b \rangle \in R$ is $aRb$. Similarly, $aRbRc$ is shorthand for $aRb \wedge bRc$.

## Identity relation
An identity relation is one where an element in a set is mapped to itself. So for some set $A$ we say that: $$Id_{A} \triangleq \{ \ \langle x,y \rangle \in A^2 \ | \ x =_{A} y \ \}$$
Identity relations exist on all sets.

## Higher order relations
So far, the above was discussing $\text{binary}$ relations. But this can be generalised to $n\text{-ary}$ relations. An $n \text{-ary}$ relation $R$ between the sets $A_{1}, A_{2}, \dots , A_{n}$ is the subset of $A_{1} \times A_{2} \times \dots \times A_{n}$, so its the case that $R \subseteq A_{1} \times A_{2} \times \dots \times A_{n}$.
Binary relations are $n=2$.
Predicates define a relation of $n=1$, as they form a subset of the set they are selecting from.
A way to thing of relations like $n=3+$ is for example like the relation that describes the surface of some object for instance. So $x^2 + y^2 + z^2 = 1$ relates 3 elements together to define all the points on a sphere.

# Representations
## Directed graphs
One way to represent *relations* is as a collection of arrows between the elements in the sets which you're relating. The sets are the circles, and each arrow represents an element in the *relation*.
![[Pasted image 20231104133940.png|500]]
You can even represent a binary relation like this.
![[Pasted image 20231104134159.png|500]]

## Matrix
For some relation $R$ of type $A \times B$, where $A = \{ a_{1},a_{1},\dots,a_{n} \}, \ B = \{ b_{1},b_{2},\dots,b_{m} \}$, we can represent $R$ with a $m \times n$ matrix of boolean values $T$ and $F$. For some $1\leq i\leq n$ and $1\leq j\leq m$, we have that 
$$
M(i,j) = \begin{cases} 
      T & \langle a_{i}, b_{j} \rangle \in R \\
      F & Otherwise \\
\end{cases}
$$
Where $M(i,j)$ is the $i^{th}$ row and $j^{th}$ column of the matrix $M$.
So for example we might have a matrix like this: 
$$
\begin{pmatrix}
T & T & T \\
F & T & F
\end{pmatrix}
$$
for an $|A| = 2$ and $|B|=3$.

# Operators
Since relations are sets, [[Set Theory#Set operations|set operators]] still work on them. However, there are unique operators on relations that override set operations, in the context of a broad relation.
For some $R,S \subseteq A \times B$, the following operations are defined:
$$
\begin{gathered}
\text{Relation Union}: & R \cup S \triangleq \{ \ \langle a,b \rangle \in A \times B \ | \ aRb \vee aSb \ \} \\
\text{Relation Intersection}: & R \cap S \triangleq \{ \ \langle a,b \rangle \in A \times B \ | \ aRb \wedge aSb \ \} \\
\text{Relation Compliment}: & \overline{R} \triangleq \{ \ \langle a,b \rangle \in A \times B \ | \ \langle a,b \rangle \not\in R \ \} \\
\text{Inverse relation}: & R^{-1} \triangleq \{ \ \langle b,a \rangle \in B \times A \ | \ aRb \ \} \\
\end{gathered} \\
$$

## Composition
There is also a more unique operation on relations, *composition*. For some $R \subseteq A \times B$ and $S \subseteq B \times C$, the composition of $R$ and $S$ is $R \circ S$, and is defined as: $$R \circ S \triangleq \{ \ \langle a,c \rangle \in A \times C \ | \ \exists b \in B ( aRb \wedge bRc ) \ \}$$
Composition can only occur when the types of the relations being composed match up.

### Properties of Composition
- Composition is associative, so $R \circ (S \circ T) = (R \circ S) \circ T$ and so on, so therefore we can just omit the brackets and write $R \circ S \circ T$.
- If $R,S \subseteq A^2$, composition of those is not commutative, so $R \circ S \ne S \circ R$.
- If $R \subseteq A^2$, then $R \circ R^{-1} \ne Id_{A}$.

# Properties of Relations
Lets consider some $R$ which is a binary relation on $A$

## Reflexive
Saying that $R$ is reflexive means that every element of $A$ that $R$ includes has to have a relation to itself. Another way of understanding it is that the identity on $A$ must be a subset of $R$, so $Id_{A} \subseteq R$. The formal definition is: $$R \ \text{is reflexive} \triangleq \forall x \in A ( \ xRx \ )$$

## Irreflexive
Saying that $R$ is irreflexive means that every element of $A$ that $R$ includes should never have a relation to itself. Another way of understanding it is that the identity on $A$ must not be a subset of $R$, so $Id_{A} \not\subseteq R$. The formal definition is: $$R \ \text{is irreflexive} \triangleq \forall x \in A ( \ \langle x,x\rangle \not\in R \ )$$
**NOTE:** irreflexivity isn't the opposite of [[#Reflexive|reflexivity]]. A relation can be not reflexive (by having one element without an arrow to itself) and also not irreflexive (by having one element with an arrow to itself). In-fact, $\emptyset$ is simultaneously reflexive and irreflexive (but this is a vacuous result).

## Symmetric
Saying that $R$ is symmetric means that every element in $R$ has some inverse. The arrows between the elements go both ways. The formal definition is: $$R \ \text{is symmetric} \triangleq \forall x,y \in A ( \ xRy \implies yRx \ )$$
## Anti-symmetric
Saying that $R$ is anti-symmetric means that no element in $R$ has an inverse. The arrows between the elements never go both ways. The formal definition is: $$R \ \text{is anti-symmetric} \triangleq \forall x,y \in A ( \ xRy \wedge yRx \implies x =_{A} y \ )$$
**NOTE:** anti-symmetry isn't the opposite of [[#Symmetric|symmetry]]. A relation can be not symmetric (by having one pair of elements without symmetric arrows) and also not anti-symmetric (by having one pair of elements with symmetric arrows). In-fact, the identity relation is simultaneously symmetric and anti-symmetric.

## Transitive
Saying that $R$ is transitive means that means that if $a$ points to $b$, which in turn points to $c$, then $a$ must have a direct arrow to $c$ as well. The formal definition is: $$R \ \text{is transitive} \triangleq \forall x,z \in A ( \ \exists y \in A( \ xRy \wedge yRz \ ) \implies xRz \ )$$
So if we know $R$ is transitive, then $R \circ R = R$, all the new direct links that you usually create with composition, already exist.

### Transitive Closure
The transitive closure is a way to turn a non-transitive relation into a transitive relation. In fact, it is the smallest transitive relation containing $R$. Consider some $R$ that is a binary relation on set $A$.
![[Pasted image 20231104163913.png|500]]
The $\text{transitive closure of} \ R$, written as $R^+$, is achieved by composing $R$ with itself over and over again, until it has achieved transitivity:
$$
\begin{gathered}
& R^1=R \\
& R^2 = R \circ R \\
& R^3 = R^2 \circ R \\
& \vdots \\
& R^n = R^{n-1} \circ R \\
& \vdots \\
\text{transitive closure of} \ R: & R^+ \triangleq R \cup R^2 \cup \dots \cup R^n \cup \dots
\end{gathered}
$$
It can be intuitively be thought of as, $aR^+b$ if there is any path between $a$ and $b$ in $R$, even if we have to take multiple trips. So $R^+$ ends up looking like this:
![[Pasted image 20231104172119.png|500]]
If $A$ is finite and $|A| = n$, then $R$ needs to be composed with itself at **most**, $n$ times (since any more than that involves repeating the same path; this follows from the [[Pigeonhole Principle]]). Meaning that $R^+ = R^n$ for all possible $A$, $n$, $R$. Composing further is redundant, since $R^+ = R^n = R^{n+1}$. But sometimes, it can take less composing steps to achieve $R^+$.

If the transitive **and** reflexive closure of $R$ is written as $R^*$.

#### Transitive Reduction
The *transitive reduction* $R^-$, of the transitive relation $R$ is the smallest set $S$ such that $S \subseteq R$ and $S^+=R$, so: $$R^- = \{ \ \langle a,c \rangle \in R \ | \ \neg\exists b \in A ( \ a \ne b \wedge b \ne c \wedge aRb \wedge bRc \ ) \  \}$$
Transitive reductions are not necessarily unique. The are used as a way to compress a transitive relation, as all the information is still stored in the transitive reduction, and if need be, the original relation can be reconstructed with transitive closure.
