
The aim of this note is to try and make a list of all possible prove that $an+b$ has infinitely many primes type of question. This is an open note in the sense it is never complete 

> [!theorem] Infinite Primes 
> There are infinite Primes of the form $2k+1$ equivalently there are infinity many primes

`\begin{proof}`
We can see this is a direct result of [[Fundamental Theorem of Arithmetic]].
Let us assume there are finitely many primes with the larges prime being $p_{k}$ where $p_{i}$ represents $i^{th}$ prime.
Lets define $N$ such that
$$
N=p_{1}p_{2}p_{3}\dots p_{k}+1
$$
> [!claim|1.1] 
> Let $q$ be the smallest divisor of $N \implies q|N$ and $q$ is a prime

Lets prove this my contradiction if $q$ is not a primes $\exists \ 1< a,b<q\in \mathbb{N}$ such that $a\cdot b=q \implies a|q$ this contradicts the fact that $q$ is smallest hence $q$ is a prime.
$q\neq p_{i} \ \forall \ 1\leq i\leq k$ as none of $p_{i}|N$ 
We assumed there are finitely many primes but now found a new prime which is not equal to any of the other prime this shows that our assumption is false and there infinitely many prime.

Note: Even though we said its a direct consequence of [[Fundamental Theorem of Arithmetic]] we haven't used it in our theorem but can be used to make a simpler Proof

`\end{proof}`


> [!theorem] Infinite primes of form $3k+1$
> There are infinitely many primes of form $3k+1$
> 

