Let's recall the formula for the recurrence and our guess that is $O(n^{2})$. $T(n) = 3 T( \lfloor n / 4 \rfloor) + \Theta(n^{2})$
Now, since our guess is $O(n^{2})$ we use the substitution method and want to prove that $T(n)\leq dn^{2}$. Therefore,
$$
\begin{align}
T(n)  & \leq 3 T(\lfloor n / 4 \rfloor ) + cn^{2} \\
  & \leq 3d(n / 4)^{2} + cn^{2} \\
  & \leq \left( \frac{3}{ 16} \right) dn^{2} + cn^{2} \\
 & \leq dn^{2} 
\end{align}
$$
For all value of $c < (\frac{3}{16})d$. ( This comes solving the inequality).
For the base case we need a $n_{0}$ sufficient large such that $dn^{2} \geq d \geq T(n)$ where $1 \leq n < n_{0}$ which dominates the constant hidden by $\Theta$.
We cannot choose c arbitrarily, however, we can choose d free.

## References
[[E- Solving a recurrence with recursion tree method Example 1 T(n) = 3 T(n 4) + cn²]]