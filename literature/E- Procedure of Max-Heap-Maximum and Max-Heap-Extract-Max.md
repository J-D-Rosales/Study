<span style="color:yellow">IDEA:</span>
![[Procedure of Max-Heap-Maximum.png]]

This pseudo code is assuming lots of things. Recall information for [[Example of mapping objects with index in heaps]] [[¿What are the ways to map application to and from array indices?]] [[¿What are the basic operations of a Priority Queue?]]. Also, recall that we assume that the pointers are updated, also that max-heapify compares basing on the key, and that actualize the key attribute for each object.
Now, for The first procedure, it's obviously $\Theta(1)$. It return the root.
For the second procedure, we can call it $O(lgn)$ + whatever operation is incurred Max-heapify for mapping priorities. 
In essence, the first element is changed for the last, because we would like to decrease an element (therefore decrease an index). So, putting the last element works, however still we need to do Max-Heapify in the new root to ensure the heap property. [[What it's the heap property?]]

<span style="color:yellow">Evidencia:</span>

**Tags:**
#examples 
**Referencias**:
[[6.5 Priority Queues]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts

