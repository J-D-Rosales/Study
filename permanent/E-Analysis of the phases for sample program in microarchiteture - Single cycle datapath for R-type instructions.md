![[Datapath enhancements for R-typw instructio.png]]
What's the difference from the other datapath we've seev?
To allow the R-type instructions such as add, sub, and, or, and slt we need to use the alu, and the two register. Therefore we put a mux to know through a signal what to choose (if is 0 it choose the value from register, if it's 1 it choose the immediate).
Recall that the ALUControl has 000 -> sum, 001 -> substraction, 010 -> and, 011 -> OR , 101-> slt
Now, we want to write the data onto register file, however, Result will need to choose between S-Instructions and R-type instructions. Therefore, we use a mux, and connect the ALUResult to the 0 in the mux, the signal that allows that will be ResultSrc. Don't worry about sw instruction and the possibility of write in a register, because RegWrite is going to solve that problem-


# References
[[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath sw instruction]]
[[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath lw instruction]]