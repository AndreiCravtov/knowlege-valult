# Ratio Test
This is a test for proving a [[Convergence of Sequences#Convergence to a Limit|sequence converges]]. It works by checking if a sequence converges to $0$ or not. This can be generalised to any sequence $a_{n}$ that converges to some limit $L$, by creating a second sequence $b_{n}=a_{n}-L$. If $b_{n}$ now converges to $0$ then $a_{n}$ converges to $L$.

## Formal definition
The sequence $a_{n}$ converges towards $0$ if the following holds: $$\exists c \in \mathbb{R} \ ( \ 0\leq c < 1 \ ), \exists N \in \mathbb{N} \ \text{such that} \ \forall n \geq N \ \left(  \ \left\lvert  \frac{a_{n+1}}{a_{n}}  \right\rvert \leq c  \  \right)$$
Here we just have to find one example of $c$ and $N$ for which this holds to prove that the sequence $a_{n}$ converges.
## Example usage
Consider for sequence $a_{n} = 3^{-n}$ (for all $n\geq 1$), we have: $$\left\lvert  \frac{a_{n+1}}{a_{n}}  \right\rvert = \left\lvert  \frac{3^{-(n+1)}}{3^{-n}}  \right\rvert = \left\lvert  \frac{3^{-n}\left( \frac{1}{3} \right)}{3^{-n}}  \right\rvert = \frac{1}{3} < 1$$
Thus if we chose $c = \frac{1}{3}$ and $N = 1$, then the ratio test definition holds and we can say that $a_{n}$ converges to $0$.

## Proof
Consider that we have a sequence $(a_{n})_{n\geq 1}$ that passes this test. Thus by definition, we have that for all $n>N$, 
$$
\begin{aligned}
\left\lvert  \frac{a_{n+1}}{a_{n}}  \right\rvert \leq c \implies |a_{n+1}| \leq c|a_{n}| \\
\text{and} \ |a_{n}| \leq c|a_{n-1}| \\
\text{and} \ |a_{n-1}| \leq c|a_{n-2}| \\
\dots \\
\text{and} \ |a_{N+1}| \leq c|a_{N}|
\end{aligned}
$$
So if we combine these inequalities, we get the following singular inequality: 
$$
\begin{gathered}
|a_{n}| \leq c|a_{n-1}| \leq c^2|a_{n-2}| \leq \dots \leq c^{n-N}|a_{N}| \\
\text{so} \\
|a_{n}| \leq c^{n-N}|a_{N}| = \frac{|a_{N}|}{c^N}c^n \\
\text{so} \\
|a_{n}| \leq \frac{|a_{N}|}{c^N}c^n
\end{gathered}
$$
Let $k = \frac{|a_{N}|}{c^N}c^n$ be a constant. Since we know that $0 \leq c < 1$, then the sequence $b_{n} = kc^n$ (for all $n>1$) converges to $0$ (which is easily provable), and the sequence $-b_{n}$ also converges to $0$. We then use that to bound $a_{n}$ like this: 
$$
\begin{gathered}
|a_{n}| \leq \frac{|a_{N}|}{c^N}c^n \\
-\frac{|a_{N}|}{c^N}c^n \leq a_{n} \leq \frac{|a_{N}|}{c^N}c^n \\
-kc^n \leq a_{n} \leq kc^n \\
-b_{n} \leq a_{n} \leq b_{n} \\
\end{gathered}
$$
Then using the [[Sandwich Theorem|sandwich theorem]] we can say that since both $-b_{n}$ and $b_{n}$ converge to $0$, and all $a_{n}$ are sandwiched between them, so $a_{n}$ must also converge to $0$.
# Limit Ratio Test
This is a test based on the [[#Ratio Test|ratio test]], and works by thinking about the limit of the ratio of consecutive terms. Sometimes the choice of $N$ and $c$ aren't very obvious with the [[#Ratio Test|ratio test]] alone, so this test is used instead to determine if a sequence converges to $0$.

## Formal definition
The sequence $a_{n}$ converges towards $0$ if the following holds: $$r=\lim_{ n \to \infty } \left\lvert  \frac{a_{n+1}}{a_{n}}  \right\rvert \ \ \ \ \text{and} \ \ \ \ r < 1 $$
## Example usage
Consider for sequence $a_{n} = \frac{1}{n!}$ (for all $n\geq 1$), we have: $$\left\lvert \frac{a_{n+1}}{a_{n}} \right\rvert = \left\lvert \frac{\frac{1}{(n+1)!}}{\frac{1}{n!}} \right\rvert = \left\lvert \frac{\frac{1}{n!}\left( \frac{1}{n+1} \right)}{\frac{1}{n!}} \right\rvert = \frac{1}{n+1}$$
So we take $r$ to be the limit of that final expression: $$r = \lim_{ n \to \infty } \left( \frac{1}{n+1} \right)_{n\geq 1} = 0 $$
Thus $r = 0 < 1$ and so the ratio limit test passes an we can say that $a_{n}$ converges to $0$.

## Proof
Consider that we have a sequence $(a_{n})_{n\geq 1}$ that passes this test. Thus by definition, we have a sequence $b_{n} = \rvert \frac{a_{n+1}}{a_{n}} \lvert$ such that $\lim_{ n \to \infty } b_{n} = r$, $r<1$. This means that for all $\varepsilon>0$ we can find some $N \in \mathbb{N}$ such that for all $n>N$ we have $|b_{n}-r|<\varepsilon$. We can unpack this inequality into: 
$$
\begin{gathered}
|b_{n}-r|<\varepsilon \\
-\varepsilon < b_{n} - r < \varepsilon \\
r-\varepsilon < b_{n} <r + \varepsilon
\end{gathered}
$$
Since $r<1$ then $\frac{1-r}{2} > 0$ so we can pick it as our $\varepsilon$. Thus for $\varepsilon = \frac{1-r}{2}$ there is some $N$ such that for all $n>N$, $r-\varepsilon < b_{n} <r + \varepsilon$ holds. Let this $N$ in particular be $N^{'}$. This simplifies to:
$$
\begin{gathered}
r - \varepsilon < b_{n} < r + \varepsilon \\
r - \frac{1-r}{2} < b_{n} < r + \frac{1-r}{2} \\
\frac{3r-1}{2} < b_{n} < \frac{r+1}{2}
\end{gathered}
$$
Since $r<1$ then, $\frac{r+1}{2} < 1$ also. Hence we can now apply the [[#Ratio Test#Formal definition|ratio test]], choosing $c = \frac{r+1}{2} < 1$ and $N=N^{'}$, we have:
$$
\begin{gathered}
b_{n} < \frac{r+1}{2} \\
\left\rvert \frac{a_{n+1}}{a_{n}} \right\lvert < \frac{r+1}{2} = c \\
\left\rvert \frac{a_{n+1}}{a_{n}} \right\lvert < c
\end{gathered}
$$
The above result holds for all $n>N=N^{'}$, and thus $a_{n}$ converges to $0$ according to the [[#Ratio Test#Formal definition|ratio test]].