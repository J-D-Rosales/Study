<span style="color:yellow">IDEA:</span>
It's a representation of a tree made in an array $A[1\dots n]$ where $n$ is the number of node of a perfect binary tree at the height of the current heap. The heap represented in the array has index, where we could retrieve the information about his children, where $2i$ is for the left child and $2i + 1$ is for the right child. 
The heap has an attribute that is *A.heap-size* which is and integer $0< heap.size \leq n$. Which tell us the number of nodes the heap has. 
The nodes are fulfilled from left to right at the last level, where the tree could not be completed.
The root will contain the max or the min element depending on the kind of the heap, the child's also accomplish this property.
<span style="color:yellow">Evidencia:</span>
Recall an example of a max heap.
![[Max-heap view as binary tree and an array.png]]
The way to retrieve the information is
![[Procedure for returning elements on a heap (parent, left child and right child).png]]

**Tags:**
#definiton 
**Referencias**:
[[6.1 Heaps]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[Max-heap view as binary tree and an array.png]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

