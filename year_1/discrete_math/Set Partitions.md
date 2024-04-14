If we divide a [[Set Theory|set]] into non-overlapping parts we get the partition of a set. The formal definition of the set partition is as follows:
$$
\begin{gathered}
\text{partition of} \ A \triangleq \{ \ A_{1},\dots,A_{n} \ \} \\
\text{such that} \\
\forall i \in \mathbb{N} \ ( \ 1 \leq i \leq n \implies A_{i} \neq \emptyset \ ) \\
\text{and} \\
A = A_{1} \cup \dots \cup A_{n} \\
\text{and} \\
\forall i,j \in \mathbb{N} \ ( \ 1 \leq i,j \leq n \ \wedge \ i \not= j \implies A_{i} \cap A_{j} = \emptyset \ )
\end{gathered}
$$
Or, where each of these partition sets must be non-empty, together they must cover all of the original set, and none of them should overlap with each other.

**NOTE:** $A_{1} \cup \dots \cup A_{n}$ can be written as $\cup^n_{i=1}A_{i}$ for convenience.