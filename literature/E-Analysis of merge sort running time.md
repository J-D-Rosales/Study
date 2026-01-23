Let's recall the fórmula
[[¿How it's expressed the running time in divide and conquer algorithms?]]
Now, we see that for merge-sort a = 2, b = 2. Now, for the merge-procedure [[Merge Sort Procedure Pseudo Algorithm.png]] so, since the merge-procedure takes $\Theta(n)$ time, $C(n) = \Theta(n)$. So, the formula will be:
$$
T(n) = \begin{align}
c  &  & \text{if n = 1} \\
2\left( T\left( \frac{n}{2} \right) \right) + cn  &  & \text{ if n > 1}
\end{align}
$$
we'll put a constant c as the time it requires for a problem of size 1 and the time per element 
as well as the time per array element in the divide and conquer steps. (It is unlikely to have the same constant, this is done for educational purposes).
[[E- Recursion tree analysis for merge sort algorithm]]

#examples 

# references
[[2.3 Designing algorithms Real]]
[[E- Recursion tree analysis for merge sort algorithm]]
[[E- Merge sort algorithm divide and conquer analysis]]
[[¿How it's expressed the running time in divide and conquer algorithms?]]
[[E- Merge sort Procedure Analysis]]
[[D- Divide and conquer approach]]