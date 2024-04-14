Partial functions, as opposed to [[Mathematical Functions|total functions]], are a special kind of relation that assigns each element from of one set to at most one element of another set.

# Formal Definition
Let $f$ be a relation on $A\times B$. The relation $f$ is a partial function if every element in $A$ is mapped to at most one element in $B$: $$f \ \text{is a partial function} \triangleq \forall b_{1},b_{2} \in B ( \ \exists a \in A(\langle a,b_{1}\rangle \in f \wedge \langle a, b_{2} \rangle \in f) \implies b_{1} = b_{2} \ )$$
A partial function is said to be **undefined** for those elements of $A$ that do not map to an image in $B$. This **undefined** value is often referred to as $\bot$ (bottom). And so, for any partial function $f: A \to B$ can be extended to a total function $f: A \to B \cup \{ \bot \}$ by mapping all of the originally undefined elements the  $\bot$ element.

**NOTE:** although all total functions are also partial functions, when 'partial function' is used, it is assumed that we are talking about partial functions which are *not* total functions.
