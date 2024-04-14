Sometimes we wish to say that two objects which are not *strictly equal* to each other, are nonetheless *equivalent* to each other. For instance '$2+2$' is *equivalent* to '$4$' but it isn't *strictly equal* to it. These types of relations are called Equivalence [[Relations on Sets|Relations]].

# Formal Definition
Let there be some $R$ which is a binary relation on $A$. Then we say that: $$R \ \text{is an equivalence relation} \triangleq R \ \text{is reflexive} \ \wedge \ R \ \text{is symmetric} \ \wedge \ R \ \text{is transitive}$$
The short hand that $a$ and $b$ are equivalent under $R$ is $a \sim_{R} b$. If it is clear that we are talking about $R$ (or if it doesn't matter), then we can drop the subscript, and it becomes $a \sim b$.

# Equivalence Classes
We can use an equivalence relation $R$ to [[Set Partitions|partition a set]] in a natural way, such that all elements in a partition are equivalent to each other.

## Formal Definition
Let there be some $R$ which is a binary relation on $A$. For any $a \in A$, the equivalence class of $a$ (with respect to $R$), written as $[a]_{R}$ is defined as: $$[a]_{R} \triangleq \{ \ x \in A \ | \ a \sim_{R} x \ \}$$
When the relation $R$ is apparent (or irrelevant), we instead write just $[a]$. All elements in $A$ have an equivalence class, since $R$ is reflexive and so every element has at least one relation.

The set of equivalence classes produced from $A$ over equivalence relation $R$ is sometimes called '$quotient \ set \ A/R$' or '$quotient \ set \ A/\sim_{R}$', defined as: $$quotient \ set \ A/R \triangleq \{ \ X \in \wp A \ | \ \exists a \in A ( X = [a]_{R} ) \ \}$$
The above states that to get the set of equivalence classes, we first select all subsets of $A$, then eliminate any subsets that are not the equivalence classes of one of the elements in $A$.

## Representation
We can represent the partitioning of sets by an equivalence relation with the following chart:
![[Pasted image 20231104163450.png]]