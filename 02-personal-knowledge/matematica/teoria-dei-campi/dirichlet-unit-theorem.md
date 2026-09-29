---
aliases:
- Dirichlet's unit theorem
- Dirichlet theorem on units
- Unit theorem
- Teorema delle unità di Dirichlet
---

# Dirichlet unit theorem

> Let
> - $K$ a [[Number field]] with $r_1$ real embeddings and $r_2$ pairs of complex-conjugate embeddings
> - $\mathcal O_K$ its [[Number field|ring of integers]]
> - $\mu(K)$ the finite group of roots of unity contained in $K$
>
> Then
> $$\mathcal O_K^\times\cong\mu(K)\times\mathbb Z^{r_1+r_2-1}.$$
> Equivalently, there are multiplicatively independent units $\varepsilon_1,\ldots,\varepsilon_{r_1+r_2-1}$ such that every unit is uniquely of the form
> $$\zeta\varepsilon_1^{m_1}\cdots\varepsilon_{r_1+r_2-1}^{m_{r_1+r_2-1}},
> \qquad \zeta\in\mu(K),\quad m_i\in\mathbb Z.$$
>
> > [!dim]- #### Proof sketch
> > 1. By [[The ring of integers is the maximal order]], $\mathcal O_K$ is free of rank $n=r_1+2r_2$ over $\mathbb Z$. Its Minkowski embedding
> >    $$\Phi:K\hookrightarrow\mathbb R^{r_1}\times\mathbb C^{r_2}\cong\mathbb R^n$$
> >    therefore identifies $\mathcal O_K$ with a full [[Lattice]].
> > 2. Define the logarithmic homomorphism
> >    $$\lambda(\alpha)=\big(\log|\sigma_i(\alpha)|,\ 2\log|\tau_j(\alpha)|\big)_{i,j}
> >    \in\mathbb R^{r_1+r_2}.$$
> >    For a unit $u$, multiplicativity of the field norm and $N_{K/\mathbb Q}(u)=\pm1$ give
> >    $$\sum_k\lambda_k(u)=\log|N_{K/\mathbb Q}(u)|=0.$$
> >    Hence $\lambda(\mathcal O_K^\times)$ lies in the hyperplane
> >    $$H=\left\{x\in\mathbb R^{r_1+r_2}:\sum_kx_k=0\right\},
> >    \qquad \dim H=r_1+r_2-1.$$
> > 3. The kernel is $\mu(K)$. Indeed, $\lambda(u)=0$ means that every conjugate of $u$ has absolute value $1$; these units lie in a bounded region of the lattice $\Phi(\mathcal O_K)$, so there are finitely many of them. A finite subgroup of $K^\times$ consists of roots of unity.
> > 4. The image $\Lambda=\lambda(\mathcal O_K^\times)$ is discrete: a bounded set of logarithmic vectors bounds every conjugate of the corresponding units, and a bounded region meets $\Phi(\mathcal O_K)$ in finitely many points.
> > 5. **(Crux)** The image is cocompact in $H$. For $x\in H$, construct a symmetric convex body $B_x\subseteq K\otimes_{\mathbb Q}\mathbb R$ whose bounds in the Archimedean coordinates are proportional to $e^{x_i}$ at real places and $e^{x_j/2}$ at complex places. Its volume is independent of $x$ because $\sum x_i=0$. Taking that volume sufficiently large, [[Minkowski's Convex Body Theorem]] gives $0\ne\alpha_x\in\mathcal O_K\cap B_x$. The construction makes $\lambda(\alpha_x)-x$ uniformly bounded and $|N_{K/\mathbb Q}(\alpha_x)|$ uniformly bounded. There are only finitely many integral ideals of bounded [[Norm of an ideal|ideal norm]], so $(\alpha_x)$ belongs to a finite list $(\beta_1),\ldots,(\beta_s)$. Writing $\alpha_x=u\beta_j$ shows that every $x\in H$ is within a fixed distance of some $\lambda(u)$. Thus $H/\Lambda$ is compact.
> > 6. A discrete cocompact subgroup of the real vector space $H$ is a lattice of rank $\dim H$. Therefore
> >    $$\mathcal O_K^\times/\mu(K)\cong\Lambda\cong\mathbb Z^{r_1+r_2-1},$$
> >    and the quotient being free makes the exact sequence split.
>
> > [!important]
> > The rank comes from the product formula, which confines logarithms of units to the codimension-one hyperplane $H$; [[Minkowski's Convex Body Theorem]] is the input proving that the image fills $H$ up to bounded error rather than lying in a smaller subspace.

