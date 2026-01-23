<span style="color:yellow">IDEA:</span>
First, to analyze this, we need to see the pseudo code:
[[A-pseudocode for Insertion sort]]

So, for $j = 1, 2,3,\dots n$ to a.length we denote $t_{j}$ the number of times the while loop is executes in line 5 for that value of j. Comments are not executable.
So, taking the in consideration we will have:
![[Insertion_sort_algoirthm_time_analysis.png]]

The running time of the algorithm is the sum of each statement executed. A statement that takes $c_{i}$ times to be executed and it's gonna be executed $n$ times will contribute $c_{i}n$ times to the total running time (this propertie does not hold for everything).

![[F-Total Execution time for Insertion sort algorithm]]

As intended depending on the input, the running time will vary
**Best time** A sorted array. If we have a sorted array, the comparison of the while will be just 1. therefore $t_{j} = 1$.
$$
T(n) = c_{1}n + c_{2}(n-1) + c_{4}(n-1) + c_{5}(n-1) + c_{8}(n-1)
$$
which is a **linear function**, $an+b$.
The worst case, which is the typically analyzed would be when the array is in decreasing order, therefore we need to check every possible input for j. and the worst case (solving the sums would be).
$$
T(n) = c_{1}n + c_{2}(n-1) + c_{4} (n-1) + c_{5}\left( \frac{n(n+1)}{2} -1 \right) + c_{6} \left( \frac{n(n+1)}{2 }  \right) + c_{7} \left(  \frac{n(n+1)}{2}  \right) + c_{8}(n-1)
$$
This is a **cuadratic function**.
# References