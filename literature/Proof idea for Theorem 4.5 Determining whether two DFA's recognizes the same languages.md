<span style="color:yellow">IDEA:</span>
The idea here is used the theorem [[Theorem 4.4 for decidable langauge]]
We are going to construct a language C, that recognizes A, or recognizes B but not both (in accept state). The language of C will be the **symmetric difference**.
$$
L(C) = (L(A) \cap \overline{L(B)}) \cup (\overline{L(A)} \cap L(B))
$$
Here $L(C) = \emptyset$ iff $L(A) = L(B)$.
Remember that the class of regular languages are closed under intersection and union and complement. 

<span style="color:yellow">Evidencia:</span>
![[proof idea for theorem 4.5 Determining whether two DFA's recognizes the same languages.png]]

**Tags:**

**Referencias**: [[C-TOC- ch 4.1 Decidable languages]]

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[¿What it's decidability in Turing Machines?]]
[[Theorem 4.2 of decidable langauge NFA]]
[[Proof for Theorem 4.4 for decidable langauge.png]]
[[Proof idea for Theorem 4.1 of decidable language DFA]]
[[Proof idea for Theorem 4.4 of decidable langauge NFA.png]]
<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>

x
<span style="color:	#87CEEB">South: What does this lead to</span>
Non- regular languages idea on how to proof that. 
