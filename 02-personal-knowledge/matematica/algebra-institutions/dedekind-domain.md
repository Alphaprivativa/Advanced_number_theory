---
aliases:
- Dedekind domains
- Definition 4.1
---

# Dedekind domain

> Let
> - $A$ a [[Dominio di integrità|domain]]
>
> Then the following are equivalent, and $A$ is called a ==Dedekind domain== when one of them holds
> 1. $A$ is [[Anello Noetheriano|Noetherian]], every non-zero prime ideal is maximal, and $A$ is [[Integral element|integrally closed]]
> 2. $A$ is a [[Anello Noetheriano|Noetherian]] domain of [[Krull dimension]] $1$ and $A_{\mathfrak p}$ is a [[Regular local ring|regular local ring]] of dimension $1$, i.e. a ==discrete valuation ring==, for every non-zero prime $\mathfrak p \le A$
>
> > [!dim]- #### Proof
> > "Every non-zero prime is maximal" and $\dim A = 1$ are the same condition for a domain, and *local* and *dimension $1$* come for free in $A_{\mathfrak p}$ (see the remark below), so the two lists differ only in their last entry and the equivalence is exactly [[Integral closedness is equivalent to all localizations being DVRs]].
>
> > [!note]
> > $(1)$ is the classical formulation used in number theory, $(2)$ the local-algebra one.
>
> > [!important] Only *regular* is a hypothesis in $(2)$
> > Of the three words "regular local ring of dimension $1$", the other two are automatic and are stated only to name the situation.
> > - ==local== is free, for any commutative ring and any prime: in $A_{\mathfrak p}=S^{-1}A$ with $S = A\setminus\mathfrak p$, an element $a/s$ with $a \notin \mathfrak p$ has inverse $s/a$, so the non units are exactly the elements of $\mathfrak p A_{\mathfrak p}$. These form an ideal, which therefore contains every proper ideal and is the ==unique maximal ideal==. This is the whole point of localizing at $\mathfrak p$, and it says nothing about $A$ - $\mathbb Z$ is not local, every $\mathbb Z_{(p)}$ is.
> > - ==dimension $1$== is free given $\dim A = 1$: $\dim A_{\mathfrak p}= \operatorname{ht}\mathfrak p$, and in a domain $(0)$ is prime, so $0 \subsetneq \mathfrak p$ forces $\operatorname{ht}\mathfrak p \ge 1$, while $\dim A = 1$ caps it at $1$.
> > - ==regular== is the real requirement: for a Noetherian local domain of dimension $1$ it is equivalent to $\mathfrak p A_{\mathfrak p}$ being ==principal== and to $A_{\mathfrak p}$ being ==integrally closed==. So "Dedekind" $=$ "Noetherian, dimension $1$, integrally closed", and it is normality that is being asked for.
>
> > [!idea] What each axiom of $(1)$ pays for
> > - Noetherianity gives the "maximal counterexample" argument and finite generation of ideals ([[Ideals of a Noetherian ring contain a product of primes]]);
> > - "prime $\Rightarrow$ maximal" is what makes primes the atoms of the factorization;
> > - integral closedness is what forbids $II^{-1} = I$, via the [[Characterization of integral elements via finitely generated modules|determinant trick]].
>
> > [!warning]
> > - **Dropping regularity leaves a perfectly good Noetherian domain of dimension $1$.** For $A = \mathbb K[x,y]/(y^2-x^3)$ the localization at $\mathfrak m = (x,y)$ is local of dimension $1$ but ==not regular==, $\mathfrak m A_{\mathfrak m}$ needing two generators. The failure is visible as the cusp of the curve, and as the fact that $A$ is not integrally closed in its [[Campo delle frazioni|fraction field]], which contains $y/x$.
> > - **A Dedekind domain need not be a [[Dominio a fattorizzazione unica|UFD]] at the level of elements.** Unique factorization is recovered only after passing from elements to ideals ([[Unique factorization of ideals into prime over Dedekind Domains]]), and the failure is measured precisely by the [[Ideal group|ideal class group]], which is trivial exactly when $A$ is a [[Dominio a ideali principali|PID]].
>
> > [!example]
> > Every PID is Dedekind - in particular $\mathbb Z$ and $\mathbb K[x]$ - and so is the ring of integers $\mathcal O_K$ of a number field, being defined as an integral closure.

## Properties

![[Integral closedness is equivalent to all localizations being DVRs]]

![[Dedekind domains are the smooth affine curves]]

![[Invertibility of ideals in Dedekind domains]]

![[Unique factorization of ideals into prime over Dedekind Domains]]

![[Domains whose ideals factor into primes are Dedekind]]

![[Unique factorization of fractional ideals]]

## Other properties

- [[Ideal group]] - the ideal class group, the invariant measuring how far $A$ is from a [[Dominio a ideali principali|PID]]
- [[Steinitz classification over a Dedekind domain]]
