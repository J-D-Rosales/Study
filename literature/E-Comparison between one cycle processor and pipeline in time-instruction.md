![[Timing diagram for single cycle processor and pipelined.png]]As we can see, the while the fetch instruction of the second instruction is handled, the decode state in the first instruction is taken place. So, it reduces the throughput, however, since not all instruction have the same length, it means that the latency would be different. the latency is longer for pipelined processor than for the single cycle, but equal it's a great better performance of timing.

# REfernces
[[C-ARCH-Design-cap 7.5 Pipeline]]
[[D- PIpeline microarchitecture]]