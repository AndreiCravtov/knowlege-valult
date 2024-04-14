***Uniform continuity*** is a stronger form of [[Continuity|continuity]], therefore any *uniformly continuous* function is ***also*** *continuous*.

# Formal definition
Let $(X,d_{X})$ and $(Y,d_{Y})$ be [[Metric Space|metric spaces]], and let $f:X \to Y$ be a function. Given some $A \subseteq X$ We say that: $$f \ \text{is uniformly continuous on} \ A \ \ \iff\ \ \forall \varepsilon>0,\exists\delta>0,\forall a,b \in A: \ \ d_{X}(a,b)<\delta \implies d_{Y}\big(f(a),f(b)\big)<\varepsilon$$This definition is quite similar to that of [[Continuity#Formal definition|continuity]]. The difference is that with *regular* ***continuity***, $\delta$ can depend on **both** $\varepsilon$ and some $x_{0} \in A$. On the other hand, ***uniform continuity*** has the restriction that $\delta$ can only depend on $\varepsilon$, and not any $x_{0} \in A$.

## Intuition
The way to understand it is to look back at the box model in the [[Limit of a Function#Intuition|epsilon-delta]] definition, where the $\delta$ and $\varepsilon$ formed a box around some function like so: 
```desmos-graph
left=-1; right=10;
top=15; bottom=-1;
---
(7.25,12.5) | hidden | black | label: `f(x)=2x, \ 1 \leq x \leq 6`

f(x)=2x | 1<=x<=6 | black


(-0.2, 7) | hidden | red | label: `L`
y=7 | x>0 | red
(-0.2, 10) | hidden | #990000 | label: `L + \varepsilon`
y=10 | x>0 | #990000 | dashed
(-0.2, 4) | hidden | #990000 | label: `L - \varepsilon`
y=4 | x>0 | #990000 | dashed

(3.5, -0.04) | hidden | blue | label: `p`
x=3.5 | y>0 | blue
(5, -0.04) | hidden | #000099 | label: `p + \delta`
x=5 | y>0 | #000099 | dashed
(2, -0.04) | hidden | #000099 | label: `p - \delta`
x=2 | y>0 | #000099 | dashed
```
See, with *regular [[Continuity|continuity]]*, the size and shape of this box **can change and adapt** depending on which $x_{0}$ we pick. However, ***uniform continuity*** grantees that the size and shape of this box **will not change** based on $x_{0}$.

So for example, $f(x)=2x$ is uniformly continuous and here is a sketch of the same-sized delta-epsilon box being moved around for different values of $x_{0}$, to demonstrate that this is the case:
```desmos-graph
left=-1; right=10;
top=15; bottom=-1;
---
(7.25,12.5) | hidden | black | label: `f(x)=2x, \ 1 \leq x \leq 6`

f(x)=2x | 1<=x<=6 | black

y=8 | 4>=x>=3 | red
y=6 | 4>=x>=3 | red
x=4 | 8>=y>=6 | red
x=3 | 8>=y>=6 | red

y=10| 5>=x>=4 | blue
y=8 | 5>=x>=4 | blue
x=5 | 10>=y>=8 | blue
x=4 | 10>=y>=8 | blue

y=6 | 3>=x>=2 | green
y=4 | 3>=x>=2 | green
x=3 | 6>=y>=4 | green
x=2 | 6>=y>=4 | green
```

On the other hand, something like $f(x)=\frac{1}{x}$ is not **uniformly continuous**, but just *regular* **continuous**. And so the size and shape of the delta-epsilon boxes change:
```desmos-graph
left=-0.3; right=5;
top=5; bottom=-0.3;
---
f(x)=1/x | x>0 | black

y=4 | 0.5>=x>=0.25 | green
y=2 | 0.5>=x>=0.25 | green
x=0.5 | 4>=y>=2 | green
x=0.25 | 4>=y>=2 | green

y=2 | 2>=x>=0.5 | red
y=0.5 | 2>=x>=0.5 | red
x=2 | 2>=y>=0.5 | red
x=0.5 | 2>=y>=0.5 | red

y=0.5 | 4>=x>=2 | blue
y=0.25 | 4>=x>=2 | blue
x=4 | 0.5>=y>=0.25 | blue
x=2 | 0.5>=y>=0.25 | blue
```
