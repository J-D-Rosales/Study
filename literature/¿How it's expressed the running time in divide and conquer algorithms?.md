<span style="color:yellow">IDEA:</span>
Let put $T(n)$ the running time, then it will have two cases:
1. When n <= c , which is a constant, therefore it will take $\Theta(1)$ time to execute.
2. When the problem can be divided into sub problems. Let's say the problems can be divided into $a$ sub problems, which is $\frac{1}{b}$ the size of the original. It takes $T\left( \frac{n}{b} \right)$ time to solve one problem of size $\frac{n}{b}$, and so it takes time $aT\left( \frac{n}{b} \right)$ to solve $a$ of them. If we take $D(n)$ time to divide the problem and $C(n)$ to combine the solutions of the sub problems into the solution to the original problem, we get then:

$$
T(N) = \begin{align}
\Theta(1)  & \text{ if n <= c} \\
aT\left( \frac{n}{b} \right)  + D(n) + C(n)  & \text{ otherwise }
\end{align}
$$


<span style="color:yellow">Evidencia:</span>


**Tags:**

**Referencias**:
[[2.3 Designing algorithms Real]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[E- Merge sort Procedure Analysis]]
[[D- Divide and conquer approach]]
[[E- Merge sort algorithm divide and conquer analysis]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

