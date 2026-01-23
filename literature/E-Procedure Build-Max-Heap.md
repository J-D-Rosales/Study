![[Build-Max-Heap Pseudocode.png]]

By the property that $A\left[ \left\lfloor  \frac{n}{2}  \right\rfloor + 1\dots n\right]$ are leafs, we can count each leaf as 1-element trivial max-heap. The idea will be use the Max-Heapify Procedure [[E-Procedure of Max-Heapify]] to run onto the remaining nodes. In doing so, we'll accomplish to make every node a max-heap, and finally turning all the array into a heap.
<span style="color:yellow">Examples</span>:
Visual representations of the procedures are left as a reference in the book [[B-Introduction-to-algorithms - Cormen]]

#examples 
## References
[[6.3 Building a Heap]]
[[D- of a Heap (Binary)]]
[[¿What are the basic procedures of a heap and what's it's complexity?]]