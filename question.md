
$X_1 , X_2 , · · · X_n$ be mutually independent random variables, each having the uniform distribution on {1, 2, · · · , N }. Let $U_n$be the smallest of $X_1 , · · · X_n$ and $V_n$ be the largest. Find the distributions of $U_n$ and $V_n$ .

Let $A_{r}$ is the event that all of $X_{i}$'s will be less than or equal to  $r$  
$P(A_{r})=\left( \frac{r}{N} \right)^{n}$ and $P(U_{n}=r)=P(A_{r})-P(A_{r-1})=\left( \frac{r}{N} \right)^{r}-\left( \frac{r-1}{N} \right)^{n}$


let $A_{i}$ be the event that the $i^{th}$ pair is a couple and
$$
\begin{align}
I_{i} & =\begin{cases}
1\quad \text{if event } A_{i}  \\
0\quad \text{if not event} A_{i} 
\end{cases}  \\
X & =\sum_{i=1}^{10} I_{i}  \\
P(I_{i}=1 ) & =\frac{\binom{10 }{1}\binom{10}{1}}{\binom{20 }{2}}=\frac{10}{19} \\
\mathrm{E} \left[ X \right] & =\sum_{i=1}^{10} E[I_{i} ]    \\
& =\sum_{i=1}^{10} \frac{10}{19}  \\
& = \frac{10*10}{19}=\frac{100}{19}  \\
\end{align}
$$