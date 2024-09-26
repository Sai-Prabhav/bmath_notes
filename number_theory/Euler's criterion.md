>[!theorem] Euler's criterion
>let $p$ be and odd prime and $\gcd(a,p)=1$
>$$
a^{\frac{(p-1)}{2}}\equiv 
\begin{cases}
1 \ \pmod{p} \text{ if a was a quadratic residue}  \\
-1 \pmod{p} \text{ if a was quadratic non-residue}
\end{cases}$$
Euler's criterion can be concisely reformulated using the [Legendre symbol](https://en.wikipedia.org/wiki/Legendre_symbol "Legendre symbol")
$$
\left( \frac{a}{p} \right) =a^{\frac{(p-1)}{2}}
$$

`\begin{proof}`
$$
a^{p-1}\equiv1\pmod{p}
$$
from [[Fermat's Little Theorem]]
which can be written as
$$
\left(  a^{\frac{p-1}{2}} -1 \right)\left(  a^{\frac{p-1}{2}} +1 \right)\equiv0\pmod{p}
$$
Therefore either
$$
a^{\frac{p-1}{2}}\equiv{1} \pmod{p}
$$
or 
$$
a^{\frac{p-1}{2}}\equiv{-1} \pmod{p}
$$

Case one: ($a$ is a quadratic residue)
let $r$ we a primitive root of $p$ as $a$ is a quadratic residue
$a\equiv r^{2k} \pmod{p}$ for some $k\in \mathbb{N}$
$$
\begin{align}
a^{\frac{p-1}{2}} & \equiv{1} \pmod{p} \\
\left(  r^{2k}  \right)^{\frac{p-1}{2}} & \equiv{1} \pmod{p} \\
 r^{2k\cdot \frac{p-1}{2}} & \equiv{1} \pmod{p} \\
 r^{k\cdot {p-1}} & \equiv{1} \pmod{p} \\
 \left(  r^{{p-1}} \right) ^{k}& \equiv{1} \pmod{p} \\
 \left(  1\right) ^{k}& \equiv{1} \pmod{p} \\
\end{align}
$$
this proves that 
$$
a^{\frac{p-1}{2}}\equiv{1} \pmod{p}
$$

Case two: ($a$ is a quadratic non-residue)
$a\equiv r^{2k+1} \pmod{p}$ for some $k\in \mathbb{Z}$ as $a$ is a quadratic non-residue

lets assume

$$
a^ \left( { \frac{p-1}{2}+1} \right) \equiv{1} \pmod{p}
$$
$$
\begin{align}
a^{\frac{p-1}{2}+1} & \equiv{1} \pmod{p} \\
\left(  r^{2k}  \right)^{\frac{p-1}{2}} \cdot r^{\frac{p-1}{2}}& \equiv{1} \pmod{p} \\
 r^{2k\cdot \frac{p-1}{2}} \cdot r^{\frac{p-1}{2}} & \equiv{1} \pmod{p} \\
 r^{k\cdot {p-1}} \cdot r^{\frac{p-1}{2}} & \equiv{1} \pmod{p} \\
 \left(  r^{{p-1}} \right) ^{k} \cdot r^{\frac{p-1}{2}}& \equiv{1} \pmod{p} \\
 \left(  1\right) ^{k} \cdot r^{\frac{p-1}{2}}& \equiv{1} \pmod{p} \\
  r^{\frac{p-1}{2}}& \equiv{1} \pmod{p}
\end{align}
$$
Which contradicts $r$ is a primitive root of $p$ 
Therefore
$$
  r^{\frac{p-1}{2}} \equiv{-1} \pmod{p}
$$

`\end{proof}`
