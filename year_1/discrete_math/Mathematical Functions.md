Functions are a special kind of relation that assigns each element from of one set to exactly one element of another set. These are said to be **total** functions, as opposed to [[Partial Functions|partial functions]].

# Formal Definition
Let $f$ be a relation on $A\times B$. The relation $f$ is a function if every element in $A$ is mapped to exactly one element in $B$:
$$
\begin{gathered}[C]
f \ \text{is a function}
\end{gathered}
\begin{gathered}[C]
& \triangleq &
\end{gathered}
\begin{gathered}[C]
f \ \text{is a partial function} \\
\text{and} \\
\forall a \in A,\exists b \in B(\langle a,b \rangle \in f)
\end{gathered}
$$
We therefore say that $f$ is a function from $A$ to $B$, or $f: A \to B$. The set of all functions from $A$ to $B$ is denoted as $B^A$ and defined as: $$B^A \triangleq \{ \ f \in \wp(A \times B) \ | \ f \ \text{is a function} \ \}$$Notice how $f \in B^A$ is equivalent to $f: A \to B$, therefore $A \to B$ is equivalent to $B^A$. Hence, if we want to write for example $\forall f \in B^A(\dots)$, it is entirely acceptable to say $\forall f: A\to B(\dots)$.

For some $a \in A$, $f(a)$ is the shorthand for: the unique $b \in B$ such that $\langle a,b\rangle \in f$, and $f$ is said to **map** $a$ to $b$. We also can say that $b$ is the **image**, and $a$ is the **pre-image**/**inverse image**, under $f$.

## Domains, co-domains, ranges
In the above example, $A$ is the **domain**, and $B$ is the **co-domain**. However, it is possible that $f$ does not map to all of $B$, but only some of it. Those element of $B$ which are mapped to, form a subset of the co-domain called the **range**. The range, the set of all images of $f$, is often written as $f[A]$, the [[#Image Sets|image set]] of $f$.

Here is a visualisation:
![[Pasted image 20231105171626.png|400]]
The red is the **domain**, the blue is the **co-domain**, and the yellow is the **range**.

## Multivariate Function Syntax
If there is a function with a [[#Domains, co-domains, ranges|domain]] of an $n\text{-ary}$ product $A=X^n$, then we don't write $f(\langle a_{1},a_{2},\dots,a_{n} \rangle)$, instead we write $f(a_{1}, a_{2},\dots,a_{n})$ and call $f$ a **multivariate** function that takes $n$ arguments.

## Function Equality
For two functions $f: A \to B$ and $g: A \to B$, functional equality is defined as: $$f =_{A\to B} g \triangleq \forall a \in A(\ f(a) =_{B} g(a) \ )$$
So two functions are equal when they have the same domain and return the same value for every element of that domain.

Here we notice that the definition of function equality is equivalent to set equality in it's effect. And it makes sense because functions are just sets. So $f \ \text{and} \ g \ \text{are function equal} \iff f \ \text{and} \ g \ \text{are set equal}$.

## Image Sets
For some $f: A \to B$, and if $V \subseteq A$, then $f[V]$ is the image of $V$ under $f$. It is defined as: $$f[V] \triangleq \{ b \in B \ | \ \exists a \in V(b=f(a)) \}$$
The **range** of $f$ is the same as $f[A]$ and it is the case that $f[A] \subseteq B$. It is also true that, unless $f$ is [[#Surjective Functions|surjective]], $f[A] \ne B$. 

# Properties of Functions
The following properties only hold for total functions. [[Partial Functions|Partial functions]] need to be either extended, or their domain restricted, so that they become total, and then the properties would hold.
Let $f: A \to B$ be a function.

## Surjective Functions
$f$ is surjective (onto) if the range is equal to the co-domain, or $f[A] = B$: $$f \ \text{is surjective} \triangleq \forall b \in B, \exists a \in A ( \ f(a) = b \ )$$
We can also say that $f$ is a surjection. Notice that: $$f \ \text{is surjective} \implies |A| \geq |f[A]| = |B|$$

## Injective Functions
$f$ is injective (one-to-one) if every element $a \in A$ uniquely maps to some element $b \in f[A]$: $$f \ \text{is injective} \triangleq \forall a,a' \in A ( \ f(a) = f(a') \implies a =_{B} a' \ )$$
We can also say that $f$ is a injection. Notice that: $$f \ \text{is injective} \implies |A| = |f[A]| \leq |B|$$
This result is just the application of the [[Pigeonhole Principle|Pigeonhole principle]].

## Bijective Functions
$f$ is bijective if it is [[#Surjective Functions|surjective]] and [[#Injective Functions|injective]]: $$f \ \text{is bijective} \triangleq f \ \text{is surjective} \wedge f \ \text{is injective}$$
We can also say that $f$ is a bijection. Notice that: $$f \ \text{is bijective} \implies |A| = |f[A]| = |B|$$

# Operations on Functions
Since functions are relations, we can define identity, composition, and inverse of functions.

## Identity Function
Just like there is an [[Relations on Sets#Identity relation|identity relation]] there is an identity function. In fact, the identity relation on some set $A$ is also the identity function on $A$ and is denoted as $Id_{A}$. For functions, it is defined by: $$Id_{A}(a) = a$$

## Function Composition
Let $f:A\to B$ and $g:B\to C$ be arbitrary functions. The composition of $f$ and $g$ is written as $g \circ f: A \to C$ is defined as: $$g \circ f(a) \triangleq g(f(a))$$ for every element $a \in A$. From this definition we can derive the result $$g \circ f(a) \ =_{C} \ c \iff \exists b \in B (\ f(a) =_{B} b \wedge g(b) =_{C} c \ )$$
**NOTE:** functional and [[Relations on Sets#Composition|relational composition]] are different in their notation. Relations are read in infix notation. So for some relation $R$ it is read as $aRb$ or "$a$ relates to $b$". On the other hand, functions are read in prefix notation. So $f(a)$ or "$f$ applied to $a$". It is possible to convert functional composition notation to relational composition notation, since functional composition is a special case of relational composition where all relations being composed are functions.

### Properties
#### Associativity of Composition
Just like [[Relations on Sets#Properties of Composition|relational composition]], functional composition is associative. Or, for some $f: A \to B$ and $g: B \to C$ and $h: C \to D$: $$h \circ (g \circ f) = (h \circ g) \circ f$$

#### Bijectivity of Composition
For some $f: A \to B$ and $g: B \to C$, if $f$ and $g$ are [[#Bijective Functions|bijective]], so is their composition. For formally: $$f \ \text{is bijective} \wedge g \ \text{is bijective} \implies g \circ f \ \text{is bijective}$$

## Function Inverses
We cannot use the [[Relations on Sets#Operators|relational inverse]] definition for functions, since the relational inverse of a function is not always a function. For some $f: A \to B$, and $g: B \to A$, we have that: 
$$
\begin{gathered}
g \ \text{is the left inverse of} \ f \triangleq \forall a \in A(g \circ f(a) = a) \\
\text{so we can deduce that} \\
g \ \text{is the left inverse of} \ f \iff g \circ f(a) = Id_{A} \\
\\ \\
g \ \text{is the right inverse of} \ f \triangleq \forall a \in A(f \circ g(a) = a) \\
\text{so we can deduce that} \\
g \ \text{is the right inverse of} \ f \iff f \circ g(a) = Id_{A} \\
\\ \\
g \ \text{is the inverse of} \ f \triangleq g \ \text{is the left inverse of} f \ \wedge \ g \ \text{is the right inverse of} f
\end{gathered}
$$
**NOTE:** when writing $f^{-1}$ we usually mean functional, rather than relational, inverses.

### Interactions with Injection and Surjection
Notice also that a function is [[#Surjective Functions|surjective]] if and only if it has a right inverse: $$f: A \to B \ \text{is surjective} \iff \exists g: B \to A (\ g \ \text{is the right inverse of} \ f \ )$$and similarly, a function is is [[#Injective Functions|injective]] if and only if it has a left inverse: $$f: A \to B \ \text{is injective} \iff \exists g: B \to A (\ g \ \text{is the left inverse of} \ f \ )$$
### Interactions with Bijection
If some $f: A \to B$ has an inverse function $f^{-1}$ then $f$ is a [[#Bijective Functions|bijection]], and $f^{-1}$ is unique. So: $$f^{-1} \ \text{is the inverse of} \ f \implies f \ \text{is a bijection} \wedge f^{-1} \ \text{is unique}$$

We can also relate it back to [[Relations on Sets#Operators|relational inverses]], namely that if some $f: A \to B$ is a [[#Bijective Functions|bijection]] then it's **relational inverse**, $f^{-1}$, is also a function, and also the  inverse function of $f$. So: $$f \ \text{is a bijection} \implies f^{-1} \ \text{is the inverse function of} \ f \wedge f^{-1} \ \text{is a bijection}$$


