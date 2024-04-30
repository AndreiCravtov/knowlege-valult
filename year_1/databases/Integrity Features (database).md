#database-theory #relational-model

# Integrity Constraint
boolean expression evaluate to $TRUE$ for database to be "consistent"; relational model comes with two generic integrity rules that apply to every database:

<u>entity integrity</u>: primary key attributes don't permit nulls -- but nulls dont exist anyways so who cares.
<u>relational integrity</u>: no unmatched foreign key values. foreign key value for which there doesn't exists an equal value of the corresponding candidate key

integrity constraints apply to variables not values - hence keys and key constraints only make sense with [[Relvars|relvars]].


# Key Constraints
## Super Key
A ***super key*** *(or key)* of a [[Relation (database)#Relation|relation]] $R(\vec{A})$ is a *subset* of the [[Relation (database)#Attribute Heading|attribute heading]] $\vec{A}$ for which the values in any [[Relation (database)#Relation|extent]] are unique across all [[Relation (database)#Tuple|tuples]]. In other words, a ***super key*** is a subset $\vec{K} \subseteq \vec{A}$ of ***columns*** that, put together, will *uniquely identify* every ***row*** in $R(\vec{A})$. This is called the ***uniqueness property***. The <u>attribute heading</u> of every <u>relation</u> satisfies the ***uniqueness property***, therefore every <u>relation</u> has at least <u>one</u> ***super key***.

Formally, a ***super key*** $\vec{K} \subseteq \vec{A}$ of a [[Relation (database)#Relation|relation]] $R(\vec{A})$ satisfies the ***uniqueness property***, defined as
$$\large
\text{$\vec{K} \subseteq \vec{A}$ is a super key of $R(\vec{A})$} \ \ \triangleq \ \ 
\forall t_{1},t_{2} \in R: \ \ t_{1}[\vec{K}] = t_{2}[\vec{K}] \implies t_{1} = t_{2}
$$
where $t[\vec{K}]: Tuple(\vec{K})$ represents the [[Relation (database)#Tuple Projection|projection]] of [[Relation (database)#Tuple|tuple]] $t: Tuple(\vec{A})$ on the [[#Attribute|attributes]] in $\vec{K}$.

For some ***super key*** $\vec{K} \subseteq \vec{A}$ of $R(\vec{A})$ and [[Relation (database)#Attribute|attribute]] $A \in \vec{A}$, if $A \notin \vec{K}$ then $\vec{K} \cup \{ A \}$ is *also* a ***super key*** of $R(\vec{A})$. If we *claim* that $\vec{K} \subseteq \vec{A}$ is a ***super key***, and later find *duplicate values* in the same attributes of $\vec{K}$, then $\vec{K}$ has been ***violated*** and is <u>not</u> a ***super key***. 

## Candidate Key
A ***candidate key*** *(or minimal key)* of [[Relation (database)|relation]] $R(\vec{A})$, is a [[#Super Key|super key]] is a $\vec{K} \subseteq \vec{A}$ of $R(\vec{A})$ that cannot be further subdivided into another <u>super key</u>; this is the ***irreducibility  property***. Every <u>relation</u> has at least <u>one super key</u> (their [[Relation (database)#Attribute Heading|attribute heading]]) which is either ***irreducible*** or contains an ***irreducible*** subset. Therefore every <u>relation</u> has at least <u>one</u> ***candidate key***.

Formally, a ***candidate key*** $\vec{K} \subseteq \vec{A}$ of a [[Relation (database)#Relation|relation]] $R(\vec{A})$ satisfies the ***irreducibility  property***, defined as
$$\large
\text{$\vec{K} \subseteq \vec{A}$ is a candidate key of $R(\vec{A})$} \ \ \ \ \triangleq \ \ \ \ 
\text{$\vec{K}$ is a super key of $R(\vec{A})$} \ \wedge \
\nexists \vec{C} \subset \vec{K} \left( \text{$\vec{C}$ is a super key of $R(\vec{A})$} \right)
$$
Candidate keys are generally preferred (over <u>super keys</u>), as they allow us to enforce <u>stronger</u> uniqueness constraints.

## Primary Key
The ***primary key*** is a [[#Candidate Key|candidate key]] of a [[Relation (database)|relation]], which has been selected as as the *default* <u>candidate key</u> when no *other* <u>candidate keys</u> is explicitly stated.

# Foreign Keys
A ***foreign key*** (despite it's name) is not a [[#Relational Keys|key]], but instead a *references* a [[#Relational Keys|key]]. In particular, the ***foreign key*** $\vec{F}$ of [[#Relations|relation]] $R(\vec{A})$ *referencing* [[#Relational Keys|key]] $\vec{K}$ of [[#Relations|relation]] $S(\vec{B})$, is a *subset* of [[#Attributes|attributes]] $\vec{F} \subseteq \vec{A}$ for which the ***values*** in the [[#Extent|extent]] of $R$ also appear as ***values*** of [[#Attributes|attributes]] $\vec{K}$ in the [[#Extent|extent]] of $S$; it is denoted as $R(\vec{F}) \fk S(\vec{K})$. More succinctly, a ***foreign key*** is a set of ***columns*** in *one* [[#Relations|relation]], who's ***values*** are found in *another* [[#Relations|relation]]'s [[#Relational Keys|key]] ***columns***. 

Formally (recall that $R(\vec{A})$ and $S(\vec{B})$ are *aliases* for the [[#Extent|extents]] of $R$ and $S$ respectively, and [[#Tuple|tuples]] $t_{R} \in R(\vec{A}), t_{S} \in S(\vec{B})$ are [[Mathematical Functions|functions]]), a ***foreign key*** is defined as
$${\large
\begin{aligned}
\text{$\vec{F} \subseteq \vec{A}$ is a} \ \underline{\text{foreign key}} \ \text{of} \ \underline{\text{relation}} \ R(\vec{A}) \\
\textit{referencing} \ \underline{\text{key}} \ \vec{K} \ \text{of} \ \underline{\text{relation}} \ S(\vec{B})
\end{aligned} \ \triangleq \ 
\forall t_R \in R(\vec{A}), \exists t_S \in S(\vec{B}), \forall A \in \vec{F}, \exists B \in \vec{K}: \ \ t_R(A) = t_S(B)
}$$
A _foreign key_ is a subset of attributes _{A}_ in a relation _R1_ that corresponds with a key of another relation _R2_, with the property that the [projection](https://en.wikipedia.org/wiki/Projection_(relational_algebra) "Projection (relational algebra)") of _R1_ on _{A}_ is a subset of the projection of _R2_ on _{A}_. In other words, if a tuple in _R1_ contains values for a foreign key, there must be a corresponding tuple in _R2_ containing the same values for the corresponding key.
TODO^

# Functional Dependency
key functional dependency...