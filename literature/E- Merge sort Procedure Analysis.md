The merge sort procedure, will use Merge as procedure. 
MergeSort(a,p,r). If p>= r then the sub array has at most 1 element, so it's sorted. If not the procedure it's gonna be split in half the array and check that again.

![[Merge Sort Procedure Pseudo Algorithm.png]]

When you see $\lceil  \rceil$ or $\lfloor  \rfloor$ , we use them as an easy way to verify $\frac{n}{2}$. 
To sort the entire sequence of n items, we merge the arrays of 1, after that arrays of 2, and so on, until we get $\frac{n}{2}$, and we merge them having (by loop invairant) the n array sorted. 

# References
[[2.3 Designing algorithms Real]]
[[E- Merge sort algorithm divide and conquer analysis]]