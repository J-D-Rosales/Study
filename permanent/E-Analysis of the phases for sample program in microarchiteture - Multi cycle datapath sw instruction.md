![[Enhaced datapath for sw instruction.png]]

To enhance this, we are gonna make the same steps as lw. The only difference is that we add the RD2 to save ot store the data. REmeber,since we are not storing nothing on a register, we don't need the A3, or WD3, we just need the entrace Adr in the Data memory, then, when the address that is A1 + immediate, is set up in the data memory we write that with the data from A2. 

# Referencias
[[C-ARCH-Design-cap 7.4 MultiCycle  Processor]]
[[E-Analysis of the phases for sample program in microarchiteture - Multi cycle datapath lw instruction]]