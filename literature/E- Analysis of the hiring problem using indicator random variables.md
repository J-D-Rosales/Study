We are taking in consideration that randomly the office sent us one candidate.
Let denote $X$ the random variable whose number equals the number of times an applicant is hired. By equation in san pincho.
$$
E[X] = \sum_{x = 1}^{n} x Pr\{ X = x \}
$$
It means "The expected value of the number of applicants that were hired is equal to the probability of hire 1,2,3,4...n applicants multiplied by it's probability and sum up everything".
However, this is hard (no joke).
Therefore we'll do the next.
Let's use the indicator random variable $X_{i}$ that is associated with the event when an applicant is hired.
$$
X_{i} = I\{ \text{The ith applicant is hired} \} = \begin{cases}
1 & \text{ if hired}
0 & \text{if no hired}
\end{cases}
$$
Now, we now that the count of $X$ is:
$$
X = X_{1} + X_{2} + \dots X_{n}
$$
Now, let's dive into the probability of a ith applicant. If the ith applicant enter, the probability of him being the best of that local group is $\frac{1}{i}$. Because, as far as now, the group has i-1 candidates and one is the best. Therefore, since everything is random, the next person as the probability of beating the whole group of $\frac{1}{i}$. Imagine from the principle. The first person in enter has the possibility of 100% of being the best (there is no one else). The second person has 50 % of being the best, because they have the same probability. And so on.Think about lottery ticker, not hiring, so the probability that a person has the lottery ticket is reducing by the umber of persons that are there.
The probability that the new wins it's the probability that wins the greater. For example if there was 10 people, and one of them is the winner. THe probability that a new win him is 1/10, because the winner has the probbaility of 9/10.
So, we reach $E[X_{i}] = \frac{1}{i}$.
$$
E[X] =E\left[  \sum_{i = 1}^{n} X_{i} \right] = \sum_{i = 1}^{n} E\left[ X_{I} \right] = \sum _{i = 1}^{n} \frac{1}{i} = \ln n + O(1)
$$
That is harmonic series [[F- formulas of sums and sumatorias#^4cdd54]]


# Referencias
[[5.2 Indicator random variables]]