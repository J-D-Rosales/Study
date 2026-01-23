<span style="color:yellow">IDEA:</span>
The intuitive idea is that no matter how small is the change for the order of $n$, when $n$ is sufficiently large n dominated on other constants or $n$ of lower order.
To formally used that, we need to take a look in the formal definition, however it is simply to said that it is true (see evidence).


<span style="color:yellow">Evidencia:</span>
Let's say we have $f(n) = an^{2} + bn +c$. a cuadratic function. Eliminating the constants and $n$, we can have $f(n) = \Theta(n^{2})$. to formally describe this, we use the formal definition as follow:
We take the constants $c_{1} = \frac{a}{4}, c_{2} = \frac{7a}{4},$ and $n_{0} = 2*max\left( \frac{|b|}{a}, \sqrt{ |c| / a } \right)$, Then you can verify that:
$0 \leq c_{1} f(n) \leq g(n) \leq c_{2}f(n)$. for all $n\geq n_{0}$. 
IN resume, for any polynomial
$$
p(n) = \sum _{i = 0}^{d} a_{i}n^{i}
$$
where $a_{i}$ are the constants. 
Since, a polynomial that is constant is $n^{0}$ we can express that as $\Theta(1)$

**Tags:**

**Referencias**:
[[3.1 Asymptotic notation]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[¿How to justify that a function is in certain notation?]]
[[¿What are the types of asymptotic functions?]]
[[D- of Theta Notation]]
[[¿What's the meaning of asymptotic notation?]]
[[¿How to use correctly asymptotic notation and abuse and don't misuse it?]]
<span style="color:	#87CEEB">East: Opposite</span>

x
<span style="color:	#87CEEB">North: Theme Question</span>
x

<span style="color:	#87CEEB">South: What does this lead to</span>
x
