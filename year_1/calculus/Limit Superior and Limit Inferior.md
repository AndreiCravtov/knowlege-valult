Using the definition of [[Convergence of Sequences#Convergence to a Limit|convergence to limits]], as well as [[Infimum and supremum|supremum and infimum]], we can define the notions of the ***Limit Superior***, or $\lim \sup$, and ***Limit Inferior***, or $\lim \inf$, of [[Sequences|sequences]]. Begin by taking some sequence $a_{n}: \mathbb{N} \to \mathbb{R}$ and using it to construct two secondary sequences: 
$$
\begin{gathered}
(S_{n})_{n\geq 0} = \sup \{\ a_{N} \ | \ N \in \mathbb{N} \text{ such that } N \geq n \ \} \\
(I_{n})_{n\geq 0} = \inf \{\ a_{N} \ | \ N \in \mathbb{N} \text{ such that } N \geq n \ \}
\end{gathered}
$$
Each of the terms of the sequences represents the maximum (or supremum) and minimum (or infimum) of the original sequence's tail, respectively.
For example, for sequence $(a_{n})_{n\geq 1} = \frac{1}{x}\cos\left( \frac{10x}{\pi} \right)$, we can see the corresponding terms $S_{1}, L_{1}, S_{5}, L_{5}, S_{9}, L_{9}$ are circled. They are the maximum and minimum of each of the tails formed by the choice of $n$, respectively.
```desmos-graph
left=-1; right=17;
top=2; bottom=-2;
---
x=1 | #0000ff
(1.75, 1.5) | hidden | label:`n=1` | #0000ff
10(y+1)^2+(x-1)^2=0.1 | #0000ff 
10(y-0.5)^2+(x-2)^2=0.1 | #0000ff 

x=5 | #5555ff
(5.75, 1) | hidden | label:`n=5` | #5555ff
10(y+0.2)^2+(x-5)^2=0.1 | #5555ff
10(y-0.16)^2+(x-6)^2=0.1 | #5555ff

x=9 | #7777ff
(9.75, 0.5) | hidden | label:`n=9` | #7777ff
10(y+0.1)^2+(x-9)^2=0.1 | #5555ff
10(y-0.09)^2+(x-10)^2=0.1 | #5555ff

n = 15
N = [1,2,...n]
a(x) = 1/x*\cos(\frac{10x}{\pi}) | hidden
(N, a(N)) | red
```
We can then use $S_{n}, L_{n}$ to define the $\lim \sup$ and $\lim \inf$ as such: 
$$
\begin{gathered}
\limsup_{n\to \infty } a_{n} = \lim_{ n \to \infty } S_{n} \\
\liminf_{n\to \infty } a_{n} = \lim_{ n \to \infty } I_{n} \\
\end{gathered}
$$
Which can be read as, the **Limit Superior** is the limit of the sequence of maximums, and the **Limit Inferior** is the limit of the sequence of minimums, of some given common sequence.

**NOTE:** Because *Limit Superiors* and *Inferiors* use [[#Convergence to a Limit]] under the hood, they can converge to [[Convergence of Sequences#Convergence to Infinity|infinity]]

## Results With $\lim\sup$ and $\lim \inf$
### Relation to $\lim$
One of the results of these two operations is their correspondence with the regular [[#Convergence to a Limit|limit of a sequence]], namely for some $a_{n}: \mathbb{N} \to \mathbb{R}$ $$\liminf_{n\to \infty} a_{n} = \limsup_{n\to \infty} a_{n} = L \iff \lim_{ n \to \infty } a_{n} = L $$
Which means that once you found the limit of a sequence, you can be pretty sure that the *limit superiors* and *inferiors* are of the same value. Conversely, if you found that the *limit superior* and *inferior* are of the same value, that means the limit is of that value too.