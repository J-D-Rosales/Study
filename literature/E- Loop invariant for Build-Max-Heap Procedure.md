Let's recall the procedure first.
[[E-Procedure Build-Max-Heap]]
![[Build-Max-Heap Pseudocode.png]]

Then our Loop invariant will be:
	At the start of each iteration of the for loop, the nodes $i,i+1\dots n$ is the root of a max heap
Let's then recall the process it needed.
**Initialization**: Prior the first iteration $i= \left\lfloor  \frac{n}{2}  \right\rfloor$, indeed $\left\lfloor  \frac{n}{2}  \right\rfloor, \left\lfloor  \frac{n}{2}  \right\rfloor +1. \dots n$ is a leaf on the heap, and trivially it's the root of a max heap
**maintenance**: At the start of each iteration, the children of $i$ are numbered higher than i. Therefore, by the loop invariant the children are heaps. Also, the $i$ index, when we apply the Max-Heapify procedure, we'll see that it respects the property of the heaps in $i+1,i+2,\dots n$, so it just transforms i in a heap. Decrementing the count of i, will do the same, so the loop invariant holds.
**termination**: We see it finishes with $i = 0$, indeed all of the i before $1,2,3,\dots n$ are heaps. Especially the $1$ index, that is the root. So the loop invariant holds making the procedure $\left\lfloor  \frac{n}{2}  \right\rfloor$ iterations. 

## References
[[6.3 Building a Heap]]