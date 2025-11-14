<span style="color:yellow">IDEA:</span>
The thing we need to make is to compare the registers and if they are equal go to the target addres. Now, since the ALU is not being used during the decode, we use that to make the sum between the immediate and the PC , therefore we get the Target addres. Once we have that, we compare with the substraction (Aluop  = 01) if they are equal (signal zero activated), if they are, the PCwirte is activated, and we continue to the target addres, storing that onto PC. Otherwise it continues with the instructionfor PC + 4. 


<span style="color:yellow">Evidencia:</span>
![[Enhancing decode state,with branh target address calculation an BEQ state.png]]
![[Data flow during Decoda and BEQ states, for multicycle moore mahcines.png]]
**Tags:**

**Referencias**:
[[C-ARCH-Design-cap 7.4 MultiCycle  Processor]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[Analysis of the instruction sw, based on lw in moore machine for multicycle]]
[[Excuting R-type phade for moore machine, and ALUWB.png]]
<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

