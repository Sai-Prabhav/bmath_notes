> [!exercise|10]
>  In a sequence of Bernoulli trials let X be the length of run (of either successes or failures) started by the first trial. 
>   - Find the distribution of X, E(X), Var(X). 
>  -  Let Y be the length of the second run. Find the distribution of Y , E(Y ), Var(Y ), and the joint distribution of X and Y

$$
\begin{align}
\frac{1}{1-x} & =x+x^{2} +x^{3} \dots x^{n}\dots  \quad \Mod[x]<1  \\
\frac{d}{dx}\frac{1}{1-x}  & =\frac{d}{dx} (x+x^{2} +x^{3} \dots x^{n}\dots  )\\
\frac{1}{(1-x)^{2} }  & =1x^{0} +2x^{1} +3x^{2} \dots nx^{n-1}\dots  
\end{align}
$$
$$
\begin{align}
\text{let } A  & = \text{ Event of success in trial 1}   \\ 
\text{let } p  & = P(\text{ success} )  \\ 
P(X=r) & = P(X=r|A)P(A)+P(X=r|A^{c} )P(A^{c} )\\
 & = p^{r}(p-1) +(1-p)^{r}p \quad \text{r runs followed by a diffrent outcome}   \\
 & =p(1-p)\left[ p^{r-1} +(1-p)^{r-1}  \right]
\end{align}
$$
$$
\begin{align}
\ex[X] & =\sum_{i=1}^{\infty} r P(X=r)\\
& =\sum_{i=1}^{\infty} r p(1-p)\left[ p^{r-1} +(1-p)^{r-1}  \right]  \\
& =p(1-p)\sum_{i=1}^{\infty} r \left[ p^{r-1} +(1-p)^{r-1}  \right]  \\
& =p(1-p)\left\{ \sum_{i=1}^{\infty} r p^{r-1} +\sum_{i=1}^{\infty} r(1-p)^{r-1}  \right\} \\
& =p(1-p)\left\{ \frac{1}{1-p} +\frac{1}{1-(1-p)} \right\} \\
& =p(1-p)\left\{ \frac{1}{1-p} +\frac{1}{p} \right\} \\
& =\frac{p}{1-p} +\frac{1-p}{p} 
\end{align}
$$
a

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
& =\sum_{i=1}^{10} \frac{10}{19}   \\
\end{align}
$$
$$
\begin{align}
& = \frac{10*10}{19}=\frac{100}{19}  \\
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
 & = 2\sum_{i=1}^{10} \sum_{j=i+1}^{10}E\left[ I_{i}  I_{j}  \right]+\sum_{i=1}^{10} \mathrm{E} \left[ I_{i}^{2}   \right]  

\end{align}
$$
$$
\begin{align}
 & = 2\sum_{i=1}^{10} \sum_{j=i+1}^{10} \frac{1}{19\times17}+\sum_{i=1}^{10} \mathrm{E} \left[ I_{i}  \right] \\
 & = 2\times 45 \times\frac{1}{19\times17}+\sum_{i=1}^{10} \frac{1}{19}  \\
 & = \frac{90}{19\times17}+ \frac{10}{19}  \\
 & = \frac{260}{19\times17} 
\end{align}
$$

$$
\begin{align}
\mathrm{Var} \left[ Y \right]  & =\mathrm{E} \left[ Y^{2}  \right] -\mathrm{E} \left[ Y \right] ^{2}  \\
 & =\frac{260}{19\times 17}-\left( \frac{10}{19} \right)  ^{2} \\
 & =\frac{3240}{6137} 
\end{align}
$$

