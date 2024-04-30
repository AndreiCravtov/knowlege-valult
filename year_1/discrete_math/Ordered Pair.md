#set-theory

An ***ordered pair*** $\opair{a}{b}$ is a pair of objects. The order in which the objects appear in the pair ***is*** significant: the ordered pair $\opair{a}{b}$ is different from the ordered pair $\opair{b}{a}$ unless $a=b$. 

The the ***characteristic*** (or ***defining***) *property* of ***ordered pairs*** is:
$$\large \opair{a_{1}}{b_{2}} = \opair{a_{2}}{b_{2}} \iff a_{1} = a_{2} \wedge b_{1} = b_{2}$$

# Formal Definition
Others exist, but the ***accepted*** definition proposed by [Kuratowski](https://en.wikipedia.org/wiki/Kazimierz_Kuratowski) is
$$\large \opair{a}{b} \ \ \triangleq \ \ \{ \{ a \}, \{ a, b \} \}$$
When $a = b$, you get
$$\large \opair{a}{a} = \{ \{ a \}, \{ a, a \} \} = \{ \{ a \}, \{ a \} \} = \{ \{ a \} \}$$

Given some ***ordered pair*** $\opair{a}{b}$, the property $a \ \text{is the first component of} \ \opair{a}{b}$ is formulated as
$$\large \forall C \in \opair{a}{b}: \ \ a \in C$$
The property $b \ \text{is the second component of} \ \opair{a}{b}$ can be formulated as:
$$\large \exists C \in \opair{a}{b}: \ \ b \in C \ \ \ \ \wedge \ \ \ \ \forall C_{1},C_{2} \in \opair{a}{b}: \ \ C_{1} \ne C_{2} \implies b \not\in C_{1} \vee b \not\in C_{2}$$

Observe that for some ***ordered pair*** $\opair{a}{b}$, we have
$$\large
\begin{align}
&\bigcap \opair{a}{b} = \bigcap \Big\{ \{ a \}, \{ a, b \}  \Big\} = \{ a \} \cap \{ a, b \} = \{ a \} \\
&\bigcup \opair{a}{b} = \bigcup \Big\{ \{ a \}, \{ a, b \}  \Big\} = \{ a \} \cup \{ a, b \} = \{ a, b \}
\end{align}
$$
Which means we can extract the ***first*** and ***second*** components like this
$$\large
\begin{align}
\project{1} \opair{a}{b} &= \bigcup \bigcap \opair{a}{b} \\
&= \bigcup \{ a \} \\
&= a \\
\project{2} \opair{a}{b} &= \bigcup \Big\{ \ X \in \bigcup \opair{a}{b} \ \Big| \ \bigcup \opair{a}{b} \neq \bigcap \opair{a}{b} \implies X \not\in \bigcap \opair{a}{b} \ \Big\} \\
&= \bigcup \Big\{ \ X \in \{ a, b \} \ \Big| \ \{ a, b \} \neq \{ a \} \implies X \not\in \{ a \} \ \Big\} \\
&= \bigcup \{ b \} \\
&= b
\end{align}
$$
But in *practice* we can just *"destructure"* ***ordered pairs***, i.e $\opair{a}{b} \in X$, with it being *"syntax sugar"* for the above expressions
