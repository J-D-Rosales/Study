¿Cuándo un algoritmo es óptimo?
Cuando su complejidad coimcide con una cota inferior de P.
¿Qué es reducción?
Es un método que puede ser usado para muchas cosas, pero en este caso será para transformar un problema, obtener un cota superiro.
¿Qué es una reducción de turing?
La reducción de Turing es reducir el problema A al problema B. Eso quiere decir que SI resolvemos B, agregamos ciertos pasos y resolvemos A.
La reducción se representa por $\tau$.
¿Cuándo utilizar reducciones?
1- Cuando puedes resolver B y con B debemos encontrar la cota superior para el problema A.
2- Cuando quiero determinar una cota inferior para el problema B y conozco una cota inferor para el problema A.
La notación es  $A \infty_{poli}B$ No es infinito es el infinito cortado en su ultimo O.
DEcijoms Que A es reductible polinomialmente de para B.
poli-> polinomial.
EL algoritmo que resuellve A sera'la suma de las complejidades de resovler B y el costo de la transformación a A.
$f(n)$ suma de las dos compeljidades de reducción.
