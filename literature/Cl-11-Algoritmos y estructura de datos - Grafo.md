created: 2025-10-30
**source:**[[Presentación 11 (Grafos - intro).pptx.pdf]]
**tags:** #class 
## Resumen 
¿Qué es un grafo?
[[D- de un grafo]]
Las aplicaciones que se pueden hacer son encontrar la ruta más óptima, generar formas nuevas, etc.

¿Cuáles son los tipos de grafos?
[[D-Grafo dirigido]]
[[D-Grafo No dirigido]]
Decimos que está es la clasificación más general, por qué existen clasificaciones más profundas.

¿Qué es un camino?
[[D- Camino simple en un grafo]]

¿Cómo se representa un grafo no direccionado? y ¿Qué diferencia un grafo direccionado de uno que no?
[[Grafo direccionado vs no direccionado.excalidraw]]

¿Qué es un ciclo en un grafo y para qué sirve?
[[D- de ciclo en un grafo]]
Los grafos pueden tener ciclo, entonces serán cícliclos, y puede que no, entonces serán acíclicos.
E: Un árbol es un grafo acíclico, listas enlazadas con bucle (grafo cíclico).
E: ejemplos reales, jerarquía de una empresa, ejército y sus rangos.
GDF(): Grafo direccionado acíclico.

## ¿Cómo se puede encontrar cíclos en un grafo?
[[D-Arbol en estructuras de datos]]
Existe un teorema que dice el número de aristas será $|E| = |V| -1$

[[Transformar de un grafo a un árbol - Algoritmos]]

*Qué es un arbol de expansión?*
Es la mínima forma sin cíclos que puede salir de un grafo.
[[Ejemplo_transformación minumspaning tree]]

¿Qué es un bosque?

número de aristas es $|E| < |V|$
numero de arboles es $|V|-|A|$ (revisar ppt)

¿Cuáles son las propiedades de los grafos?
- Adyacencia: dos veritces conectaods por una arista
- Incidencia: una arista es indicente a sus vértices.
- Grado: Número de aristas incidentes a ún véritces.

Existe e lconcepto de sumidero , fuente o source, son los vértices en dónde no hay incidencia de arita. Y los sumideros son hay incidencia pero ninguna arista sale de él.

UN grafo simple no tiene loops ni múltiples arístas.

Grafo completo: TOdos los vértces están conectados con todos los vérticoes. SE le denomina $K_{4}$ para cuatro vértices y así sucesivamente.

¿QUé es densidad?
CUando la desnidad máicma es uno es grafo completo y la mínima cero.
SE defina una cota superior para un grafo no difirigo y dirigido.
¿QUé es un grafo bipartito?
CUanod puedes hacer dos conjuntos disjuntos que solo se contectan entre ellos a traves de aristas hablamos de un grafo bipartitio.
[[Ejemplo de grafo bipartito - template]]

TOdo árbol es un grafo, par aver ello colorea cada nivel de un color, y otro nivel de otro color.


La densidad va d eun avlor de 0 a 2.
Existe la formula para dirigiods y no dirifos
NO dirigido:
$$
D = \frac{2|E|}{|V|(|V|-1)}
$$
Grafo dirigido:
$$
D = \frac{|E|}{|V|(|V|-1)}
$$


**UN rafo es bipartito si u solamanto si no tiene ciclos de tamaño impar**

SI es grafo dirigido tiene dos grados, el de salida o de entrada.

¿Qué es un grafo ponderado?
CUando se colocan ponderaciones o pesos en las aristas.

¿Qué es un grafo conexo?
Es conexo si para cualquier par de vértices existe un camino entre ellos
En otra manera no es conexo.
Un grafo es fuertemente conexo cuando para vertices existe un cmannio entre ellos, de i-j, de j-i.

Existe un porblema intratable que es el del agente viajero. EN EL CUAL SE REPRESENTA LAS CIUDADES COMO VÉRTICES. LOS Caminos entre  ciudades como aristas ponderadas.

Cómo modelar un grafo?
Cómo una matriz. Tambien se puede hacer una estructura de daots para una arista y una clase para una arista.
- Matriz de adyacencia
- Listas de adyacencia

Para un grafo disperso no es bueno usar la matriz de adyacencia.

Para un grafo no dirgido la matriz sirmpe será simétrica.

# Minimum spaning Tree

DEbmos saber que el árbol generador mínimo será un grafo generador si concecta a todos los vértices, con la menor cantidad de pesos.

Se trata el caso en que los pesos no son negativos.

LOs algoritmos de prim y kruskal son golosos.

Se tiene una invariante que es que en cada iteración la arista siempre está consitutido en un minum spaning tree.

UNa arista es segura si se cumple la invariante en esa arista.

Para hacer el algoritmo genérico se tien un pseudocódigo:
en dódnee mientras en  conjunto de aristas pueda recibir una arista del spaning tree entonces seguimos colcoando aristas, o vertices  si ya noquedan más entonces, se acabo y encontraste el minimum spaning tree.

¿Cómo enocntrar aristas seguras?

on el algoritmos dónde se hace un corte. 
Exist eun teorema dódne se dice que G un peso d aristas y el A que está en el mimum spacning tree , y delta un corte que repeta el conjunto a}, entonces una arista en un arita seguraa.

## Referencias a notas permanentes
