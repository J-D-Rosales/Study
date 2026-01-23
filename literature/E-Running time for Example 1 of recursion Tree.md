First, let's see the tree again:
![[Recursion Tree for Example 1.png]]

Now, let's see all the sum's, to know the running time.
$$
cn^{2} + \left( \frac{3}{16} \right)cn^{2} + \left( \frac{3}{16} \right)^{2} cn^{2} \dots \left( \frac{3}{16} \right)^{i} cn^{2} + \Theta(n^{\log_{4} 3})
$$
We can put this as a sum:
$$
\sum _{i = 0}^{i = \log_{4} n} \left( \frac{3}{16} \right)^{i} cn^{2} +\Theta(n^{\log_{4} 3})
$$
By the property of sums ![[F- formulas of sums and sumatorias#^51c108]]
we have
$$
\frac{\left( \frac{3}{16} \right)^{\log_{4} n +1} - 1}{\frac{3}{16}-1} cn^{2} + \Theta(n^{\log_{4} 3})
$$
However, we now that if $i = \infty$, that is minor that the actual sum. And the property ![[F- formulas of sums and sumatorias#^d5d60a]]
$$
T(n) < \sum_{i=0}^{\infty} \left( \frac{3}{16} \right)^{i}cn^{2} + \Theta(n^{\log_{4} 3}) = \frac{1}{1-\frac{3}{16}}cn^{2} + \Theta(n^{\log_{4} 3})
$$
And that's $O(n^{2})$.

## References
[[E- Solving a recurrence with recursion tree method Example 1 T(n) = 3 T(n 4) + cn²]]
