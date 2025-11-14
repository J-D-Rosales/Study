<span style="color:yellow">IDEA:</span>
We use forwarding to solve the data hazard of Read after Write. We'll use some logic and a hazard unit to handle when we need to make the read from the second part of the instruction or the result in alu, or just the register file. [[How a hazard is solve via hardware in pipeline architecture?]]
<span style="color:yellow">Evidencia:</span>
![[Screenshot from 2025-11-09 12-31-53.png]]

Recall the next
![[Abstract pipeline ilustratinf forwarding.png]]

As you can see we need the 3 results, from the 4 cycle, from the 5 cycle and from the reigster file in the 5 cycle. That's what multiplexer does. By a signal it can choose what source to use in the alu. Now, We'll need also the RegWrite right? Becuase if we not need to write nothing, why would us matter about the forwarding? 
FInally, we use the register Rs1E, and Rs2E to compare from the other stages, it means, if the register is the source of another instructions, then we need to activate the alarm or signal to control unit, in order to use the correct operand to that instruction and solve the hazard. The simple logic is shown before:
![[Logic for forwarding in a pipeline processor hazard unit - riscv.png]]
As you see the logic is similar from the stage. And of course the logic for Rs2E would be the same, except that you need to change the name. 
Recall that Rs1E should be different to cero, because x0 is hardcode to cero, therefore, it just does not make sense to spend hardware on that.

**Tags:**

**Referencias**:
[[C-ARCH-Design-cap 7.5 Pipeline]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[How a hazard is solve via hardware in pipeline architecture?]]
[[D- of hazard in pipeline processor]]
<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>
Hazards

<span style="color:	#87CEEB">South: What does this lead to</span>
How to make with stalls?
