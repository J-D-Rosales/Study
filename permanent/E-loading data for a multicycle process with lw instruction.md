![[Load data from memory.png]]
Having the result in ALUOut, we want to read that, so we use a mux and a signal AdrSrc to know what is going to pass through that. In this case it should pass the ALUOut, after that we read the data (remember that the clk is just for the signals), and store the value in a non-architectural register, called Data. We called the wire ReadData for understanding. 

# references
[[E-Analysis of the phases for sample program in microarchiteture - Multi cycle datapath lw instruction]]
[[E-Fetching the isntruction for a multicycle process with lw instruction]]