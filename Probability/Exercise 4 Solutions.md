> [!exercise|1] 
> Let $X$ be a uniform $\{1, 2, · · · , N \}$ random variable; that is $X$ takes any of the $N$ values with equal probability $\frac{1}{N}$ . Find $\mathrm{E} \left[ X \right]$ and $\mathrm{Var} \left[ X \right]$.
  
$$
\begin{align}
E\left[ X \right]  & = \sum_{i=1}^{N}iP(X=i)\\
E\left[ X \right]  & = \sum_{i=1}^{N} \frac{i}{N}\\
E\left[ X \right]  & = \frac{1}{N}\sum_{i=1}^{N} {i}\\
E\left[ X \right]  & = \frac{1}{N} \cdot \frac{N*(N+1)}{2}\\
E\left[ X \right]  & =\frac{(N+1)}{2}\\
\end{align}
$$
$$
\begin{align}
E\left[ X ^{2}\right]  & = \sum_{i=1}^{N}i^{2}P(X=i)\\
E\left[ X ^{2}\right]  & = \sum_{i=1}^{N}i^{2} \frac{1}{N}\\
E\left[ X ^{2}\right]  & = \frac{1}{N}\cdot\sum_{i=1}^{N}i^{2} \\
E\left[ X ^{2}\right]  & = \frac{1}{N}\cdot \left( \frac{N(2N+1)(N+1)}{6} \right) \\
E\left[ X ^{2}\right]  & = \frac{(2N+1)(N+1)}{6}  \\
\end{align}
$$
$$
\begin{align}
\mathrm{Var} \left[ X \right]  & =\mathrm{E} \left[ X^{2}  \right] -(\mathrm{E} \left[ X \right] ) ^{2} \\
\mathrm{Var} \left[ X \right]  & = \frac{(2N+1)(N+1)}{6} -\left[\frac{(N+1)}{2}\right]^{2} \\
\mathrm{Var} \left[ X \right]  & = \frac{2(2N+1)(N+1)-3(N+1)^{2}}{12} \\
\mathrm{Var} \left[ X \right]  & = \frac{2\left(2N^{2} +3N+1\right)-3\left(N^{2} +2N+1\right)}{12} \\
\mathrm{Var} \left[ X \right]  & = \frac{N^{2} +0-1}{12} \\
\mathrm{Var} \left[ X \right]  & = \frac{N^{2} +0-1}{12} \\
\mathrm{Var} \left[ X \right]  & = \frac{N^{2} -1}{12} \\
\end{align}
$$
$\therefore$ The Variance of first $N$ natural numbers is $\frac{N^{2} -1}{12}$ 



> [!exercise|12]  
> 
A group of 20 people consisting of 10 men and 10 women is randomly
arranged into 10 pairs of 2 each. Compute the expectation and variance of the number of
pairs that consist of a man and a woman. Now suppose the 20 people consist of 10 married
couples. Compute the mean and variance of the number of married couples that are paired
together.

Let $A_{i}$ be the event that the $i^{th}$ pair consist of a man and women.
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
& = \frac{10*10}{19}=\frac{100}{19}  \\ \\
\mathrm{E} \left[ I_{i}I_{j}   \right]  & =\frac{\binom{10 }{1}\binom{10}{1}}{\binom{20 }{2}}\frac{\binom{9 }{1}\binom{9}{1}}{\binom{18 }{2}} \quad \text{ when } i\neq j \\
 & =\frac{10}{19} \frac{9}{17} \\
\mathrm{E} \left[ I_{i}^{2}   \right] &  =\mathrm{E} \left[ I_{i}  \right] =\frac{10}{19} \\

