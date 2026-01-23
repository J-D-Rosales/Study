
Recall the final pseudocode or procedure:
[[Procedure Find-Maximum-Subarray]]
![[Find-Maximum-Subarray.png]]
Then, let's analyze it.
If the Array it's with just one element, we see that line 1 and 2 have constant time: therefore, calling $T(n)$ the time for an array with n elements:
$$
T(1) = \Theta(1)
$$
Now, the recursive case occurs with more that 1 elements, where it is split into two. We spend $T\left( \frac{n}{2} \right)$ time to solve them and we have two (right and left), therefore the contribution for lines 4 and 5 it's:
$$
2T\left( \frac{n}{2} \right)
$$
Now recall that : [[Procedure Find-Max-Crossing-Subarray analysis]] we have that the procedure with the crossing midpoint is $\Theta(n)$. Therefore
$$
T(n) = \Theta(1) + 2T\left( \frac{n}{2} \right) + \Theta(n) + \Theta(1)
$$
$$
T(n) =2T\left( \frac{n}{2} \right) + \Theta(n)
$$
Finally , we merge both and have the next recurrence:
$$
T(n) = \begin{cases}
\Theta(1)  & \text{ n = 1} \\
2T\left( \frac{n}{2} \right)+ \Theta(n)
\end{cases}
$$
By the problem of merge sort, we've seen that this complexity is $\Theta(n\log n)$.

## References
[[4.1 The maximum-subarray problem]]