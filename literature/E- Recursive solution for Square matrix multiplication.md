![[Square-Matrix-Multiply-Recursive(A,B).png]]

We'll partitioning the matrix A,B,C as follows: four submatrix of $n /2$ size.
$$
\begin{pmatrix}
C_{11}  &  C_{12} \\
C_{21}  &  C_{22}
\end{pmatrix} =

\begin{pmatrix}
A_{11}  & A_{12} \\
A_{21}  & A_{22}
\end{pmatrix}
\cdot \begin{pmatrix}
B_{11}  & B_{12} \\
B_{21} & B_{22} 
\end{pmatrix}
$$
So, to multiply we'll have:
$$
\begin{align}
C_{11} = A_{11} \cdot B_{11} + A_{12} \cdot B_{21}, \\
C_{21} = A_{11} \cdot B_{12} + A_{12} \cdot B_{22},  \\
C_{12} = A_{21} \cdot B_{11} + A_{22} \cdot B_{21},  \\
C_{22} = A_{21} \cdot B_{12} + A_{22} \cdot B_{22}, \\
\end{align}
$$
The pseudo code works as follows:
In line 3 is the base case, that is when we just have one element multiplied by one element. 
If  $n>1$ then we do the partition. As the equation we have seen before, we just state the sume of the multiplication between both submatrices.
An important technical implementation is in the line 5, in which the partition of the matrix, could be doing by copying to a new matrix, and then sending to the function again. However, the great disadvantage of this is that it takes $\Theta(n^{2})$ to copy the elements. Therefore, it's inefficient in terms of reducing the running time. Another way of doing this is by using indices, that works better, and therefore for partition the matrix (that is still constant) will take $\Theta(1)$ time. Asymptotically makes no difference, but in practical it reduces the crossing point.
Now let's do the running time analysis, since it's not so obvious.
[[E- Analysis of running time for recursive algorithm for multiply square matrix]]

# References
[[4.2 Strassen's algorithm for matrix multiplication]]