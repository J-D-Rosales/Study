```
always@ (posedge clk)
if(reset == 0) nq <= 0;
else q <= d;
```