
![[Write back the data from the register file - riscv, multicycle.png]]

As you see the Data will go through a mux, this is because we want to differenciate on ALUout, and Data. And also because some instructions will have to go from alu to register. 
The signal to handle that is Result src. 
the destination register is taken from the Instr(11:7), and will go to the port of WD3, since regwrite is activated, it will allow to write onto the register file.
# References
[[E-loading data for a multicycle process with lw instruction]]
[[E-Analysis of the phases for sample program in microarchiteture - Multi cycle datapath lw instruction]]