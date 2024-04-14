 SQL is an implementation of a more abstract concept known as 'relational algebra'. Tables are called relations. Columns of those tables are called attributes.

## Mathematical definitions
- Relations take the form: $R(A,B,\dots)$
- $A,B,\dots$ is the set of attributes of the relation
	- The attributes $A,B,\dots$ can sometimes be written as $AB\dots$, or even $\vec{A}$ 
	- The size of the set $\vec{A}$ is what determines the **arity** of the relation $R$, so the relation $R(A_1,\dots,A_n)$ is an $n$-ary  relation
	- $Domain(A)$ is the set of values (type) that attribute $A$ can have. (i.e. INT, VARCHAR, etc.)
	- $Attrs(R)$ will return the set of attributes $\vec{A}$ for the relation $R$
- The **extent** of $R(A,B,\dots)$ is the set of **tuples** $\{\langle v_1^A, v_1^B, \dots \rangle\ , \langle v_2^A, v_2^B, \dots \rangle , \langle v_3^A, v_3^B, \dots \rangle\ , \dots \}$  which are basically like rows in the table. 

## Keys
- Keys are a set of columns that put together will uniquely identify a row for some given table. All tables have at least one key, which is all the columns put together.
- Minimum key is the smallest collection of columns that will still uniquely identify a given table. This is often the primary key, consisting of a single column
- Foreign keys are a set of columns in one table that are found in another table

## Operations
Here are a few operators defined for relations in relational algebra. All operators take relations as input and produce a relation as an output. From these basic operators, more specific operators can be constructed

| Symbol   | Name              | Type   |
| -------- | ----------------- | ------ |
| $\pi$        | Project           | Unary  |
| $\sigma$        | Select            | Unary  |
| $\times$        | Cartesian Product | Binary |
| $\cup$        | Union             | Binary |
| $-$        | Difference        | Binary |

### Project ($\pi$)
For some relation $R(A,B,\dots)$ we can do $\pi_A \ R$ which will select the attribute $A$ from $R$ and copy over all the values in the rows of $R$ (getting rid of the duplicates), and produces a new relation with only the attribute $A$ in it, along with these copied values.
If I wanted to select both $A$ and $B$ I would have instead done $\pi_{A,B} \ R$.

### Select ($\sigma$)
For some relation $R(A,B,\dots)$ we can do $\sigma_P \ R$, where $P$ is some predicate that operates over a row and either holds or doesn't. If the predicate $P$ holds, the row is kept, if it doesn't, the row is skipped. All the rows that were kept now form a new relation with all the same attributes as $R$, just with potentially fewer rows.
For instance we could do $\sigma_{A>0} \ R$, which would select all rows from $R$ where $A>0$ holds.

### Cartesian Product ($\times$)
For some relation $R(A,B,C)$ and $S(D,E)$ we can do $R \times S$ which will produce a new relation where the attributes are combined into $A,B,C,D,E$ and each of the rows in $R$ will be matched with each of the rows in $S$, and combined into one big row. So the result will be that if $R$ has $m$ rows, and $S$ has $n$ rows, then $R \times S$ has $mn$ rows.
![[Pasted image 20231011230656.png]]

### Union ($\cup$)
This operation can only work for two relations that share the same attributes. For example $R(\vec{A})$ and $S(\vec{A})$ for some attributes $\vec{A}$. $R \cup S$ will combine the rows in both relations and eliminate any duplicates

### Difference ($-$)
This operation can only work for two relations that share the same attributes. For example $R(\vec{A})$ and $S(\vec{A})$ for some attributes $\vec{A}$. $R-S$ will yield a new relations that contains all rows from $R$ that are not in $S$.