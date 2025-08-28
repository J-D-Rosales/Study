REVISAR PIAZZI.
Los circuitos tienen como idea de implementación. No es lo mismo que la lógica booleana.
No se va a evaluar cosas del tiempo. Del tiempo solo se tiene que ver el comportamiento.
# Revisión de ecuaciones booleanas.
La especificación funcional parte de la lógica booleana. 
Va a tener inputs y outputs. 
Dentro del circuito puedo tener subcircuitos. 
Todo lo que es puerto o cable es un nodo.
Prácticamente-
Tipos de circuitos:
## Circuito combinacionales
La lógica combinacional tiene las reglas:
La salida tiene una regla de que cuando algo es un output, yo no puedo tener un valor de salida de dos. 
Un output puede ir a varios aoutputs computacionales.
En un combinacional no hay loops.
Hay standrs para trabajar con voltajes, donde el potencial de referencia viene a ser menor. 
___
Debemos tener en cuenta las definiciones. El minterm y el maxterm.
Nos conviene definir dependiendo de las funciones canónicas.
a +b = b
ab = b
Los teoremas sirven en sistemas de representación, dónde se busca abaratar los gastos.
Revisar los teoremos y resolver la lista de ejercicios. Es muy muy importante. Las demostraciones, se pueden hacer.
La Nand es la que usa menos transistores.
Toda expresión se puede colocar con Nand etc
NAND me gustas.
___
Representación de formas canónicas.
Para poder respresentar tu expresión de manera estándar.
Nosotros como diseñadores sabemos cuando una expresión va a ser verdadera. Entonces:
F(A,B,C) ) = Y
Dónde Y es el resultado qeu quiero obtener.
**Suma de productos**: (minterms): A mí me interesa definir que var = 1, y var complemento = 0. 
En pocas palabras, colocamos minterms de $m_{0}\dots m_{n}$. donde se cumple
$F(A,B,C) = Y = \sum m(0,4,5)$
Tomo los 1, donde debo colocar los complementos o no, de las variables para que se ajusten al resultado. Donde se suamn todos los 1, todos los 2 y todos lo s 3.
**producto de sumas**:
En donde ahora te va a interesar los max terms. Literalmente es buscar los 1, y ver cómo aplicarlo.
Aquí son los maxTerms. M0, Mn y pregunto cuales son los maxterms qeu dan 0.
La representación de los circuitos con las formas canónicas se llaman two levels.
