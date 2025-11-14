![[Enhace datapath for beq target address calculation - Multi cycle.png]]

In this case, we just need to enhace the two register , and see if their sum is 0.
SInce, in the first step we calculate PC + 4, we need a way to remember the old PC, who's gonna be added an immediate to branch. Therefore, we add a nonarchitectural register, to hold the value of OldPc. Then, in the second step it'll perform the sum. 
NOw, depending on the zero output and the signal branch the PCWrite, will allow to write the PCtarget, or just follow the PC + 4.
Remeber the result is store in ALUOut register. Then, the assertion for zero and branch is done and see if it goes to PC target or PC + 4. The AdrSrc will not let pass the PC +4, so all good. 