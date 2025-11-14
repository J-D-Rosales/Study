<span style="color:yellow">IDEA:</span>
The logic is simple:
- Whenever a load word instruciton is handled (indicated by ResultSrcE0 = 1)
- The load's destination Register matches the RsD1 or RsD2,the source operands of the instruction in the Decode stage
we make a stall

<span style="color:yellow">Evidencia:</span>
![[Pipeline processor with stalls to solve lw data hazard.png]]

In hardware the way to do this is adding signals for each stage that is gonna needed. For example, when by the logic the stall is needed the signals are gonna be 1, meaning that the process is gonna halt for one cycle.
Also we need a asyncrhonous input clear FLushE,to make a reset when a stall is needed, therefore, the process stop and a bubble is created.
We use a signal to make assert of all signals, logic is the next:
![[locig for se stall.png]]

A warning for this is that the lwStall could accept the case for the destination of the load is x0, or when a false dependence exist, but since it's small we sacrifice that. 

**Tags:**

**Referencias**:
[[Analysis of stall hazard solution for lw instruction in pipeline]]

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
[[D- of hazard in pipeline processor]]
[[¿What are the possible hazards that can occur in a pipeline processor?]]

<span style="color:	#87CEEB">East: Opposite</span>


<span style="color:	#87CEEB">North: Theme Question</span>


<span style="color:	#87CEEB">South: What does this lead to</span>

