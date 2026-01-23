<span style="color:yellow">IDEA:</span>
```c++
for j = 2 to A.length:
	key = A[j] // this is the element we want to sort
	// search the elements from j-1 to 0
	i = j-1
	while i >0 and A[i] > A[j]:
		A[i+1] = A[i];
		i = i-1
	A[i +1] = key
	
```

What we are doing here is the next:
We start form the element 2, because the first element is trivial to positioning in the right place.
Now, we save the key which is the element we want to save, and well loop all over the elements trying to find the element that it's minor to $A[j]$, therefore when it's find it, replace it. 
Also, we copy the number like moving a window, as the example below.
<span style="color:yellow">Evidencia:</span>
 1 2 4 3
 1 2 4 4
 1 2 3 4

**Tags:**

**Referencias**:
[[2.1 Insertion sort _Real]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[2.1 Insertion sort _Real]]
[[A-pseudocode for Insertion sort]]
[[Intuition Idea for insertion sort algorithm]]
[[E- description of the sorting problem]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

