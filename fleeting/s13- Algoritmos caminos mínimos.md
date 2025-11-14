Al tener un grafo orientado, pondremos a cada arista un peso asociado.

EL problema de los caminos mínimos con el mismo origen, se usa Diferentes algorimos.

¿Qués es una estimación de distancias?
Para cada grafo queremos detemrinar la distancia entre dos vértices que sea mínimo.

Lo que veremos, asocian un vértide un valor, y cuando el algoritmo termino se hace una estimaciń superior. En el BFS Y DFS tenía una estimación de infinito.

Un ciclo es negativo si la suma de las aritas es negativa.

Un teorema dice que si existe un camino de $v_{i}$ a $v_{j}$ , entonces un subcamino entre ellos tambien será un camino mínimo.

Esto no se cumple si el grafo tuviera ciclos negativos.

SI exist eciclo negativo al llegar al ciclo de negativo, entonces se va por el ciclo negativo y se reduce el camino y su peso. Por lo que, el verdadero caminomínimo será diferente.

# Concepto de relajación
UNa relajación es cuendo conseguimos realiar relajar el destino, et.

EL algoritmo de lso vecinos es hacer relajación. Dónde cad vez mejoramos la estimación.

Vamos a tener que aplanar el grafo para poder aplnar el grafo dond es $O(v+ E)$ basado en DFS.
Hacer un DAG, dónde se ha ordenado topológicamente.

Ese algoritmo es DAG-Shortest.Paths.


### ALgoritmos basados en relajación.
A lo largo del algoritmo las porpiedades o invariantes siepre valoes

Lemma 24.11, La  es taimación del vértice v, siempre son mayores a la distancia. ADemás la distancia nunca amumenta. Además, la estimación queda igual al a distancia una ve que el algoritmo termine.

En dag shortest path diremso que solo se teeoms que relajar los vértices para relajar en ese orden de la ordenación topológica, se podrá hallar el camino mínimo.
