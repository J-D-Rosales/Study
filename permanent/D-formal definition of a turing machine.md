<span style="color:yellow">IDEA:</span>
We add the L(left) or R(Right), to make a delta function $\delta (q,a) = (r, b,L)$, which means, from state q, the tape points to a, then we go to r, replacing the a for b, and moving to L
>[!note] Turing machine
>A **turing machine** is a 7-tuple , $\left( Q,\sum, \Gamma, \delta, q_{0},q_{accept}, q_{reject} \right)$ where $Q, \Gamma, \delta$ are finite sets. 
>1. $Q$ is the set of the states
>2. $\sum$ is the input alphabet not containing the blank symbol
>3. $\Gamma$ is the tape alphabet, where blanck symbol $\in \Gamma$ and $\sum \subseteq \Gamma$,
>4. $\delta : Q \times \Gamma  \to Q \times \Gamma  \times \{ L,R \}$ is the transition function,
>5. $q_{0} \in Q$ is the start state
>6. $q_{accept} \in Q$ is the start state
>7. $q_{reject} \in Q$ is the reject state

<span style="color:yellow">Evidencia:</span>


**Tags:** #definiton 

**Referencias**:
[[How turing machines are a better representation of languages in compute theory]]
[[C-TOC- ch 3.1 Turing machines]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[Schematic of a Turing machine.png]]
<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>
x

<span style="color:	#87CEEB">South: What does this lead to</span>
Uses of a turing machine
