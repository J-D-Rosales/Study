<span style="color:yellow">IDEA:</span>
NOw, to execute the I-type instructions such addi, or ori, we just need to put the Execute but with a differnent source, the immediate. After that is the same. 
WIth JAL, it's a little bit more complicated, we need to store the PC+4 address, and have the PCTarget. We could, in fact calculate the PCTarget, in the first steps, as in branch, however, we need to allow the result src 00 to write the address onto the PC. Also, we need to store the PC +4, in the register. Therefore, to choose the addres, we would need the PCUptade [[E-Analysis of the Moore machine for a control unit in the multi cycle system]]
finally we write the PC +4 on the register and return to the Fetch instruction.

<span style="color:yellow">Evidencia:</span>
![[Enhaced main FSM, executel and JAL states.png]]
![[Data flow during the JAL state.png]]
**Tags:**

**Referencias**:
[[C-ARCH-Design-cap 7.4 MultiCycle  Processor]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[E-Analysis of the phases for sample program in microarchiteture - Multi cycle datapath sw instruction]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

