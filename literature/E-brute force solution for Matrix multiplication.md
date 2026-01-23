![[Square-Matriz-Multiply(A,B).png]]

The algorithm for multiplying matrices works as follows:
First, the lines 1-2 just start the variables. Then, the lines 3-7 computes the entries of each row i, and for each row i, the next line computes the $c_{ij}$ (sum) for each column j.
We initialize then the sum to be 0, and we loop from k to n, multiplying for each case. Finally we return C.
The running time is  $\Theta(n^{3})$ time. But there are better algorithms that reduce that time into $o(n^{3})$.
## References
[[4.2 Strassen's algorithm for matrix multiplication]]