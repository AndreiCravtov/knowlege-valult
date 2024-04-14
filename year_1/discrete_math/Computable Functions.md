The notion of *computability*, is the idea that a [[Mathematical Functions|function]] can be solved in a finite amount of steps. For example $f(x)= \sqrt{ 2 }$ is is *not computable*, as reaching the answer requires infinite steps. On the other hand $f(x) = x^2$ is *computable*, as you can reach the answer with a finite amount of steps.

There are many many formalisations of *computability* that were created (by Hilbert, Kurt Gödel, Alonzo Church, Stephen Kleene, Emil Post, Alan Turing, and Andrey Markov, and so on) but all of them have been shown to be equivalent to [Turing Completeness](https://en.wikipedia.org/wiki/Turing_completeness), and therefore it is said that there is only **one** notion of *computability*. 

# General Recursive Function
The **Ackermann Function**, $Ack(x,y)$, is a computable, and yet it is not [[#Primitive Recursive Function|primitively recursive]]. It is defined as the following 
$$
\begin{gathered}
Ack(0,y) = Succ(y) \\
Ack(Succ(x),0) = Ack(x,1) \\
Ack(Succ(x),Succ(y)) = Ack(x, \ Ack(Succ(x),y))
\end{gathered}
$$
In order to resolve this issue, [[#Primitive Recursive Function|primitive recursion]] is extended into the class of *general recursive* (sometimes *partial recursive*) functions $\mathcal{F}_{rec} \subset \cup_{k=1}^{\infty}( \mathbb{N}^k \to \mathbb{N})$, by introducing the *rule of minimisation*, defined as following:
$$
\begin{gathered}
\textit{Minimisation:} & \text{For some} \ g: \mathbb{N}^{k+1} \to \mathbb{N} \in \mathcal{F}_{rec}, \\ & \text{we define} \ f:\mathbb{N}^{k} \to \mathbb{N} \ \text{as:} \\ \\
& f(x_{1},\dots,x_{k}) = \mu y[g(y,x_{1},\dots,x_{k})=0] \\
\textit{So} \ f \ \textit{is in} \ \mathcal{F}_{rec}
\end{gathered}
$$
Where '$\mu y$' expresses the search for the smallest argument $y$ for which the condition inside the square brackets, holds. If this value does not exists, the search never terminates (so $f$ is [[Partial Functions|partial]].)

**NOTE:** General Recursion is equivalent to [Turing Completeness](https://en.wikipedia.org/wiki/Turing_completeness), meaning all programs can be expressed as *generally recursive* functions.

## Primitive Recursive Function
The class of *primitive recursive* functions $\mathcal{F}_{pr} \subset \cup_{k=1}^{\infty}( \mathbb{N}^k \to \mathbb{N})$, is generated by these rules:
$$
\begin{gathered}
\textit{Initial functions:} & Zero(x) = 0 & \textit{Zero Function} \\
& Proj^n_{i}(x_{1},\dots,x_{n}) = x_{i} \ \ \ \ (1\leq i\leq n) & \textit{Projection} \\
& Succ(x) = x + 1 & \textit{Successor} \\
\textit{Are all in} \ \mathcal{F}_{pr}
\end{gathered}
$$
$$
\begin{gathered}
\textit{Composition:} & \text{For some} \ g_{1},\dots g_{m}: \mathbb{N}^k \to \mathbb{N}, \ h:\mathbb{N}^{m}\to \mathbb{N} \in \mathcal{F}_{pr}, \\ & \text{we define} \ f:\mathbb{N}^{k} \to \mathbb{N} \ \text{as:} \\ \\
& f(x_{1},\dots,x_{k}) = h(g_{1}(x_{1},\dots,x_{k}),\dots,g_{m}(x_{1},\dots,x_{k})) \\
\textit{So} \ f \ \textit{is in} \ \mathcal{F}_{pr}
\end{gathered}
$$
$$
\begin{gathered}
\textit{Recursion:} & \text{For some} \ g: \mathbb{N}^k \to \mathbb{N}, \ h:\mathbb{N}^{k+2}\to \mathbb{N} \in \mathcal{F}_{pr}, \\ & \text{we define} \ f:\mathbb{N}^{k+1} \to \mathbb{N} \ \text{as:} \\ \\
& f(0,x_{1},\dots,x_{k}) = g(x_{1},\dots,x_{k}) \\
& f(Succ(y),x_{1},\dots,x_{k}) = h(y,f(y,x_{1},\dots,x_{k}), x_{1},\dots,x_{k}) \\
\textit{So} \ f \ \textit{is in} \ \mathcal{F}_{pr}
\end{gathered}
$$

**i.e.** we can re-define the function $Add(x,y)=x+y$ in term of the *primitive recursive* schema as such: 
$$
\begin{gathered}
Add(0,x) = Proj^1_{1}(x) = x \\
Add(Succ(y),x) = Succ(Proj_{2}^3(y,Add(y,x),x)) = Add(y,x) + 1
\end{gathered}
$$

There are many other functions out there that can be defined in terms of the *primitive recursive* schema, such as:
- $Pred(x) = x - 1$
- $Mult(x,y) = x*y$
- $Fact(x)=x!$