
# Definitions
A set is a collection of items. The vast majority of maths is based on [Zermelo–Fraenkel set theory](https://en.wikipedia.org/wiki/Zermelo%E2%80%93Fraenkel_set_theory), so it's rules will be implicitly assumed when working with sets. 

When non-conventional rules are needed, they will be explicitly stated. Like for example [[Naive Set Theory|naive set theory]].

## Set construction
There are a few ways to construct sets:
- $\{ \ a_1,\dots,a_n \ \}$ which is just some, possibly arbitrary, enumerated collection of elements.
- $\{ \ x \in A \ | \ P(x) \ \}$ which means, all elements of $A$ which also satisfy the predicate $P$. This is known as the axiom of comprehension.
- $\{ \ x \ | \ P(x) \ \}$ which means, all objects in existence which satisfy the predicate $P$. This form of construction must be avoided unless it is an axiomatic assertion. For an explanation of why, see [[Naive Set Theory#Problem|naive set theory]].

Sets are defined with the $\triangleq$ symbol. This means it is an equality you don't have to check
i.e.
- $\mathbb{N} \triangleq \{ \ 1,2,3, \dots \ \}$ 
- $\emptyset \triangleq \{ \}$ 
and so on...
## Set operations
There are quite a few operations and symbols defined for sets. Here are a few of them. Notice how some of these definitions are axiomatic, for example the definition of $A \cup B$, while others are constructed using these axiomatic definitions, like $A \cap B$.
### Comparisons
- $A \subseteq B \triangleq \forall x \in A ( \ x \in B \ )$
- $A \subset B \triangleq A \subseteq B \ \wedge \ B \not\subseteq A$
- $A = B \triangleq A \subseteq B \ \wedge \ B \subseteq A$

### Creating Sets
- $A \cup B \triangleq \{ \ x \ \vert \ x \in A \ \vee \ x \in B \ \}$ 
- $A \cap B \triangleq \{ \ x \in A \cup B \ \vert \ x \in A \ \wedge \ x \in B \ \}$
- $A \setminus B \triangleq \{ \ x \in A \cup B \ \vert \ x \in A \ \wedge \ x \notin B \ \}$
- $A \ \Delta \ B \triangleq (A \setminus B) \cup (B \setminus A)$
- $A,B \ \text{are disjoint} \triangleq A \cap B = \emptyset$
- $\wp A \triangleq \{ \ V \ | \ V \subseteq A \ \}$ (see [[Power Sets|power sets]])
- $A \times B \triangleq \{ \ \langle a, b \rangle \ | \ a \in A \ \wedge \ b \in B \ \}$ (see [[Cartesian Products|Cartesian product]])

## Properties of operators
Here are a few properties of the operators introduced above. Each of these can be rigorously proven.
$$
\begin{gathered}

\begin{gathered}[c]
\text{Idempotence} \\
A \cup A = A \\
A \cap A = A
\end{gathered}
\ \ \ \ \
\begin{gathered}[c]
\text{Commutativity} \\
A \cup B = B \cup A \\
A \cap B = B \cap A \\
A \Delta B = B \Delta A
\end{gathered}
\ \ \ \ \
\begin{gathered}[c]
\text{Associativity} \\
A \cup (B \cup C) = (A \cup B) \cup C \\
A \cap (B \cap C) = (A \cap B) \cap C \\
\end{gathered}
\\
\begin{gathered}[c]
\text{Empty set} \\
A \cup \emptyset = A \\
A \cap \emptyset = \emptyset \\
A \Delta A = \emptyset
\end{gathered}
\ \ \ \ \
\begin{gathered}[c]
\text{Distributivity} \\
A \cup (B \cap C) = (A \cup B) \cap (A \cup C) \\
A \cap (B \cup C) = (A \cap B) \cup (A \cap C) \\
\end{gathered}
\ \ \ \ \
\begin{gathered}[c]
\text{Absorption} \\
A \cup (A \cap B) = A \\
A \cap (A \cup B) = A \\
\end{gathered}

\end{gathered}
$$
