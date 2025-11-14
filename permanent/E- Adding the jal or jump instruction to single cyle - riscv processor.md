![[Enhanced datapahway for jal - single cycle risc-v.png]]
![[ImmSrc encoding single cycle adding jump instruction.png]]

The changes we need to make are adding a jump signal to the unit processor, to jump whenever the instruction is putting, it means:
![[Enhaced control unit for jal.png]]
Therefore PCSource will have the value of 1, so it'll jump to the PCTarget no matter what. HOwever, we need to store the value of PC + 4, because ¿How we'll return to the caller? Therefore we add a new mux to make the result in the register file.
Recall that we do not need to add another digit in ImmSrc because it is handled with 11. 

# References
[[E-Analysis of the phases for sample program in microarchiteture - Single cycle datapath beq instruction]]