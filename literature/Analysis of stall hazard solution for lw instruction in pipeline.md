<span style="color:yellow">IDEA:</span>
To stall, the instruction we just need to make a bubble. A bubble is a unused stage propagating through the pipeline. Since a stall is basically stop the pipeline it reduces performance, so it should be used just when it's necessary
<span style="color:yellow">Evidencia:</span>
![[abstract pipeline diagram illustrating stall to solve hazards.png]]
What we see here is that when you tried to apply forwarding with the lw state, it goes wrong. Therefore, we stall the state, in order to be possible to add that s7 register and don't overwrite nothing.
In order to make a stall all the rest of the states need to mantain it's previous value, so no architectural state is change. 
[[Solving the lw isntruction data hazard with stall in the microarchitecture]]

**Tags:**

**Referencias**:
[[C-ARCH-Design-cap 7.5 Pipeline]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)
[[D- of hazard in pipeline processor]]
Related concepts

<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

