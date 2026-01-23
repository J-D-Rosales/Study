So, in order to solve this $T(n) = 2T(\lfloor n / 2 \rfloor) + n$, first we need to make a guess.
We have seen problems like this, so we guess that $T(n) = O(n\log n)$, that is an upper bound.
So, now, to prove this, we need to prove that $T(n) \leq cn\log n$ for an appropriate c. However, in order to do this, we make strong induction. Saying that it works for $m <n$, being m specifically $\lfloor n / 2 \rfloor$. Yielding: $T(\lfloor n / 2 \rfloor) = c \lfloor n / 2 \rfloor \log \lfloor n / 2 \rfloor$. So, substituting into the main recurrence:
$$
\begin{align}
T(n)  & \leq 2( c \lfloor  n / 2 \rfloor \log \lfloor n / 2 \rfloor) +n \\
 & \leq cn\log ( n / 2) + n \\
 &  = cn \log n - cn \log 2 + n \\
 & = cn \log n - cn + n \\
 & \leq cn \log n
\end{align}
$$
the last step is accomplish if $c \geq 1$.
Now, we need to prove that for boundary condition. If we assume that $T(1) = 1$, we've got a problem. Since, the base case for the induction is wrong, $1 \log_{1} = 0$. and therefore, the proof is not complete. However, we take the advantage of the asymptotic notation where $n > n_{0}$, so we choose $n_{0} > 1$, where we use the base case for inductive hypothesis to be $T(2)$ and $T(3)$. Remember that the base cases of the recurrence is still $T(1) = 1$, but we use the base cases of the inductive hypothesis in order to avoid the last problem. So, for $n\geq_{4}$ all n's when divided by 2, are going to fall into $T(2)$ or $T(3)$, therefore proving for both of them, will essentially lead to the prove of the base cases. Now, we can complete the proof by choosing a $c \geq 2$ in which $T(2) \leq c 2\log 2$ and $T(3) \leq c 3 \log 3$ .

# References
[[4.3 The substitution method for solving recurrences]]
