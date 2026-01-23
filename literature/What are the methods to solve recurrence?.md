<span style="color:yellow">IDEA:</span>
In essence they are three, that is convert into a asymptotic notation of the form $\Theta$ or $O$.
1. **Substitution method**: Consists in guess what could be the form, then use mathematical induction to prove or wrong out answer.
2. **Recursion-tree method**:Transform the recurrence into a tree in which each node is the cost incurred at various levels of recursion. We use bounding summations to solve the recurrence.
3. **master method**: Provide a solution for recurrences of the next form :
$$
T(n) = aT\left( \frac{n}{b} \right) + f(n)
$$
Where $a\geq 1,b> 1$ and $f(n)$ it's a given function. This characterized a problem divided in a parts which takes $\frac{1}{b}$ time to solve it and $f(n)$ it's the time it takes the divide and combine steps.


<span style="color:yellow">Evidencia:</span>


**Tags:**

**Referencias**:
[[B-Introduction-to-algorithms - Cormen]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[E-Analysis of merge sort running time]]
[[E-Analysis of Insertion sort Algorithm - time analysis]]

<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

