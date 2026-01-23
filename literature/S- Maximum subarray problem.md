[[E- Transformation of The Maximum subarray problem stock market into a Maximum subarray problem]]
Since we've transform the problem, we are going to take a divide and conquer approach.
We have a complete array,  $A[low\dots high]$, So, the idea is to divide the problem, in smaller problems in which we can handle better, let's called the midpoint *mid*, So we have the arrays:
$A[low\dots mid]$ and $A[mid+1\dots high]$. Therefore the maximum subarray must be in one of the next three places:
1. $A[low\dots mid]$
2. $A[mid + 1\dots high]$
3. crossing the mid between the first and the second.
For the first two, it's really easy, we just have the same problem in small scale, and therefore, we search the maximum subarray in the subarray. However for the third we need an algorithm to known how to get the maximum subarray crossing that point.
[[Procedure Find-Max-Crossing-Subarray analysis]]
Having the procedure for the crossing midpoint, let's wrap all together.
[[Procedure Find-Maximum-Subarray]]