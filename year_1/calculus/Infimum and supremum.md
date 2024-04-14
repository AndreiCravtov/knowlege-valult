Infimum is the greatest lower bound, and supremum is the lowest upper bound.

# Formal definition
Consider a [[Partial Order|partially ordered set]] $P$. Now consider a nonempty subset $S \subseteq P$. Let $l,u \in P$ so:
1. If $\forall s \in S \ (\ s \leq u \ )$ then $u$ is said to be the ***upper bound*** of $S$.
2. If $\forall s \in S \ (\ l \leq s \ )$ then $l$ is said to be the ***lower bound*** of $S$.
3. The ***supremum*** of $S$, or $sup(S)$, is said to be the least of the possible upper bounds of $S$.
4. The ***infimum*** of $S$, or $inf(S)$, is said to be the greatest of the possible lower bounds of $S$.
This can be visualised like this:
```desmos-graph
left=-0.1; right=10
top=4; bottom=-4
---
3<=x<8 | -1<y<1 | blue

(3,0) | label:Infimum | red
(2.5,0) | orange
(2,0) | orange
(1.5,0) | orange
(1,0) | orange
(0.5,0) | orange

(8,0) | label:Supremum | magenta
(8.5,0) | purple
(9,0) | purple
(9.5,0) | purple
```
Where the partially ordered set set $P$ is defined to be $P = \mathbb{R}$, and the subset $S$ is defined as $S \triangleq \{ \ s\in \mathbb{R} \ | \ 3\leq s < 8 \ \}$. We can see that there are lots of lower bounds (orange dots) and lots of upper bounds (purple dots) but there is only one supremum and infimum.
The supremum and infimum of $S$ don't need to actually be members of $S$, they just need to be members of $P$. This is seen in our example as $sup(S)=8$ but $8 \notin S$.

# Properties
## Uniqueness
The infimum and supremum, if they exist, are unique. This can be proven just by following the definitions:
1. Suppose that a supremum exists for some set $X$.
2. Let $L_{1}$ and $L_{2}$ both be the supremum of $X$.
3. Since $L_{1}$ is an upper, and $L_{2}$ is the supremum of $X$, we have $L_{2}\leq L_{1}$
4. Since $L_{2}$ is an upper, and $L_{1}$ is the supremum of $X$, we have $L_{1}\leq L_{2}$
5. When we combine both inequalities we get $L_{1} = L_{2}$.
6. Therefore there exists only one supremum.
Proving the same for infimum has a similar structure.