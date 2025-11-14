created: 2025-11-04
**source:**[[C-ARCH-Design-cap 7 - MICROARCHITECTURE]]
**tags:** #book_chapter 
## Resumen 
To know what this is recall the definition [[D-Multi cyle Microarcuitecture]]
Why we need a new way to handle the instructions?
[[Multi cycle architecture vs Single Cycle architecture, what are the pros and cons?]]

[[¿How a multi cycle processor is designed - riscv - microarchitecture?]]

the processor just adress the heavy instruction one at the time, it means, they keep the delay for the short instructions approximately equal. 
## 7.4.1 Multicycle Datapath 
As we begin before, fisrt we need to start by the memory and the arquitectural state
[[State elements of a RISC-V processor multicycle with unified instructions - data memory]]

Now, the signals for this part are going to change, so let's start with the fisrt instruction to be handled
[[E-Analysis of the phases for sample program in microarchiteture - Multi cycle datapath lw instruction]]
Having all of this micro architecture, we can now, handle more instructions just by adjusting some little things.
For the sw instruction:
[[E-Analysis of the phases for sample program in microarchiteture - Multi cycle datapath sw instruction]]
Now, with the R-type instructions we don't need anything extra, since we need the to registers and the register that is going to be written.

Finally we do the $beq$ instruction
[[E-Analysis of the phases for sample program in microarchiteture - Multi cycle datapath beq instruction]]
## 7.4.2 Multicycle control

the control cycle process the same as in the single cycle. [[Single control processor unit.png]]
![[Complete multicycle processor.png]]

Now, an importante part is the control unit. 
[[How the control unit for multicycle is bounded?]]
Since the control unit is a Fsm machine, we can divide it's steps.
¿How can we analyse the moore machine?
[[E-Analysis of the Moore machine for a control unit in the multi cycle system]]

Now, ¿How can we assert more instructions using the same FSM moore machine?
We can! Actually, it's just add another state.
[[Analysis of the instruction sw, based on lw in moore machine for multicycle]]

[[Analysis of the instruction R-type based on the moore machine for multicyle]]

FInally we have the beq instruction

[[Analysis of the instruction beq, based on moore machine for multicycle]]

¿How can we expand that to more instruction?
INstructions like addi, or Jal, does not need more hardware, but just change or add the states. 
[[Analysis of the instruction I-type and jal  based on the moore machine for multicyle]]

The final moore machine will look like:
![[Complete multicycle control FSM.png]]

## 7.4.4 Performance Analysis
Now, let's focus on how to make a good performance analysis
[[¿How we do a performance analysis in a multicycle processor?]]
We'll assume that register file is faster than memory and that writing memory is faster than reading memory.
Then we we'll have two ways

[[¿What it's the critical path in a multicycle processor?]]

FInally the equation will be

[[Equation for performance analysis in a multicycle processor]]

When we solver a problem concerning to this , ( see the book ) 

[[¿The multicycle is always faster than One cycle processor?]]
The Multicycle is gonna be cheaper that single cycle, most of the time, however, depends on the technology and the parts you are using for implement this.
## Referencias a notas permanentes
