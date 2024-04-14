The indicator function (**characteristic function** of a subset of a set) is a [[Mathematical Functions|function]] to indicate the set membership of an element it is applied to.

# Formal Definition
For some set $A$, let there be some subset $B \subseteq A$. The subset indicator function of $B$, or $\chi_{B}: A \to \{ 0,1 \}$ is defined as: $$\chi_{B}(a) = \begin{cases} 
1 & a \in B \\
0 & a \not\in B 
\end{cases}
$$
Notice too, that [[Mathematical Functions#Multivariate Function Syntax|multivariate syntax]] applies. Which means if $A = A_{1} \times A_{2} \times A_{3} \times\dots \times A_{n}$ then: $$\chi_{B}(a_{1}, a_{2}, a_{3}, \dots, a_{n}) = \begin{cases} 
1 & \langle a_{1}, a_{2}, a_{3}, \dots, a_{n} \rangle \in B \\
0 & \langle a_{1}, a_{2}, a_{3}, \dots, a_{n} \rangle \not\in B 
\end{cases}$$
The indicator function is also written as $1_{B}, I_{B}, \ \text{or} \ f_{B}$. This is only used when the surrounding set $A$ is implicitly assumed, so there is no need to express it.