Is one approach at defining the integral of a function on an interval.
# Formal Definitions
There are two types of Reimann integral, **upper** and **lower**. For some function $f:[a,b] \to \mathbb{R}$, the **upper integral** is defined as such $$\overline{\int_{a}^{b}} f(x) \, dx = inf \{ \ U(f,P) \ | \ P \ \text{is a partition of} \ [a,b] \ \}$$
Which essentially means, select the [[Infimum and supremum|infimum]] of all the possible [[#Lower and Upper sums|upper sums]] of $f$.
Similarly, the **lower integral** is defined as such $$\underline{\int_{a}^{b}} f(x) \, dx = sup \{ \ L(f,P) \ | \ P \ \text{is a partition of} \ [a,b] \ \}$$Which essentially means, select the [[Infimum and supremum|supremum]] of all the possible [[#Lower and Upper sums|lower sums]] of $f$.
We can use these definitions to define the property of being **Reimann integrable**: $$f \ \text{is Reimann integrable} \ \ \triangleq \ \ \overline{\int_{a}^{b}} f(x) \, dx = \underline{\int_{a}^{b}} f(x) \, dx$$
If $f$ is Reimann integrable, we call the common value of the upper and lower integrals, the **Reimann integral**, and it is denoted as such $$\int_{a}^{b} f(x) \, dx = \overline{\int_{a}^{b}} f(x) \, dx = \underline{\int_{a}^{b}} f(x) \, dx$$

## Improper Reimann Integral
Some functions are not bounded, for instance $f:[a,\infty) \to \mathbb{R}$, and so cannot be Reimann integrable in the usual sense. Instead, we must use limits to correct these issues. So for the function above it would be $$\text{Improper Reimann integral of} \ f \triangleq \lim_{ x \to \infty } \int^x_{a} f(x) \, dx$$If the limit evaluates to a real number, then we can say that the improper Reimann integral converges, otherwise it diverges.

## Partition
The idea of a partition is that you split the interval you are integrating over into a finite number of sub-intervals. So for some number $n \in \mathbb{N}^+$ we have that $$P \ \text{is a partition of} \ [a,b] \ \triangleq \ P = \{ r_{i} \ | \ 0 \leq i \leq n, \ a=r_{0}, \ b=r_{n}, \ r_{i} < r_{i+1} \}$$
Intuitively speaking, you are essentially picking a finite number of points between $a$ and $b$ and putting them in a set, which is called the partition of the interval. And the points don't even have to be equidistant from each other.

For example, if I have the interval $[1,10]$ then $P = \{ 1, 2, 5, 9, 10 \}$ is partition with $n=4$
```desmos-graph
left=-1; right=15;
top=0.1; bottom=-0.1;
---
1<=x<=10 | -0.01<y<0.01 | blue
(1,0) | red
(2,0) | red
(5,0) | red
(9,0) | red
(10,0) | red
```

Another way of writing the partition $P$ is $$P: a=r_{0}<r_{1}<\dots <r_{r}<\dots<r_{n-1}<r_{n}=b$$
### Subintervals
Given some partition $P$ of interval $[a,b]$, each closed interval $[r_{i},r_{i+1}]$ for $0\leq i < n$ is called a subinterval of $P$.

So, going back to our example above, we would have that $[1,2],[2,5],[5,9],[9,10]$ are all subintervals of $P=\{ 1,2,5,9,10 \}$. Notice how the number of subintervals (4) is the same as the $n$ we picked (also 4).
```desmos-graph
left=-1; right=15;
top=0.1; bottom=-0.1;
---
(1,0) | blue
(10,0) | blue

-0.02<=y<=0.02 | 1<=x<=2 | red
-0.02<=y<=0.02 | 2<=x<=5 | green
-0.02<=y<=0.02 | 5<=x<=9 | yellow
-0.02<=y<=0.02 | 9<=x<=10 | magenta
```

### Norm of a Partition
The **norm** of a partition $P$, denoted as $||P||$, is the largest length of the subintervals in $P$. Mathematically, we say: $$||P||  \triangleq max \{  r_{i+1} - r_{i} \ | \ 0\leq i < n   \}$$So going back to our example, the $||P||$ of $P=\{ 1,2,5,9,10 \}$ is $9-5=4$.

### Refining Partitions
If we have $P_{1}$ and $P_{2}$ which are partitions of $[a,b]$, and $P_{1}$ is a subset of $P_{2}$, then $P_{2}$ is a refines $P_{1}$. This is written as: $$P_{2} \ \text{refines} \ P_{1} \triangleq P_{1} \subset P_{2}$$It is easy to understand intuitively, as $P_{2}$ has the same, and more, points as $P_{1}$, hence it can be understood to be more 'fine grained'.

Going back to our example of $P = \{1,2,5,9,10\}$. A refinement of $P$, $P'$ could for example be $P' = \{ 1,2,3,4,5,9,10 \}$. It has the same, and more, elements as $P$.

## Sums
Let there be some function $f: [a,b] \to \mathbb{R}$, and a [[#Partition|partition]] $P$ of $[a,b]$ given by $$P: \ \ \ \ a=r_{0}<r_{1}<\dots<r_{i}<\dots<r_{n-1} < r_{n}$$
For any [[#Subintervals|subinterval]] of the form $[r_{i}, r_{i+1}]$ (for $0\leq i < n$), we define $\Delta r_{i} = r_{i+1}-r_{i}$.

### Reimann sum
Choose one element $s_{i} \in [r_{i}, r_{i+1}]$ from each of the [[#Subintervals|subintervals]] of $P$. This forms the sequence $(s_{i})_{0 \leq i<n}$. Then the Reimann sum for $P$, and the corresponding choices of $s_{i}$, is $$S(f, P, (s_{i})_{0 \leq i<n})= \sum^{n-1}_{i=0} \Delta r_{i} f(s_{i})$$
Notice how Reimann sums aren't unique. Depending on your choice of elements from each subinterval, you may get a different sum.
For example, for $f: [1,10] \to \mathbb{R}$, we choose $P= \{ 1,2,5,9,10 \}$, which forms the partitions $[1,2],[2,5],[5,9],[9,10]$. We then choose $s_{i} = 1.5, \ 4, \ 7, \ 9.3$, and we get the following visualisation
```desmos-graph
left=-1; right=11;
top=6; bottom=-1;
---

f(x) = (x/6.6)*\sin(0.9x)+2 | 1 <= x <= 10 | #5555ff

0<=y<=f(1.5) | 1<=x<=2 | red
x=1.5 | 0<=y<=f(1.5) | red

0<=y<=f(4) | 2<=x<=5 | green
x=4 | 0<=y<=f(4) | green

0<=y<=f(7) | 5<=x<=9 | yellow
x=7 | 0<=y<=f(7) | yellow

0<=y<=f(9.3) | 9<=x<=10 | magenta
x=9.3 | 0<=y<=f(9.3) | magenta
```
The sum of the areas of the rectangles is the Reimann sum of $P$

### Lower and Upper sums
The lower and upper sums are special cases of the [[#Reimann sum]], where the choice for $s_{i}$ is determined by the smallest (for lower sum) and largest (for upper sum) element per [[#Subintervals|subinterval]].
To define it formally, we have to use [[Infimum and supremum|supremum and infimum]] as a way to obtain the minimal and maximal elements. For some function  Define the following: 
$$
\begin{gathered}
M_{i} = sup \{ \ f(x) \ | \ r_{i} \leq x \leq r_{i+1} \  \} & & \text{(for } 0\leq i < n \text{)} \\
m_{i} = inf \{ \ f(x) \ | \ r_{i} \leq x \leq r_{i+1} \  \} & & \text{(for } 0\leq i < n \text{)}
\end{gathered}
$$
Notice how $M_{i}$ and $m_{i}$ are just special cases of $s_{i}$ in the Reimann sums. This means the definition of lower and upper sums will look very similar to it:
$$
\begin{gathered}
U(f, P) = \sum^{n-1}_{i=0} M_{i} \Delta r_{i} \\
L(f, P) = \sum^{n-1}_{i=0} m_{i} \Delta r_{i}
\end{gathered}
$$
It is the case that $U(f,P)$ overestimates  the area under the curve, while $L(f,P)$ underestimates it. And as the partition $P$ gets more and more [[#Refining Partitions|refined]], the upper and lower sums are closer and closer to the true area under the curve. The standard result for the relation of upper and lower sums is $L(f,P) \leq S(f,P)$.

Continuing from the Reimann sums visualisation, the upper sum, choosing the maximum values, would look like this:
```desmos-graph
left=-1; right=11;
top=6; bottom=-1;
---

f(x) = (x/6.6)*\sin(0.9x)+2 | 1 <= x <= 10 | #5555ff

0<=y<=f(2) | 1<=x<=2 | red
x=2 | 0<=y<=f(2) | red

0<=y<=f(2.25) | 2<=x<=5 | green
x=2.25 | 0<=y<=f(2.25) | green

0<=y<=f(8.9) | 5<=x<=9 | yellow
x=8.9 | 0<=y<=f(8.9) | yellow

0<=y<=f(9) | 9<=x<=10 | magenta
x=9 | 0<=y<=f(9) | magenta
```
While the lower sum, choosing the minimum values, would look like this:
```desmos-graph
left=-1; right=11;
top=6; bottom=-1;
---

f(x) = (x/6.6)*\sin(0.9x)+2 | 1 <= x <= 10 | #5555ff

0<=y<=f(1) | 1<=x<=2 | red
x=1 | 0<=y<=f(1) | red

0<=y<=f(5) | 2<=x<=5 | green
x=5 | 0<=y<=f(5) | green

0<=y<=f(5.45) | 5<=x<=9 | yellow
x=5.45 | 0<=y<=f(5.45) | yellow

0<=y<=f(10) | 9<=x<=10 | magenta
x=10 | 0<=y<=f(10) | magenta
```

# Properties
Using the definitions of [[Infimum and supremum|supremum and infimum]], we can show the following properties to hold: for a bounded function $f:[a,b] \to \mathbb{R}$
- $\int_{a}^b f(x) \, dx = c \iff \forall \varepsilon \in \mathbb{R}^+, \exists P (\ P \ \text{is a partition of} \ [a,b] \ \wedge \ (c-L(f,P) < \varepsilon) \ \wedge \ (U(f,P) - c < \varepsilon) \ )$
- $\int_{a}^b f(x) \, dx = c \iff \forall \varepsilon \in \mathbb{R}^+, \exists \delta \in \mathbb{R}^+, \forall P (\ P \ \text{is a partition of} \ [a,b] \ \wedge \ ||P||<\delta \ \implies \ |S(f, P, (s_{i})_{0\leq i<n})| < \varepsilon \ )$
Using the definitions of [[Continuity|continuous functions]] and [[Uniform Continuity|uniform continuity]], we can show that for $f: [a,b] \to \mathbb{R}$, $$f \ \text{is a continuous function on} \ [a,b] \implies f \ \text{is Reimann integrable} $$
Some more useful results:
- $\int^{b}_{a} sf(x) + tg(x) \, dx = s\int^{b}_{a} f(x) \, dx + t\int^{b}_{a} g(x) \, dx \impliedby f,g \ \text{are integrable}$
- $\int^b_{a} c \, dx = c(b-a), \ \text{where} \ c \in \mathbb{R} \ \text{is a constant}$
- $\int^c_{a} f(x) \, dx = \int^b_{a} f(x)  \, dx + \int^c_{b} f(x) \, dx \impliedby \text{the integrals exist for} \ a<b<c$
- $\forall x \in [a,b] (f(x) \geq 0) \implies \left( f \ \text{is integrable over} \ [a,b] \implies \int^b_{a} f(x)  \, dx \geq 0 \right )$

