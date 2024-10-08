8. let $p>5$ be a prime what is the period of $\frac{1}{p}$?
> [!claim] 
> Period of $\frac{1}{p}$ is order of $10\mod{p}$ 

 `\begin{proof}`
 let $m$ be the order of $10 \mod{p}$ then $p|10^{m}-1$ 
 so 
 $$
\frac{10^{m}-1}{p}=r \ \ \text{where } r \in \mathbb{Z}^{+}
$$
Note that 
$$
\frac{10^{m}-1}{p}=r\leq(10^{m}-1)
$$
so r has at most $r$ has at most $m$ digits now,

$$
\begin{align} 
\frac{1}{p} & =\frac{1}{10^{m}-1}r\\
 & =\frac{1}{10^{m}}\left( \frac{1}{1-10^{-m}} \right) {r} \\
 & =\frac{1}{10^{m}}r \sum_{j=0}^{\infty}10^{-m}j \\
 & =\frac{r}{10^{m}}+\frac{r}{10^{2m}}\dots\ \\
 & =0.\overline{00\dots r }\ \overline{00\dots r } \ \overline{00\dots r }\dots
\end{align}
$$
we have added in $k$ zeros to pad for the m digits so we have $m=k+\text{digits of }r$
$\implies$ periodicity of $\frac{1}{p}$ is $m$ 
`\end{proof}`


2. last $2025$ digits of $3^{10^{2024}}$ ?

$$
\begin{align} 
3^{\varphi(2^{2025})} & \equiv1 \pmod{2^{2025}}\\
3^{2^{2024}} & \equiv{1}\pmod{2^{2025}} \\
3^{10^{2024}} & \equiv{1}\pmod{2^{2025}} 
\end{align}
$$


$$
\begin{align}
3^{\varphi(5^{2023})} & \equiv1\pmod{5^{2025}} \\
3^{4\cdot 5^{2024}} & \equiv 1 \pmod{5^{2025}} \\
3^{10^{2024}} & \equiv 1 \pmod{5^{2025}} \\
\implies3^{10^{2024}} & \equiv 1 \pmod{10^{2025}} \\
\end{align}

$$
#20-sep 