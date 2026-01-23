<span style="color:yellow">IDEA:</span>
> [!tip] Theorem 4.1 (Master Theorem)
> Let $a \geq 1$ and $b > 1$ be constants, and let $f(n)$ be a driving function that is defined and nonnegative on all sufficiently large reals. Define the recurrence $T(n)$ on $n \in \mathbb{N}$ by:
> 
> $$T(n) = aT(n/b) + f(n)$$
> 
> where $aT(n/b)$ actually means $a' T(\lfloor n/b \rfloor) + a'' T(\lceil n/b \rceil)$ for some constants $a' \geq 0$ and $a'' \geq 0$ satisfying $a = a' + a''$. 
> 
> Then the asymptotic behavior of $T(n)$ can be characterized as follows:
> 
> 1. If there exists a constant $\epsilon > 0$ such that $f(n) = O(n^{\log_b a - \epsilon})$, then:
>    $$T(n) = \Theta(n^{\log_b a})$$
> 
> 2. If there exists a constant $k \geq 0$ such that $f(n) = \Theta(n^{\log_b a} \lg^k n)$, then:
>    $$T(n) = \Theta(n^{\log_b a} \lg^{k+1} n)$$
> 
> 3. If there exists a constant $\epsilon > 0$ such that $f(n) = \Omega(n^{\log_b a + \epsilon})$, and if $f(n)$ additionally satisfies the **regularity condition** $af(n/b) \leq cf(n)$ for some constant $c < 1$ and all sufficiently large $n$, then:
>    $$T(n) = \Theta(f(n))$$

^8ab843

<span style="color:yellow">Evidencia:</span>


**Tags:**
#theorem 
**Referencias**:
[[4.5 The master method to solve recurrences]]


