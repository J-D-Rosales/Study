Un estado es un snapshop, como una imagen, en ese instante de tiempo.
Un estado se preserva, tiene que guardarse en un circuito secuencial. 
Al establecer una FCM,
debemos establecer lo que es un concenso, un semáforo, Pensar en la solución más general posible.
En la parte de implementación de FCM, no pensar en casos muy difíciles.
Imagínese un semáforo, 
El concenso inicia con colcoarlo como autómatas. En cada estado colocamos las luces, dónde si arrancamos con rojo, pasa directo a verde. 
Es así, que colocamos en verde primero para tener una secuencia.
Ya sabemos como representar un FDM, ahora vamos a implementarlo.
___
Tenemos una señal que es clock que es periódica. 
Existe una definición, que el snapshot debe quedarse estable durante un tiempo de T (periodo), la información en todo ese estado no se debe alterar.
Tengo que implementar con una buena definición del FDM.
Todos los estados asociados deben ser finitos.
NO podemos tener infinitos cables de cobre.
Cualquier transición entre estados están bien definidas.
- Determinismo en pocas palabras.
___
La memoria no es un elemento secundario de computación. La memoria es tan importante como lo que procesa. 
___
**Lógica de estado**: Debemos tener una lógica, porque puede dpender de un grupo de entradas.
___
Tengo noción del estado previo para saber el estado siguiente. 
El estado inicial no está integrado como 0, depende de como es la implementación.
EL reset y el clock es implícito. 
___
EL FCM necesita estos tres bloques:
Sequential circuits
Combinational circuits
Outputs
___
Esto no es un porgrama, tiene 3 bloques modulares diferentes.
No intentar reducir un FCM, cuando no es necesario.
El input debe existir en ese delta de T, es un pulso. TIene que ser mayor la presencia del input al pulso. 
___
TEnemos MUR machine y Mealy machine.
DEbemos indentificar cuales son los inputs y sus outputs.
___
# FSM Example.
Una máquina detectores de bits.
Las tablas, se hacen con next state logic.
La codificación que se aplica se llama $\log_{2}(N)$, full-binary encoder.
Es techo, y se coloca en secuencia. Existen otros tipos de encoding.
