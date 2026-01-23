<span style="color:yellow">IDEA:</span>
It could be divided into three procedures.
1. The Max-heapify compute the indices for the heap (since we are working in an array)
2. If the current node-problem $A[i]$ is greater than it's children's $A[left],A[right]$, there is no problem, the heap property it's accomplished.
3. If the current node-problem is less than it's children's then we change the values (not the indices) of the greater values of it's children with the current node and by recurrence apply the Max-Heapify to the index of that node (because, now the new children might not accomplish the heap property).

<span style="color:yellow">Evidencia:</span>
![[Max-Heapify-Pseudocode.png]]
![[Max-Heapify procedure.png]]

**Tags:**

**Referencias**:
[[6.2 Maintaining the Heap property]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[¿What are the requirements to apply Max-Heapify?]]
[[What it's the heap property?]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

