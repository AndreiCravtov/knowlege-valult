A group action can be thought of as a transformation that a [[Group|group]] can perform on some other set, including itself. For instance, [[Real Numbers|real]] addition $(+)$ can be thought of as a group action, because the group of real numbers can perform *addition transformation* on real numbers.

# Formal Definition
A group actions can be split into *left* and *right*. If the group is [[Group#Abelian group|commutative]], then there isn't a meaningful difference between the two.

## Left Group Action
If $G$ is a [[Group|group]] with the identity element $e \in G$, and $X$ is a set, then a (left) group action $\alpha$ of $G$ on $X$ is a [[Mathematical Functions|function]] $\alpha: G \times X \to X$, that satisfies these axioms for all $g,h \in G, x \in X$:
$$
\begin{align}
\text{Identity:} &&& \alpha(e,x) = x \\
\text{Compatibility:} &&& \alpha(g, \alpha(h, x)) = \alpha(gh, x)
\end{align}
$$
If the action $\alpha$ is obvious from the context, then it can be replaced by $(\cdot)$ notation as such: 
$$
\begin{align}
e \cdot x = x \\
g \cdot (h \cdot x) = (gh) \cdot x
\end{align}
$$
## Right Group Action
If $G$ is a [[Group|group]] with the identity element $e \in G$, and $X$ is a set, then a (right) group action $\alpha$ of $G$ on $X$ is a [[Mathematical Functions|function]] $\alpha: X \times G \to X$, that satisfies these axioms for all $g,h \in G, x \in X$:
$$
\begin{align}
\text{Identity:} &&& \alpha(x,e) = x \\
\text{Compatibility:} &&& \alpha(\alpha(x,g),h) = \alpha(x, gh)
\end{align}
$$
If the action $\alpha$ is obvious from the context, then it can be replaced by $(\cdot)$ notation as such: 
$$
\begin{align}
x \cdot e = x \\
(x \cdot g) \cdot h = x \cdot (gh)
\end{align}
$$
# Properties
## Free Group Action
The group action $(\cdot)$ of $G$ on $X$, is called ***free*** if, for all $g \in G$ we have $$\exists x \in X \bigg[g \cdot x = x \bigg] \implies g = e_{G}$$
For example, we can say that [[Real Numbers|real]] addition is a *free* action, since the statement $a + b = b$ would imply that $a = 0$, for all $a \in \mathbb{R}$ where such a $b \in \mathbb{R}$ exists.

## Transitive Group Action
The group action $(\cdot)$ of $G$ on $X$, is called ***transitive*** if, for any $x,y \in X$, there exists some $g \in G$ such that $$g \cdot x = y$$For example, we can say that [[Real Numbers|real]] addition is a *transitive* action, because for any $a,b \in \mathbb{R}$, we define $c = b - a$, and hence $a + c = b$ holds.