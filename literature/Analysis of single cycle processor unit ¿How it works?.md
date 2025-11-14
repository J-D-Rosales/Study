<span style="color:yellow">IDEA:</span>
- op
- funct3
- funct7
However for Risc-V only the 5 bit of funct7 is used, so we just consider op (*Instr 6:0*), funct3(*Instr 14:12*), and funct7_5 (*Instr30*).
THe processor unit also produces internal signal branch and ALUOp used in controller. 
The standard for the operation are show in the table. 
![[Alu Decoder truth table - single cycle processor.png]]
<span style="color:yellow">Evidencia:</span>
![[Single control processor unit.png]]

**Tags:**

**Referencias**: [[D- Single cycle Microarcuitecture]]
[[C-ARCH Design- cap 7.3 SINGLE-CYCLE PROCESSOR]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[D- Control processor unit in computer architecture]]
[[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath sw instruction]]
<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>
SIngle cycle processor

<span style="color:	#87CEEB">South: What does this lead to</span>
Multicyle
