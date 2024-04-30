basically the "model" universe where everything about the DB lives - with special constructs and semantics to enable proper representations of how RMDBS behave

![[Pasted image 20240423010223.png|1000]]
![[Pasted image 20240424220859.png|800]]
![[Pasted image 20240424220931.png|800]]

"Fourth, we have said a type is a set of values (more precisely, a named set of values), but it would be more correct to say it is the set of all values that satisfy a certain type constraint."


"In particular, scalars are nominally typed whilst relations and tuples are structurally typed." 
so "tuples and relations" - are fundamentally DIFFERENT types (non-scalar) to all other types (scalar types) - and are produced by TYPE GENERATORS?? - and are possibly fixed in the sense that you cannot add your own?? - in the sense that if you have arrays, those cant be such a type??? which makes sense because the only kinds of values that tuples can have are scalar??? maybe?? or can tuples have other tuples as their content - or even other relations - and so on. more on that topic
![[Pasted image 20240424224520.png|800]]
but the fact that values only ever appear INSIDE tuples i.e. $\langle attribute \ name, \ type \ name, \ value \rangle$ suggests that this "tag" is always implicitly present when dealing with any values - as such - maybe we DONT need to create ourselves headaches like that :)

Interesting idea: maybe have function $Values: \text{salar type names} \to \text{possible values that type}$ so we could use $v: T$ as synonym for $v \in Values(T)$ - which is pretty neat; but all values must them come with a flag that uses it's type; so perhaps a "value" can be the tuple $(T,v)$ where $v \in Values(T)$ and $v: T$ means $(T,v) \in ScalarTypes \times Values(T)$ ?? hard to say. 

the set of values a scalar type $T$ can have is called it's $possreps$ (possible representations) all scalar types come with associated operators - at the very LEAST $=$, if it is *ordinal* then also $<$ - so one way of thinking about it might be the triple $\langle label, possreps, operators \rangle$ - the set of operators supported might be the set of operators in THETA-joins 
![[Pasted image 20240424222825.png|800]]
![[Pasted image 20240424222851.png|800]]
^more on what are operators


![[Pasted image 20240424032914.png|800]]
^example of user defined types

but then they also have to have *selectors* (or is it just user types that do?) which are functions that help you create LITERALS of this type. and every selector needs to create a mapping between $possreps$ i.e. the literals, and the actual underlying types. for example, you can have $Point$ type with $possreps$ $cartesian(x,y)$ and $polar (r,\theta)$ which both map to the exact same type but are created from different literals. the underlying values are "atomic" and hidden to the user - but the $possreps$ can include visible components - and possreps are the ones that can, i guess, be "relation-typed"? so i guess that makes it $\langle label, possreps, selectors, operators \rangle$. 
![[Pasted image 20240424230222.png|800]]
![[Pasted image 20240424230246.png|800]]
![[Pasted image 20240424230343.png|800]]



but THEN - types can also have arbitrary constraints too? that also reference the component by name? and those are basically just predicates on the set of possible values that CAN be?? so its just like this maybe?? 
$$Type \ \text{type\_name} \ Ordinal \ Possrep \ \{ c : CHAR \ | \ P_{1}(c) \wedge P_{2}(c) \wedge \dots \}$$
where $P_{1},P_{2}, \dots$ are the constraints on that type - predicates. 

EXAMPLE SYNTAX
![[Pasted image 20240424040439.png|800]]
^this [part II, tutorial D](https://www.dcs.warwick.ac.uk/~hugh/TTM/DTATRM.pdf)

Treating operators as relations:
![[Pasted image 20240424060220.png|800]]
![[Pasted image 20240424060106.png|800]]
![[Pasted image 20240424060144.png|800]]
