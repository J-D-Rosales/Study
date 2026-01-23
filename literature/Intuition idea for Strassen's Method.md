<span style="color:yellow">IDEA:</span>
Strassen's Method for multiply matrices was funded by the idea that we do not need to multiply eight time, but seven and therefore it can be reduced the running time of the algorithm.
The steps to perform the Strassen's Method is in four steps:
- Divide the matrix A,B,C into $n / 2 \times n / 2$ submatrices, this takes $\Theta(1)$ since it is done by index calculation.
- Create 10 matrices $S_{1},S_{2}\dots,S_{10}$ of size $n / 2 \times n / 2$, that's gonna be sum's and subtractions of the matrices previously created. The time to this is $\Theta(n^{2})$.
- We create 7 matrices $P_{1},P_{2}\dots,P_{7}$. Where each is of size $n / 2 \times n / 2$ we compute the the new matrices with the 10 we have created.
- By adding and subtractions of the $P_{i}$ matrices we are going to get and copy to $C_{11}, C_{12}, C_{21}, C_{22}$.  We can do this in $\Theta(n^{2})$ time. 

<span style="color:yellow">Evidencia:</span>
We can make a running time for the recurrence:
![[F-Strassen's algorithm recurrence#^c337d6]]
By analysis this lead as to $T(n) = n^{lg_{7}}$.
**Tags:**

**Referencias**:
[[4.2 Strassen's algorithm for matrix multiplication]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[4.2 Strassen's algorithm for matrix multiplication]]
[[¿When we can eliminate constants in recursive algorithm and when it affects asymptotically?]]
[[E- Analysis of running time for recursive algorithm for multiply square matrix]]
[[E- Recursive solution for Square matrix multiplication]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

