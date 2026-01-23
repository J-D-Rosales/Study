### Linearity
$$
\sum ^{n} _{k = 1} (ca_{k} + b_{k}) = c\sum_{k = 1} ^{n} a_{k}  +\sum ^{n}_{k = 1} b_{k}
$$
Exploit the property for the Theta notation.
$$
\sum _{k = 1}^{n}  \Theta(f(k)) = \Theta\left(  \sum_{k = 1}^{n} f(k) \right )
$$
### Arithmetic Series
$$
\sum_{k = 1} ^{n} k = \frac{n(n+1)}{2} = \Theta(n^{2})
$$
### Sums of Squares and cubes
$$
\sum_{k = 0}^{n} k^{2} = \frac{n(n+1)(2n +1)}{2}
$$
$$
\sum ^{n}_{k = 0} k^{3} = \frac{n^{2}(n+1)^{2}}{4}
$$
### Geometric Series
For real $x \not = 1$, the summation 
$$
\sum_{i=0}^{n} x^{k} = 1 + x + x^{2}+ \dots+ x^{n} 
$$
Which is equal to
$$
\sum_{i=0}^{n} x^{k} = \frac{x^{n+1}-1}{x-1}  
$$

^51c108

When the summation is infinitive and the value of $|x| < 1$ , we have
$$
\sum ^{\infty}_{k = 0} x^{k} = \frac{1}{1-x}
$$

^d5d60a

### Harmonic Series

^4cdd54

The harmonic number is
$$
H_{n} = 1 + \frac{1}{2} + \frac{1}{3} + \dots \frac{1}{n} = \sum _{k = 1} ^{n} \frac{1}{k} = \ln n + O(1)
$$
### Integrating and differentiating series.
By integrating or differentiating the formulas above, additional formulas arise. 
$$
\sum_{k = 0} ^{\infty} k x^{k} = \frac{x}{(1-x)^{2}}
$$
for $|x| <1$.
### Telescoping series
For any sequence $a_{0},a_{1},\dots a_{n}$.
$$
\sum ^{n}_{k = 1} (a_{k}- a_{k-1}) = a_{n} -a_{0}
$$
Sum telescopes when each of the terms is added in exactly once and subtracted out exactly one.
<span style="color:yellow">Example of Telescoping series</span>
$$
\sum_{k = 1}^{n-1} \frac{1}{k(k+1)}
$$
Since, we can write each term as
$$
\frac{1}{k(k+1)} = \frac{1}{k} - \frac{1}{k+1}
$$
we get
$$
\sum_{k = 1}^{n-1} \frac{1}{k(k+1)} = \sum_{k = 1}^{n-1} \left( \frac{1}{k} - \frac{1}{k+1} \right) = 1 - \frac{1}{n}
$$

## Referencias
[[E-Running time for Example 1 of recursion Tree]]