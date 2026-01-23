<span style="color:yellow">IDEA:</span>
The loop invariant can be states as:

*At the start of each iteration of the for loop, the elements of the Array $A[1,2,3\dots j-1]$ stay the same but in sorter order*

**Initialization**:
The first iteration is j = 2. The sub array then is formed by $A[1]$, therefore it is trivially sorted, and of course the loop invariant it's true.
**maintenance**: The next iteration of j, we see that what we are doing is search the correct position for $A[j]$, therefore we look upon $A[j-1], A[j-2]\dots$ and insert in correct position. So the remain elements that are already sorted, will be sorted after the iteration. Then incrementing the counter for j preserves the loop invariant.
**termination**: The condition that breaks the loop is the next: j > A.length  = n. Therefore, the loop terminates on j+1, and substituting that into the first array we have $A[1,2,\dots n]$ in sorted order (the elements). Therefore, the algorithm is correct.


<span style="color:yellow">Evidencia:</span>


**Tags:**

**Referencias**:

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts

<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

