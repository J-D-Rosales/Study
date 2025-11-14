created: 2025-11-02
**source:**[[C-ARCH-Design-cap 7 - MICROARCHITECTURE]]
**tags:** #book_chapter 
## Resumen 
### 7.1.1 Architectural State and Instruction Set
To understand architecture you'll need to understand the topics we've discussed.
[[D- of a microarchitecture of computers]]
The difference between both, architecture and microarchitecture is that while architecture is based on the high level programs, the michroartuitecture analize how an architecture is designed.

The most common ways of micrarchitecture is single cycle, multicycle, and pipeline.
[[D- of an Architectural state]]
RIsc-v has a set of instructions, for 32 bits it's 32 registers and a stack pointer.
We'll use the minimum istructions to write useful programs
[[¿What are the minimum instructions to write useful programs]]

## 7.1.2 Design Process
We can divide the microarchitecture on two parts, the control and the datapath. 
[[Single cycle processor - control- datapath.excalidraw]]
the datapath uses the control unit to make operations and we add combiantional logic to connect the different pieces of elements we have in the microarchitecture.

the memory is split into two, register file and main memory.
[[¿Why the memory in a microarchitecture is divided into two?]]

To start the cycle we need to put a reset to initialize the PC counter, it's not mandatory to be 0, you can choose. 
¿How the pieces works?
![[State elements of a RISC-V processor.png]]
[[Anlysis of a PC counter in Michroarquitecture]]
[[Analysis of a Instruction memory in Microarchitecture]]
[[Analysis of a Register file in Microarchitecture]]
[[Analysis of a Data memory in microarchitecture]]

All of the components are combinational, just the signals are activated or changed in the rising edge of clock.
### 7.1.3 Michroarquitectures
The division is as we mentioned in tree.
[[D- Single cycle Microarcuitecture]]
[[D-Multi cyle Microarcuitecture]]
[[D- PIpeline microarchitecture]]
## Referencias a notas permanentes
