#abstract-algebra 

A group action can be thought of as a transformation that a [[Group|group]] can perform on some other set, including itself. For instance, [[Real Numbers|real]] addition $(+)$ can be thought of as a group action, because the group of real numbers can perform *addition transformation* on real numbers.

The reason we make ***group actions*** is that we usually want to <u>separate</u> the *particular transformations* found in algebraic structures, and <u>distil</u> them into their own *(usually multiplicative)* [[Group|group]] under *(usually)* [[Mathematical Functions#Function Composition|function composition]]. Thus we can study their properties <u>independently</u> from their *"natural habitat"* - and when we are ready to reintegrate them we can define that as an ***action*** that this <u>group</u> performs on its algebraic structure.

A ***group action*** on a [[Vector Space|vector space]] is called a [representation](https://en.wikipedia.org/wiki/Group_representation "Group representation") of the <u>group</u>. In the case of a finite-dimensional vector space, it allows one to *identify* many <u>groups</u> with [[Group#Subgroup|subgroups]] of [[Invertible Matrix#General Linear Group of Invertible Matrices $ operatorname{GL}_{n}(F)$|general linear group]] $\operatorname{GL}_{n}(F)$ of $n \times n$ [[Invertible Matrix|invertible matrices]] over [[Field|field]] $F$.

# Formal Definition
A group actions can be split into *left* and *right*. If the [[Group|group]] is [[Group#Abelian group|commutative]], then there isn't a difference between the two.
## Left Group Action
If $G$ is a [[Group|group]] with the identity element $e \in G$, and $X$ is a nonempty set, then a ***(left) group action*** $\alpha$ of $G$ on $X$ is a [[Mathematical Functions|function]] $\alpha: G \times X \to X$, that satisfies these <u>axioms</u> for all $g,h \in G, x \in X$:
$$\large
\begin{align}
\text{Identity:} && \alpha(e,x) &= x \\
\text{Compatibility:} && \alpha(g, \alpha(h, x)) &= \alpha(gh, x)
\end{align}
$$
The <u>group</u> $G$ is then said to ***act on $X$ from the left***. A set $X$ together with an action of $G$ is called a ***(left) $G$-set***. 

It can be <u>notationally convenient</u> to [[Mathematical Functions#Currying, Uncurrying, and Partial Application|apply currying]] to ***action*** $\alpha: G \times X \to X$. The resulting function $\mathtt{curry}(\alpha): G \to (X \to X)$ assigns each $g \in G$ its <u>unique</u> [[Mathematical Functions#Bijective Functions|bijection]] $\sub{\alpha}{g}:X \to X$ via [[Mathematical Functions#Currying, Uncurrying, and Partial Application|partial application]] $\sub{\alpha}{g} = \mathtt{curry}(\alpha)(g)$. The ***identity*** and ***compatibility*** <u>axioms</u> then become
$$\large
\begin{align}
\text{Identity:} && \sub{\alpha}{e}(x) &= x \\
\text{Compatibility:} && \sub{\alpha}{g}(\sub{\alpha}{h}(x)) &= (\sub{\alpha}{g} \circ \sub{\alpha}{h})(x) = \sub{\alpha}{gh}(x)
\end{align}
$$
where $\circ$ is [[Mathematical Functions#Function Composition|function composition]]. The ***compatibility*** <u>axiom</u> can be shortened to $(\sub{\alpha}{g} \circ \sub{\alpha}{h}) = \sub{\alpha}{gh}$ and states that the <u>function composition</u> is compatible with the <u>group multiplication</u>; they form a [commutative diagram](https://en.wikipedia.org/wiki/Commutative_diagram "Commutative diagram"). 

If ***action*** $\alpha$ is obvious from the context, it can be replaced by a dot $(\cdot): G \times X \to X$ or with nothing at all, with the ***identity*** and ***compatibility*** <u>axioms</u> then becoming
$$\large
\begin{align}
\begin{aligned}
e \cdot x &= x \\
g \cdot (h \cdot x) &= (gh) \cdot x
\end{aligned} &&&&
\begin{aligned}
\sub{}{e}(x) &= x \\
\sub{}{g}(\sub{}{h}(x)) &= \big({\sub{}{g}(\cdot)} \circ {\sub{}{h}(\cdot)} \big)(x) = {\sub{}{gh}(x)}
\end{aligned}
\end{align}
$$
Therefore, for every $g \in G$ and its <u>inverse element</u> $g^{-1} \in G$, the <u>bijections</u> $\sub{\alpha}{g}, \sub{\alpha}{g^{-1}}$ are [[Mathematical Functions#Function Inverses|functional inverses]] i.e. $\sub{\alpha}{g} =  (\sub{\alpha}{g^{-1}})^{-1}$. Thus an *equivalent* definition is: for any [[Group#Group Homomorphism|group homomorphism]] $\mathtt{curry}(\alpha)$ from $G$ into [[Group#Symmetric Group of a Set $ operatorname{Sym}(X)$|symmetric group]] $\operatorname{Sym}(X)$, we [[Mathematical Functions#Currying, Uncurrying, and Partial Application|apply uncurrying]] $\alpha =\mathtt{uncurry}(\mathtt{curry}(\alpha))$ to get the ***(left) group action*** $\alpha: G \times X \to X$ of <u>group</u> $G$ on set $X$.

## Right Group Action
If $G$ is a [[Group|group]] with the identity element $e \in G$, and $X$ is a nonempty set, then a ***(right) group action*** $\alpha$ of $G$ on $X$ is a [[Mathematical Functions|function]] $\alpha: X \times G \to X$, that satisfies *analogous* axioms for all $g,h \in G, x \in X$:
$$\large
\begin{align}
\text{Identity:} && \alpha(x,e) &= x \\
\text{Compatibility:} && \alpha(\alpha(x,g),h) &= \alpha(x, gh)
\end{align}
$$
with $\alpha(x,g)$ often being shortened to $x \cdot g$ or $xg$ when action $\alpha$ is obvious from the context.

The difference between [[#Left Group Action|left actions]] and ***right actions*** actions is the order in which $gh$ acts on $x$ - for any $g,h \in G$ and $x \in X$. For a <u>left action</u> $h$ acts *first*, and $g$ *second*. Conversely, for a right action $g$ acts *first*, and $h$ *second*. Because of the formula $(gh)^{-1} = h^{-1}g^{-1}$, a l<u>eft action</u> can be constructed from a ***right action*** by <u>composing</u> with the <u>inverse operation</u> of the <u>group</u>. Also, a ***right action*** of a group $G$ on $X$ can be considered as a <u>left action</u> of its [[Group#Opposite Group $G { mathrm{op}}$|opposite group]] $G^{\mathrm{op}}$ on $X$.

# Properties
## Free Group Action
The group action $(\cdot)$ of $G$ on $X$, is called ***free*** if, for and $g \in G$ and $x \in X$ we have
$$\large g \cdot x = x \implies g = e_{G}$$
For example, we can say that [[Real Numbers|real]] addition is a *free* action, since the statement $a + b = b$ would imply that $a = 0$, for all $a \in \mathbb{R}$ where such $b \in \mathbb{R}$ exists.

## Transitive Group Action
The group action $(\cdot)$ of $G$ on $X$, is called ***transitive*** if, for every $x,y \in X$, there exists some $g \in G$ such that
$$\large  g \cdot x = y$$
For example, we can say that [[Real Numbers|real]] addition is a *transitive* action, because for any $a,b \in \mathbb{R}$, we define $c = b - a$, and hence $a + c = b$ holds.

# Orbits and Stabilisers
Consider a group _G_ acting on a set _X_. The _orbit_ of an element _x_ in _X_ is the set of elements in _X_ to which _x_ can be moved by the elements of _G_. The orbit of _x_ is denoted by _G_⋅_x_:

𝐺⋅𝑥={𝑔⋅𝑥:𝑔∈𝐺}.

![{\displaystyle G{\cdot }x=\{g{\cdot }x:g\in G\}.}](https://wikimedia.org/api/rest_v1/media/math/render/svg/cf07be5473d2e0459718618f2c1f0f380ec880c3)

The defining properties of a group guarantee that the set of orbits of (points _x_ in) _X_ under the action of _G_ form a [partition](https://en.wikipedia.org/wiki/Partition_of_a_set "Partition of a set") of _X_. The associated [equivalence relation](https://en.wikipedia.org/wiki/Equivalence_relation "Equivalence relation") is defined by saying _x_ ~ _y_ [if and only if](https://en.wikipedia.org/wiki/If_and_only_if "If and only if") there exists a _g_ in _G_ with _g_⋅_x_ = _y_. The orbits are then the [equivalence classes](https://en.wikipedia.org/wiki/Equivalence_class "Equivalence class") under this relation; two elements _x_ and _y_ are equivalent if and only if their orbits are the same, that is, _G_⋅_x_ = _G_⋅_y_.
#todo NOT DONE YET
https://en.wikipedia.org/wiki/Group_action#Orbits_and_stabilizers

# Principal Homogeneous Space for a Group: $G$-torsor
Let $X$ be any nonempty set and $G$ be a [[Group|group]] with the identity element $1 \in G$.

When $X$ is equipped with a [[#Left Group Action|(left) group action]] $\alpha: G \times X \to X$ of <u>group</u> $G$ which acts [[#Free Group Action|freely]] and [[#Transitive Group Action|transitively]], then $X$ is a ***(left) $G$-torsor*** - or ***(left) principal homogeneous space*** for <u>group</u> $G$.
When $X$ is equipped with a [[#Right Group Action|(right) group action]] $\alpha: X \times G \to X$ of <u>group</u> $G$ which acts [[#Free Group Action|freely]] and [[#Transitive Group Action|transitively]], then $X$ is a ***(right) $G$-torsor*** - or ***(right) principal homogeneous space*** for <u>group</u> $G$.
If $G$ is [[Group#Abelian group|commutative]], then there isn't a difference between the two.

Here is what this means explicitly for ***right $G$-torsor*** - with analogous interpretations for ***left $G$-torsors*** being self-evident. We call $X$ a ***right $G$-torsor*** when equipped with a [[Mathematical Functions|map]] $(\cdot):X \times G \to X$ for which for which these hold
$$\large
\begin{align}
\text{Identity:} && \forall x \in X, \forall g,h  \in G&:
\ \ x \cdot 1 = x \\
\text{Compatibility:} &&& \ \ \ \ \ \ \wedge \ x \cdot (gh) = (g \cdot g) \cdot h \\
\text{Free:} && \forall x \in X, \forall g \in G&: \ \ x \cdot g = x \implies g = I_{V} \\
\text{Transitive:} && \forall x,y \in X, \exists g \in G&: \ \ x \cdot g = y
\end{align}
$$
All together, this implies that for every $x \in X$, the [[Mathematical Functions|map]] $G \to X; g \mapsto x \cdot g$ is [[Mathematical Functions#Bijective Functions|bijective]]. So $X$ looks exactly like $G$ except that which point is the identity has been forgotten, i.e. 'throw away the origin', its a *generalisation* of [[Affine Space|affine spaces]].

For every $x,y \in X$ there exists <u>exactly one</u> $g \in G$ such that $x \cdot g = y$. We use this to define the *"quotient"* $(\backslash): X \times X \to G$ which sends $(x,y) \in X \times X$ to that unique element $x\backslash y = g \in G$ for which $x \cdot g = y$. Define ternary operator of type $X \times X \times X \to X$
$$\large
x/y \cdot z \ \ \triangleq \ \ x \cdot (y \backslash z)
$$
what serves as an <u>affine</u> generalisation of <u>group</u> multiplication and which is sufficient to both <u>characterise</u> a ***principal homogeneous space*** algebraically and intrinsically characterise the <u>group</u> it is associated with.

We get from the above operations these identities:
![[Pasted image 20240430113820.png|1000]]
#todo https://en.wikipedia.org/wiki/Principal_homogeneous_space#Applications
IDEA: $\operatorname{Iso}(V,W)$ is a (right) $\operatorname{GL}(V)$-torsor + $\operatorname{Iso}(W,V)$ is a (left) $\operatorname{GL}(V)$-torsor under composition as group action - so....???