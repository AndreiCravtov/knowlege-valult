
The sandwich theorem is a result that makes it easier to prove that some [[Convergence of Sequences#Convergence to a Limit|sequence is convergent]] to a limit. But to use it, you need two different *known* sequences that both converge to the same limit, and they must bound the unknown sequence.

# Theorem
Let $(l_{n})_{n\geq 1}$ and $(u_{n})_{n\geq 1}$ such that $l_{n} < u_{n}$ and $\lim_{ n \to \infty } l_{n} = L$ and $\lim_{ n \to \infty} u_{n} = L$. Then suppose some sequence $(a_{n})_{n\geq 1}$, then we have:
$$\exists N \in \mathbb{N} \ \text{such that} \ \forall n\geq N \ ( \ l_{n} \leq a_{n} \leq u_{n} \ ) \implies \lim_{ n \to \infty } a_{n} = L $$
The way to visualise it is like this:
```desmos-graph
left=-1; right=51;
top=0.1; bottom=-0.01;
---
n = 55
N = [1,2,...n]
u(x)=\frac{1}{x} | hidden
a(x)=\frac{1}{2x} | hidden
l(x)=\frac{1}{8x} | hidden
(N, u(N)) | red
(N, a(N)) | green
(N, l(N)) | blue
```
The upper and lower bounding sequences converge to $L=0$, so the sequence that is sandwiched between them also converges to $L=0$.

## Proof of Theorem
Let $(l_{n})_{n\geq 1}$ and $(u_{n})_{n\geq 1}$ such that $l_{n} < u_{n}$ and $\lim_{ n \to \infty } l_{n} = L$ and $\lim_{ n \to \infty} u_{n} = L$. Then suppose some sequence $(a_{n})_{n\geq 1}$ exists. From the definition of a converging sequence, we can find $N_{1}$ and $N_{2}$ such that for all $n>N_{1}$ we have $|l_{n}-L|<\varepsilon$, and for all $n>N_{2}$ we have $|u_{n}-L|<\varepsilon$.
Then we take $N^{'}=max(N_{1}, N_{2})$, so that $N^{'}>N_{1},N_{2}$. So let $n>N^{'}$, then we know that $|l_{n}-L|<\varepsilon$ and $|u_{n}-L|<\varepsilon$ simultaneously.
Therefore, this together with the fact that $l_{n} < u_{n}$ gives us:
$$
\begin{gathered}
|l_{n}-L|<\varepsilon \iff -\varepsilon<l_{n}-L<\varepsilon \\
\text{and} \\
|u_{n}-L|<\varepsilon \iff -\varepsilon<u_{n}-L<\varepsilon \\
\text{so} \\
L - \varepsilon < l_{n} < L + \varepsilon \ \ \text{and} \ \ L - \varepsilon < u_{n} < L + \varepsilon \\
\text{so} \\
L-\varepsilon<l_{n}<u_{n}<L+\varepsilon
\end{gathered}
$$
We know by assumption of the sandwich theorem, that this holds for $a_{n}$: $$\exists N \in \mathbb{N} \ \text{such that} \ \forall n\geq N \ ( \ l_{n} \leq a_{n} \leq u_{n} \ )$$
Hence, for all $n > max(N, N^{'})$ we conclude that: 
$$
\begin{gathered}
L-\varepsilon < l_{n} \leq u_{n} \leq u_{n} < L+\varepsilon \\
L-\varepsilon < u_{n} < L+\varepsilon \\
-\varepsilon < u_{n} - L < \varepsilon \\
|u_{n} - L| < \varepsilon
\end{gathered}
$$
Since the $n$ was an arbitrary natural number larger than $max(N,N^{'})$, this proves that $a_{n}$ converges to $l$ as it meets the convergence definition.

# Using the Theorem
# Example: $a_{n} = \frac{\sin n}{n}$
We can see that $a_{n}$ oscillates around it's limit of $L=0$. We therefore create $l_{n} = -\frac{1}{n}$ and $u_{n} = \frac{1}{n}$, which both converge to $L=0$, in order to help us prove it.
```desmos-graph
left=-1; right=51;
top=0.1; bottom=-0.1;
---

n = 55
N = [1,2,...n]

u(x) = 1/x | hidden
a(x) = \sin(x)/x | x > 0 | green
l(x) = -1/x | hidden

(N, u(N)) | red
(N, a(N)) | green
(N, l(N)) | blue
```
We know (can easily prove) that both $\lim_{ n \to \infty } l_{n} = 0$ and $\lim_{ n \to \infty } u_{n} = 0$. We also know that the $\sin n$ function has a property that $-1 \leq \sin x \leq 1$. Which means $-\frac{1}{n} \leq \frac{\sin n}{n} \leq \frac{1}{n}$. So this inequality holds for all $n$ including $n > N$, which means that the sandwich theorem is satisfied and $a_{n}$ also converges to $L=0$.