created: 2025-11-03
**source:**[[C-ARCH-Design-cap 7 - MICROARCHITECTURE]]
**tags:** #book_chapter 
## Resumen 
[[D- Single cycle Microarcuitecture]]
As it says we'll do in one cycle. Therefore, the signals by the control determine what instructions are gonna be doing at a given time. 

## 7.1.3 Sample program
We'll use an example program to explain how the instruction is done. We skip the explanation because it was done in chapter 6.
![[Sample program exercising different types of instructions -RISC-V - architecture.png]]
We'll assume that initially register x5 has the value of 6 and x9 contains 0x2004. Memory location 0x200 contains the value of 10
## 7.3.2 Single - Cycle datapath
In base on our sample program we'll do an example on how the microarchitecture is working. 
Remember that the PC counter will address or contain that, that's gonna be executed
[[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath lw instruction]]
that's was for the lw isntruction, now let's analice the other instruction with the knowing of the lw. 
[[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath sw instruction]]
Recall that in this example the PC is 0x1004, and after the instruction will go to 0x1008. 
[[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath for R-type instructions]]
"
In our example, the PC is 0x1008. Thus, the instruction memory
reads out the or instruction 0x0062E233. The register file reads source
operands 6 from x5 and 10 from x6. ALUControl is 011, so the ALU
computes 6 | 10 = 01102 | 10102 = 11102 = 14. The result is written
back to x4. Meanwhile, the PC is incremented to 0x100C
""
Finally we analyse the beq instruction
[[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath beq instruction]]
Then the complete figure or structure is:
[[Single cycle processor - control- datapath.excalidraw]]

## 7.3.3 Single single Control
To understand this we need to understand What a control processor unit is
[[D- Control processor unit in computer architecture]]
[[Analysis of single cycle processor unit ¿How it works?]]

To practice your ability we left the and excersive, you need to say the signals and the path it'll follows.
[[E-single cycle processor operation and]]
## 7.3.4 More instructions
In order to add new instructions, sometimes we just need to adjust the numbers, other times we need to add hardware. 
E: The addi instructions does not need to add anything, just add a new row to the main decoder, with opcode, needed.
However, for exampĺe with the jal, or jump we need to make analysis
[[E- Adding the jal or jump instruction to single cyle - riscv processor]]

## 7.3.5 Performance analysis
Remember the section and the formulas from [[¿How a performance in a computer system is analyse?]]
[[C-ARCH Design- cap 7.2 Performance Analysis]]
From the equation [[Equation to calculate the execution time in computer performance]]
The CPI it's gonna be 1, because the cycle por instruction is just one in a single cycle processor.
Now, the time for an instruction to be made it's done by the critical path.
-> here it should be the definition for a critical path
[[E-Critical path for lw instruction single cycle riscv]]
So, when we know the critical path we can make a performance analysis.
[[E- Performance analysis for lw instruction single cycle riscv]]
There is not gonna be exact number and it depends on the tecnology used by your procesador.
## Referencias a notas permanentes
