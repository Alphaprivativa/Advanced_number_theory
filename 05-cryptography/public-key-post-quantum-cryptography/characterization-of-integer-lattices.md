---
aliases:
- Characterization of rank of an integer lattice
- Characterization of the coorder of an integer lattice
- triangular basis
- triangular basis of a submodule of a free abelian group
- submodules of a free abelian group are free
- echelon basis of a submodule
- Free modules over PID split
---

# Characterization of integer lattices

> Let
> - $M := \left\langle g_1,\ldots, g_m \right\rangle_{\mathbb Z}\cong \mathbb Z^m$ a ==free== $\mathbb Z$-module of rank $m$
> - $\Lambda\le M$ a [[Integer Lattices|Lattice]] in $M$, or a  $\mathbb Z$-submodule of $M$
>
> Then
> 1. $\Lambda$ is a ==Free== $\mathbb Z$-module and admits a ==triangular== basis: there are pivots $1\le j_1<j_2<\ldots<j_h\le m$ such that
>    $$\eta_i:= \sum\limits_{j=j_i}^m c_{i,j} g_j\quad \quad \text{ with } c_{i,j_i}\ne 0\quad \forall\, i=1,\ldots,h$$
>    So $\Lambda = \left\langle \eta_1,\ldots,\eta_h \right\rangle\cong \mathbb Z^h$
> 2. Any basis for the lattice $\Lambda$ has the same length and said length is $\le m$
> 3. $\Lambda$ can be seen as the image of $N$ the matrix having $\eta_i$ as columns, we will write
>    $$\Lambda = \mathscr L(N)$$
> 4. $N=ADB$ with $A\in\operatorname{GL}_m(\mathbb Z)$, $B\in\operatorname{GL}_h(\mathbb Z)$ and $D\in M_{m,h}(\mathbb Z)$ in [[Smith normal form]], whose nonzero diagonal entries satisfy $0<d_1\mid\cdots\mid d_h$. Then
>    $$\mathbb Z^m/\Lambda \cong \left(\bigoplus\limits_{i=1}^h \mathbb Z_{d_i}\right)\oplus \mathbb Z^{m-h}\quad \text{where } d_i\text{ diagonal elements of }D$$
>    so the co-order of $\Lambda$ is finite if and only if $h=m$, and in that case
>    $$|\mathbb Z^m/\Lambda|= \prod\limits_{i=1}^m|d_i| =|\det N|$$
> 5. For ==any== $h$ the matrix $N^TN \in M_h(\mathbb Z)$ is non singular and the ==determinant== of the lattice
>    $$\det \Lambda := \sqrt{\det\left(N^TN\right)}$$
>    does not depend on the basis chosen. For $h=m$ it is $|\det N|$, so it extends the co-order formula of $(4)$ to lattices which are not of full rank
>    
> > [!dim]- #### Proof
> > 
> > - $(1):$ We make an induction on $m$, the case $\Lambda =0$ being trivial with $h=0$ and no pivot:
> >   - $m=1:$ Then we are in $\mathbb Z$ we know it is a [[Dominio a ideali principali|PID]], then any submodule has one generator. Then
> >     $$\Lambda = \langle \eta_1\rangle$$
> >     clearly $\eta_1 = c_{1,1}g_1$ with nonzero $c_{1,1}\in \mathbb Z$, and $j_1=1$
> >   - $m>1:$ let $s= \sum\limits_{j} c_j g_j$ be a generic element of $\Lambda$ and let
> >     $$G_1:= \left\langle g_2,\ldots,g_m \right\rangle_{\mathbb Z}\cong \mathbb Z^{m-1}$$
> >     then
> >     - if there is no $s$ such that $c_1 \ne 0$ then $\Lambda \le G_1$ and by induction we find a triangular basis for $\Lambda$, with all its pivots $\ge 2$
> >     - if there is $s$ such that $c_1\ne 0$ then the $c_1>0$ appearing in $\Lambda$ form a non empty set of positive integers, so by well ordering we may let $\eta_1= \sum\limits_j c_{1,j}g_j$ be an element of $\Lambda$ with minimal positive $c_{1,1}$, and $j_1=1$. Then $c_{11}$ divides the $c_1$ of any $s$: dividing in $\mathbb Z$, which is an [[Dominio Euclideo|ED]],
> >       $$c_1 = qc_{11}+r\quad \quad 0\le r<c_{11}$$
> >       the element $s-q\eta_1 \in \Lambda$ has $r$ as coefficient of $g_1$, so $r=0$ by minimality of $c_{11}$. Hence
> >       $$s-q\eta_1 \in G_1\cap \Lambda\Longrightarrow \Lambda = \mathbb Z\eta_1 + \left(G_1\cap \Lambda\right)$$
> >       Now we consider $G_1$ as above, so by induction
> >       $$\Lambda \cap G_1= \left\langle \eta_2,\ldots,\eta_h \right\rangle$$
> >       with pivots $1<j_2<\ldots<j_h$, and the $\eta_i$ generate the lattice $\Lambda$. Morever they are independent since, reading the coefficient of $g_1$ in
> >       $$\sum\limits_i \lambda_i \eta_i=0$$
> >       and using that $\eta_2,\ldots,\eta_h \in G_1$ have no $g_1$ component, we get $\lambda_1c_{11}=0$, hence $\lambda_1=0$ because $c_{11}\ne 0$. Then $\sum\limits_{i>1}\lambda_i\eta_i=0$ and by induction $\{\eta_i\}_{i>1}$ are independent so
> >       $$\lambda_i=0 \quad \forall\, i =1,\ldots,h$$
> > - $(2):$ The construction of $(1)$ gives one $\eta_i$ for each pivot $j_i \in\{1,\ldots,m\}$, so $h \le m$. If $N,N'$ are the matrices of two basis, of lengths $h,h'$, then every column of $N'$ lies in $\Lambda$ and conversely, so via change of basis
> >   $$N A=N'\quad \quad N' B=N \quad \quad A \in M_{h,h'}(\mathbb Z),\ B\in M_{h',h}(\mathbb Z)$$
> >   This means $N AB= N$ but $N$ has trivial kernel, its columns being independent, so $AB-I_h=0$. Via the same reasoning $BA-I_{h'}=0$. Then
> >   $$h=\operatorname{rk}(AB)\le \min(h,h')\quad \quad h'=\operatorname{rk}(BA)\le \min(h,h')$$
> >   hence the two basis have same number of elements, and $A \in \operatorname{GL}_h(\mathbb Z)$.
> > - $(3):$ consider $N$ the matrix having the $\eta_i$ of $(1)$ as columns, then it is the wanted matrix
> > - $(4):$ Apply [[Smith normal form]] to $N$: if $UNV=D$, set $A=U^{-1}$ and $B=V^{-1}$, giving $N=ADB$. Since $B$ is $\mathbb Z$-invertible $B\mathbb Z^h=\mathbb Z^h$, and $A^{-1}$ is an automorphism of $\mathbb Z^m$, so
> >   $$\Lambda = N\mathbb Z^h=ADB\mathbb Z^h = AD\mathbb Z^h \Longrightarrow \mathbb Z^m/\Lambda \cong A^{-1}\mathbb Z^m/D\mathbb Z^h= \mathbb Z^m/D\mathbb Z^h$$
> >   Now $D\mathbb Z^h = d_1\mathbb Z \oplus \ldots \oplus d_h \mathbb Z\oplus 0$, so the quotient splits coordinatewise
> >   $$\mathbb Z^m/D\mathbb Z ^h\cong \left(\bigoplus\limits_{i=1}^h \mathbb Z_{d_i}\right)\oplus\mathbb Z^{m-h}$$
> >   The $d_i$ are non zero, $N$ having rank $h$, so this is finite exactly when the free part $\mathbb Z^{m-h}$ vanishes, i.e. when $h=m$. Then $D$ is square and
> >   $$|\mathbb Z^m/\Lambda|=\prod\limits_{i=1}^m |d_i|=|\det D|=|\det N|$$
> >   the last equality because $|\det A|=|\det B|=1$
> > - $(5):$ $N^TN$ is the Gram matrix of the $\eta_i$, and it is non singular: if $N^TN\mathbf x=0$ then
> >   $$\|N\mathbf x\|^2=\mathbf x^TN^TN\mathbf x=0 \Longrightarrow N \mathbf x =0\Longrightarrow \mathbf x =0$$
> >   the columns of $N$ being independent. In particular $\det(N^TN)>0$ and the square root is defined. By $(2)$ any other basis is $N'=NA$ with $A \in \operatorname{GL}_h(\mathbb Z)$, so
> >   $$\det\left(N'^TN'\right)=\det\left(A^TN^TNA\right)=(\det A)^2\det\left(N^TN\right)=\det\left(N^TN\right)$$
> >   Finally for $h=m$ the matrix $N$ is square and $\det(N^TN)=(\det N)^2$, so $\det \Lambda = |\det N|$
> 
> > [!dim]- #### Alternative proof (of induction step)
> > Induction over $m$
> > - for $m=1:$ we have $M =\left\langle g_1 \right\rangle_{\mathbb Z}\cong \mathbb Z$ then any $\mathbb Z$-module in $M$ is an ideal, since $\mathbb Z$ is a [[Dominio a ideali principali|PID]] this means it is principal, so $\Lambda = \left\langle \eta_1 \right\rangle$
> > - for $m>1:$ Consider $\widetilde M:=\left\langle g_2,\ldots,g_m \right\rangle_{\mathbb Z}$ then we consider the [[Short exact sequence]]
> >   
> >   ![[QuiverSVG 20260909141216.svg|invertb|1000]]
> >   
> >   Then 
> >   - $(\Lambda+\widetilde M)/\widetilde M\subseteq M/\widetilde M = \left\langle [g_1] \right\rangle\cong \mathbb Z$ hence this is an ideal of $M/\widetilde M$ hence generated by one element $[\eta_1]$ with $\eta_1 \in \Lambda$ with $\eta_1=\sum\limits_{i}c_{1,i}g_i$ with $c_{1,1}\ne 0.$
> >   - By induction $\Lambda \cap \widetilde M$ admits a basis $\eta_2,\ldots,\eta_k$
> > 
> >   We claim $\eta_1,\ldots,\eta_k$ form a basis.
> >   - They generate since $a[\eta_1]=a\eta_1+ \Lambda \cap \widetilde M$ and all elements of $\Lambda$ are multiples of this class by the projection $\pi$.
> >   - They are independent since 
> >     $$0 = \sum\limits_{j} c_j \eta_j \Longrightarrow 0=\pi\left(\sum\limits_j c_j \eta_j\right)=c_1[\eta_1]$$
> >     Now $(\Lambda + \widetilde M)/\widetilde M\subseteq \mathbb Z$, so there is no torsion element, hence $c_1=0$. Then
> >     $$\sum\limits_{j>1}c_j\eta_j=0 \underset{\begin{matrix}\text{induction}\end{matrix}}{\Longrightarrow}c_j=0 \quad \forall\,j >1$$
> 
> > [!important]
> > The alternative proof shows how the short exact sequence
> > ![[QuiverSVG 20260909141216.svg|invertb|1000]]
> > Splits trough an homomorphism $s:(\Lambda+\widetilde M)/\widetilde M \longrightarrow \Lambda$ sending $[\eta_1] \longmapsto \eta_1$. This induces the splitting of the module
> > $$\Lambda = (\Lambda \cap \widetilde M) \oplus \mathbb Z\eta_1$$

## Other properties

- [[Hermite normal form]] - normalization of a triangular basis in fixed ambient coordinates
- [[Smith and Hermite normal forms]] - the two integral reduction algorithms and their divisibility properties
