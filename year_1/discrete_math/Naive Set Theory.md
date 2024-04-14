# Definitions
Naive set theory is a type of [[Set Theory|set theory]] which is characterised by its lack of rules regarding the construction of sets

As defined by [Greorg Cantor](https://en.wikipedia.org/wiki/Georg_Cantor), a set is a collection of definite and separate unique objects. There are no restrictions on how sets can be constructed.

# Problem
Russel's paradox proves a glaring hole in naive set theory.
He first defined the set $R$ that contains all sets that aren't members of themselves
$$R \triangleq \{ \ x \ \vert \ x \notin x \ \}$$
If this definition holds (as it does in naive set theory) then $R$ is both a member of itself, and is not a member of itself.
$$R \in R \iff R \notin R$$
Which is a logical contradiction, showing that the definition of $R$ can't hold, so naive set theory must be wrong.

# Solution
The general solution for this problem was to restrict what can be a set. Either the elements in a set have to be listed out (i.e. $\{ \ a_1,\dots,a_n \ \}$), or selected from an existing set (i.e. $\{ \ x \in A \ | \ P(x) \ \}$).

Some set constructions are exceptions, such as the union set. Those are accepted as axiomatic definition, chosen carefully to not lead to contradictions.

Using this new restriction, we can reformulate Russel's set as selecting from $S$ (the set of all sets) $$R \triangleq \{ \ x \in S \ | \ x \notin x \ \}$$
Which leads to the exact same paradox. However, we can now say thatt $R$ cannot be a set, and since it is selecting from $S$, it too cannot be a set. Thus, in this more well defined set theory, the set containing all sets does not exist.

Furthermore, when speaking of $\forall x \dots$ or $\exists x \dots$, you have to select from a set. You cannot speak of "all things", as it isn't well defined. This together with the fact that the set of all sets does not exist means that you might be able to show that some property $P(O)$ holds for an arbitrary set $O$ but cannot then say $\forall O ( \ P(O) \ )$ since we would need to select $O$ from the set of all sets, which does not exist.

The formal name of the most common solution is called [Zermelo–Fraenkel set theory](https://en.wikipedia.org/wiki/Zermelo%E2%80%93Fraenkel_set_theory) and it is what future mentions of [[Set Theory|set theory]] will follow.
