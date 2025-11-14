<span style="color:yellow">IDEA:</span>
The idea is to phrase the intuition in a way we can conclude satisfactorily that we can build a turing machine.
$$
D = \{ p|p \text{ is a polynomial with an integer root} \}
$$
However, to solve this we first concentrate on:
$$
D = \{ p|p \text{ is a polynomial over x with an integer root} \}
$$
The Turing machine that recognizes it goes as folloES:
M1 =
- On input p : where p is a polynomial over the variable x.
- Evaluate p with x succesively to the values $0,1-1,2,-2\dots$. If at any point the polynomial evaluates 0, then accept.
For multivariable is similar.
Now, we need to convert that lenguage in a decider. We can do so knowing that the roots for a polynomial with a single vairable lies between:
$$
\pm k \frac{c_{max}}{c_{1}}
$$
where k is the number of terms in the polynomial, $c_{max}$ is the coefficient with the largest absolute value and c1 is the coefficient of the highest order term.
Remember, no root encounter, rejects.

<span style="color:yellow">Evidencia:</span>


**Tags:**

**Referencias**:
[[C-TOC- ch 3.3 Definition of an Algorithm]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[Intution for Hilbert's problem on algorithms]]
[[C-TOC- ch 3.3 Definition of an Algorithm]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

