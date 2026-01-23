Let's recall our variables.
Our sample space $S = \{ H,T \}$.
$X_{i}$ -> The indicator random variable associated with the event that the ith flip will trun H.
$X_{i} = I\{ \text{The ith flip result in event H} \}$. 
Now, let's denote $X$ the number of Heads that were after n flips.
$$
X = \sum _{i  = 0 } ^{ n} X_{i}
$$
To know the compute number, take the expected value of both of them.
[[F- 5.2 for n flip coins and the expected value]]
Now, remember the lemma [[F-Lemma 5.1 for expected value in an indicator random variable]]. Where it shows that for every $X_{i}$ with $i = \{ 1,2,3\dots n \}$ the expected value is $E[X_{i}] = \frac{1}{2}$. However, the formula just applies when it's the expected value of the sum not the sum of expected value. But, by Linearity of expectation we can assure that. That applies even when there is dependency among the random variables. 
Therefore:
$$
\begin{align}
E[X]  & = \sum_{i = 0}^{n} E[X_{i}] \\
 & = \sum_{i=0}^{n} \frac{1}{2} \\
 & = \frac{n}{2}
\end{align}
$$

# Referencias
[[5.2 Indicator random variables]]