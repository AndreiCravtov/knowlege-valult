A ***tuple**** is an *ordered list* of objects. An $n$***-tuple*** is a ***tuple*** of $n$ elements. 

It is the *extrapolation* of [[Ordered Pair|ordered pairs]], as such it has these properties:
$$\large \langle a_{1}, a_{2}, \dots, a_{n} \rangle = \langle b_{1}, b_{2}, \dots, b_{n} \rangle \iff a_{1} = b_{1} \wedge a_{2} = b_{2} \wedge \dots \wedge a_{n} = b_{n}$$


# Formal Definition
Using the ***accepted*** [Kuratowski](https://en.wikipedia.org/wiki/Kazimierz_Kuratowski) definition of [[Ordered Pair|ordered pair]], we can define ***tuples***.

The $n$-tuple $\large \langle a_{1}, a_{2}, \dots, a_{n} \rangle$ is defined as $\large \langle a_{1}, a_{2}, \dots, a_{n-1} \rangle \to a_{n}$ with the $0$-tuple being defined as the empty set $\emptyset$. Here $a \to b$ is an *alias* for $\opair{a}{b} = \{ \{ a \}, \{ a, b \} \}$.

So with this definition:
$$\large
\begin{align}
&\langle\rangle &&&&= \emptyset  \\
&\langle 1 \rangle &&= \langle\rangle \to 1 &&= \emptyset \to 1 \\
&\langle 1,2 \rangle &&= \langle 1 \rangle \to 2 &&= (\emptyset \to 1) \to 2 \\
&\langle 1,2 \rangle &&= \langle 1, 2 \rangle \to 3 &&= ((\emptyset \to 1) \to 2) \to 3 \\
&\dots
\end{align}
$$
