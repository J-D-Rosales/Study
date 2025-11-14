![[Add base address to offset.png]]

want we want to do know is sum the base address with offset, so we use the ALUControl, with the code 000 in order to do so. After that we save the value of ALUResult, and on the other rising edge of the clock, we spill ALUOut. 
[[E-loading data for a multicycle process with lw instruction]]