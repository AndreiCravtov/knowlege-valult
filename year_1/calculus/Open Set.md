An ***open set*** is a generalisation of the idea of *open intervals*; the idea that the *points near* a point in an ***open set***, are themselves *also* in that ***open set***. For example, the set of points $x$ and $y$ for which $x^2 + y^2 < r^2$ is the red circle
![[Pasted image 20240314023341.png]]
This red circle is an ***open set***; any point we pick, all the points near it are also within the red circle.

# Formal Definition
A subset $U$ of a [[Metric Space|metric space]] $(X,d)$ is an ***open set*** if for every point $p \in U$, there exists $\varepsilon>0$ for which the [[Balls in Metric Spaces#Formal Definition|open ball]] $B(\varepsilon;p)$ contained by $U$. Equivalently, $U$ is an ***open set*** if for every point $p \in U$, there exists a [[Neighbourhood#Neighbourhood of a Point|neighbourhood]] $V_{p} \subseteq \mathcal{N_{p}}$ of $p$ contained by $U$. This means that no matter which point you pick in $U$, the points close to it are also in $U$.