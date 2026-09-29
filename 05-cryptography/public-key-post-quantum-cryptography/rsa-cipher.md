---
aliases:
- Textbook RSA
- RSA key generation
- Total-break RSA
- RSA-total-break
---

# RSA

> ### Textbook RSA scheme
> Let
> - $p,q$ be distinct odd primes, $N=pq$, and $\varphi(N)=(p-1)(q-1)$
> - $e$ be an integer with $1<e<\varphi(N)$ and $\gcd(e,\varphi(N))=1$
> - $d$ be the least positive inverse of $e$ modulo $\varphi(N)$
>
> Then the ==textbook RSA scheme== has public key $(N,e)$ and private exponent $d$. For a message $m\in\mathbb Z/N\mathbb Z$, encryption computes $c=m^e\bmod N$, and decryption computes $c^d\bmod N$.
>
> > [!dim]- #### Proof of correctness
> > Write $ed=1+k\varphi(N)$. Modulo either prime $\ell\in\{p,q\}$, if $m=0$ then $m^{ed}=m$; otherwise [[Piccolo Teorema di Fermat|Fermat's little theorem]] gives the same identity since $\ell-1$ divides $\varphi(N)$. The [[Teorema cinese del resto|Chinese remainder theorem]] gives $m^{ed}=m\bmod N$.

## Properties

![[Wiener attack on RSA]]

> ### RSA and factorization
> Let
> - $(N,e,d)$ be RSA parameters as above
> - $\text{RSA-total-Break-Adv}$ be the advantage of an adversary that, given $(N,e)$, recovers the private exponent $d$
> - $\text{Fact-Adv}$ be the advantage of an adversary that, given $N$, recovers a nontrivial factor
> - $\text{RSA-Adv}$ be the advantage of an adversary that, given $(N,e)$ and $c$, recovers $m$ with $c=m^e\bmod N$
>
> Then
> $$\text{RSA-total-Break-Adv}\le \text{Fact-Adv}\le \text{RSA-Adv}.$$
>
> > [!dim]- #### Proof
> > - factorization $\le$ RSA  since one can easly use a factorization attacker as subroutine to break RSA secrecy
> > - RSA-total-break $\le$ factorization: This uses a [[Rabin miller pimality test]] like argument: consider $k=ed-1$ then for any $x\longleftarrow \mathbb Z_{\varphi(N)}$ we have
> >   $$x^k=1$$
> >   So write $k=2^ru$ get the smallest $i$ such that $x^{2^iu}=1$ then $y:=x^{2^{i-1}u}=-1$ with small probability by [[Rabin miller pimality test]] so it is more probabile $y-1\ne 0\mod \varphi(N)$ but 
> >   $$(y-1)(y+1)=0\mod \varphi(N)$$
> >   so $\text{gcd}(y-1,N)$ is a factor
>
> > [!note] Reading of the chain
> > The left-hand inequality is an equivalence up to polynomial factors: factoring and total-breaking RSA are mutually reducible. The right-hand inequality is one-directional, it encodes $p,q \Longrightarrow d \Longrightarrow$ inversion, and its converse is not known in general.

## Other properties

- [[Square root extraction and integer factorization]]