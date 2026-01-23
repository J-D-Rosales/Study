<span style="color:yellow">IDEA:</span>
Essentially exists two forms.
1. **Changing the object:** It is made by a **Handles** (in this context is additional information that keeps track of the index). So, an object have inside himself the index to go exactly his position in the array. Also, when the object is swap or change its index, the index is update automatically.
2. **Mapping (hash table)**: Implement inside the priority queue (as a black box), doing so you are coordinating the changes in the heap, and automatically can paired them with the change in the hash table. Normally this would take $O(1)$, but technically (and with a bad implementation) this could lead to $\Theta(n)$ (rarely).


<span style="color:yellow">Evidencia:</span>
In order to see it crearly, there is an example:
[[Example of mapping objects with index in heaps]]

**Tags:** #Question_to_practice 

**Referencias**:
[[6.5 Priority Queues]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[D- of a Heap (Binary)]
[[Example of mapping objects with index in heaps]]
[[¿What we need to take in consideration when we want to implement a priority queue with a heap?]]
[[¿What are the basic operations of a Priority Queue?]]
[[D- of a Priority Queue]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

