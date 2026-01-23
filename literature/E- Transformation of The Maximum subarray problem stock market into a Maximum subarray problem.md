[[E- Maximum subarray problem stock-market]]
[[E- Brute force solution for Maximum subarray problem stock-market]]
We would like to have a better way to solve this problem. So, we see that the array can be transformed into which days we got profit and which days not, and the only goal would be how can we have the largest sum of profit.
See the next 
![[Example of the chart showing the cost per day for the maximum subarray poroblem.png]]

The rows in the figure shows the the difference in prices for the day $i$ between the prices after the day $i-1$ and day $i$. 
The maximum contiguous subarray that have the largest sum is **the maximum subarray**.
It see not much help because the time still is $\begin{pmatrix}n-1  \\ 2 \end{pmatrix}$ = $\Theta(n^{2})$ for a period of n days of course.


## References
[[4.1 The maximum-subarray problem]]