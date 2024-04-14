When dealing with functions of the type $f: \mathbb{R}^n \to \mathbb{R}$ ($n>1$), the ***partial derivative*** is simply the [[Differentiation of Real Functions|derivative]] of $f$ with respect to one of it's variables - with the others held constant. It is called ***partial***, because it only tells you about the behaviour of ***one*** of the variables. 

# Formal Definition
Let $U \subseteq \mathbb{R}^n$ be an [[Open Set|open set]] and $f: U \to \mathbb{R}$ be a function. Fix some point $\pmb {a} = (a_{1},\dots,a_{n}) \in U$. When the $i$-th component of $\pmb a$ is picked, we can reduce $f$ to single-variable function, defining $f_{a_{i}}(x) = f(a_{1},\dots,a_{i-1},x,a_{i+1},\dots,a_{n})$. The ***partial derivative*** of $f$ at $\pmb a$ with respect to the $i$-th variable $x_{i}$, is defined as the [[Differentiation of Real Functions|derivative]] of $f_{a_{i}}$ at $a_{i}$
$$
\begin{align}
\dfrac{\partial}{\partial x_{i}}f(\pmb a) = f_{a_{i}}'(a_{i})
&= \lim_{ h \to 0 } \frac{f_{i}(a_{i} + h) - f_{i}(a_{i})}{h} \\
&= \lim_{ h \to 0 } \frac{f(a_{1},\dots,a_{i-1},a_{i} + h,a_{i+1},\dots,a_{n}) - f(a_{1},\dots,a_{i-1},a_{i},a_{i+1},\dots,a_{n})}{h} \\
&= \lim_{ h \to 0 } \frac{f(\pmb a + h \pmb{e_{i}}) - f(\pmb a)}{h}, \ \text{the $i$-th component of $\pmb{e_{i}}$ is $1$ and the rest are $0$}  
\end{align}
$$
The ***partial derivative*** $\dfrac{\partial}{\partial x_{i}}f(\pmb a)$ is often also denoted as $\dfrac{\partial f}{\partial x_{i}}(\pmb a)$ or $f'_{x_{i}}(\pmb a)$. As with regular [[Differentiation of Real Functions|differentiability]], the *point-wise* property can be extended to:
$$f \ \text{is partially differentiable with respect to} \ x_{i} \iff \forall \pmb a \in U: \ \ f \ \text{is partially differentiable with respect to} \ x_{i} \ \text{at} \ \pmb a$$
If $U'_{x_{i}} \subseteq U$ is the set of points at which $f$ is *partiality differentiable with respect to $x_{i}$*, we can form a function that *maps* every $\pmb x \in U'_{x_{i}}$ to $\dfrac{\partial}{\partial x_{i}}f(\pmb x)$. This function is called the ***partial derivative*** of $f$ with respect to $x_{i}$; denoted as $\large f'_{x_{i}}$, $\dfrac{\partial f}{\partial x_{i}}$ or $\dfrac{\partial }{\partial x_{i}}f$.

## Mixed Partial Derivatives 
Just like with regular [[Differentiation of Real Functions#$n$-differentiable Functions|differentiability]], we can define the ***$n$-th partial derivative*** of $f$ with respect to $x_{i}$, as:
$$
\huge
f^{(n)}_{x_{i}} = \begin{cases}
f'_{x_{i}} & n=1  \\
\big(f^{(n-1)}_{x_{i}}\big)' & n>1  \\
\end{cases}
$$
It is also often denoted as $\dfrac{\partial^n f}{\partial x_{i}^n}$ or $\dfrac{\partial^n}{\partial x_{i}^n}f$. But unlike regular [[Differentiation of Real Functions#$n$-differentiable Functions|differentiability]], we can also have ***mixed partial derivatives***, by first differentiating with respect to one variable, and then another, and then another, and so on.

We define the ***$n_{k}$-th partial derivative*** with respect to $x_{i_{k}}$, of the ***$n_{k-1}$-th partial derivative*** with respect to $x_{i_{k-1}}$, *and so on...*, of the the ***$n_{1}$-th partial derivative*** with respect to $x_{i_{1}}$, of $f$, as:  
$$
\huge
f^{(n_{1},\dots,n_{k-1},n_{k})}_{x_{i_{1}} \dots x_{i_{k-1}} x_{i_{k}}} = \bigg( f^{(n_{1},\dots,n_{k-1})}_{x_{i_{1}} \dots x_{i_{k-1}}} \bigg)^{(n_{k})}_{x_{i_{k}}}
$$
It is also often denoted as:
$$
\huge
\dfrac{\partial^{n_{k} + n_{k-1} + \dots + n_{1}} f}{\partial x_{i_{k}}^{n_{k}}\partial x_{i_{k-1}}^{n_{k-1}}\dots\partial x_{i_{1}}^{n_{1}}} \ \ \ \ \text{or} \ \ \ \ 
\dfrac{\partial^{n_{k} + n_{k-1} + \dots + n_{1}} }{\partial x_{i_{k}}^{n_{k}}\partial x_{i_{k-1}}^{n_{k-1}}\dots\partial x_{i_{1}}^{n_{1}}}f
$$
So for example, $f^{(1,2,3)}_{xyz}(a) = \dfrac{\partial^6f}{\partial z^3 \partial y^2 \partial x}= ( ( f'_{x} )''_{y} )'''_{z}(a)$

### Schwarz's Theorem
In general, ***mixed partial derivatives*** can't commute, i.e. $\dfrac{\partial^{2} f}{\partial x \partial y} \neq \dfrac{\partial^{2} f}{\partial y \partial x}$. Yet, it would be really useful if they could.

Recall that $f: U \to \mathbb{R}$ where $U \subseteq \mathbb{R}^n$ is an [[Open Set|open set]]. Let $V_{\pmb a}$ be some [[Neighbourhood#Neighbourhood of a Point|neighbourhood]] of $\pmb a$, such that $V_{\pmb a} \subseteq U$. For any $i,j \in \{ 1,2,\dots,n \}$, if $\dfrac{\partial^2 f}{\partial x_{i} \partial x_{j}}$ and $\dfrac{\partial f^2}{\partial x_{j} \partial x_{i}}$ exist for all points in $V_{\pmb a}$, and are both [[Continuity|continuous]] at $\pmb a$, then these ***mixed partial derivatives*** can commute at $\pmb a$, i.e. $\dfrac{\partial^{2} f}{\partial x_{i} \partial x_{j}}(\pmb a) = \dfrac{\partial^{2} f}{\partial x_{j} \partial x_{i}}(\pmb a)$.

# Examples
Here are  a few simple examples, with [[Gradient|gradient]]:
$$
\begin{align}
&\text{For} \ f(x,y) = x^2 + y^2, \ \text{we have} \
&&\dfrac{\partial f}{\partial x} = 2x \
&&\text{and}&& \ \dfrac{\partial f}{\partial y} = 2y, &&\text{hence}&& \nabla f = (2x,2y) \\
&\text{For} \ f(x,y) = x^3y^2, \ \text{we have} \
&&\dfrac{\partial f}{\partial x} = 3x^2y^2 \
&&\text{and}&& \ \dfrac{\partial f}{\partial y} = 2x^3y^2, &&\text{hence}&& \nabla f = (3x^2y^2,2x^3y^2) 
\end{align}
$$
