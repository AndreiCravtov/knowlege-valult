The **cardinality** of some [[Set Theory|set]] $A$, is a measure of the number of elements of that set, denoted as $|A|$. For example, the set $A=\{ 2,4,6 \}$ contains 3 elements, and therefore a cardinality of 3, denoted as $|A| = 3$. The notion of cardinality naturally works with finite sets, but is also extensible to infinite sets.

# Formal Definitions
We can use the [[Mathematical Functions#Properties of Functions|properties of functions]] to define the way we compare cardinals of sets.

## Equinumerosity 'relation'
Two [[Set Theory|sets]], $A,B$ are said to be equinumerous when there exists a [[Mathematical Functions#Bijective Functions|bijection]] between the two. This fact is often dented as $A \approx B$, $A \sim B$ or $|A|=|B|$. The formal definition is as follows: $$A \approx B \triangleq \exists f: A \to B ( \ f \ \text{is bijective} \ )$$
If $A \approx B$ then $A$ and $B$ are said to have the same **cardinality**.
The equinumerous 'relation' between two sets does have the properties of an [[Equivalence Relations|equivalence relation]], namely it is [[Relations on Sets#Properties of Relations|reflexive, symmetric and transitive]], in the broad sense of those definitions. However, since [[Naive Set Theory#Solution|Russel proved]] that no set containing all sets can exists, and relations are defined on sets. Hence, *equinumerosity* isn't really a relation, but it behaves similarly to one.

## $|A| \leq |B|$
As seen in the [[Mathematical Functions#Injective Functions|injective functions]] description, set $A$ being less than or equal to set $B$ is implied by the existence of an injective function between the two sets. Therefore we can turn it into a definition like so: $$|A| \leq |B| \triangleq \exists f: A \to B (f \ \text{is injective})$$

# $|A| < |B|$
The notion of cardinality being strictly less can be defined in terms of [[#$ A leq B $|less than or equal to]], in a manner similar to how other [[Orderings#Strict Partial Orde|strict inequalities]] are defined $$|A| < |B| \triangleq |A| \leq |B| \wedge |A| \ne |B|$$
Meaning, there does exists an injective function between $A$ and $B$, but no bijective function exists.

## Finite Sets
Intuitively, we understand that a set with a finite amount of elements should have it's cardinality be an element of the set $\mathbb{N}$. Indeed, we can use this intuition do define that for some set $A$, it being finite is defined as: $$A \ \text{is finite} \triangleq |A| < |\mathbb{N}|$$
This means that if $|A|$ is [[#$ A < B $|strictly less than]] $|\mathbb{N}|$ then it is finite.

## Countable Sets
Countable sets, then, are those who's cardinality is [[#$ A leq B $|less than or equal to]] $\mathbb{N}$. Or another way of thinking about it is that the set is either [[#Finite Sets|finite]] or it is [[#Equinumerosity 'relation'|equinumerous]] to $\mathbb{N}$. This can be expressed as 
$$
\begin{gathered}
A \ \text{is countable} \triangleq |A| \leq |\mathbb{N}| \\ \\
\textit{or equivalently} \\ \\
A \ \text{is countable} \triangleq A \ \text{is finite} \vee A \approx  \mathbb{N}
\end{gathered}
$$

## Infinite Sets
### Countably Infinite Sets
For some set $A$ that is not [[#Finite Sets|finite]], meaning $|A| = |\mathbb{N}|$, we have it that $|\mathbb{N}| = |A| = \aleph_{0}$. This, $\aleph_{0}$, is the notation for *countable infinity*, the first type of infinity.

### Uncountable Sets
Uncountable sets are the negation of countable sets. In particular, those who's cardinality is [[#$ A < B $|more than]] $\mathbb{N}$. This can be expressed as $$A \ \text{is uncountable} \triangleq |A| > |\mathbb{N}|$$
For example, using [[Cantor's Theorem]], we can deduce that $\wp\mathbb{N}$ is uncountable.

### Generalising Infinities
Using [[Cantor's Theorem]], we can deduce that $$|\mathbb{N}| = \aleph_{0} < |\wp\mathbb{N}| = \aleph_{1} < |\wp(\wp\mathbb{N})| = \aleph_{2} < |\wp(\wp(\wp\mathbb{N}))| = \aleph_{3} < \dots$$
Goes on for ever, with each type of infinity being much greater than the other. This means that $\aleph_{0}$ is the only countable infinity, and the rest $\aleph_{1},\aleph_{2},\aleph_{3}\dots$, are uncountable infinities.

# Properties of Cardinality
## Union and Intersection
For any sets $A,B$ then the following holds
$$|A \cup B| = |A| + |B| - |A \cap B|$$

## Result using Cantor-Bernstein theorem
We can employ the [[(Dual) Cantor-Bernstein theorem|Cantor-Bernstein]] theorem to prove that if for two sets $A,B$, if $|A|$ is [[#$ A leq B $|more than or equal to]] $|B|$, and $|B|$ is more than or equal to $|A|$, then $|A|$ is [[#Equinumerosity 'relation'|equal to]] $|B|$. That is, $$|A| \leq B \wedge B \leq A \iff |A| = |B|$$
Or more broadly, $$\exists f:A \to B, \exists g: B \to A (f,g \ \text{are injective} \vee f,g \ \text{are surjective}) \implies |A|=|B|$$

## Common Equinumerosity Results
Here are a few common [[#Equinumerosity 'relation'|equinumerosity]] results: $$\mathbb{N} \approx \mathbb{N}^2, \ \mathbb{R} \approx \mathbb{R}^2,\  \mathbb{N} \approx \mathbb{Z}, \ \mathbb{N} \approx \mathbb{Q}, \  \wp \mathbb{N} \approx \mathbb{R},  \ \mathbb{C} \approx \mathbb{R}$$

## Countability Results
- $V \subseteq \mathbb{N} \implies V \ \text{is countable}$
- $A \ne \emptyset \implies A \ \text{is countable} \iff \exists f:\mathbb{N} \to A (f \ \text{is surjective}) \iff \exists f:A \to \mathbb{N}(f \ \text{is an injection})$
- $\mathbb{R} \ \text{is not countable}$ 