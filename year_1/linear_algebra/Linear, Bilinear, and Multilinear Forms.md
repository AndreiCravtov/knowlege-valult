#linear-algebra 

A ***multilinear form*** on [[Vector Space|vector space]] $V$ over [[Field|field]] $F$, is a [[Bilinear and Multilinear Maps|multilinear map]] $f: V^k \to F$, also called a ***$k$-linear form***. For the case $k=1$ we retrieve the [[#Linear Form|linear form]], or ***linear functional***, on $V$. For the case $k=2$ we retrieve the [[#Bilinear Form|bilinear form]] on $V$.

# Special Types of Multilinear Maps
## Linear Form
A ***linear form*** (or ***linear functional***) is a [[Linear Map|linear map]] from a [[Vector Space|vector space]] to its [[Field|field]] of scalars. For some <u>vector space</u> $V$ and <u>field</u> $F$, the [[Function Space#Space of Linear Transformations $ mathcal{L}(V,W)$,$ mathrm{Hom}(V,W)$|space of linear transformations]] $\mathrm{Hom}(V,F)$ containing every ***linear form*** on $V$, is called the [[Dual Space (algebraic)|dual space]] of $V$ and is denoted by $V^*$.

## Bilinear Form - Symmetric, Skew-Symmetric, Alternating, Reflexive
A ***bilinear form*** is a [[Bilinear and Multilinear Maps|bilinear map]] $B:V \times V \to F$ for some [[Vector Space|vector space]] $V$ over field $F$. 

We define a ***bilinear form*** $B$ to be
- ***Symmetric:*** if $B(\mathbf{v}, \mathbf{w}) = B(\mathbf{w}, \mathbf{v})$ for all $\mathbf{v},\mathbf{w} \in V$
- ***Altering:*** if $B(\mathbf{v}, \mathbf{v}) = \mathbf{0}_{V}$ for all $\mathbf{v} \in V$
- ***Skew-symmetric/antisymmetric:*** if $B(\mathbf{v}, \mathbf{w}) = -B(\mathbf{w}, \mathbf{v})$ for all $\mathbf{v},\mathbf{w} \in V$. Every ***alternating form*** is ***skew-symmetric***.
- ***Reflexive:*** if $B(\mathbf{v}, \mathbf{w}) = 0 \implies B(\mathbf{v}, \mathbf{w}) = 0$ for all $\mathbf{v},\mathbf{w} \in V$. Every ***bilinear form*** is ***reflexive*** *if and only if* it is ***symmetric*** or ***altering***

### Maps to Dual Space
#todo Every bilinear form _B_ on V defines a pair of linear maps from V to its [dual space](https://en.wikipedia.org/wiki/Dual_space "Dual space") _V_∗. Define _B_1, _B_2: _V_ → _V_∗ by....
https://en.wikipedia.org/wiki/Bilinear_form#Maps_to_the_dual_space

### Degenerate Bilinear Form
#todo In [mathematics](https://en.wikipedia.org/wiki/Mathematics "Mathematics"), specifically [linear algebra](https://en.wikipedia.org/wiki/Linear_algebra "Linear algebra"), a **degenerate bilinear form** _f_ (_x_, _y_ ) on a [vector space](https://en.wikipedia.org/wiki/Vector_space "Vector space") _V_ is a [bilinear form](https://en.wikipedia.org/wiki/Bilinear_form "Bilinear form") such that the map from _V_ to _V_∗ (the [dual space](https://en.wikipedia.org/wiki/Dual_space "Dual space") of _V_ ) given by _v_ ↦ (_x_ ↦ _f_ (_x_, _v_ )) is not an [isomorphism](https://en.wikipedia.org/wiki/Isomorphism "Isomorphism"). An equivalent definition when _V_ is [finite-dimensional](https://en.wikipedia.org/wiki/Dimension_(vector_space) "Dimension (vector space)") is that it has a non-trivial kernel: there exist some non-zero _x_ in _V_ such that

𝑓(𝑥,𝑦)=0![{\displaystyle f(x,y)=0\,}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c2ce3a0f39594f0057b4ce0d1a007509281fd6ac) for all 𝑦∈𝑉.![{\displaystyle \,y\in V.}](https://wikimedia.org/api/rest_v1/media/math/render/svg/3264f032336179ae6f829b7168b2ce0fec5e7085)
https://en.wikipedia.org/wiki/Degenerate_bilinear_form

# (covariant) $k$-tensor
#todo
A multilinear 𝑘![{\displaystyle k}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c3c9a2c7b599b37105512c5d570edc034056dd40)-form on 𝑉![{\displaystyle V}](https://wikimedia.org/api/rest_v1/media/math/render/svg/af0f6064540e84211d0ffe4dac72098adfa52845) over 𝑅![{\displaystyle \mathbb {R} }](https://wikimedia.org/api/rest_v1/media/math/render/svg/786849c765da7a84dbc3cce43e96aad58a5868dc) is called a (**covariant**) **𝑘![{\displaystyle {\boldsymbol {k}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c5007edd8c173fdfa24afccd09ea3ba5fb2a12a9)-tensor**, and the vector space of such forms is usually denoted 𝑇𝑘(𝑉)![{\displaystyle {\mathcal {T}}^{k}(V)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ec72f2cebf6fac3e0dc913989b7fd7e7f31b6577) or 𝐿𝑘(𝑉)![{\displaystyle {\mathcal {L}}^{k}(V)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/cb370ceb715716e50e43f866068cd08a0694b40e).[[2]](https://en.wikipedia.org/wiki/Multilinear_form#cite_note-2)
[[Function Space#Vector Space of (covariant) $k$-Tensors $ mathcal{T} k(V)$, $ mathcal{L} k(V)$]]

Given a 𝑘![{\displaystyle k}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c3c9a2c7b599b37105512c5d570edc034056dd40)-tensor 𝑓∈𝑇𝑘(𝑉)![{\displaystyle f\in {\mathcal {T}}^{k}(V)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/3935764ae3f56a9256ae48392eed298a1855b1fa) and an ℓ![{\displaystyle \ell }](https://wikimedia.org/api/rest_v1/media/math/render/svg/f066e981e530bacc07efc6a10fa82deee985929e)-tensor 𝑔∈𝑇ℓ(𝑉)![{\displaystyle g\in {\mathcal {T}}^{\ell }(V)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/50617dd8f6de3b52e154153198ee1b173c6bd7b1), a product 𝑓⊗𝑔∈𝑇𝑘+ℓ(𝑉)![{\displaystyle f\otimes g\in {\mathcal {T}}^{k+\ell }(V)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/f932f78797ace79346dd191f0f5168a79d095e5a), known as the **tensor product**, can be defined by the property

(𝑓⊗𝑔)(𝑣1,…,𝑣𝑘,𝑣𝑘+1,…,𝑣𝑘+ℓ)=𝑓(𝑣1,…,𝑣𝑘)𝑔(𝑣𝑘+1,…,𝑣𝑘+ℓ),![{\displaystyle (f\otimes g)(v_{1},\ldots ,v_{k},v_{k+1},\ldots ,v_{k+\ell })=f(v_{1},\ldots ,v_{k})g(v_{k+1},\ldots ,v_{k+\ell }),}](https://wikimedia.org/api/rest_v1/media/math/render/svg/5a5af983e87ec319e6547f189898b3b17e0afb89)

for all 𝑣1,…,𝑣𝑘+ℓ∈𝑉![{\displaystyle v_{1},\ldots ,v_{k+\ell }\in V}](https://wikimedia.org/api/rest_v1/media/math/render/svg/04723de1f0e19f20df14cb53ffae1b46921928d5). The [tensor product](https://en.wikipedia.org/wiki/Tensor_product "Tensor product") of multilinear forms is not commutative; however it is bilinear and associative:

𝑓⊗(𝑎𝑔1+𝑏𝑔2)=𝑎(𝑓⊗𝑔1)+𝑏(𝑓⊗𝑔2)![{\displaystyle f\otimes (ag_{1}+bg_{2})=a(f\otimes g_{1})+b(f\otimes g_{2})}](https://wikimedia.org/api/rest_v1/media/math/render/svg/61fb7a8afda6b5de6f680886fd73c3d508235889), (𝑎𝑓1+𝑏𝑓2)⊗𝑔=𝑎(𝑓1⊗𝑔)+𝑏(𝑓2⊗𝑔),![{\displaystyle (af_{1}+bf_{2})\otimes g=a(f_{1}\otimes g)+b(f_{2}\otimes g),}](https://wikimedia.org/api/rest_v1/media/math/render/svg/eb8609e289888cb5fcea61f1416ca97f3d41f933)

and

(𝑓⊗𝑔)⊗ℎ=𝑓⊗(𝑔⊗ℎ).![{\displaystyle (f\otimes g)\otimes h=f\otimes (g\otimes h).}](https://wikimedia.org/api/rest_v1/media/math/render/svg/b1497a139f6c68b97c1beede2ad32b10d0f20c92)

If (𝑣1,…,𝑣𝑛)![{\displaystyle (v_{1},\ldots ,v_{n})}](https://wikimedia.org/api/rest_v1/media/math/render/svg/8ab0b34f196f25857f60aa90852f6ebba17a21ba) forms a basis for an 𝑛![{\displaystyle n}](https://wikimedia.org/api/rest_v1/media/math/render/svg/a601995d55609f2d9f5e233e36fbe9ea26011b3b)-dimensional vector space 𝑉![{\displaystyle V}](https://wikimedia.org/api/rest_v1/media/math/render/svg/af0f6064540e84211d0ffe4dac72098adfa52845) and (𝜙1,…,𝜙𝑛)![{\displaystyle (\phi ^{1},\ldots ,\phi ^{n})}](https://wikimedia.org/api/rest_v1/media/math/render/svg/740f9ad9a09d6975fb174a6288fe6368a5517c60) is the corresponding [dual basis](https://en.wikipedia.org/wiki/Dual_basis "Dual basis") for the [dual space](https://en.wikipedia.org/wiki/Dual_space "Dual space") 𝑉∗=𝑇1(𝑉)![{\displaystyle V^{*}={\mathcal {T}}^{1}(V)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/a5ddf3b5f541e084637132161d131ea202b62574), then the products 𝜙𝑖1⊗⋯⊗𝜙𝑖𝑘![{\displaystyle \phi ^{i_{1}}\otimes \cdots \otimes \phi ^{i_{k}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/85e6e707f9494760ff30ad7ec0b94949f2c4fb36), with 1≤𝑖1,…,𝑖𝑘≤𝑛![{\displaystyle 1\leq i_{1},\ldots ,i_{k}\leq n}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c38ecfde9e53e26e12f50f9df992a47bf89ca504) form a basis for 𝑇𝑘(𝑉)![{\displaystyle {\mathcal {T}}^{k}(V)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ec72f2cebf6fac3e0dc913989b7fd7e7f31b6577). Consequently, 𝑇𝑘(𝑉)![{\displaystyle {\mathcal {T}}^{k}(V)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ec72f2cebf6fac3e0dc913989b7fd7e7f31b6577) has dimension 𝑛𝑘![{\displaystyle n^{k}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/53af70c07e0932d85d2fdb70c56360544c3a0b5a).