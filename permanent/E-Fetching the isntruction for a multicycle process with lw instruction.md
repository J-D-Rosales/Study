Idea: 
In order to fetch the instruction we add a IRWrite nonarchitectural signal, that will tell us if it's able to read the instruction or not on every rising edge of the clock. 

evidence:
![[Fetching the instruction for a multi cycle process.png]]
![[Read one source from register file an extend second source from immediate field.png]]

After the instruction is readed, we pass the address of register one to A1 and pass the immediate to the extend. THe ImmSrc as we see [[ImmSrc encoding single cycle adding jump instruction.png]], we put the immediate source to expand that, ImmExt.  
Remember that we pass 31:7, and the extend will know how to handle that. 


# References