We are going to do the analysis based on the next pseudo algorithm:
![[Dijkstra Pseudo implemenetation.png]]

Realizando el análisis algorítmico podemos ver lo siguiente:
Hasta la linea 2 todo es $O(1)$ ya que solo son inicializaciones.
La llamada 3 es O(v) Porqué se hace una inserción V veces.
La línea 4 se hace $O(V)$ veces, dónde se realiza la llamada a extract-min.
Después para cada vértice se relaja entonces se hace $(O(E))$ llamadas.
 De aquí el tiempo total es:

Total time: $O(V)$ insert  + $O(V)$ extract min + $O(E)$ Decrease Key.

Ahora dependiendo de la implementación  puede variar, en ese sentido, se puede implementar con un vector, un heap o un Fibonacci heap.

- Vector = $O(V^{2} + E)$
- FIla de prioridad = $O((V+E)lgV$
- Heap de fibonacci = $O(V \log V  + E)$
# References
[[Cl-13- Dijkstra Algorithm]]
[[What is Dijkstra Algorithm?]]