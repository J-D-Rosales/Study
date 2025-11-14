
The process for an instruction is generally, fetch, decode, Memadrres, Memread, MemWB (Memory write back)
# Fetching the instruction

[[E-Fetching the isntruction for a multicycle process with lw instruction]]
When fetching the isntruction you could say why we don't hold the value on a non-architectural register?  However, the value will not change while executing the instruction, it means, we'll not have the necessity to store the value, and therefore we'll save space and memory and one component. 
[[E-Addressing and sum the address for a multicycle process with lw instruction]]
[[E-loading data for a multicycle process with lw instruction]]
Finally we want to write the data readed into a register, however, be careful, because other isntructions will want to write data from the ALU to the register, therefore we use a mux, to forget about that probelma
[[E-writing data for a multicycle process with lw instruction]]
For the last step we actualize the PCounter to address the other instruction.
[[E-Actualizing the PCounter for a multicycle process with lw instruction]]
# Referencias
[[C-ARCH-Design-cap 7.4 MultiCycle  Processor]]