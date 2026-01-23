See [[E- Maximum subarray problem stock-market]]
In order to solve this we can do the next:
Check all the possible ways we have to have profit, it means the buy date precedes the sell. The forms to do this choosing two from two is: $\begin{pmatrix} n \\ 2\end{pmatrix}$, which is $\Theta(n^{2})$. Since the best is to evaluate the dates in constant time, then this approach would take $\Omega(n^{2})$ time.

# References
[[4.1 The maximum-subarray problem]]