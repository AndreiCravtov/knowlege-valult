#database-theory #relational-model 

***Relational algebra*** is a collection of [[#Relational Operators|operators]], which define a <u>language</u> for talking about <u>manipulations</u> of database [[|relation]] values.

# Relational Operators
***Relational operations*** are those which take [[|relations]] as <u>input</u>, and produce a [[|relation]] as their <u>output</u>. As with other similar logical/mathematical systems, many of the operators can be defined in terms of each other. So you can pick lots of *equally powerful* <u>primitive operators</u> from which all others are derived. I chose to use the [[#ALGEBRA - A Logical Genesis Explains Basic Relational Algebra|ALGEBRA]] - as formulated in [The Third Manifesto](http://www.thethirdmanifesto.com/) by [Hugh Darwen](https://en.wikipedia.org/wiki/Hugh_Darwen) and [C.J. Date](https://en.wikipedia.org/wiki/Christopher_J._Date).

## ALGEBRA - A Logical Genesis Explains Basic Relational Algebra
The name ***ALGEBRA*** stands for ***A Logical Genesis Explains Basic Relational Algebra*** - a doubly recursive acronym. As the name suggests, it has a strong foundation in logic and makes full use if it's principles.

### Primitive Operators
#### Sheffer Stroke - $\uparrow$
https://en.wikipedia.org/wiki/Sheffer_stroke <- this
used to build out $AND,NOT,OR$ as with logic
given the relations $(\vec{A}, R)$ and $(\vec{B}, S)$, **it is required that if $R$ and $S$ have common attributes then those attributes have the same type**, definition of $R \uparrow S$ is
$$
\begin{align}
R \uparrow S &= (\vec{C}, \{ t : Tuple(\vec{C}) \ | \ \neg(t[\vec{A}] \in R \wedge t[\vec{B}] \in S) \}) \\
\vec{C} &= \vec{A} \cup \vec{B}
\end{align}
$$
with normal <u>set union</u> and <u>tuple projection</u>. could also be called non-conjoin

#### Remove - $\rho$
remove $\rho$ the *compliment* of project $\pi$
with project you specify what to keep $\project{A,B,C}R$
with remove you specify what NOT to keep $\remrel{A,B,C}R$
meant to be the counterpart to the existential quantifier
given the relation $(\vec{A}, R)$ and $\opair{A}{T} \in \vec{A}$, definition of $\remrel{A}R$ is
$$
\begin{align}
\remrel{A}R &= (\vec{B}, \ \{ t[\vec{B}] \ | \ t \in R \}) \\
\vec{B} &= \vec{A} \setminus \{ \opair{A}{T} \}
\end{align}
$$
with normal <u>set difference</u> and <u>tuple projection notation</u>
and multiple application with subset $\vec{B} \subseteq \vec{A}$ where $\vec{B} = \{ A_{1}, A_{2}, \dots, A_{n} \}$
$$\remrel{\vec{B}}R = \remrel{A_{1},A_{2},\dots,A_{n}}R = \remrel{A_{1}} \remrel{A_{2}} \dots \remrel{A_{n}} R$$

### Derived Operators
#### Not ($\notrel{R}$)
as in logic, defined not can be defined with $\notrel{R} = P \uparrow P$, semantics of NOT for relation $(\vec{A}, R)$
$$\notrel{R} = (\vec{A}, \{ t : Tuple(\vec{A}) \ | \ t \notin R \})$$

#### And ($\&$)
given that $\uparrow$ is not-and, not-not-and *is* and, hence $R \andrel S = \notrel{R \uparrow S}$
a synonym of [[#Natural Join ($ Join$)|natural join]], could also be called conjoin
given the relations $(\vec{A}, R)$ and $(\vec{B}, S)$, **it is required that if $R$ and $S$ have common attributes then those attributes have the same type**, definition of $R \andrel S$ is
$$
\begin{align}
R \andrel S &= (\vec{C}, \{ t : Tuple(\vec{C}) \ | \ t[\vec{A}] \in R \wedge t[\vec{B}] \in S \}) \\
\vec{C} &= \vec{A} \cup \vec{B}
\end{align}
$$
with normal <u>set union</u> and <u>tuple projection</u>.

#### Or ($|$)
using DeMorgan's law, we define $R \orrel S = \notrel{\notrel{R} \andrel \notrel{S}} = \notrel{R} \uparrow \notrel{S}$, could also be called disjoin
given the relations $(\vec{A}, R)$ and $(\vec{B}, S)$, **it is required that if $R$ and $S$ have common attributes then those attributes have the same type**, definition of $R \orrel S$ is
$$
\begin{align}
R \orrel S &= (\vec{C}, \{ t : Tuple(\vec{C}) \ | \ t[\vec{A}] \in R \vee t[\vec{B}] \in S \}) \\
\vec{C} &= \vec{A} \cup \vec{B}
\end{align}
$$
with normal <u>set union</u> and <u>tuple projection</u>.

#### Rename ($\rename{R}{A \mapsto B}$)
given the relation $(\vec{A}, R)$ and $\opair{A}{T} \in \vec{A}$, and assuming there exists no type $T'$ such that $\opair{B}{T'}$, the definition of $\rename{R}{A \mapsto B}$ is
$$
\begin{align}
\rename{R}{A \mapsto B} &= (\vec{B}, Bs \ ) \\
\vec{B} &= (\vec{A} \setminus \{ \opair{A}{T} \}) \cup \{ \opair{B}{T} \} \\
Bs &= \{ \ ts \ | \ \exists tr \exists v ( \ \  tr \in R \wedge v \in T \wedge \langle A,T,v \rangle \in tr \wedge ts = ( tr \setminus \{ \langle A,T,v \rangle \}) \cup \{ B, T, v \} \ \ ) \ \} \\
\end{align}
$$
![[Pasted image 20240424060252.png|800]]
with normal <u>set difference</u> and <u>set union</u> (although it might be useful to define a tuple-level operator, maybe $t[A \mapsto B]$?? while we are at it, we could also do $\vec{A}[A \mapsto B]$?? then the whole thing will just be $(\vec{A}[A \mapsto B], \{ t[A \mapsto B] \ | \ t \in R \})$)
$$\large
\begin{align}
\rename{R}{A \mapsto B} &= (\vec{A}[A \mapsto B], \ \{ t[A \mapsto B] \ | \ t \in R \} ) \\
\end{align}
$$

#### Compose ($\circ$)
Derived meta-operator $COMPOSE := AND + REMOVE$ that generalises functional composition (since functions *are* relations in the world of relational model, and operators too are relations - or more accurately ***relcons*** - constant ***relvalrs***) could potentially be related to semijoins???? OR MAYBE IT IS [[Relations on Sets#Composition|set-theoretic relation composition]] analoge??? #todo
^you can encode functions as relations (e.g. $n$-input function as $n+1$-ary relation) and then apply those "relation functions" to other relations by composition. e.g. we could turn $(+): \mathbb{Z} \to \mathbb{Z}$ into a $3$-ary relation $PLUS$ and then apply to some $2$-ary relation $TWO\_AND\_TWO = \{ 2, 2 \}$ like this $TWO\_AND\_TWO \circ PLUS$ and the result will contain $\{ 4 \}$ - 

given the relations $(\vec{A}, R)$ and $(\vec{B}, S)$, **it is required that if $R$ and $S$ have common attributes then those attributes have the same type**, definition of $R \circ S$ is
$$
\begin{align}
R \circ S = \remrel{\vec{A} \cap \vec{B}}(R \andrel S)
\end{align}
$$
with normal <u>set intersection</u>. $n=0$ means $R \circ S = R \ \& \ S = R \times S$

#### Transitive Closure ($R^+$)
transitive closure of $R$ written as $R^+$ #todo
for some <u>binary</u> relation $(\vec{A}, R)$ with attributes of the same type, i.e. $\vec{A} = \{ \opair{A}{T}, \opair{B}{T} \}$, we define $R^+$ as
$$
R^+ = (\vec{A}, \ \{ \opair{a}{b} : Tuple(\vec{A}) \ | \ \opair{a}{b} \in R \vee \exists c:T(\opair{a}{c} \in R \wedge \opair{c}{b} \in R^+) \})
$$
The tuple $\langle a:T,b:T \rangle$ appears in $R^+$ if and only if it appears in $R$, or there exists a value $c:T$ such that the tuple $\opair{a:T}{c:T} \in R$ and the tuple $\opair{c:T}{b:T} \in R^+$, which is recursive - analogue of [[Relations on Sets#Transitive Closure|set-theoretic transitive closure]].
![[Pasted image 20240424051719.png|800]]
The $\text{transitive closure of} \ R$, written as $R^+$, is achieved by composing $R$ with itself over and over again, until it has achieved transitivity:
$$
\begin{gathered}
& R^1=R \\
& R^2 = R \circ R \\
& R^3 = R^2 \circ R \\
& \vdots \\
& R^n = R^{n-1} \circ R \\
& \vdots \\
\text{transitive closure of} \ R: & R^+ \triangleq R \cup R^2 \cup \dots \cup R^n \cup \dots
\end{gathered}
$$
It can be intuitively be thought of as, $aR^+b$ if there is any path between $a$ and $b$ in $R$, even if we have to take multiple trips.
^set theoretic definition #todo

## Common Operators
### Project ($\pi$)
$\pi$ (project) is an inversion of remove $\rho$, i.e. it keeps the attributes specified and nothing else.
for $R(\vec{A})$ and $A \in \vec{A}$ defined as $\project{A}R = \remrel{\vec{A} \setminus \{ A \}}R$
or $\vec{B} \subseteq \vec{A}$ where $\vec{B} = A_{1}, A_{2}, \dots$ it is $\project{\vec{B}}R = \project{A_{1},A_{2},\dots} R = \remrel{\vec{A} \setminus \vec{B}}R$
semantically equivalent: for $\project{A}R$ is then
$$
\begin{align}
\project{A}R &= (\vec{B}, \ \{ \ t[\vec{B}] \ | \ t \in R \ \}) \\
\vec{B} &= \{ \opair{A}{T} \}
\end{align}
$$

### Select ($\sigma$) 
For relation $(\vec{A}, R)$, consider some predicate $P: Tuple(\vec{A}) \to Boolean$ - we can define a relation $\select{P} = (\vec{A}, \{ t : Tuple(\vec{A}) \ | \ P(t) \})$. As such, the selection $\select{P}R$ is defined as $\select{P} \ \& \ R$ - effectively only picking the rows of $R$ that also satisfy the predicate $P$:
$$\select{P}R = (\vec{A}, \{ t \in R \ | \ P(t) \})$$
this predicate should be quantifier free - i.e. you can evaluate it's truth value with just that tuple and no other information

### Product ($\times$)
$\times$ (product) is a special case of and $\&$ where the two relations have no common attributes. if there are common attributes and we still want the semantics of product $\times$, we can disambiguate the common attribute names with rename $\rename{R}{A \mapsto B}$

### Union ($\cup$)
$\cup$ is a special case of <u>or</u> ($|$) where the attributes of the two relations are the same - has the effect of performing a set union on the body of the two relations. For relations $R(\vec{A})$ and $S(\vec{A})$, the actual semantically equivalent of $R \cup S$ will be
$$\large
R \cup S = (\vec{A}, R \cup S)
$$

### Intersection ($\cap$)
$\cap$ is a special case of <u>and</u> ($\&$) where the attributes of the two relations are the same - has the effect of performing a set intersection on the body of the two relations. For relations $R(\vec{A})$ and $S(\vec{A})$, the actual semantically equivalent of $R \cap S$ will be
$$\large
R \cap S = (\vec{A}, R \cap S)
$$

### Difference ($-$)
for two relations $(\vec{A}, R)$ and $(\vec{A}, S)$, the difference $R - S = R \andrel \notrel{S}$ is the tuples in $R$ that don't appear in $S$.
$$R - S = (\vec{A}, R \setminus S)$$
### Divide ($\div$)
Given some relation $(\vec{A}, R)$ and $\vec{B} \subseteq \vec{A}$, we can split $R$ it into a divisor $D \subseteq \project{\vec{B}} R$ and the value $V = \remrel{\vec{B}} R$ being divided. The division operator $R \div D$ only selects those tuples $v \in V$ that, when paired with <u>each and every</u> tuple $d \in D$, form combinations $v \cup d$ that are <u>all</u> present in $R$. Thus we can define $R \div D$  as
$$\large
\begin{align}
V \times D & \ \ \text{// contains every combination of values being divided, and divisor} \\
(V \times D) - R & \ \ \text{// the possible combinations that could have been in $R$, but weren't} \\
R \div S &= V - \remrel{\vec{B}}((V \times D) - R) \ \ \text{// the missing rows removed from $R$,} \\
&\text{and the resulting subset of $V$ being selected} 
\end{align}
$$
The following semantically equivalent description of $R \div D$ that summarises what's going on
$$\large
R \div S = ( \ \vec{A} \setminus \vec{B}, \ \{ \ r \in \remrel{\vec{B}}R \ | \ \forall s \in S (r \cup s \in R) \ \} \ )
$$
![[Pasted image 20240420184340.png|800]]

## Join Operators
### Natural Join ($\Join$)#
the join operator is $\Join$ is a synonym of [[#And ($ &$)|and]]
![[Pasted image 20240420181001.png|800]]

### Semi Join ($\ltimes,\rtimes$)
$$\Large
R \ltimes S = R \Join \project{Attrs(R) \cap Attrs(S)}(S)
$$
![[Pasted image 20240420181443.png|800]]

### Theta Join ($\thetajoin$)
$$\Large
R \thetajoin S = \sigma_{\theta} R \times S
$$

### Equi Join $\thetajoin[A = B]$
$$\Large
R \thetajoin[A=B] S = \sigma_{R.A = S.B} R \times S
$$

## Group and Ungroup
#todo
![[Pasted image 20240424224520.png|800]]

# Select Project Join (SPJ)
#todo
If a product of tables is formed, where a selection is then done that compares the attributes of those tables, we say that a join has been performed. Normally not all columns of the product are returned, and therefore a project is also required.
![[Pasted image 20240420174350.png|800]]

# Equivalences
#todo sort..
![[Pasted image 20240420184519.png|800]]
![[Pasted image 20240420184540.png|800]]
![[Pasted image 20240420184602.png|800]]
