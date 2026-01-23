<span style="color:yellow">IDEA:</span>
The idea is not to go through all possible combinations of $w$ but see the next:
We know that is a start variable gets a variable that cannot be replaced by a terminal, then it would be empty. Therefore what we'll do is mark all terminals, and see if other variables can be replaces by it, if so, then we mark the variable, and do that for the rest. Remember, that if it is marked then it could be marked and replaced by a terminal. Finish when there is no more to be marked and of course if the start variable is not marked, the reject, if not accept.



<span style="color:yellow">Evidencia:</span>
![[TM for proof the testiness problem for E_CFG.png]]

**Tags:** #proof_idea 

**Referencias**:
[[C-TOC- ch 4.1 Decidable languages]]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)
[[Theorem 4.8 Emptiness testing problem for CFG]]
[[Theorem 4.7 Decidability for CFG languages]]
[[E-Configuration that yields other, rightwar and forward]]
Related concepts

<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

