<span style="color:yellow">IDEA:</span>
A multitape Turing machine it's an ordinary turing machine but with multiple tapes. So, it has more heads to point on each head, and initially we start at the tape 1. 
The transition function works as follows:
$$
\delta: Q \times \Gamma^{k} \to Q \times \Gamma^{k} \times \{ L,R,S \}^{k},
$$
where k is the number of tapes. So the expression
$$
\delta (q_{i},a_{1},\dots,a_{k}) = (q_{j}b_{1},\dots,b_{k},L,R\dots,L)
$$
This means that if the machine is in state $q_{i}$ it goes to the state $q_{j}$ and reads the inputs $b_{1}$ to $b_{k}$ and directs each head to move left or right (or stay if you want).

<span style="color:yellow">Evidencia:</span>


**Tags:** #definiton 

**Referencias**:
[[C-TOC- ch 3.2 Variants of Turing Machines]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[D- Turing recognizable language]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

