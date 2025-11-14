<span style="color:yellow">IDEA:</span>
To solve this problem we predict what can possibly occur and if that prediction is wrong, we flush that instructions. That time lost is called *branch missprediction penalty*

<span style="color:yellow">Evidencia:</span>
![[Abstract pipeline diagram illustrating flushing when a branch is taken.png]]

What we see here it's the prediction we assume, it means that we say beq it's not gonna branch, if we are wrong therefore we flush the other instructions as if nothing has happened.
How can we do this via microarchitecture
[[analysis of control hazard via microarchitecture with instruction beq]]


**Tags:**

**Referencias**:
[[C-ARCH-Design-cap 7.5 Pipeline]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[D- of hazard in pipeline processor]]
[[How a hazard is solve via hardware in pipeline architecture?]]
[[Pipeline processor with stalls to solve lw data hazard.png]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

