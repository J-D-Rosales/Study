![[REcursion tree for merge sort.png]]

Here we can see the next. 
From the fórmula [[E-Analysis of merge sort running time]]
FOr the first step we got T(n) that is divide that steps into two.
Now, each level has $2^{i}$ nodes and each contribute $c\left( \frac{n}{2^{i}} \right)$ steps, therefore each one contributes $cn$ steps.
Since this is a tree, the number of level is $lgn +1$ where n is the number of leaves. The +1 it's because of the root. It can be show by mathematical induction why this works. WE are assuming that the input size is a power of 2.
Now, the total cost will be:
$cn(\log n +1)$ (the number of levels times the cost of each level).
so the final time is:
$\Theta n\log n$
# References
[[E-Analysis of merge sort running time]]
[[2.3 Designing algorithms Real]]
[[¿How it's expressed the running time in divide and conquer algorithms?]][[E- Merge sort Procedure Analysis]]