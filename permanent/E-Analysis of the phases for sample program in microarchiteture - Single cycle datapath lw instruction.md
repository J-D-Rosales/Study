We endure you to see the program located:
![[Sample program exercising different types of instructions -RISC-V - architecture.png]]

The order of the instructions are analyzed as follow, and the graph is shown in there:
[[Steps to perform an execution for a single cycle datapath - microarchitecture]]
1. At the best beginning we fetch the instruction of 32 bits labeled Instr, by instruction memory. Also we put the PC on 0x1000 (assume), then we start the execution.
2. Here, depeding on the instrucción and the decode of the isntraction we'll have different results. On this case we'll do *lw* instruction, but the rest is analogous . The address of the source operand is stored in **rs1**  instr(19:15). Then, it reads the register value onto A1. (9). 
3. the lw also requires an offset. the offset is stored in the 12 bits of inmidiate, since this is an I-type instruction, we then extend this value in order to be able to make the sum on the alu, we extend that with the sign it has. In the figure the -4 is extended from 12 bits to 32 bits. 
4. Now the instruction will add that immediate to the base address, so address we want -> offset + base addres, that operation  will be handled by the alu. and the address it's going to be read by the memory will be in ALUResult. On our case 0x200. The operands are SrcA and SrcB. Remember that the ALUControl specifies the operation that's goint to be done, E: 000 is sum.
5. After that, we go to data memory that recieves the result from our previous process as an input(address) to read, The data is read from the data memory on to ReadData bus and then written back to the register file (remember that we want to load a word, therefore we need to grab on some value).
6. We want to write back the value on some register (this case x6). then A3 will store the address of the register we want to write, and WD3, will have the value to write, in the instruction it's gonna be the register destination (rd). Remember that just on the rising edge of the clock the value will be written if the signal allows to it. 
7. Finally we increment the value of PC to be PC+4, we do it by 4 because RISC-V is byte addressable. We'll not use the alu for this, because is heavy, instead we have an adder. This complete the datapath for the lw isntruction+
