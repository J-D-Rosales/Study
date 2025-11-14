<span style="color:yellow">IDEA:</span>
The arquitecture of Taco bell is robust and well defined:
![[Arquitectura de taco bell aws.png]]

The way it goes is by events:
1. A costumer wants an order and send it trough his phone
2. The order goes to the delivery aggregation and is send it to API gateway
3. The Api gateway (it's the application in amplify sometimes) go to the event bridge
4. The event bridge analize the event and send it to step function
5. The step function and lambda make an output depending on the input
6. The order is send it again to the delivery agregation

<span style="color:yellow">Evidencia:</span>


**Tags:** #examples

**Referencias**:
[[literature/Taco Bell Order Middleware - Enabling Delivery Orders at Massive Scale|Taco Bell Order Middleware - Enabling Delivery Orders at Massive Scale]]

## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
- Arquitetura serverless
- Aws services
<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>
¿Why is Taco Bell arquitecture well defined?
Taco Bell arquitectures
<span style="color:	#87CEEB">South: What does this lead to</span>
Arqtuiectura serverless.
