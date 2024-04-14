Sometimes we wish to define functions and prove they are [[Mathematical Functions#Properties of Functions|bijective/surjective/injective]] however, we cannot write down a formula for it. Luckily, we can sketch a diagram to represent the function, and this diagram will be accepted in #exam s as a valid proof.

# Examples
## Building $f: \mathbb{N} \to \mathbb{N}^2$ bijection
![[Pasted image 20231124181044.png]]The diagram above defines the function $f$ clearly, such that it is obvious that it is bijective, because all elements of the [[Mathematical Functions#Domains, co-domains, ranges|co-domain]] gets visited, and visited only once. The way to read this would be i.e. $f(0) = \langle 0,0 \rangle, f(1) = \langle 0,1 \rangle, f(2) = \langle 1,0 \rangle, \dots$ and so on.

## Building $f: [0,1] \to [0,1]^2$ surjection
We can take the real number line interval from 0 to 1, like this one
```desmos-graph
left=-0.1; right=1.1;
---

-1<= y <= 1 | 0<= x <=1 | red
(0,0) | blue
(1,0) | blue
```
Now we can think of it as a line, and therefore, we can contort it into a 2D unit-square as follows
![[Pasted image 20231124181652.png|400]]
The unit-square is a representation of $[0,1]^2$, with $\langle 0,0 \rangle, \langle 0,1 \rangle, \langle 1,0 \rangle, \langle 1,1 \rangle$ being mapped to the four corners of it. Then we take the same pattern and repeat it, but **more densely**.
![[Pasted image 20231124182119.png|400]]
And then even **more densely**.
![[Pasted image 20231124182157.png|400]]
It is clear that as we repeat this increase in density, the line that is being contorted gets closer and closer to filling out the unit square. So we say that if we take the **limit** of this densening process, we get a function from the line (i.e. $[0,1]$) to the unit-square (i.e. $[0,1]^2$) where every point on the square is visited. Thus we can say that the function defined by this process, is [[Mathematical Functions#Surjective Functions|surjective]]. 