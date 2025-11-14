<span style="color:yellow">IDEA:</span>
To enhance this we implement two signals in order to restart the registers (arquitectural state). When the logic is asserted, the reset flush the other registers and we come back were we once where.
<span style="color:yellow">Evidencia:</span>
The logic for this is done by FLushD and FlushE
![[logic for the Control hazard for beq instructio.png]]

For the microarchitecture we'll do the next.
![[Expanded Hazard unit for handling branch control hazard.png]]

As you see, the flush D is gonna restart in case of miss prediction. Remember that at most the result for branch or not is gonna be in cycle 3, so the other two isntructions at most will arrive at the register file. Therefore, what we need to restart is The flush E and Flush D. Depeding of course on the logic. FOr example for PCsrcE, it's gonna say if we are gonna jump, if not, we'll continue as normal. 

**Tags:**

**Referencias**:
[[Analysis of solution when solving control hazard for pipeline - beq]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[D- of hazard in pipeline processor]]
<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>
x

<span style="color:	#87CEEB">South: What does this lead to</span>

x