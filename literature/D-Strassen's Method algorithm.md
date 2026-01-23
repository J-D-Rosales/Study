In order to understand this algorithm, you should check:
[[E- Analysis of running time for recursive algorithm for multiply square matrix]]
and having the intuition idea:
[[Intuition idea for Strassen's Method]]
Now in the step 2, we have the next 10 sums.
$$
\begin{align}
S_{1}  &  = B_{12}  -  B_{22}, \\
S_{2}  &  = A_{11}  + A_{12},  \\
S_{3}  &  = A_{21} + A_{22},  \\
S_{4}  &  = B_{21} - B_{11},  \\
S_{5}  &  = A_{11} + A_{22},  \\
S_{6}  &  = B_{11} + B_{22},  \\
S_{7}  &  = A_{12} - A_{22} ,  \\
S_{8} &  = B_{21} + B _{22},  \\
S_{9}  &  = A_{11} - A_{21},  \\
S_{10}  &  = B_{11} + B_{12}
\end{align}
$$
This takes $\Theta(n^{2})$. After that, we recursively multiply the next:
$$
\begin{align*} P_1 &= A_{11} \cdot S_1 &&= A_{11} \cdot B_{12} - A_{11} \cdot B_{22}, \\ P_2 &= S_2 \cdot B_{22} &&= A_{11} \cdot B_{22} + A_{12} \cdot B_{22}, \\ P_3 &= S_3 \cdot B_{11} &&= A_{21} \cdot B_{11} + A_{22} \cdot B_{11}, \\ P_4 &= A_{22} \cdot S_4 &&= A_{22} \cdot B_{21} - A_{22} \cdot B_{11}, \\ P_5 &= S_5 \cdot S_6 &&= A_{11} \cdot B_{11} + A_{11} \cdot B_{22} + A_{22} \cdot B_{11} + A_{22} \cdot B_{22}, \\ P_6 &= S_7 \cdot S_8 &&= A_{12} \cdot B_{21} + A_{12} \cdot B_{22} - A_{22} \cdot B_{21} - A_{22} \cdot B_{22}, \\ P_7 &= S_9 \cdot S_{10} &&= A_{11} \cdot B_{11} + A_{11} \cdot B_{12} - A_{21} \cdot B_{11} - A_{21} \cdot B_{12}. \end{align*}
$$
Having this we can finish the multiplication by doing the next:
$C_{11} = P_{5}+ P_{4}-P_{2}+P_{6}$
$C_{12} = P_{1}+ P_{2}$
$C_{21} = P_{3} + P_{4}$
$C_{22} = P_{5} + P_{1} + -P_{3} + P_{7}$

Copying all of that which have a time of $\Theta(n^{2})$ we have the multiplied matrix. 
Therefore the running time asymptotically is minor. $T(n) = \Theta(n^{\log7})$
# References
[[4.2 Strassen's algorithm for matrix multiplication]]