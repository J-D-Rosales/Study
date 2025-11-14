
![[Dijkstra Pseudo implemenetation.png]]

I recommend you the example on excalidraw on how the algorithm works:
[[Dijkstra Algorithm.excalidraw]]

The analysis is the next:
The first line it's going to initialize the the source from the graph,It means set his value to 0, because it's cero the distance (it's trivial).
Now, we have a set S that will store the vertex, Now it's cero.
Q it's going to be a priority queue, it means it will gives has the less weight of the graph (in order to mark that vertex).
Now, we loop until the priority queue it's empty, meaning that we have no more vertex to add. 
When we add a new vertex, we relax the neighbors of them.
Finally we devolve, the distance of every vertex. d it's for distance and pi it's for parent (since it's a directed graph.)
# References
[[What is Dijkstra Algorithm?]]
[[D-Grafo dirigido]]