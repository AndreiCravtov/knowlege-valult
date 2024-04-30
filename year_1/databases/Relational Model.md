#database-theory #relational-model 

The ***relational model*** is a formal system [formal system](https://en.wikipedia.org/wiki/Formal_system "Formal system") *(and approach to managing data)* using [[|tuples]] *(or rows)*, [[|attributes]] *(or columns)* and [[|relations]] *(or tables)*. One interpretation is that each <u>tuple</u> represents [logical](https://en.wikipedia.org/wiki/Logic "Logic") [proposition](https://en.wikipedia.org/wiki/Propositions "Propositions") about its contents, and every <u>relation</u> therefore represents a <u>logical proposition</u> equivalent to the conjunction it's <u>tuple propositions</u>. The <u>database</u>, in turn, contains a set of <u>relations</u>, and thus it represents a <u>logical proposition</u> equivalent to the conjunction it's <u>relation propositions</u>. From this perspective, a <u>databases</u> are just *(highly structured)* [truth values](https://en.wikipedia.org/wiki/Truth_value).

It broadly consists of these five components
1. An open-ended collection of [[#Scalar Type|scalar types]], including <u>at least</u> the type $Boolean$ 
2. A [[|relation type generator]] and an interpretation for relations of the generated types generated
3. Facilities for definition [[|relvars]] of such generated type
4. A [[|relational assignment]] operator for assigning relation <u>values</u> to relation <u>variables</u>
5. A [[Relational Algebra|relational algebra]] *(or equivalent language)*, for manipulating relation <u>values</u>

# Values and Types
In the relational model, all ***values*** are have a ***data type*** (*or data domain*), writing $v : \mathcal{T}$ to denotes that ***value*** $v$ is of ***type*** $\mathcal{T}$. Types can be either [[#Scalar Type|scalar]] or <u>non-scalar</u> ([[|tuple]] and [[|relation]]). The difference with the main difference being that <u>scalar values</u> have no *"visible components"* and are [nominally typed](https://en.wikipedia.org/wiki/Nominal_type_system), i.e. type-checking is done with <u>labels</u>, on the other hand <u>non-scalar values</u> do have *"visible components"* and are [structurally typed](https://en.wikipedia.org/wiki/Structural_type_system), i.e. the type-checking is done by the *actual structure* of the value.

That means that the same set of possible scalar values could be paired with different labels and hence different types. On the other hand, <u>structural typing</u> means there's only one type of that kind - the one corresponding to that structure.

## Scalar Type
a scalar value is type constraints + actual values set + possreps + selectors + readonly operators + updateable operators

possreps are - too - typed




everything is "typed". there are two main kinds of types: "scalar" and "composite"

![[Pasted image 20240424223446.png|800]]
![[Pasted image 20240424223548.png|800]]
![[Pasted image 20240424223621.png|800]]
![[Pasted image 20240424223719.png|800]]
![[Pasted image 20240424223742.png|800]]
![[Pasted image 20240424223801.png|800]]







# Variables and Updates
Databases aren't static, they change all the time. This idea is represented by the database variable

this idea must be represented in the relational model. 


# Database: variable, assignment, constraint, value
basically database variables are conceptually what hold the entire database value - and any smaller variables: relvars, tuple vars, etc, are just "pseudovariables" in the sense that - changing them is the same as changing the database variable. thus all "updating" operators really just define a transformation from some currend DB value to a new one. 

how the actual change in values (of the DB variable) is completely orthoganal. maybe you want to encode it all as a function, or a Deterministic transition thingy, or whatever. 

A database value then is a tuple - where each attribute is relation-typed, and it is each of these attribute values that are "relvars".
together, it also comes with the "context" that stores type information, constraint information, and so on


![[Pasted image 20240425002029.png|800]]
![[Pasted image 20240425002044.png|800]]
![[Pasted image 20240425002117.png|800]]
![[Pasted image 20240425002146.png|800]]





