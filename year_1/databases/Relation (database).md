#database-theory #relational-model

A ***relation*** *(or table)* is a [[Set Theory|set]] of [[#Attribute|attributes]] *(or columns)*, paired with a corresponding [[Set Theory|set]] of [[#Tuple|tuples]] $\langle v_{1}, v_{2}, \dots, v_{n}\rangle$ *(or rows)*
![[Pasted image 20240422080352.png|800]]


# Relation
A ***relation*** *(or table)*, is the [[Ordered Pair|pair]] $(\vec{A}, R)$ where $\vec{A}$ is its [[#Attribute Heading|attribute heading]] and $R$ the ***body*** *(or extent)* of that ***relation*** - a [[Set Theory|set]] of [[#Tuple|tuples]] of [[#Data Type|type]] $Tuple(\vec{A})$. For *notational convenience*, ***relations*** are denoted by their <u>body</u> $R$. The <u>attribute heading</u> of $R$ can instead be *explicitly* denoted by $Attrs(R)$. Thus we can write $t \in R$ to denote a [[#Tuple|tuple]] $t$ in the <u>body</u> of ***relation*** $R$. The ***degree*** *(or -arity)* of ***relation*** $R$ is *precisely* ***degree*** *(or -arity)* of <u>attribute heading</u> $\vec{A}$; given $\vec{A} = A_{1},\dots,A_{n}$, we call $R$ an $n$***-ary relation***. The ***cardinality*** of ***relation*** $R$, denoted by $|R|$, is the number of [[#Tuple|tuples]] in the <u>body</u> of $R$ (i.e. [[Cardinality of Sets|cardinality]] of the <u>body</u> of $R$).

Just as [[#Tuple|tuples]] are <u>values</u> and have a [[#Data Type|data type]], so are ***relations*** and they *also* have a <u>data type</u>. Formally, every <u>tuple</u> $t: Tuple(\vec{A})$ is a [[Dependent Functions|dependent function]] of the type type $\mathcal{T}(\vec{A})$, defined as
$$\Large
\mathcal{T}(\vec{A}) \ \ \triangleq \ \
\begin{gathered}
{\large \sub{\prod}{A \in Names(\vec{A})} Domain(A)}
\end{gathered}
$$
so the <u>body</u> $R$ being a set of such <u>tuples</u> makes it a *subset* of $\mathcal{T}(\vec{A})$. As such, the [[Power Sets|power set]] $\wp\mathcal{T}(\vec{A})$ will contain all possible <u>bodies</u> $R$, i.e. all possible subsets of $\mathcal{T}(\vec{A})$. With this, we can create the <u>data type</u> for all ***relations*** with <u>attribute heading</u> $\vec{A}$
$$\large \Big(Relation(\vec{A}), \ \ \wp\mathcal{T}(\vec{A}) \Big)$$
with $Relation(\vec{A})$ being the <u>name</u> of this <u>data type</u>, and $\wp\mathcal{T}(\vec{A})$ being the set of <u>all possible values</u> of this <u>data type</u>. You can therefore *simply* write $R: Relation(\vec{A})$, or even $R(\vec{A})$, to denote ***relation*** $R$ with <u>heading</u> $\vec{A}$. As with tuples, if you know that $\vec{A} = A,B,\dots$, you can *spread* the <u>attributes</u>, i.e. $R(A,B,\dots)$.

Just like [[#Attribute Heading|headings]] and [[#Tuple|tuples]], ***relation*** <u>bodies</u> being a *set* makes them *inherently* <u>unordered</u>; order of <u>tuples</u> not significant. We can *(assuming that $\vec{A} = A,B,\dots$)* denote the ***body*** of a relation as $\{  \langle v_1^A, v_1^B, \dots \rangle\ , \langle v_2^A, v_2^B, \dots \rangle , \langle v_3^A, v_3^B, \dots \rangle\ , \dots \}$ where the each *element* in the *angle brackets* is an <u>atomic value</u>, with superscript indicating associated <u>attribute</u>, and subscript indicating which ***tuple*** they belong to. Just just like with [[#Tuple|tuples]], for any ***relation*** $R(\vec{A})$ we can use *standard* <u>dot-qualification</u> syntax to access <u>attributes</u> from $\vec{A}$ by name, i.e. $\codename{R}{A}$ for some attribute $A \in \vec{A}$.

Here is an example
![[Pasted image 20240422164347.png|800]]

---
#todo below

## Relation Schema
A relation schems is the pair $(\vec{A}, C)$ where $\vec{A}$ is a heading and $C(R)$ is a predicate defined for all relations $R(\vec{A})$. A relation $R(\vec{A})$ satisfies $(\vec{A}, C)$ if $R$ satisfies $C$. #todo

A heading paired with a set of constraints defined in terms of that heading is called a **relation schema**. A relation can thus be seen as an instantiation of a relation schema if it has the heading of that schema and it satisfies the applicable constraints.

Sometimes a <u>relation schema</u> is taken to include a name - a relational database definition can thus be thought of as a collection of named <u>relation schemas</u>

## visualisation
another way to visualise relations as a set of points in a certain n-dim space with tuples as coordinates and attributes as the dimentions - maybe euclidean space/vector space/metric space/affine space

## table_dum and table_dee tables
The ***empty tuple*** *(or $0$-tuple)* is <u>the</u> ***tuple*** $t: Tuple()$ which contains *no values*, and is equal to the empty set $\emptyset$.

that means there can be exactly two empty relations: DUM $\{  \}$ and DEE $\{ \{  \} \}$.
these are used to mean: DUM=FALSE and DEE=TRUE, and also DEE=0 relational algebra - somehow.... #toco 

---
#todo above

# Tuple
With respect to an [[#Attribute Heading|attribute heading]] $\vec{A}$, a ***tuple*** *(or row)* $t$ is a [[Set Theory|set]] containing *exactly* $n = |\vec{A}|$ [[#Attribute Value|attribute values]] $(A_{i}, v_{i})$, *exactly* one <u>atomic value</u> per [[#Attribute|attribute]] in $\vec{A}$. This *allows* such a ***tuple*** $t$ to be a [[Mathematical Functions#Surjective Functions|surjective map]] from each <u>attribute name</u> $A_{i}$ to the corresponding <u>atomic value</u> $v_{i}: Domain(A_{i})$. This also that means the ***degree*** *(or -arity)* of ***tuple*** $t$ is *precisely* ***degree*** *(or -arity)* of <u>attribute heading</u> $\vec{A}$ - in this case $n = |\vec{A}|$ so $t$ is an $n$***-tuple***. 

A ***tuple*** is a <u>value</u> and (just like other <u>values</u>) it has a [[#Data Type|data type]]. Formally, every ***tuple*** $t$ (with respect to <u>attribute heading</u> $\vec{A}$) is a [[Dependent Functions|dependent function]] of the type $\mathcal{T}(\vec{A})$, defined as
$$\Large
\mathcal{T}(\vec{A}) \ \ \triangleq \ \
\begin{gathered}
{\large \sub{\prod}{A \in Names(\vec{A})} Domain(A)}
\end{gathered}
$$
In other words, for every ***tuple*** $t \in \mathcal{T}(\vec{A})$ and [[#Attributes|attribute]] $A \in \vec{A}$, the <u>atomic value</u> $t(A)$ will belong to $Domain(A)$. With this, we can create the <u>data type</u> for all ***tuples*** with <u>attribute heading</u> $\vec{A}$
$$\large \Big(Tuple(\vec{A}), \ \ \mathcal{T}(\vec{A}) \Big)$$
with $Tuple(\vec{A})$ being the <u>name</u> of this <u>data type</u>, and $\mathcal{T}(\vec{A})$ being the set of <u>all possible values</u> of this <u>data type</u>. You can therefore *simply* write $t: Tuple(\vec{A})$, to denote ***tuple*** $t$ with <u>heading</u> $\vec{A}$. If you know that $\vec{A} = A,B,\dots$, you can even *spread* the <u>attributes</u>, i.e. $t: Tuple(A,B,\dots)$.

A ***tuple*** being a *set* makes it *inherently* <u>unordered</u>; order of <u>atomic values</u> not significant. We can *(assuming that $\vec{A} = A,B,\dots$)* denote these *(relational)* ***tuples*** as $\langle v_1^A, v_1^B, \dots \rangle\ , \langle v_2^A, v_2^B, \dots \rangle , \langle v_3^A, v_3^B, \dots \rangle\ , \dots$ where the each *element* in the *angle brackets* is an <u>atomic value</u>, with superscript indicating associated <u>attribute</u>, and subscript indicating which ***tuple*** they belong to (assuming there are *multiple* ***tuples***). Additionally, for any ***tuple*** $t: Tuple(\vec{A})$ and *attribute* $A \in \vec{A}$ we can define $\codename{t}{A}$ as an *alias* for $t(A)$, allowing us to use *standard* <u>dot-qualification</u> syntax to access <u>atomic values</u>.

Here is an example of a tuple
![[Pasted image 20240422164154.png|800]]

## Tuple Projection
If you have some ***tuple*** $t: Tuple(\vec{A})$ with [[#Attribute Heading|attribute heading]] $\vec{A}$ and [[#Attribute|attributes]] $\vec{B} \subseteq \vec{A}$, then the ***projection*** of ***tuple*** $t$ on [[#Attribute|attributes]] $\vec{B}$, denoted by $t[\vec{B}]$, is defined to be the [[Mathematical Functions#Domain Restriction|domain restricted]] function $\frestrict{t}{Names(\vec{B})}$
$$\large t[\vec{B}] \ \ \triangleq \ \ \frestrict{t}{Names(\vec{B})} = \{ \ v_{A} \in t \ | \ Name(v_{A}) \in Names(\vec{B}) \ \}$$
Thus, the ***tuple projection*** $t[\vec{B}]: Tuple(\vec{B})$ will *only* contain [[#Attribute Value|attribute values]] from $t$ *associated* with [[#Attribute|attributes]] in $\vec{B}$ - it's new [[#Attribute Heading|attribute heading]]. This is a useful primitive for working with ***tuples***, and is used to define more complicated operations.
^tuple "remove" is $t^\complement[\vec{B}] = t[\vec{A} \setminus \vec{B}]$ for convenience $t^\complement[A_{1},A_{2},\dots] = t[\vec{A} \setminus \{ A_{1},A_{2},\dots \}]$


# Attribute
An ***attribute*** *(or column)* is the [[Ordered Pair|pair]] $(A, \mathcal{D})$ where $A$ is the <u>attribute name</u> (*string*, *number*, or any other *identifier*), and $\mathcal{D}$ is the [[#Data Type|data type]] (i.e. characters, strings, numbers, and so on) associated with that <u>attribute name</u>.

For *notational convenience*, ***attributes*** are denoted by their <u>attribute name</u> $A$. The associated <u>data type</u> of $A$ is instead *explicitly* accessed with $Domain(A)$. If you <u>absolutely have to</u>, you can *explicitly* access the <u>attribute name</u> with $Name(A)$.

## Attribute Value
An ***attribute value*** *(or component, or cell)* is the [[Ordered Pair|pair]] $(A, v)$, where $A$ is an <u>attribute name</u> and $v: Domain(A)$ is the actual <u>atomic value</u> associated to that <u>attribute name</u>, with $v$ being of associated <u>data type</u> of $A$. 

***Attribute values*** are denoted by $v_{A}$. You can *explicitly* access the <u>atomic value</u> with $Value(v_{A})$ and associated <u>attribute name</u> with $Name(v_{A})$.

## Attribute Heading
An ***attribute heading***, denoted by $\vec{A}$, is *just* a [[Set Theory|set]] of [[#Attribute|attributes]] where the <u>attribute names</u> are all ***unique***. It can also be written as the *list* of individual <u>attributes</u> that make it up, i.e. $A,B,C,\dots = \vec{A}$ or $ABC\dots = \vec{A}$. Being a *set* makes $\vec{A}$ *inherently* <u>unordered</u>; order of <u>attributes</u> not significant. The ***degree*** *(or -arity)* of an ***attribute heading*** $\vec{A}$ is the number of <u>attributes</u> that it contains, which is the [[Cardinality of Sets|cardinality]] $|\vec{A}|$ of $\vec{A}$.

Notice that any ***attribute heading*** $\vec{A}$ is just a <u>set</u> of [[Ordered Pair|pairs]] $(A, \mathcal{D})$, and thus it is a [[Relations on Sets|mathematical relation]]. More interestingly, the ***uniqueness*** of the <u>attribute names</u> allows $\vec{A}$ to be a [[Mathematical Functions#Surjective Functions|surjective function]] from <u>attribute names</u> to their <u>data types</u>. This means we can define $Domain$ an *alias* for $\vec{A}$, allowing us to ***reinterpret*** *(and formalise)* the $Domain$ notation from earlier as a <u>well-defined function</u> that maps <u>attribute names</u> (in the ***heading***) to their associated <u>data types</u>.

Although $\vec{A}$ can *itself* refer to just the set of <u>attribute names</u>, we can use $Names(\vec{A})$ *explicitly* the set of <u>attribute names</u>. $Names(\vec{A})$ could also double as the [[Mathematical Functions#Domains, co-domains, ranges|domain]] of the <u>function</u> $Domain$.

Here is an example
![[Pasted image 20240422164301.png|800]]

# Data Type
A ***data Type*** *(or data domain)* is a *named* [[Set Theory|set]] of <u>values</u>: all possible values of some specific kind, i.e. characters, strings, numbers, and so on. The fact that ***data types*** are *named* means that <u>different</u> *names* but <u>same</u> *sets of values*, still means that they are *still* <u>different</u> ***data types***.

Formally, a ***data type*** it is the [[Ordered Pair|pair]] $(\mathcal{D}, \mathcal{V})$ consisting of its <u>name</u> $\mathcal{D}$ and <u>set of values</u> $\mathcal{V}$. For *notational convenience* we ***overload*** [[Set Theory#Set operations|set operators]] like $v \in \mathcal{D}, \ \mathcal{D}' \subseteq \mathcal{D}, \ \mathcal{D}_{1} \cup \mathcal{D}_{2}, \dots$ to mean $v \in \mathcal{V}, \ \mathcal{V}' \subseteq \mathcal{V},  \ \mathcal{V}_{1} \cup \mathcal{V}_{2}, \dots$, as a way to <u>compartmentalise</u> and <u>abstract away</u> the complexity. For further *notational convenience* we define $v: \mathcal{D}$ to be an *alias* for $v \in \mathcal{D}$, to provide further clarity that this <u>not</u> an *arbitrary set* but rather a ***data type***.

If you <u>absolutely have to</u>, you can *explicitly* access the <u>name</u> with $Name(\mathcal{D})$ and <u>set of values</u> with $Values(\mathcal{D})$.

## Nullable Types
To represent ***nullable types***, a special ***null*** element has to be added *explicitly* to $Values$ (usually $\mathrm{NULL}$ or $\bot$) and then the type is considered ***nullable***. There is no *out-of-the-box* handling for ***null***, and many even discourage it's use.