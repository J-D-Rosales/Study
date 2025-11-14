![[Write data to memory with the sw instruction.png]]

The difference with the load word instruction are that we use the extend another way and the immediate is cut it in parts. it means it is stored in $Instr_{31:25,11:7}$ . (The extend will receive all the bits, it means 31:7). Now, a control signal ImmSrc decides which source use as an immediate (we have seen the way it should be handled is different). If it is 1, it's sw, and if 0 is lw. 
After the path we have seen in the analysis of lw [[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath lw instruction]]. We add the A2 register, that goes to register file which reads the data from the register onto RD2. Since we want to Write the data, we put this result as an input on the Data Memory. A signal *MemWrite* will tell us if it's gonna write, if it's 1 it's gonna write if it's 0, not. 

