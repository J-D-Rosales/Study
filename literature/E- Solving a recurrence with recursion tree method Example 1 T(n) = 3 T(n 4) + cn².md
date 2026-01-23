First, we are going to represent the equation $T(n) = 3 T\left( \lfloor \frac{n}{4}  \rfloor\right) + \Theta(n^{2})$ as a recursion tree.
We are going to use sloppiness for convenience. We ignore the floor, since usually don't matter. (it's sloppiness that we can tolerate). Next, we will say that n is an exact power of 4, that is another sloppiness we can tolerate. 
![[Recursion Tree for Example 1.png]] ^8cb05e

As the equation suggest, the root represents the cost of the top of the recursion. Part(a) shows how the recursion is divided into 3 subproblems that takes 1/4 of the input. Therefore, doing the recursion into the new nodes, we have a $c(n / 4)^{2}$ cost, that's because we substitute the cost on the equation. Then, we do that again, and so on.

Since the inputs are powers of 4, then we will see that each subproblem size for a node depth $i$ is $\left( \frac{n}{4^{i}} \right)^{2}$. The base case, or when it hits is in $T(1)$,  so $\frac{n}{4^{i}} = 1$ and so $\log_{4} n = i$. And so the tree has $\log_{4} n +1$ levels. 

To determine the cost of each level of the tree, we see that we divide the problem into 3 subproblems, therefore each level has $3^{i}$ nodes. Now, the sum of the cost of each level, it's $c\left( \frac{n}{4^{i}} \right)^{2}$. Because, we go down from the root, and dividing by 4 the size of the problem. Multiplying we have $3^{i}\cdot c\left( \frac{n}{4^{i}} \right)^{2}$ and simplifying $\left( \frac{3}{16^{i}} \right)cn^{2}$.
Now at the bottom level of recursion we have that $i = \log_{4} n$. Therefore we have $3^{\log_{4} n}$ nodes, and the cost of them is constant, $T(1)n^{\log_{4} 3}$ (by logarithm property), which is $\Theta(n^{\log_{4} 3})$. 
[[E-Running time for Example 1 of recursion Tree]]
[[What happends when the cost of the root dominates the total cost of the three in analyzing the running time? ]]
Now we can use the substitution method to verify our guess.
[[E- of using substituion method to solve the recurrence for Example 1]]

## References
[[4.4 The recursion tree method for solving recurrences]]