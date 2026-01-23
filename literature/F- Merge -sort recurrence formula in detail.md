$$
T(n) = \begin{cases}
\Theta(1)  & \text{if n = 1} \\
T(\lceil n/ 2  \rceil )  + T(\lfloor n / 2 \rfloor ) + \Theta(n) & \text{if n > 1}
\end{cases}
$$

## References
[[What are the technicalities in recurrences we often ignore?]]