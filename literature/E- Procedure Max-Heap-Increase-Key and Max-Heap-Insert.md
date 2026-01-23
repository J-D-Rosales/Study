<span style="color:yellow">IDEA:</span>
![[Procedure Max-Heap-Increase-Key and Max-Heap Insert.png]]

As before, we are making some assumptions. For example that in the step of changing keys, all is updated, for the index and for the keys in the object. Also, that the comparisons are made by the pointers, etc.
In the first procedure we start with a comparison, that takes $\Theta(1)$. Then, since One element has increase it's key (the element was in the array), we just need to search, where it's the right position for him. We do that comparing its father, so if the key is greater we climb up, until we can not climb up. In that precise instant, we arrive at our spot, and the heap property is preserved.(See the example). We could say, that it looks like insertion sort, but comparing with the father of the element. [[2.1 Insertion sort _Real]], [[A-pseudocode for Insertion sort]]. The running time is $O(lgn)$, because the maximum comparison is until it comes to root.
___
The second procedure starts the same.
First we check that there are plenty of space for the array. Then, we update +1 the size (the new element or object will come there). The key of the new object is set as $-\infty$. We put the element in the array and map the object to index heap-size in the array. 
Then we update the key calling the procedure we see before. The process has a running time of $O(lgn)$, because of the Max-Heap-Increase-Key.


<span style="color:yellow">Evidencia:</span>
![[E- for procedure Max-Heap-Increase-Key.png]]

**Tags:** #algorithm 
#examples 
**Referencias**:
[[6.5 Priority Queues]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[D- of a Heap (Binary)]]
[[¿What are the basic operations of a Priority Queue?]]
[[D- of a Priority Queue]]
[[D- of a loop invariant]]
[[¿What are the ways to map application to and from array indices?]]
[[¿What are the basic operations of a Priority Queue?]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

