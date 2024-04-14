If a set of $n$ distinct objects are partitioned into $k$ subsets, such that $0 < k < n$, then at least one subset will contain $\geq 2$ elements.

# Formal Proof
Let $|A|=n$, and $P_{A} = \{ A_{1},\dots,A_{k} \}$ be a [[Set Partitions|partition]] of $A$, so each $A_{i}$ is non-empty.

**A1:** Assume that each $A_{i}$ has exactly one element.

Therefore $|A_{i}| = 1$. Since $A = U^{k}_{i=1} A_{i}$, we know that $|A| = |U^{k}_{i=1} A_{i}|$, with $A_{i}$ pairwise disjoint, so $|A| = U^{k}_{i=1} |A_{i}|$. Since $|A|=n$ and $U^{k}_{i=1} |A_{i}| = k$, we have that $n=k$, which contradicts $n > k$. Reject **A1**. Not all $A_{i}$ have exactly one element. Since $A_{i}$ are non-empty, then some $A_{i}$ must have $\geq2$ elements.