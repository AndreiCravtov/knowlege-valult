A power set is the [[Set Theory|set]] of all the subsets of some given set. The power set of $A$ is denoted as $\wp A$, where $\wp A$ is defined as: $$\wp A \triangleq \{ \ V \ | \ V \subseteq A \ \}$$
# Examples
Here are a few examples:
$$
\begin{gather}
\wp \{ a, b \} = \{ \emptyset, \ \{ a \}, \ \{ b \}, \ \{ a, b \} \} \\
\wp \emptyset = \{ \ \emptyset \ \} \\
\dots
\end{gather}
$$
# Precedence
Since the power set operator is unary, the normal [[Mathematical Reasoning#Operator precedence|precedence rules]] apply, so $\wp A \cap B = (\wp A) \cap B$, etc.

# Cardinality
Let there be some finite set $A$ for which $|A| = n \in \mathbb{W}$. Given that, the [[Cardinality of Sets|cardinality]] of $\wp A$ is: $$|\wp A| = 2^n$$
This can be proven by counting. For some $A = \{ a_1, \dots, a_n \}$, a subset $V$ ($V \subseteq A$) can be thought of as a binary number of length $n$, where each digit of that number represents if the element corresponding to it is included or not.

So $b = b_1\dots b_n$ where $a_i \in V \implies b_i = 1$ and $a_i \notin V \implies b_i = 0$. From this setup, the total number of $n$-length binary numbers is the same as the total number of subsets of $A$, both of which are $2^n$.