\end{align}
$$
$$
\begin{align}
\mathrm{E} \left[ X^{2}  \right]  & =\mathrm{E} \left[ \sum_{j=1}^{10} \sum_{i=1}^{10} I_{i}I_{j}   \right]  \\
& =\sum_{j=1}^{10} \sum_{i=1}^{10} \mathrm{E} \left[ I_{i}I_{j}   \right] \\
& =2\sum_{j=1}^{10} \sum_{i=j+1}^{10} \mathrm{E} \left[ I_{i}I_{j}   \right] +\sum_{i=1}^{10} E[I_{i}^{2}  ]\\
& =2\sum_{j=1}^{10} \sum_{i=j+1}^{10} \frac{90}{19\times17}+\sum_{i=1}^{10} E[I_{i}  ]\\
& =2\times {4}5\times \frac{90}{19\times17}+\sum_{i=1}^{10} \frac{10}{19}\\
& =\frac{8100}{19\times17}+\frac{100}{19}\\
& =\frac{9800}{19\times17}\\
\end{align}
$$
$$
\begin{align}
\mathrm{Var} \left[ X \right]  & =\mathrm{E} \left[ X^{2}  \right] -\mathrm{E} \left[ X \right] ^{2}  \\
& =\frac{9800}{19\times17} -\left( \frac{100}{19} \right)  ^{2} \\
& =\frac{9800}{19\times17} -\left( \frac{100}{19} \right)  ^{2}  \\
& =\frac{16200}{6137} \\
\end{align}
$$

Now let $B_{i}$ be the event that $i^{th}$ pair is a married couple 
And lets redefine our indicator function and let $Y$ be the random variable number of married couples
$$
\begin{align}
I_{i}=\begin{cases}
1 \quad \text{if the even $B_{i}$ occurs} \\
0 \quad \text{Otherwise}
\end{cases} 
\end{align}
$$

$$
\begin{align}
P(B_{i} ) & =\frac{\binom{10 }{1}}{\binom{20}{2}}\\
& =\frac{10}{10\cdot19}\\
& =\frac{1}{19}\\ \\

\end{align}
$$

$$
\begin{align}
\mathrm{E} \left[ I_{i}  \right] &  =\frac{1}{19} \\
	\mathrm{E} \left[ Y \right]  & =E\left[ \sum_{i=1}^{10} I_{i}  \right]\\
  & =\sum_{i=1}^{10}E\left[  I_{i}  \right]\\
  & =\sum_{i=1}^{10} \frac{1}{19}\\
  & =\frac{10}{19}\\
\end{align}
$$
$$
\begin{align}
\mathrm{E} \left[ I_{i}I_{j}   \right] & = \frac{1}{19} \frac{\binom{9}{1}}{\binom{18}{2}} \quad ; i\neq j\\
& = \frac{1}{19} \frac{1}{17}  \\
\mathrm{E} \left[ I_{i}^{2}   \right]  & =\mathrm{E} \left[ I_{i}  \right] =\frac{1}{19}
\end{align}
$$
$$
\begin{align}
\mathrm{E} \left[ Y^{2}  \right] &  =E\left[ \left( \sum_{i=1}^{10}I_{i}   \right)\left( \sum_{j=1}^{10}I_{j}   \right) \right] \\
 & =E\left[  \sum_{i=1}^{10} \sum_{j=1}^{10}I_{i}  I_{j}  \right]\\
 & = \sum_{i=1}^{10} \sum_{j=1}^{10}E\left[ I_{i}  I_{j}  \right]\\
 & = 2\sum_{i=1}^{10} \sum_{j=i+1}^{10}E\left[ I_{i}  I_{j}  \right]+\sum_{i=1}^{10} \mathrm{E} \left[ I_{i}^{2}   \right] \\
 & = 2\sum_{i=1}^{10} \sum_{j=i+1}^{10} \frac{1}{19\times17}+\sum_{i=1}^{10} \mathrm{E} \left[ I_{i}  \right] \\
 & = 2\times 45 \times\frac{1}{19\times17}+\sum_{i=1}^{10} \frac{1}{19}  \\
 & = \frac{90}{19\times17}+ \frac{10}{19}  \\
 & = \frac{260}{19\times17} \\
\end{align}
$$

$$
\begin{align}
\mathrm{Var} \left[ Y \right]  & =\mathrm{E} \left[ Y^{2}  \right] -\mathrm{E} \left[ Y \right] ^{2}  \\
 & =\frac{260}{19\times 17}-\left( \frac{10}{19} \right)  ^{2} \\
 & =\frac{3240}{6137} 
\end{align}
$$
