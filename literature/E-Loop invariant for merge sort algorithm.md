<span style="color:yellow">IDEA:</span>
The loop invariant will be:
*At the start of each iteration the the subarray $A[p\dots k-1]$ contains the k - p smallest elements of $L[1\dots n_{1}+1]$ and $R[1\dots n_{2} +1]$ in sorted order. Moreover, $L[i]$ and $R[j]$ are the smallest elements of their arrays that have not been copied into A*.

**Initialization**: At the start of the iteration k = p, so the array $A[p\dots k-1]$ it's empty. Therefore, i =1 and j = 1, so $L[1]$ and $R[1]$ are the smallest elements of their array that have not been copied into A, because it's empty.
**maintenance**: Let's assume that $L[i] \leq R[j]$, then the smallest element that have not been copied into A is $L[i]$. So, the array $A[p\dots k-1]$ still contains the k-p smallest elements, after line 14 copies the elements to A, then the sub array $A[p\dots k]$ will contain the k-p +1 smallest elements. Incrementing the k and i, establish the loop invariant. If the other case is asserted, then the 16 and 17 will handle that, and still the loop invariant will be preserved.
**Termination**: At the termination k = r +1, by the loop invariant the subarray $A[p\dots k-1]$, which is $A[p\dots r]$ contains the k-p = r-p +1 smallest elements from $L[1\dots n_{1} + 1]$, and $R[1\dots n_{2} +1]$, in sorted order. L and R contains $n_{1} + n_{2} + 2 = r - p + 3$ elements.  Just the two largest ($\infty$) have not been copied into A. 

<span style="color:yellow">Evidencia:</span>


**Tags:** #examples 
**Referencias**:
[[2.3 Designing algorithms Real]]
[[E- Merge sort algorithm divide and conquer analysis]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[Intuition for merge sort algorithm]]
<span style="color:	#87CEEB">East: Opposite</span>
[[E-Analysis of Insertion sort Algorithm - time analysis]]
[[A-pseudocode for Insertion sort]]

<span style="color:	#87CEEB">North: Theme Question</span>
[[D- Divide and conquer approach]]

<span style="color:	#87CEEB">South: What does this lead to</span>
[[2.3 Designing algorithms Real]]
