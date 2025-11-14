![[Abstract view of pipeline operation.png]]Here, we can analyse the operations of the pipeline as clock is doing in time. 
The blocks are the representative, IM for Instruction memory, RF for register file, etc. [[¿What are the stages in a pipeline microarchitecture?]]
Now, As you see, the instructions are handled as normal, just that on each cycle a instruction uses different parts of the pipeline processor. Some instructions indeed even not used some blocks, like sw does not used to write back a register file.

Also, in Register file, what we would use it's two parts to handle the writing and reading.
In the first place, we'll write , and in the second part we would write. This way, data can be
written by one instruction and read by another within a single cycle.

A problem with this kind of architecture is hazards. 
Imagine that in the second instruction we would like to use not s10, but s2, then we could not use it, because is not read it still, so it produces a problem. This will be addressed with *forwarding stalls* and *flushes*.

# references
[[C-ARCH-Design-cap 7.5 Pipeline]]
[[D- PIpeline microarchitecture]]
[[Pros and cons of pipeline - microarchitecture]]
