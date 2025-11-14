Recall that the critical path for the lw instruction will be [[Critical path for lw isntructions.png]]
Therefore, we can say that the times are:
$$
Tc _ single = t pcq _ PC + tmem + max [tRFread , tdec + text + tmux ]
+ t ALU + tmem + tmux + tRFsetup
$$
However, the slower path that is going to be the most common would be:
$$
Tc _ single = t pcq _ PC + 2tmem + tRFread + t ALU + tmux + tRFsetup
$$
This is becuase max would the tRFread.

# REferences
[[¿How a performance in a computer system is analyse?]]
[[C-ARCH Design- cap 7.2 Performance Analysis]]