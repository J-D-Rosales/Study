The procedure, and the pseudocode are easy.
![[Heapsort pseudocode algorithm.png]]

Here, we first called the Build Max Heap procedure [[E-Procedure Build-Max-Heap]]. Then, we know that the greater of all elements is in the top of the heap, I mean the root. Therefore, we just change the $A[n]$ position of the array with greater element, therefore $A[n]$ is now, our new root. Now, we need to ensure the rest is a max-heap also, we know that the children of the root are max-heaps. However, might be not. Therefore, we change the value of A.heap-size by 1 and apply the Max-Heapify procedure [[E-Procedure of Max-Heapify]] to the root, then it will make $A[1\dots n-1]$ a max-heap. We continue doing the process, until $i = 2$.  That is because, when we change the last two, the array will be in order.

The whole procedure is going to take $\Theta(nlgn)$ time. Because the for takes $n$ time, and each time is calling a procedure that takes $O(lgn)$ time. Therefore that is the total time. And since, the Build-Max-Heap takes $O(n)$ time, the running time holds.
## References
[[6.4 the heapsort algoritthm]]