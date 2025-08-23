Repaso de los objetos para entenderlos. Ver la imagen
El set Q sería: $\{ q_{1},q_{2},q_{3} \}$
$\Sigma = \{ 0,1 \}$
$q_{0}: q_{1}$
$F; \{ q_{2} \}$
Esta parte será más desafiante de entender.
El último símbolo. 
El estado de transición q1 lee el símbolo s, llega a $q_{j}$.
___
En el concepto de resolver problemas, decimos que es tener un input y dar un output.
En una primera versión, se queria restringir el dominio de los inputs. Dependiendo de lo que sucedo, el AFD, nos va  a decir si nos interesa o no.
Vamos a procesar símbolo a símbolo.
Cada símbolo que tenemos será procesado en un estado. Por ejemplo 011. tendrá tres estados, q1,q2,q3.
En una cadena, sabremos cuál será el final del estado del input que colocaremos.
La idea del AFD, es que no haya ambigüedad.
$\epsilon$ que es no cadena, no significa que no reciba nada. Pero como no hay nada, se queda en el estado incial.
EN principio toda cadena puede ser leído por un AFD.
El AFD aceptará la cadena si el último estado pertenece al F. Esto porque la máquina solo acepta el estado q2.
El estado de aceptación se representa con un círculeta extra.
F puede ser vacio.
Es así que no necesariamente los estados tienen que estar conectados, mientras cumpla la definición.
Surgió la frase:
"el conjunto de cadenas aceptadas por M(un AFD)" -> Lenguaje de Zipzep.
El M es machine. Pero se puede usar A.
El conjunto de cadenas, lo llamremos L de lenguaje, se le llama lenguaje reconocido. por A.
Todo AFD va a reconocer exactamente a un lenguaje L. Otra notación es L(A) -> a cada AFD le queremos asociar un lenguaje asociado.
La notación que represente todas las cadenas son $\Sigma^{*}$
Un lenguaje puede ser reconocido por más de un AFD.
Otra forma de definir el lenguaje reconocido por M, es $L = \{  w|M \text{ accepts } w \}$
Tambien escribimos $L = L(M)$.
Todo en el AFD ya está definido, no puede reconocer más de un lenguaje.
Las cadenas siempre entran de izquierda a derecha
___
*otra perspectiva*.
"Un lenguaje L es reconocido por algún AFD". = "L es regular"
Un lenguaje L es regular si puedes construir un AFD que lo reconozca.
Dónde un AFD son aquellos que son reconocidos por alguien y aquellos que no.