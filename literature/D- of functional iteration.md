<span style="color:yellow">IDEA:</span>
Let $f(n)$ be a function over the reals, for non negative numbers i we define
$$
f^{(i)}(n) = \begin{cases}
n & \text{if } i = 0 \\
f(f^{(i-1)}(n)) & \text{if } i > 0
\end{cases}
$$



<span style="color:yellow">Evidencia:</span>
If $f(n) = 2n$ then $f^{(i)}(n) = 2^{i}n$

**Tags:**

**Referencias**:
[[3.2 Standard notations and common functions]]
