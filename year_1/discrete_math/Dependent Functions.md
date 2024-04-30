A ***dependent function*** is a [[Mathematical Functions|function]] whose *type of return value* varies with its *argument* (i.e. there is no fixed [[Mathematical Functions#Domains, co-domains, ranges|codomain]]). Read more [here](https://en.wikipedia.org/wiki/Dependent_type#%CE%A0_type).

# Formal Definition
Let $\mathbf{D}$ be a set of *types*, where $\bigcup\mathbf{D}$ is the *union* of all these types, and let $\mathcal{T}: I \to \mathbf{D}$ be a *family of types* [[Indexed Family|indexed]] by $I$. The set of ***dependent functions*** ${\large \sub{\prod}{i \in I}} \mathcal{T}(i)$ consists of only [[Mathematical Functions|functions]] $f: I \to \bigcup\mathbf{D}$ such that every $i \in I$ maps to $f(i) \in \mathcal{T}(i)$. In formal notation, this is expressed as:
$$\large
\prod_{\Large i \in I} \mathcal{T}(i) \ \ \triangleq \ \ 
\left\{ \ f: I \to \bigcup\mathbf{D} \ \Big| \ \forall i \in I: f(i) \in \mathcal{T}(i) \ \right\}
$$
If the [[Mathematical Functions|function]] $f$ is an element of ${\large \sub{\prod}{i \in I}} \mathcal{T}(i)$, then just like with regular [[Mathematical Functions#Function type notation|function type notation]], we can write $f: {\large \sub{\prod}{i \in I}} \mathcal{T}(i)$ to denote that $f$ is a ***dependent function***.