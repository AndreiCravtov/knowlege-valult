Continuity is the idea that small changes of *inputs to a function* result in small changes to the *output of that function*; there are no abrupt changes in value - known as discontinuities. This concept requires that the [[Mathematical Functions#Domains, co-domains, ranges|domain and range]] of the function are [[Metric Space|metric spaces]], since measuring changes in input and output require a notion of *distance*.

# Formal definition
Let $(X,d_{X})$ and $(Y,d_{Y})$ be [[Metric Space|metric spaces]], and let $f:X \to Y$ be a function. We can now say that for any $x_{0} \in X$ $$f \ \text{is continuous at} \ x_{0} \ \triangleq \ \forall \varepsilon>0,\exists \delta>0,\forall x \in X: \ \ d_{X}(x,x_{0}) < \delta \implies d_{Y}(f(x),f(x_{0}))<\varepsilon$$
and if $f$ is continuous for every $x_{0} \in X$, then we say that it is ***continuous***: $$f \ \text{is continuous} \ \triangleq \ \forall x_{0} \in X: \ \ f \ \text{is continuous at} \ x_{0}$$
## Limit Definition
We can notice that the definition of ***continuity*** is similar to [[Limit of a Function#Finite Limit at a Point|the definition of limits]]. In fact, we can write an *equivalent* the definition of continuity for any $x_{0} \in X$ using [[Limit of a Function#Deleted vs non-Deleted Limits|deleted limits]] like this: $$f \ \text{is continuous at} \ x_{0} \ \triangleq \ \lim_{ x \to x_{0} } f(x) = f(x_{0})$$and if we are talking about a [[Limit of a Function#Deleted vs non-Deleted Limits|non-deleted limit]], then the existence of *any* limit $L \in Y$ at $x \in X$ would imply that $L=f(x_{0})$ and $f$ is continuous at $x_{0}$:
$$
\begin{align}
\exists L \in Y: \lim_{ x \to x_{0} } f(x) = L && \iff && \lim_{ x \to x_{0} } f(x) = f(x_{0}) \\
&& \iff && f \ \text{is continuous at} \ x_{0}
\end{align}
$$
The limit definitions make it *very obvious* that if $f$ ***approaches*** a point, then ***it is*** that point 
![[Pasted image 20240208204335.png|400]]

## Open Ball Definition
We can also rewrite the definition of continuity in terms of [[Balls in Metric Spaces|open balls]]. More specifically, the definition of continuity for any $x_{0} \in X$ is: $$f \ \text{is continuous at} \ x_{0} \ \triangleq \ \forall \varepsilon>0,\exists \delta>0: \ \ f[B(x_{0};\delta)] \subseteq B(f(x_{0});\varepsilon)$$That is, for every $\varepsilon>0$ I can find, you must give me a $\delta>0$ such that the [[Mathematical Functions#Image Sets|image]] of $B(x_{0};\delta)$ under $f$ is a *subset* of $B(f(x_{0});\varepsilon)$.

# Properties of Continuity
## Composing Continuous Functions
Because continuity can be [[#Limit Definition|defined with limits]], we can apply [[Limit of a Function#Limit Composition Theorem|limit composition]] to *continuous* functions.

Let $(X,d_{X})$ and $(Y,d_{Y})$ and $(Z, d_{Z})$ be [[Metric Space|metric spaces]]. Consider the functions $f: A \to B_{1}$ and $g: B_{2} \to C$, where $A \subseteq X$ and $B_{1},B_{2} \subseteq Y$ and $C \subseteq Z$ and $f[A] \subseteq B_{2}$ (the [[Mathematical Functions#Image Sets|image set]] of $f$ is a subset of $g$'s [[Mathematical Functions#Domains, co-domains, ranges|domain]]). If $f$ is **continuous** at $x_{0} \in A$, and $g$ is **continuous** at $f(x_{0}) \in B_{2}$, then $g \circ f$ is *continuous* at $x_{0} \in A$. This can be expressed [[#Limit Definition|in terms of limits]] like this:
$$\lim_{ x \to x_{0} } f(x) = f(x_{0}), \lim_{ x \to f(x_{0}) } g(x) = g(f(x_{0})) \ \ \ \ \implies \ \ \ \ \lim_{ x \to x_{0} } g(f(x))= g(f(x_{0})) $$

When working with [[Real Numbers|real]] continuous functions, we can apply [[Limit of a Function#Examples|these results]] to them. More formally, let $f: A \to B_{1}$ and $g: A \to B_{2}$ — with $A,B_{1},B_{2} \subseteq \mathbb{R}$, be functions *continuous* at $x_{0} \in A$. Then, for any $\lambda \in \mathbb{R}$, then we get:
- For any $\lambda \in \mathbb{R}$, $\ \lambda f$ is *continuous* at $x_{0}$
- The combination $f \pm g$ is *continuous* at $x_{0}$
- The product $f \cdot g$ is *continuous* at $x_{0}$
- When $g(x_{0}) \ne 0$, $\frac{f}{g}$ is *continuous* at $x_{0}$
When $f$ and $g$ are *continuous* (i.e. for all $x_{0} \in A$), then the above results become:
- For any $\lambda \in \mathbb{R}$, $\ \lambda f$ is *continuous*
- The combination $f \pm g$ is *continuous*
- The product $f \cdot g$ is *continuous*
- When $0 \not\in g[A]$, $\frac{f}{g}$ is *continuous*

## Minima and Maxima
For some continuous function $f:I \to \mathbb{R}$ (where $I=[a,b]$), the [[Mathematical Functions#Image Sets|image set]] of $f$ is denoted by $f[I]$. Then it is true that: $$\exists s,i \in I: \ \ f(s) = \sup \{ f[I] \} \ \text{ and } \ f(i) = \inf \{ f[I] \}$$What this is saying is that all real functions over a [[Infimum and supremum#Formal definition|bounded]] closed interval attain their [[Infimum and supremum|supremum and infimum]] within that closed interval.

## Intermediate Value theorem
The idea is that a continuous function takes all values between any pair of it's values. So for some continuous function $f: [a,b] \to \mathbb{R}$, define $m=\min\{ f(a), f(b) \}$ and $M = \min \{ f(a), f(b) \}$, hence we have: $$\exists s \in \mathbb{R}, \exists c \in (a,b): \ \ m < s < M \implies f(c)=s$$This means that: there exists some $s \in \mathbb{R}$ such that if $m < s < M$, then there exists a $c \in (a,b)$ where $f(c)=s$.