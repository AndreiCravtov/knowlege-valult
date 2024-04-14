A ***Normed vector space*** is a [[Vector Space|vector space]] together with a way to measure the *"length"* of it's vectors (called the **Norm** of vectors).

# Formal Definition
Given a [[Vector Space|vector space]] $V$ over [[Field#Subfield|subfield]] $F$ of the [[Complex Numbers|complex numbers]] $\mathbb{C}$, it becomes a ***Normed vector space*** when equipped with a function $\lvert \lvert \cdot \rvert \rvert: V \to \mathbb{R}$, called the ***Norm***, such that the *Norm* satisfies these properties:
- **Triangle inequality:** $\lvert \lvert \pmb u + \pmb v \rvert \rvert \leq \lvert \lvert \pmb u \rvert \rvert + \lvert \lvert \pmb v \rvert \rvert$, for all $\pmb u, \pmb v \in V$.
- **Absolute homogeneity**: $\lvert \lvert a \pmb v \rvert \rvert = \lvert a \rvert \cdot \lvert \lvert \pmb v \rvert \rvert$ for all $\pmb v \in V$ and all $a \in F$.
- **Positive definiteness:** $\lvert \lvert \pmb v \rvert \rvert = 0 \iff \pmb v = \pmb 0$, for all $\pmb v \in V$.
In the above $|a|$ is the [[Absolute value|absolute value]] of scalar $a$, and $\pmb 0 \in V$ is the zero vector.

## Induced Metric
A norm induces a [[Metric Space#Formal Definition|metric]], called its **(norm) induced metric**, by the formula $$d(x,y) = \lvert \lvert y-x \rvert  \rvert $$which makes any *Normed vector space* into a [[Metric Space|metric space]].

# Properties
## Unit Vector
A ***unit vector*** a vector of length $1$, or "unit". If we have a *Normed vector space* $V$, then the for any $\pmb v \in V$, the **unit vector** $\pmb{\hat{v}}$ is $$\pmb {\hat{v}} = \frac{\pmb v}{\lvert \lvert \pmb v \rvert  \rvert }$$
