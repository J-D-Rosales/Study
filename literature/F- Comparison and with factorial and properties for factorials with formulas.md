
[[D- of Factorial]]
[[D- Stirling's approximation]]

A weak upper bound of the factorial is
$$
n! = \leq n^{n}
$$
we can have better approximations, and the notations are bounded:
$$
\begin{align}
n!  &  = o(n^{n}) \\
n!  &  = \omega (2^{n}) \\
\log(n!)  & = \Theta(n \log n) 
\end{align}
$$

The next equation comes from the last equation and striling's approximation

$$
n! = \sqrt{ 2\pi n } \left( \frac{n}{e} \right)^{n} e^{\alpha n}
$$
where
$$
\frac{1}{12n +1} < \alpha_{n} < \frac{1}{12n}
$$
# References
[[3.2 Standard notations and common functions]]