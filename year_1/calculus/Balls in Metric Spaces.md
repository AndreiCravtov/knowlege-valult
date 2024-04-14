***Metric balls*** generalise the concept of *equidistance* to arbitrary [[Metric Space|metric spaces]]. They represent sets of points that are all within a certain distance - *radius*, from a central point. Intuitively, we can conceptualise it as a circle or sphere; that is where the name ***ball*** comes from. 
![[Pasted image 20240220173837.png|400]]

# Formal Definition
Let $(M,d)$ be a [[Metric Space|metric space]]. Select a ***central point*** $c \in M$, and a ***radius*** $r>0$. There are two *types of balls*: ***open*** and ***closed***; ***open balls*** exclude the *boundary points*, while ***closed balls*** include them. A *boundary point* $x \in M$ is one for which $d(x,c)=r$. We define both as:
$$
\begin{align}
\text{The} \ \underline{\textbf{open ball about}} \ c \ \underline{\textbf{of radius}} \ r && \triangleq &&& B(c;r) = \{ x \in M \ | \ d(x,p) < r \} \\
\text{The} \ \underline{\textbf{closed ball about}} \ c \ \underline{\textbf{of radius}} \ r && \triangleq &&& B[c;r] = \{ x \in M \ | \ d(x,p) \leq r \}
\end{align}
$$
A ***unit ball*** (*open* or *closed*) is a ***ball*** of radius $1$.

## Deleted Metric Ball
Notice that according to the above definitions, we have $c \in B(c;r) \subseteq B[c;r]$; the ***central point*** $c$ is included within the *ball*. By ***deleting*** the *central point* $c$ from the *ball*, we ***puncture*** it. Hence we call the *non-empty* set $B(c;r) \setminus \{ r \}$ or $B[c;r] \setminus \{ r \}$, a ***deleted ball***, or ***punctured ball***.