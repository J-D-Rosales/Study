![[Screenshot from 2025-11-09 10-53-40.png]]

As we can see, the a) it's the single processor, and the  b) it's the pipeline processor. We add the registers to know where the stage was, you can make a parallel to arquitectural states for one cycle processor. 
Recall that in order to write and after that read in regiser file, we would make the write on the posedge of the clock, that way we can handle the two instructions in just one cycle. 
However, since all instruction have to advance in unison there is a problem.
The A3, it's just passed from the instructionD, therefore, since the ResultW is from the fetch state, it could write incorrectly in other register, because they are in different stages. The next figure solve that problem.
![[Corrected pipelined datapath.png]]

Now, the RdD signal pipeline through the stages, therefore there is no overwrite.
You must notice that PC has the same problem, but we'll fixed that as a hazard.
# references
[[¿How the datapath for a Pipeline is handled?-riscv]]
[[D- of an Architectural state]]
