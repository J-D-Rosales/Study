<span style="color:yellow">IDEA:</span>
NOw, we want to make the R-type instructions, in this case we can't reuse the states we've already use, therefore we need to create two more. In essence, the signals for execute are will be to let pass the rs1, and rs2, then 10 for ALUSrcA, and 00 for ALUSrcB. We need to change the ALUOp, because it's different for R-type, however that is logic for the control unit. 
After that, we need to write that data, so we put RegWrite and ResultSrc 00 to let the result pass to the input WD3. 
finally we come back to the fetch isntruction to calculate the next PC. 

<span style="color:yellow">Evidencia:</span>
![[Excuting R-type phade for moore machine, and ALUWB.png]]
![[Data flow duting the ExecuteR and ALUWB states.png]]
**Tags:**

**Referencias**: [[C-ARCH-Design-cap 7.4 MultiCycle  Processor]]

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath for R-type instructions]]

<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>
Multicycle

<span style="color:	#87CEEB">South: What does this lead to</span>
Machine morre, 
