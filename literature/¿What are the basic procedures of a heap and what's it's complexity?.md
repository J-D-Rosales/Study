<span style="color:yellow">IDEA:</span>
The basic procedures are:
- **Max-Heapify-procedure**: It maintains the property of the heap, and runs in $O(lg(n))$ time. It need some properties before used such as the children need to accomplish the heap property, so need to be careful using this.
- **Build-Max-Heap**: It helps to build a max-heap from an unordered array. It runs in $O(n)$ time.
- **Heap-sort**: It helps to sort the array of elements. It runs in $O(nlg(n))$ time.
- **Max-Heap-Insert,Max-Heap-Extract,Max-Heap-Increase-Key,Max-Heap-Maximum**: Helps when try to build the priority queue. It runs in $O(lg(n))$ time. And add the time for mapping between objects (heap) and the indices inside the array. 


<span style="color:yellow">Evidencia:</span>
When we talk about mapping it refers to the time when an object (document for example) is change let's say it's priority, and we need to find the index of that object. So, before we ask that we have mapped the index like Documento1-> 0, Document2 -> 4, etc. Therefore, there is a time into mapping the object into the index, to actualize the heap.

**Tags:**
#Question_to_practice 
**Referencias**:
[[6.1 Heaps]]

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[¿How can we calculate the height of a heap and what's it's complexity?]]
[[¿What are types of a heap and when to use it?]]
[[D- of a Heap (Binary)]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