`\begin{proof}`
[Stack exchange proof](https://math.stackexchange.com/a/4663883/1299918) 

Let $p_{i}$ be primes of the form $3k+1$.
We prove that there are infinitely primes of form $3k+1$ by of contradiction by assuming that there are finitely many primes of form $3k+1$
Let $N=(2p_{1}p_{2}p_{3}\dots p_{n})^{2}+3$.
Let $q$ be a prime and $q|N\implies q\neq \ p_{i} \forall \ i$.
$$
\begin{align}
N & \equiv0\pmod{q}\\
(2p_{1}p_{2}p_{3}\dots p_{n})^{2}+3& \equiv0\pmod{q}\\
(2p_{1}p_{2}p_{3}\dots p_{n})^{2}& \equiv-3\pmod{q}\\
\end{align}
$$
this shows $\left( \frac{-3}{q} \right)=1$
Case I: $q\equiv{1}\pmod{4}$
$$
\begin{align}
\left( \frac{-3}{q} \right) & =1 \\
\left( \frac{-1}{q} \right)\left( \frac{3}{q} \right) & =1 \\
\left( \frac{3}{q} \right) & =1 \ \ \ \ \text{as } q\equiv{1}\pmod{4}\\
\left( \frac{q}{3} \right) & =1 \ \ \ \ \text{as } q\equiv{1}\pmod{4}\\
\implies q & \equiv1,0 \pmod{3} 
\end{align}
$$

Case II: $q\equiv3\pmod{4}$

$$
\begin{align}
\left( \frac{-3}{q} \right) & =1 \\
\left( \frac{-1}{q} \right)\left( \frac{3}{q} \right) & =1 \\
-\left( \frac{3}{q} \right) & =1 \ \ \ \ \text{as } q\equiv{3}\pmod{4}\\
-1\cdot-1\cdot\left( \frac{q}{3} \right) & =1 \ \ \ \ \text{as } q\equiv{3}\pmod{4}\\
\left( \frac{q}{3} \right) & =1 \\
\implies q & \equiv1,0 \pmod{3} 
\end{align}
$$
This shows that q should be congruent to $1,0 \pmod{3}$ in both cases  
If $q|3\implies q=3\implies{3}|N$ as $q$ is prime but 
$$
\begin{align}
	N & \equiv (2p_{1}p_{2}p_{3}p_{4}\dots p_{n})^{2} +3 \pmod{3}\\
	N & \equiv (2\cdot1\cdot1\cdot1\cdot1\dots 1)^{2} +3 \pmod{3}\\
	N & \equiv (2)^{2} +3 \pmod{3}\\
	N & \equiv 1 \pmod{3}\\
\end{align}
$$
This contradicts the fact $3|N$ there for $q\equiv 1\pmod{3}$.
This contradicts the fact that there are finitely many primes of the form $3k+1$ 

$\therefore$ There are infinitely many primes of the form $3k+1$


`\end{proof}`

> [!theorem] Infinite primes of form $3k-1$
> There are infinitely many primes of form $3k-1$

`\begin{proof}`
We prove this by contradiction lets assume there are finitely many primes of the form $3k-1$ 
let $p_{i}$ be $i^{th}$ prime of the form $3k-1$ 
Let 
$$
N=3p_{1}p_{2}p_{3}\dots p_{n}-1
$$
using [[Fundamental Theorem of Arithmetic]] we can write $N$ as
$$
N=q_{1}^{e_{1}}q_{2}^{e_{2}}\dots q_{r}^{e_{r}}
$$
where $q_{j}$ are prime divisors of $N$.
Note: $q_{j}\neq p_{i}\ \  \forall \ \ i,j$
All of $q_{j}$ can't be of the form $3k+1$ as then the product $N$ will also be of the form $3k+1$ so at least one of $q_{j}$ be of the form $3k-1$ but that contradict the fact that $p_{i}$ are the only primes of form $3k-1$.
$\therefore$ There are infinitely many primes of the form $3k-1$ 


`\end{proof}`

> [!theorem] Infinite primes of form $4k-1$
> There are infinitely many primes of form $4k-1$

`\begin{proof}`
We prove this by contradiction lets assume there are finitely many primes of the form $4k-1$ 
let $p_{i}$ be $i^{th}$ prime of the form $4k-1$ 
Let 
$$
N=4p_{1}p_{2}p_{3}\dots p_{n}-1
$$
using [[Fundamental Theorem of Arithmetic]] we can write $N$ as
$$
N=q_{1}^{e_{1}}q_{2}^{e_{2}}\dots q_{r}^{e_{r}}
$$
where $q_{j}$ are prime divisors of $N$.
Note: $q_{j}\neq p_{i}\ \  \forall \ \ i,j$ 
All of $q_{j}$ can't be of the form $4k+1$ as then the product $N$ will also be of the form $4k+1$, so at least one of $q_{j}$ must be of the form $4k-1$. But that contradict the fact that $p_{i}$ are the only primes of form $4k-1$.
$\therefore$ There are infinitely many primes of the form $4k-1$ 
`\end{proof}`
> [!theorem] Infinite primes of form $4k+1$
> There are infinitely many primes of form $4k+1$

We prove this but contradiction, let assume that there are finitely many primes of the form $4k+1$.
Let $P$ be the highest prime of form $4k+1$ .
let
$$
N=(P!)^{2}+1
$$
Let $q$ be a prime such that $q|N \implies q \nmid (P!)^{2}$ then 
$$
\begin{align}
N & \equiv 0 \pmod{q} \\
(P!)^{2}+1& \equiv 0 \pmod{q} \\
(P!)^{2}& \equiv -1 \pmod{q} \\
\left[ \left( P! \right) ^{2} \right] ^{\frac{q-1}{2}} & \equiv \left( -1 \right) ^{\frac{q-1}{2}} \pmod{q} \\
\left( P! \right) ^{q-1} & \equiv -1^{\frac{q-1}{2}} \pmod{q}\\
\end{align}
$$
From [[Fermat's Little Theorem]]  
$$
\begin{align}
\left( P! \right) ^{q-1} & \equiv -1^{\frac{q-1}{2}} \pmod{q}\\
\implies1& \equiv -1^{\frac{q-1}{2}} \pmod{q}  \\
\implies \frac{q-1}{2} & \equiv0\pmod{2}\\
\implies {q-1} & \equiv0\pmod{4}\\
\implies {q} & \equiv1\pmod{4}\\
\end{align}
$$
Note: $q\neq p \ \forall \ p<P$ 
We have shown a new prime of form $4k+1$ which is greater than $P$ this contradicts the fact that there are finitely many primes. 
$\therefore$ We have shown that there are infinitely many primes of form $4k+1$