Differentiation tries to capture and define the idea of analysing the change in a function. It can be thought of as finding the slope of a function, like this:
![[Pasted image 20231129171651.png]]

# Formal Definition
For some $A \subseteq \mathbb{R}$, if there exists an open interval $I$ for which $a \in I \subseteq A$, then fix the point $a$. This property will allow us to [[Limit of a Function#"Deleted Neighbourhood" condition|prove useful results without assuming more things]]. Now consider the function $f: A \to \mathbb{R}$, and its behaviour near the point $a$.

## Newton's Difference Quotient
We can now define ***Newton's difference quotient*** at $a$ for $f$ as:
$$
\begin{align}
\DeclareMathOperator{\dom}{dom}
&\Delta_{a}(h) = \frac{f(a+h)-f(a)}{(a + h) - a} = \frac{f(a+h)-f(a)}{h}
\end{align}
$$
We can see that the [[Mathematical Functions#Domains, co-domains, ranges|domain]] of $\Delta_{a}$ cannot include $0$, or any $h \in \mathbb{R}$ for which $f(a + h)$ is not defined. We can express these requirements as $\dom (\Delta_{a}) = \{ \ h \in \mathbb{R} \ | \ h\neq 0, \ a + h \in A \ \}$.

We can interpret $\Delta_{a}(h)$ as a function that plots the line that crosses points $(f(a), a)$ and $(f(a + h), a+h)$.
i.e. For $f(x)=x^2$ we can pick $a=1$, we have the following (*blue*) plot of $\Delta_{a}(h)$:
```desmos-graph
bottom=-1; top=5;
left=-4; right=4;
---

f(x)=x^2 | red
g(x) = (f(1+x)-f(1))/x | blue
```

## Differentiable Functions
***Differentiability***, just like [[Continuity|continuity]], is defined as a *point-wise* property. Thus, the definition is as follows:
$$f \ \text{is differentiable at} \ a \iff \exists f'(a) \in \mathbb{R}: \ \ f'(a) = \lim_{ h \to 0 } \Delta_{a}(h)$$
We call $f'(a)$ the ***derivative*** of $f$ at $a$. It is also often denoted as $\dfrac{\mathrm{d} f}{\mathrm{d} x}(a)$ or $\dfrac{\mathrm{d}}{\mathrm{d} x}f(a)$. We can spot quite easily that if $f$ is ***differentiable*** at $a$, then it is also [[Continuity|continuous]] at $a$, meaning that if $f$ is not continuous at $a$ then it can't be differentiable at $a$ either. Just like [[Continuity|continuity]], the *point-wise* property can be extended to the whole [[Mathematical Functions#Domains, co-domains, ranges|domain]] of $f$ as such:
$$f \ \text{is differentiable} \iff \forall x \in A: \ \ f \ \text{is differentiable at} \ x$$
If $A' \subseteq A$ is the set of points at which $f$ is differentiable, we can form a function that *maps* every $x \in A'$ to $f'(x)$. This function is called the ***derivative*** of $f$; denoted as $f'$, $\dfrac{\mathrm{d} f}{\mathrm{d} x}$ or $\dfrac{\mathrm{d}}{\mathrm{d} x}f$.

### Higher Order Derivatives
Since $f'$ (the ***derivative*** of $f$) is a function, we can also find it's derivative $f''$, called the $2$-nd derivative. The function $f$ is called ***$n$-times differentiable*** at $a \in A$, if the $n$-th ***derivative*** of $f$ at $a$ exists. The ***$n$-th derivative*** of $f$ is defined as:
$$
\huge
f^{(n)} = \begin{cases}
f' & n = 1 \\
\big(f^{(n-1)}\big)' & n > 1
\end{cases}
$$
It is also denoted as $\dfrac{\mathrm{d}^n f}{\mathrm{d} x^x}$ or $\dfrac{\mathrm{d}^n}{\mathrm{d} x^n}f$. We call $f^{(n)}(a)$ the ***$n$-th derivative*** of $f$ at $a$. It is also often denoted as $\dfrac{\mathrm{d}^n f}{\mathrm{d} x^n}(a)$ or $\dfrac{\mathrm{d}^n}{\mathrm{d} x^n}f(a)$. So for example, $f^{(3)}(a) = f'''(a)$ would be called the $3$-rd derivative of $f$.

### Limits are Important
It is very important to keep in mind that whatever the [[#Newton's Difference Quotient|quotient]] ends up being, it must have a limit with $h$ approaching $0$. For example, if we are trying to differentiate $f(x) = |x|$ at $x=0$, we run into the following issue: 
$$
\lim_{ h \to 0 } \frac{|x+h|-|x|}{h} = \lim_{ h \to 0 } \frac{|h|}{h}
$$
If we plot the function $g(h) = \frac{|h|}{h}$ we see this: 
```desmos-graph
top=2; bottom=-2
---

f(x) = \abs(x)/x | red
```
As $h\to 0$ from the left, i.e its [[One-Sided Limits|left-sided]] limit, it approaches $-1$. Similarly, as $h \to 0$ from the right, i.e. its [[One-Sided Limits|right-sided]] limit, it approaches $1$. Therefore we can deduce that at $x=0$, no limit for the resulting [[#Newton's Difference Quotient|quotient]] exists, and therefore $f(x)=|x|$ is not differentiable at $x=0$.

### Critical Points of Real Functions
A ***critical point*** of some function $f$, is a point for which $f$ is *not differentiable*, or for which the derivative is $0$. For instance, the function $f(x)=|x|+x^3$ has two critical points at $(0,0)$ and $\left( -\frac{1}{\sqrt{ 3 }}, \frac{2}{3 \sqrt{ 2 }} \right)$.
```desmos-graph
top=2; bottom=-2;
left=-2; right=2;
---

f(x) = \abs(x) + x^3 | red
(0,0)
( -(1/\sqrt{3}), 2/(3\sqrt{3}) )
```

# Properties of Derivatives
Let $f,g:(a,b) \to \mathbb{R}$ be two functions: 
1. Polynomial have derivatives at all points
3. $f \ \text{is differentiable in} \ (a,b) \implies f'(x_{0})=0 \ \text{for any} \ x_{0} \ \text{at at which} \ f \ \text{is maximum or minimum}$
4. $\frac{d}{dx} [f(x)g(x)] = f'(x)g(x) + g(x)f'(x)$
5. $\frac{d}{dx} [f(g(x))] = f'(g(x))g'(x)$
6. For some $a,b\in \mathbb{R}$: $\frac{d}{dx}[af(x)+bg(x)] = af'(x)+bg'(x)$

