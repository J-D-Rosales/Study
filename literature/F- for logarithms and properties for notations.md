$\forall a >0, b>0, c>0$ and n, 
$$
\begin{align}
a  & = b^{\log _{b}a} \\
\log_{c}(ab)  & = \log _{c}a + \log_{c }b \\
\log_{b}a^{n}  & = n \log_{b}a \\
\log_{b} \left( \frac{1}{a} \right)    & = -\log_{b}a \\
\log_{b}a &  = \frac{1}{\log_{a} b} \\
a^{\log_{b} c}   & = c^{\log_{b} a} 
\end{align}
$$
A serie for logarithm
$\ln(1+x) = x - \frac{x^{2}}{2}  + \frac{x^{3}}{3} - \frac{x^{4}}{4} \dots$
We also have the following inequalities for $x >-1$:
$$
\frac{x}{1+x} \leq \ln(1+x) \leq x,
$$
where both inequalities holds for x =0.
A function $f(n)$ is **polylogarithmically bounded** if $f(n) = O(lg^{k}n)$
Comparing the functios as we did with 
![[F- Hows the comparison with exponential and polynomials what formula do we use to compare?#^79d830]]

just replacing n with $\log n$ and $2^{a}$ for a in the equation
$$
\lim_{ n \to \infty } \frac{\log ^{b} n}{n^{a}} = 0
$$
Therefore, we can conclude that 
$$
\log ^{b}n  = o(n^{a})
$$



# References
[[3.2 Standard notations and common functions]]