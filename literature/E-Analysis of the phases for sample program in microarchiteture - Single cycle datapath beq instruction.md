![[Datapath enhacement for beq.png]]

We know that beq will jump to an address, then we need to calculate that, so we add an adder, to calculate the pc target. However, the ImmExt, it's not gonna do that job with the ImmSrc we already have, so we need to add another symbol to handle this kind of operation. it meand the B-type. Now, we need to calculate if the result for the two register is 0 (therefore is equal and we jump), so we have the signal Zero, that when is one, it allows the branch (the jump). 
How to choose between PcNext and PCTarget? another signal, PcSrc that is going to be handled with the signal zero, in a wat that just when Zero is 1, and Branch is 1, we allow the jump.
the rest of the signals, for example MemWrite or RegWrite are 0, because we are not doing nothing there.
