Peano Axioms were one of the first axiomatizations of the natural numbers, and survives till this day. Models of the Peano natural number can be constructed out of popular [[Set Theory|set theories]] such as [ZF](https://en.wikipedia.org/wiki/Zermelo%E2%80%93Fraenkel_set_theory).

# Formal Definition
The set of natural numbers $\mathbb{N}$ is defined by the following:
1. $0 \in \mathbb{N}$
2. $n \in \mathbb{N} \implies Succ(n) \in \mathbb{N}$
3. $=$ is an [[Equivalence Relations|equivalence relation]] on $\mathbb{N}$
4. $\forall n \in \mathbb{N} (Succ(n) \ne 0)$
5. $Succ$ is an [[Mathematical Functions#Injective Functions|injective function]]
6. For some set $V$ where $0 \in V \wedge \forall n \in \mathbb{N}(n \in V \implies n \in )$

## Mathematical Induction
The final axiom, is the axiom of induction. It allows us to conclude that for some unary predicate $P$, $$P(0) \wedge \forall n \in \mathbb{N} (P(n)\implies P(Succ(n))) \implies \forall n \in \mathbb{N}(P(n))$$
Which naturally translate to the proof steps of: prove $P$ holds for $0$, then prove that if $P$ holds for $n$, it also holds for $n+1$, and thus it holds for all $n \in \mathbb{N}$.

## Defining Operations
Now that we can define $\mathbb{N}$, we can define operations on $\mathbb{N}$, for example we can define addition and multiplication as follows:
$$
\begin{gathered}
\text{Addition:} & Add(0,n) = n \\
& Add(Succ(m),n) = Succ(Add(m,n)) \\ \\
\text{Multiplication:} & Mult(0,n) = 0 \\
& Mult(Succ(m),n) = Add(Mult(m,n),n)
\end{gathered}
$$

## Defining Orders
We can begin by defining the following relation $$<_{1} \ \triangleq \ \{ \langle n,m \rangle \in \mathbb{N}^2 \ |\ m = Succ(n) \}$$
We can then use [[Relations on Sets#Transitive Reduction|transitive closure]] on this relation to define the [[Orderings#Strict Partial Order|strictly less-than]] relation on $\mathbb{N}$ as follows $$<_{\mathbb{N}} \ \triangleq \ (<_{1})^+$$
And this can then be extended into a full [[Partial Order|partial order using the usual method]] as follows $$\leq_{\mathbb{N}} \ \triangleq \ <_{\mathbb{N}} \cup \ Id_{\mathbb{N}}$$
