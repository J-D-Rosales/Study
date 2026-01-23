<span style="color:yellow">IDEA:</span>
**First case**: When the driving function $f(n) \gg n^{\log_{b}a}$ for infinitives values of n, and $n^{\log_{b} a}\gg f(n)$ for another infinitive values of n, then the master theorem does not apply.  
 **Second case**: There is a gap between the case 1 and the case 2, because imagine $f(n) = o(n^{\log_{b} a})$, and that the watershed function does not grow polynomially faster than the driving function. 
 **Third case** : There is a gap between the case 2 and the case 3, because when $f(n) = \omega(n^{\log_{b}a})$ and the driving function grows polylogarithmically faster than the watershed function, but it does not grow polynomially faster. 

<span style="color:yellow">Evidencia:</span>
For the first case, just recall that the exponent can be varied in some ways, for example $T(n) = 2T\left( \frac{n}{2} \right) + n^{1 +\sin n}$. For some values is $n^{2}$, then we can apply the case 1 of master theorem, however, for some values is $n$ , then it's equal and we use case 2, but wait, for some values is just $\Theta(1)$ and we'll use case 3. Since, it's impossible, we cannot use the master theorem.
For the second case, take this recursion $T(n) = 2T\left( \frac{n}{2} \right) + \frac{n}{\log n}$
Now, we now that the watershed function is $n$ , and $f(n)$ is smaller but just by a logarithmic factor, it cannot trigger case 1, because: $\frac{n}{\log n} = O(n^{1-e})$, however, there is not possible way that because the exponent it's always gonna be faster than the logarithm, such $\epsilon$ it's impossible. Therefore, the master theorem does not apply.
For the third case, take a look at this recursion $T(n) = 2T\left( \frac{n}{2} \right) + n\log \log n$. (remember, that case 2, applies for a logarithm, so we use log of log). here the watershed function is $n$, and $f(n)$ the driving function grow faster but just for a polylogarithmically value, but not by a polynomially factor. Therefore, $n\log \log n = \Omega(n^{1+e})$, but it does not exist, because the exponent is faster enough to bet the logarithm.  So as you can see, it does not fit in case 2, because is heavier, but also does not fit in case 3, because isn't heavier enough.

**Tags:** #Question_to_practice 

**Referencias**:
[[4.5 The master method to solve recurrences]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[¿When to use each case and when do we know to use the master theorem?]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

