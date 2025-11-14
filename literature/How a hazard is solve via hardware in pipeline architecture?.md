<span style="color:yellow">IDEA:</span>
Via hardware we have two options, which are, connect the result that comes from the alu to the stages needed in other programs. It means, since the result is done, we just bypass to the other instruction via wire, and the other instruction can have the result before. This process is called **forwarding**
<span style="color:yellow">Evidencia:</span>
![[Abstract pipeline ilustratinf forwarding.png]]
Here the result from statge for is put it into the source of the sub operation, therefore, the instruction can be complete easyly just by making the same logic for the other instructions. For the and operation we use the first part of the RF to make The read form the other operation, since it can compute the write and read into one cycle.
**Tags:**

**Referencias**:
[[C-ARCH-Design-cap 7.5 Pipeline]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[D- PIpeline microarchitecture]]
[[Analysis of control unir for pipeline ¿How it works?]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

