<span style="color:yellow">IDEA:</span>
Is the set of functions 
$o(g(n)) = \{ f(n): \text{ for any positive constant c >0, there exists a constant } n_{0} > 0\text{ such that } 0\leq f(n)< cg(n) \text{ for all } n\geq n_{0} \}$
or
$$
\lim_{ n \to \infty } \frac{f(n)}{g(n)} = 0
$$
<span style="color:yellow">Evidencia:</span>
It means, that the functions described for $o(g(n))$ are not **asymptotically tight**. It means $2n^{2} \not = o(g(n^{2}))$ but $2n = o(g(n^{2}))$. The main difference between $O()$ notation of function is that it holds for all constant not just by some constant. It means $f(n)$ became relatively insignificant compared with $cg(n)$.
That is if we take the limit of $f(n)$ to $g(n)$ the limit is bound up to zero.

**Tags:**
#definiton 
**Referencias**:
[[3.1 Asymptotic notation]]

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[E- Analyzing equations with notations]]
[[¿How can we express notation functions in different ways?]]
[[¿What it means the running time of an algorithm if it's in Omega notation?]]
[[Theorem 3.1 for theta notation]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

