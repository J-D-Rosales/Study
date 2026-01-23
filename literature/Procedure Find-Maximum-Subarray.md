![[Find-Maximum-Subarray.png]]

The procedure starts with the base case, that is if the array has 1 element.  If that occurs we return the index, along with it's value. 
On the other hand, we need to find the mid, that is half the array, the since we have $A[low\dots mid]$ and $A[mid+1\dots high]$. then at least the arrays have 1 element. Then we find the three cases, and in lines 7-11 we just return depending on the cases, where the maximum sum it's gonna be the return with the indices. Remember that the crossing it's not a recursive part, because it's not a problem of an small instance, that's way we put it in the combine part. 

## References
[[S- Maximum subarray problem]]