The intuition idea will be:
**divide**: Divide the n-element array to two subarrays to be split in half. $\frac{n}{2}$ element each part.
**conquer**: Sort two sub sequences recursively using merge sort.
**combined**: Merge the two sorted sub sequence to produce the sorted answer.

[[Intuition for merge sort algorithm]]

Now, what we are going to do is the merge operation. 
MERGE(A,p,q,r). This means, we are going to merge the sub array of start index p to q, and the sub array of index q+1 to r. So the procedure for this is going to be $\Theta(n)$ in the worst case. It merges to form a unique sub array.

To make a pseudocode we are going to use a sentinel which is going to be $\infty$. Because when merging if we come to an infinity value, we know that that pile it's with no more values and just the other pile will have the rest.  (We could also go r-p +1 times with the algorithm where we halt when reaching that number).
![[Merge procedure from Merge sort algorithm.png]]

The explanation is simple, we create two arrays with +1 size (because of the sentinel) and assign the right index. 
Now, we do a for loop, from the start index from the big array to last (p to r), and check from the to arrays, if L is less than R then we put that value into A, because it's the minor, if not we do the opposite, and therefore our array will be sorted in $\Theta(n)$ time.

# References
[[2.3 Designing algorithms Real]]
[[D- Divide and conquer approach]]
[[D- Order of growth]]