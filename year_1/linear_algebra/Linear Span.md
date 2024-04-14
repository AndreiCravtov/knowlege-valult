Given some set of vectors $S$, the set of all vectors you can make by applying the [[Vector Space#Formal Definition|axioms of a vector space]], is called the *linear span* of $S$. Alternatively - given some vector space $V$, we can think of the *linear span* of $S \subseteq V$ as the smallest [[Linear Subspace|subspace]] of $V$ that contains $S$. Or in the case of a [[Cardinality of Sets#Finite Sets|finite]] $S$, it is the set of all of all [[Vector Space#Linear Combination|linear combinations]] of the elements in $S$.

The **linear span** of $S$ is denoted as $span(S)$. If $W = span(S)$, then we say that:
 - $S$ spans $W$
 - $W$ is spanned by $S$
 - $S$ is a spanning set of $W$

# Formal Definition
$V$ is a [[Vector Space|vector space]] over $F$. For any nonempty set $S \subseteq V$, we define the ***linear span*** of $S$ as the [[Set Theory#Set operations|intersection]] of all [[Linear Subspace|subspaces]] of $V$ that contain $S$. A **linear span** of any set is itself a subspace of $V$.

If $S$ is [[Cardinality of Sets#Finite Sets|finite]], then there's an equivalent definition of the ***linear span*** of $S$, namely: it is the set of all [[Vector Space#Linear Combination|linear combinations]] of $S$. More explicitly, if $S = \{ \pmb{v_{1}}, \pmb{v_{2}}, \dots, \pmb{v_{n}} \}$ then: $$span(S) = \left\{ a_{1}\pmb{v_{1}} + a_{2}\pmb{v_{2}} + \dots + a_{n}\pmb{v_{n}} \ | \ a_{1},a_{2},\dots,a_{n} \in F \right\}$$