---
aliases:
- smooth affine curve
- Dedekind domain, the geometric reading
- normalization resolves curve singularities
- normalization of a curve
---

# Dedekind domains are the smooth affine curves

> Let
> - $\mathbb K$ an ==algebraically closed== field
> - $A$ a finitely generated $\mathbb K$-algebra which is a [[Dominio di integrità|domain]] of [[Krull dimension]] $1$, i.e. the [[Characterization of coordinate rings for affine closed sets|coordinate ring]] of an irreducible affine curve $C$
>
> Then the maximal ideals of $A$ are the [[Points and maximal ideals in Zariski topology|points of the curve]] and $A_{\mathfrak m}=\mathcal O_{C,x}$ is the [[Local Ring Geometric|local ring at the point]], so
> $$A \text{ Dedekind} \iff \mathcal O_{C,x} \text{ regular } \forall x \in C \iff C \text{ smooth}$$
>
> > [!dim]- #### Proof
> > The axioms of a [[Dedekind domain]] are already hypotheses on $A$ except for regularity: Noetherianity is the [[Hilbert basis theorem]], and $\dim A = 1$ is "every non-zero prime is maximal" for a domain. What remains is [[Integral closedness is equivalent to all localizations being DVRs]], which turns integral closedness of $A$ into regularity of every $\mathcal O_{C,x}$.
>
> > [!note]
> > What makes the dictionary tight is ==dimension $1$==: normal implies regular in codimension $1$ always, and on a curve every point has codimension $\le 1$, so normal, regular and smooth collapse into one condition - see [[Fundamental theorem of local rings at non singular points]] for the direction giving $\mathcal O_{C,x}$ a [[Dominio a fattorizzazione unica|UFD]], hence integrally closed. In dimension $\ge 2$ they separate, $\mathbb K[x,y,z]/(xy-z^2)$ being normal but singular at the origin, which is why there is no "Dedekind" notion for surfaces.
>
> > [!warning]
> > - **The curve may be arithmetic.** $\mathbb Z$ and the rings of integers $\mathcal O_K$ are Dedekind and are not $\mathbb K$-algebras. The honest statement is "regular affine integral scheme of dimension $1$", and $\operatorname{Spec}\mathcal O_K$ is the curve.
> > - **Regular is not smooth over an imperfect field.** Smooth means regular after base change to $\bar{\mathbb K}$, so Dedekind always gives regular and gives smooth only for $\mathbb K$ perfect.
> > - **Only affine charts are covered.** A smooth projective curve has no coordinate ring, its global regular functions being just $\mathbb K$. Deleting a nonempty finite set of points gives a Dedekind ring, and different choices give different rings for the same curve - $\mathbb K[x]$ and $\mathbb K[x,x^{-1}]$ both come from $\mathbb P^1$.
>
> > [!example]
> > The cusp $A = \mathbb K[x,y]/(y^2-x^3)$ is the sharp instance of failure: a perfectly good Noetherian domain of dimension $1$ in which regularity breaks at the single point $\mathfrak m = (x,y)$, where $\mathfrak m A_{\mathfrak m}$ needs two generators. On the arithmetic side this is $A$ failing to be integrally closed in its [[Campo delle frazioni|fraction field]], which contains $y/x$.
>
> ### Normalization
> The [[Integral element|integral closure]] of a $1$-dimensional Noetherian domain is a [[Dedekind domain]], so ==normalization resolves curve singularities==.
>
> > [!example]
> > For the cusp above the integral closure is $\mathbb K[y/x]=\mathbb K[t]$ with $x = t^2$, $y = t^3$, i.e. the map $\mathbb A^1 \longrightarrow C$ that unpicks the singular point. The ring of integers $\mathcal O_K$ of a number field is Dedekind for exactly this reason, being defined as an integral closure.
