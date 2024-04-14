Sequences are [[Mathematical Functions|functions]] of the type $f: \mathbb{N} \to X$, which associate natural numbers to the elements of some set $X$. The most common type of sequence is $f: \mathbb{N} \to \mathbb{R}$.

It is convenient to define sequences over the positive natural numbers (1, 2, 3, ...) instead, to avoid to division by zero, so the function signature looks like this $f: \mathbb{N^+} \to \mathbb{R}$.

Using function notation for sequences can get cumbersome, so we use sequence notation, $a_{n} = f(n)$, where $a_{1}, a_{2}, \dots,$ are called *terms* of the sequence. The subscript for each term is called the *index variable*, or *index parameter*.

**NOTE:** be careful, don't make it ambiguous if we are referring to the function $a_{n}$ or the term of the sequence $a_{n}$ for the *index variable* of $n$.

# Examples
- $f: \mathbb{N^+} \to \mathbb{R}, \ f: n \mapsto \frac{1}{n}$, also written as $\left( \frac{1}{n} \right)_{n \geq 1}$, is a sequence: $$1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \frac{1}{5}, \dots$$
- $f: \mathbb{N} \to \mathbb{R^2}, \ f: n \mapsto \langle n, n \rangle$, also written as $(\langle n, n \rangle)_{n \geq 0}$, is a sequence: $$\begin{pmatrix} 0 \\ 0 \end{pmatrix},
\begin{pmatrix} 1 \\ 1 \end{pmatrix},
\begin{pmatrix} 2 \\ 2 \end{pmatrix},
\begin{pmatrix} 3 \\ 3 \end{pmatrix},
\begin{pmatrix} 4 \\ 4 \end{pmatrix}, \dots$$
 $f: \mathbb{N} \to \{ \text{cat}, \text{dog} \}, \ f: n \mapsto \text{cat}$, also written as $\left( \text{cat} \right)_{n \geq 0}$, is a sequence: $$\text{cat}, \text{cat}, \text{cat}, \dots$$
 
