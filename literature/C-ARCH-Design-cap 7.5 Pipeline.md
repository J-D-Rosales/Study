created: 2025-11-05
**source:** [[C-ARCH-Design-cap 7 - MICROARCHITECTURE]]
**tags:** #book_chapter 
## Resumen 
The idea of the pipeline is to make a better performance, it means improve the throughput and latency. [[D- PIpeline microarchitecture]]
[[D- of latency]]
[[D-of the throughput]]
[[¿What's the difference between latency and throughput]]
The throughput is more important that latency, because computers execute an exorbitant amount of instructions, rather than time it takes that instruction.
Pipeline processor.
[[Pros and cons of pipeline - microarchitecture]]
Now, let's see how's inside.
[[¿What are the stages in a pipeline microarchitecture?]]

NOw, n pipeline processor, the stages are pick the time by the slowest instructions, it menas the memory access in fetch or memory stage-
[[E-Comparison between one cycle processor and pipeline in time-instruction]]
Now, what we want it's to understand the abstract idea. So, we give a brief analysis in comparison with an abstract idea of the pipelined processor.
[[Abstract idea of a Pipeline processor a view of its operations - riscv - microarchitecture ]]
# 7.5.1 Pipeline Datapath
Here, we'll chop the stages into ive from the single cycle processor.
[[¿How the datapath for a Pipeline is handled?-riscv]]

# 7.5.2 Pipeline control
The control is the same as single processor [[Single control processor unit.png]]
Therefore, the signals are the same. [[Analysis of single cycle processor unit ¿How it works?]]
The change are that we need to spread that across the stages, it means we need to add registers for the control unit.
[[Analysis of control unir for pipeline ¿How it works?]]
# 7.5.3 Hazards
In pipeline when one instruction is dependent on another, a hazard occurs. 
[[D- of hazard in pipeline processor]]
[[¿What are the possible hazards that can occur in a pipeline processor?]]
There are two ways to solve the hazard: The software way and the hardware way.
[[How a hazard is solve via software in pipeline architecture?]]
[[How a hazard is solve via hardware in pipeline architecture?]]
Now, we can classified harzard the next way, into control and into data.
[[¿What is the classification for hazards?]]

For the implementation we'll have a hazard unit to make a control for all the hazards.
[[Analysis of the data hazard pipeline processor to solve via forwarding]]
However ,that's not the only way to solve that, and of course there are instructions that you cannot solve with that
### Solving Data hazards with Stalls.
Instructions such that lw, cannot be solved just using forwarding, that's why we use stalls to get rid of ti.
We say that lw has a two-cycle latency because a dependent instruction cannot use its
result until two cycles later.
[[Analysis of stall hazard solution for lw instruction in pipeline]]
### Solving control hazards
FInally we need to solve the control hazards, for example when branch or jump is needed. The most usual beq.
[[¿What is the classification for hazards?]]
If we go by our strategy to stall, we'll have several problems, the first is the performance analysis will be slower, and that it'll consume more time. Therefore, what we do is a prediction, if we predict right continue, if not, we can flush what we were doing.
[[Analysis of solution when solving control hazard for pipeline - beq]]
Now, let's see the full pipeline processor with the hazard handling. 
![[Pipelina processor with full hazard handling.png]]

The full logic for the hazard unit will be:
![[full logic for data hazard handling.png]]

## 7.5.4 Performance Analysis
We call the same analysis as for the other microarchitecure.
[[Equation for performance analysis in a multicycle processor]]

First, the CPI [[D-Cycles per instruction in performance analysis (CPI)]] would be ideally 1, however, the bubbles, and the isntruction would make this a little more. 



## Referencias a notas permanentes
