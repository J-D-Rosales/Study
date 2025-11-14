<span style="color:yellow">IDEA:</span>
WE don't need to make another FSM moore machine, we just put the op code different and since the ImmSrc is combinational, we change that, addressing that the signals will be different. For example in order to write in memory, we must, enable the MemWrite, the ADrSrc = 1, and the resultSrc to let pass to the WD3. After that we come back to the first stage, where we compute the next PC. 


<span style="color:yellow">Evidencia:</span>
![[Memory write Moore machine multicycle.png]]
![[Data flow during the memory write (MemWrite state).png]]
**Tags:**

**Referencias**: [[C-ARCH-Design-cap 7.4 MultiCycle  Processor]]

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[Analysis of the phase MemWB in a Moore Machine for a control unit in multi cycle system]]

<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

