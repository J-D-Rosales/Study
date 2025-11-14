created: 2025-11-03
**source:** [[C-ARCH-Design-cap 7 - MICROARCHITECTURE]]
**tags:** #book_chapter 
## Resumen 
It's important to make a performance analysis in computer.
Remember that an though analysis in the performance of a computer system is difficult, then trivially we state the components, but those aren't sure for every program in the world. FInally we come down to benchmarks
[[D- of a Benchmark]]
[[¿How a performance in a computer system is analyse?]]

In the past there wre some popular benchmarks such that Dhrystone, CoreMark, and SPEC.
Benchmarks in those are usually below 16kb, to not stress the instructions cache (pipeline).

The popular benchmark we use is the SPEC2017, that uses variety of programs we use now.
[[Equation to calculate the execution time in computer performance]]
The number of instructions depends on the processor architecture, reduce or amplify this leads to more complex analysis.
[[D-Cycles per instruction in performance analysis (CPI)]]

The number of seconds per cycle is the clock period, $T_{c}$
¿What factors affect the clock period?
The critical path (this determined the clock period)
The design of the microarchitecture.
The circuits an combinations ahead
E: carry-lookahead adder is faster than a ripple-carry adder

It is really important to choose the best design taking in consideration the factors that affect CPI and $T_{C}$.
Other factors affect also to performance and CPI and Tc, it's important to take consideration of these also. 

## Referencias a notas permanentes
