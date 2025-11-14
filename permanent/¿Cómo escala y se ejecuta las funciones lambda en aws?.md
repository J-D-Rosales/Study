<span style="color:yellow">IDEA:</span>
Las funciones lambda en aws contienen una cantidad de memoria asignada la cual usa un porcentaje de cpu. No obstante, se tiene un tope en el escalamiento, normalmente es 10 024 Mb. De esa manera se puede monitorear y escalar funciones lambda

<span style="color:yellow">Evidencia:</span>
Cómo ejemplo imagina una función lambda de 1024mb, su tope es 10 024. Entonces la cuota de uso será:
$$
\frac{1024}{10 024} = 10 \%
$$

**Tags:**

**Referencias**:
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

[[Taco Bell Order Middleware - Enabling Delivery Orders at Massive Scale]]
Related concepts
[[Definición de observabilidad en la nube]]
<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>
Funciones lambda

<span style="color:	#87CEEB">South: What does this lead to</span>
Un sistema se puede escalar de gran manera usando funciones lambda.
