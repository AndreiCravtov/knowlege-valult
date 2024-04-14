***Neighbourhoods*** generalise the concept of *proximity*, for arbitrary [[Metric Space|metric spaces]]. We can think of *neighbourhoods* as regions where *nearby* points gather, capturing the idea of *closeness without strict boundaries*. 

# Formal Definition
Let $(M,d)$ be a [[Metric Space|metric space]]. Select a point $p \in M$, and a subset $V \subseteq M$.

## Neighbourhood of a Point
We say that $V$ is ***a neighbourhood of*** $p$, if there exists some $r>0$ such that *the [[Balls in Metric Spaces|open ball]] about $p$ of radius $r$* is a subset of $V$. In other words, we have the following: $$V \ \text{is} \ \underline{\textbf{a neighbourhood of}} \ p \ \ \iff \ \ \exists r>0: \ \ B(p;r) \subseteq V$$From this definition, we can see that for any $r>0$, $B(p;r)$ ***is*** a neighbourhood of $p$. In fact, $B(p;r)$ is a neighbourhood of ***any*** $x \in B(p;r)$.

We can visualise $V$ being ***a neighbourhood of*** $p$ as the following:
![[Pasted image 20240220200907.png|300]]

## Uniform Neighbourhood
If we take some set $S \subseteq M$, then we can say that $V$ is ***a uniform neighbourhood of*** $S$, if there exists some $r>0$ such that for every $p \in S$ *the [[Balls in Metric Spaces|open ball]] about $p$ of radius $r$* is a subset of $V$. In other words, we have the following: $$V \ \text{is} \ \underline{\textbf{a uniform neighbourhood of}} \ S \ \ \iff \ \ \exists r>0, \forall p \in S: \ \ B(p;r) \subseteq V$$
A special case of *a uniform neighbourhood of* $S$ is called the ***$r$-neighbourhood***. For some $r>0$, the ***$r$-neighbourhood*** of $S$ is the union *the [[Balls in Metric Spaces|open balls]] of radius $r$*, about every point in $S$. In other words, we have the following: $$S_{r} \ \text{is the} \ \underline{\textbf{$r$-neighbourhood of}} \ S \ \ \iff \ \ S_{r}= \bigcup_{p \in S} B(p;r)$$From this, we can deduce that $V \ \text{is} \ \underline{\textbf{a uniform neighbourhood of}} \ S \ \ \iff \ \ \exists r>0: \ \ S_{r} \subseteq V$.

We can visualise both: $V$ being ***a uniform neighbourhood of*** $S$ and the ***$r$-neighbourhood*** of $S$, with the below image. The dashed region *around* $S$ is the ***$r$-neighbourhood*** of $S$; we can see that $V$ *encloses* that dashed region.
![[Pasted image 20240220195732.png|300]]

## Complete System of Neighbourhoods
The collection $\mathcal{N_{p}}$ of *all neighbourhoods of $p$*, is called the ***complete system of neighbourhoods of $p$***, and is defined as: $$\mathcal{N_{p}} = \{ \ V \in \wp M \ | \ V \ \text{is} \ \underline{\textbf{a neighbourhood of}} \ p \ \}$$In this definition, we select [[Power Sets|all subsets]] of $M$ and keep only those that are ***a neighbourhood of*** $p$. The result is the set containing *all neighbourhoods of $p$*.

## Deleted Neighbourhood
Just like with [[Balls in Metric Spaces#Deleted Metric Ball|metric balls]], we can see that *a neighbourhood $V$ of $p$*, ***includes*** $p$. By ***deleting*** $p$ from the *neighbourhood*, we ***puncture*** it. Hence we call the *non-empty* set $V \setminus \{ p \}$ a ***deleted neighbourhood***, or ***punctured neighbourhood***. The distinction of **deleted** and **non-deleted** neighbourhoods comes in play with the [[Limit of a Function#Deleted vs non-Deleted Limits|definition of limits]].

# Related
## Neighbourhood of Infinity of Reals
When talking about the [[Real Numbers|reals]], we can extend the intuition behind of a [[#Neighbourhood of a Point|neighbourhoods]] of a point, to ***neighbourhoods of $\pm \infty$***. Given some $V \in \mathbb{R}$, we can say that:
$$
\begin{align}
V \ \text{is} \ \underline{\textbf{a neighbourhood of}} \ +\infty \ \ \iff \ \ \exists c \in \mathbb{R}, \forall x \in \mathbb{R}: \ \ x > c \implies x \in V \\
V \ \text{is} \ \underline{\textbf{a neighbourhood of}} \ -\infty \ \ \iff \ \ \exists c \in \mathbb{R}, \forall x \in \mathbb{R}: \ \ x < c \implies x \in V \\
\end{align}
$$
It is easy to see then, that for any $c \in \mathbb{R}$, the interval $(c,+\infty)$ is ***a neighbourhood of $+\infty$***, and the interval $(-\infty,c)$ is ***a neighbourhood of $-\infty$***. 