The recurrence is split in both:
$$
T(n) = T\left( \frac{n}{3} \right) + T\left( \frac{2n}{3} \right) + \Theta(n)
$$
![[Recursion tree for the recurrence of Example 2.png]]

The pattern is simple, however, the tree is not balanced, some paths are larger than others. Therefore, to know the height we'll go to the largest.
We know it'll reach the end when hit's the bottom $\Theta(1)$.
So, since the recurrence stops in the base case $n_{0}$, 
$$
\left( \frac{2}{3} \right)^{h}n <n_{0} <= \left( \frac{2}{3} \right)^{h-1}n
$$
Why? because, it's not exact, and the value for the height is $h = \left\lfloor  \log \frac{3}{2} \left( \frac{n}{n_{0}} \right)   \right\rfloor+ 1$. You can substitute that in the equation above and see that it accomplishes for both parts.
Then, if the height is that, then it should be in $\Theta(\log n)$. (Remember that the base does not count because could left as a constant).
For all internal nodes we have $cn \cdot h$ which is  upper bounded to $O(nlgn)$.
We may be tempted that the total cost of the leaves, making an upper bound would be like a full complete binary tree. However, if you do that you'll get $O(n^{\log_{3 / 2} 2})$ which is larger than $O(nlgn)$, therefore, its leaves are greater than all internal nodes, which is false, in fact, the cost of all leaves is $O(n)$.

We can count the leaves of the tree by making a recurrence, but with the base case 1 (because of 1 leaf).
$$
L(n) = \begin{cases}
1 & \text{if n<= n0} \\
(T( n/ 3)) + (T \left( \frac{2n}{3}  \right))  & \text{if n > n0}
\end{cases}
$$
By substitution method, you'll prove the answer is $O(n)$.
Finally
$$
T(n) = \Theta(n) + O(nlgn) = O(nlgn)
$$
 
## References

[[4.4 The recursion tree method for solving recurrences]]