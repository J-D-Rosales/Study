![[Find-Max-Crossing-Subarray(A,low,mid,high).png]]

In order to understand better, we have a picture:
[[Maximum subarray crossing the midpoint]]
The algorithm works as follow:
From line 1-2 we just initialize our variables, left-sum it's gonna be the maximum sum we'll have from the left subarray, and the sum is the current value of the sum. We are going down from mid to low. From lines 3-7 we actualized sum and see if the current sum is greater than left-sum, if it is, then the left-sum need to be actualized, and we need the index in which the maximum subarray (maximum sum) was encountered. Recall that if the sum is not improving, then the left-sum would not be actualized, since there is no better than the previous we have calculate. The other part of the loop is essentially the same, just for the other part, however we need to initialize the variables as well. 
Finally we return all we need, with the maximum sum encountered.

The time it would require if the array has $n$ entries we claim to be $\Theta(n)$. Taking the array $A[low\dots high]$ and $n = high-low+1$, then we just need to count how many iterations are all together, because each iteration takes $\Theta(1)$ time. 
**left**: $mid-low +1$, **right:**  $high - mid$ **sum** = $high - low +1$ which is $n$. Then, it's linear time.

## References
[[S- Maximum subarray problem]]