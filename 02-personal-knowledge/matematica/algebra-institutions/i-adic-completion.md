---
aliases:
- completion of a ring
- completion of a filtered group
- m-adic completion
- p-adic integers
---

# I-adic completion

> Let $R$ be an abelian group with a ==filtration==, i.e. a sequence of subgroups
> $$R = \mathfrak m_0 \supseteq \mathfrak m_1 \supseteq \mathfrak m_2 \supseteq \ldots \supseteq \mathfrak m_n \supseteq \ldots$$
>
> Then the ==completion== $\hat R$ of $R$ with respect to $\mathfrak m_0 \supseteq \mathfrak m_1 \supseteq \ldots$ is the [[Inverse limit]]
> $$\hat R = \varprojlim R/\mathfrak m_i = \Big\{ g=(g_1,g_2,\ldots) \in \prod_i R/\mathfrak m_i \ \Big|\ \forall j > i\ \ g_j \equiv g_i \ (\mathfrak m_i) \Big\}$$
> where the congruences are induced by the surjection $\varphi_{j,i}\colon R/\mathfrak m_j \to R/\mathfrak m_i$, i.e. we are asking $\varphi_{j,i}(g_j) = g_i$.
>
> > [!note]
> > If $R$ is a ring and the filtration is by ideals, $\hat R$ inherits a ring structure from the inverse limit.
>
> ### I-adic completion
> Let $R$ be a ring and $I$ an ideal. Taking the filtration $R = I^0 \supseteq I \supseteq I^2 \supseteq \ldots$ (i.e. $\mathfrak m_i = I^i$) gives the ==$I$-adic completion== of $R$, denoted $\hat R_I$.

## Examples

> [!example] Completion of a polynomial ring
> Let $R = S[x_1,\ldots,x_n]$ and $\mathfrak m = (x_1,\ldots,x_n)$. Then
> $$\hat R_{\mathfrak m} \cong S[[x_1,\ldots,x_n]]$$
> the ring of formal power series. Indeed an element of $\hat R_{\mathfrak m}$ is $(g_1,g_2,\ldots)$ with $g_1 \in R/\mathfrak m \cong S$, $g_2 = [a_0 + a_1 x] \pmod{\mathfrak m^2}$, and compatibility forces $g_1 = [a_0] \pmod{\mathfrak m}$, $g_3 = [a_0+a_1x+a_2x^2]\pmod{\mathfrak m^3}$, and so on, exactly the data of a formal power series, truncated at each degree.

> [!example] The $p$-adic integers
> Let $p \in \mathbb Z$ be prime and $I=(p)$. The $I$-adic completion of $\mathbb Z$ is the ring of ==$p$-adic integers== $\widehat{\mathbb Z}_{(p)}$. Its elements can be written as $a = ([a_0]_p,[a_0+a_1p]_{p^2},\ldots)$, or more compactly as formal series $a = a_0 + a_1 p + a_2 p^2 + \ldots$ with $0 \le a_i < p$; addition and multiplication proceed as for such series, except that ==carries== must be performed (unlike for genuine formal power series). For instance, in $\widehat{\mathbb Z}_{(2)}$ one has $1+2+4+8+\ldots = -1$, where $-1 = ([-1],[-1],[-1],\ldots)$.

## Other properties

- [[Field of p-adic numbers]]
- [[p-adic valuation]]
