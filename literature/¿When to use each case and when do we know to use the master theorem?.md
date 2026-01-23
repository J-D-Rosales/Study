<span style="color:yellow">IDEA:</span>
Let's call the master theorem:
![[Theorem 4.1 (Master theorem)#^8ab843]]
Intuitively the first case is done when the **watershed function** that is $n^{\log_{b} a}$ is greater than the **driving function** ($f(n)$). That difference needs to be notable, in other words grow asymptotically faster than the watershed function, even when the difference is insignificant.
The third case is a mirror for the first case with technicalities, here the driving function needs to grow faster than the watershed function, and the regularity condition it's most of the time accomplished.
The second case arise with the premise of equal growth, just different form the $lg^{k}n$ factor. Most of the time, $k = 0$, so we don't need to worry about that.

<span style="color:yellow">Evidencia:</span>
For case like these 
$T(n) = 4 T\left( \frac{n}{2} \right) + n^{1.99}$ (rarely algorithmically)
the driving function is $n^{1.99}$ and the watershed function is $n^{2}$. It differs by $\epsilon = 0.01$, but that difference is enough to state that is case one, there should be difference, does not matter the size but the consistent growth.

**Tags:**

**Referencias**:
[[4.5 The master method to solve recurrences]]

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[What kind of technicality sometimes we ignore in the master theorem?]]
[[What kind of problem the master method solves for recurrences?]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

