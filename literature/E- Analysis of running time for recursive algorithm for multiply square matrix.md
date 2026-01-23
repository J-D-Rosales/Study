Recall the algorithm [[E- Recursive solution for Square matrix multiplication]]
![[Square-Matrix-Multiply-Recursive(A,B).png]]

Let call $T(n)$ the running time for multiply a $n\times n$ matrix. then.
From line 1-5 five using the in place method by indices is also a constant. Therefore, everything takes $\Theta(1)$ time.
Now, from line 6-9, we see that we partition the problem, into eight sub-problems. Therefore, we take $8T\left( \frac{n}{2} \right)$ problems to solve. Also, we should see or check that the sum of the matrix takes also time. since it's 4 sums, it would take each sum that gave $\frac{n^{2}}{4}$ entries $\Theta(n^{2})$. That's because the constant does not affect. To put the result of the sum of the matrix multiplication we take constant time, since we are using indices. Finally, the the equation is:
$$
T(n) = \Theta(1) + 8T(n /2) + \Theta(n^{2})
$$
Simplifying:
$$
T(n) = 8T(n / 2) + \Theta(n^{2})
$$
Combining the recursive case, it gives:
$$
T(n) = \begin{cases}
\Theta(1)  & \text{if n = 1} \\
8T(n / 2) + \Theta(n^{2}) & \text{if n > 1}
\end{cases}
$$
From the master method, or simply by checking in the tree, this lead us to the final time of $\Theta(n^{3})$. 
[[¿When we can eliminate constants in recursive algorithm and when it affects asymptotically?]]
## References
[[E- Recursive solution for Square matrix multiplication]] 