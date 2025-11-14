![[Increment PC by 4.png]]

Now, the last step is to increment the pc. However... Why we should add an adder to do such a thing, we can use the ALU for that. Therefore we make a wire, and add a mux to choose between PC,or A. And add a mux for  choose the RD2 , the immediate or the 4 (becuase is PC + 4). The signals are gonna be named ALUSrcA, and ALUSrcB for simplicity. 
The step before we have make an mux with three entries, well the third was becayse we want the ALUResult, that is PC +4, could go to PC next, with no interference of the clk. Remeber that it is cheaper to make an extra mux, that store the process on the register. 
So, coming back to PC next, by PCWrite, that is enable we can store the new instruction.

# references
[[E-writing data for a multicycle process with lw instruction]]
[[E-Analysis of the phases for sample program in microarchiteture - Multi cycle datapath lw instruction]]