The fundamental theorem of calculus is a theorem that links the concept of [[Differentiation of Real Functions|differentiating]] and [[Riemann Integral|integrating]] a function, where the two operations are inverses of each other.

# Formal Definition
For some [[Continuity|continuous]] function $f: [a,b] \to \mathbb{R}$, we can define the function $F: [a,b] \to \mathbb{R}$ with $F(x) = \int^x_{a} f(y) \, dy$. $F$ will then be [[Uniform Continuity|uniformly continuous]] in $[a,b]$, and we have: $$\forall x \in (a,b)[ \ \ F'(x)=f(x) \ \ ]$$
## Changing Variables
From [[#Formal Definition|this]] we can show that, for some [[Differentiation of Real Functions#Differentiable Functions|differentiable]] function $g : [a,b] \to [c, d]$, where $g': [a,b] \to R$ is [[Continuity|continuous]], and for some [[Continuity|continuous]] function $f : [c, d] \to R$, we define $y=g(x)$. Hence: $$\int^b_{a} f(g(x))g'(x) \, dx = \int^{g(b)}_{g(a)} f(y)  \, dy $$
Which is an equality we can use when we want to change variables.
