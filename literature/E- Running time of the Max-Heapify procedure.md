Let's recall again the Pseudo-code for the procedure.
![[Max-Heapify-Pseudocode.png]]

The running time it's analyzed as follows. 
The time to fix the relationship between $A[Parent(i)]$ $A[Left(i)]$ y $A[Right(i)]$ is $\Theta(1)$, because is just swamp and comparisons. Now, we'll have to do, in the worst case, all the possible recurrence, when the tree is not a heap yet. Therefore, we need to see how much the problem is reduced, in the worst case, in going to one of his children.
Let's called $N_{l}$: Nodes from the left child and $N_{r}$: Nodes from the right child.
We know that the right child (height h-2) will have a perfect tree if the worst case occurs, that is, when the left child have all his nodes completed. So, recalling the formula to numbers of nodes by the height:
$$
N_{r} = 2^{h-2+1}-1 = 2^{h-1}-1 
$$
remember that we are counting all the nodes, so that's why it's +1 at the exponent. For $n$ bigger's the term -1 is dismissed.
Now, for the left child:
$N_{l} = 2^{h-1+1} -1 = 2^{h}-1$
Ignoring the -1 terms for n sufficient large we have:
$N_{l} = \frac{1}{2} N_{r}$ in the worst case.
We also know that $n = N_{l}+ N_{l}$, replacing we have that $N_{r} =\frac{2}{3}n$
Therefore the running time goes as follows:
$$
T_{n} = T\left( \frac{2}{3}n \right) + \Theta(1)
$$
and by master theorem this is $O(lg(n))$.
If we analyze the case in a node of heigh h the complexity will be $O(h)$.
## References
[[6.2 Maintaining the Heap property]]
[[¿What are the requirements to apply Max-Heapify?]]