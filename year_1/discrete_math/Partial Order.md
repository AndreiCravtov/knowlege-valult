A partial order the pairing of some $A$ with a partial order relation $\leq$ on it. Partial order relations are intuitively understood as the generalisation of the $\leq$ relation on numbers. Partial orders are often as $(A,\leq)$ or $\leq_{A}$. A partial order relation is an [[Relations on Sets#Anti-symmetric|anti-symmetric]] [[Orderings#Preorder|preorder]].

# Formal definition
Given a binary relation $R$ on some set $A$: $$R \ \text{is a partial order} \triangleq R \ \text{is a preorder} \ \wedge \ R \ \text{is anti-symmetric}$$
Every partial order relation $(A,\leq)$ has a corresponding [[Orderings#Strict Partial Order|strict partial order]] $(A,<)$, where $a <_{A} b \triangleq a \leq_{A} b \wedge a \ne_{A} b$. Similarly, every [[Orderings#Strict Partial Order|strict partial order]] $(A,<)$, can be expanded to a partial order $(A,\leq)$ by $\leq_{A} = <_{A} \cup \ Id_{A}$.

# Representation
## Hasse diagrams
A way to graphically represent partial orders is using [Hasse diagrams](https://en.wikipedia.org/wiki/Hasse_diagram). The idea is that you start with the graph representation of some partial order relation $R$, where every $aRb$ would be an arrow from $a$ to $b$. You then remove all the arrows that are a result of transitivity and reflexivity, since that information is already known. Finally, we remove the direction of arrows with positioning. We assume that the direction of arrows is **up**. If $a$ is below $b$ and has a link to it, then the arrow is from $a$ to $b$.

For example, here is the $divides$ relation on $\{ 3,4,12,24,28,73 \}$:
![[Pasted image 20231105153731.png]]
We can see that $3$ and $4$ divide $12$, but that they also divide themselves, and divide $72$ and $48$.

# Properties
Let there be some partial order $(A,R)$, and $a \in A$.

## Minimal
The definition of minimal is: $$a \ \text{is minimal} \triangleq \forall b \in A(bRa \implies b =_{A} a)$$
Which says that if some element is less than $a$, that element must be $a$. Minimal elements are not unique, so a partial order can have multiple of them. If $A$ is finite and non-empty, then $(A, R)$ must have a minimal element.

For example, here is the $divides$ relation on $\{ 3,4,12,24,28,73 \}$:
![[Pasted image 20231105153731.png]]
We can see that $3$ and $4$ are both minimal elements for this relation.

## Least
The definition of least is: $$a \ \text{is least} \triangleq \forall b \in A( \ aRb\ )$$
Which says that $a$ is less than all other elements.

If $A$ is finite and non-empty, and $R$ is a [[Orderings#Total Order|total order]], then $(A, R)$ must have a least element. If a least element exists, then it is unique. It is also true that $a \ \text{is least} \implies a \ \text{is minimal}$.

For example, here is the $divides$ relation on $\{ 1,2,3,4,6,12 \}$:
![[Pasted image 20231105154935.png]]
We can see that $1$ is the least element for this relation.

## Maximal
The definition of maximal is: $$a \ \text{is maximal} \triangleq \forall b \in A(aRb \implies b =_{A} a)$$
Which says that if some element is more than $a$, that element must be $a$. Maximal elements are not unique, so a partial order can have multiple of them.

For example, here is the $divides$ relation on $\{ 3,4,12,24,28,73 \}$:
![[Pasted image 20231105153731.png]]
We can see that $72$ and $48$ are both maximal elements for this relation.

## Most
The definition of most is: $$a \ \text{is most} \triangleq \forall b \in A( \ bRa\ )$$
Which says that $a$ is more than all other elements.

If a most element exists, then it is unique. It is also true that $a \ \text{is most} \implies a \ \text{is maximal}$.

For example, here is the $divides$ relation on $\{ 1,2,3,4,6,12 \}$:
![[Pasted image 20231105154935.png]]
We can see that $12$ is the most element for this relation.

# Well-Founded Partial Orders
Well founded partial orders are those for which their corresponding [[Orderings#Strict Partial Order|strict partial orders]] are [[Well-Founded relation|well-founded]]. If the partial order is also a [[Orderings#Total Order|total order]] then it is said to be a [[Well-Order|well-order]].

## Noetherian induction
Noetherian induction, (well-founded induction) is a type of induction you can perform on a well-founded order of $(A,R)$, where: $$(\forall a \in A)[(\forall b \in A)[bRa \implies P(b)] \implies P(a)] \implies (\forall a \in A)P(a)$$
Or if:
- If $a \in A$ and, $P(b)$ holds for all $b$ such that $bRa$, then $P(a)$ holds
Then:
- $P(a)$ holds for all $P(b)$
## Application to product orders
If $(A,\leq_{A})$ and $(B,\leq_{B})$ are well-founded, then the [[Orderings#Orders on the product set $A times B$|lexicographic and product]] orders on $A\times B$ are also well-founded.

This can be used to prove certain results by re-framing a problem in terms of a well-founded lexicographic order and proving the result by [[#Noetherian induction]].

For example, one can use well-founded induction with respect to the lexicographic order of $\mathbb{N}\times \mathbb{N}$, to show that the [Ackermann function](https://en.wikipedia.org/wiki/Ackermann_function) is a [[Computable Functions|computable function]]. 