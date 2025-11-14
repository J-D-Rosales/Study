Los objetivos:
- ver los detalles de cómo trabaja el procesador
- Explicar la interacción entre hardware y software
- Modelar un microprocessor con reglas de instructions limitadas.
Entender la intrínseca de un computador. ¿Por qué funciona así?
La pregunta es cómo diseñar una arquitectura.
Toda la abstracción está basada en la matemática, la lógica booleana.

# Evolución de computadoras.
La arquitectura de computadoras es un campo muy antiguo. Así, el modelo matemático está creado. Lo que falta es el espacio físico.

# Bits and bytes
En la parte de la idea de lo que es tener un bit:
Es una dualidad, Tener un 0 o tener un 1.
Los bbits se representan físicamente con la cantidad d eboltaje, el cual mientras menos rango hay mejor, porque gasta menos energía.
El transistor hace todo esto de manera lógica..
La frecuencia d eoperación del circuitos, referencia. 

# Number systems.
La representación de números va por la precedencia histórica.
La conversión en nuestro sistema es en vases. Donde el número se multipica por la cantidad asociada como base. 
La representación hexadecimal es de 4 bits.
podemos decir entonces.
$256_{10} = 100_{16} = 000100000000_{2}$
Cómo convertimos
ejemplo
4AF16 a binario
$16^{2} \times 4 + 16^{1}\times 10 + 16^{0} \times 15 = 1199_{10}$
Ver una base en donde no se puede represntar.
El byte es algo conveniente. La aproximación hexadecimal es muy parecida. 
1byte = 8 bits.
La razón de porque se empieza desde uno es porque la maxima cantidad es $2^{n} -1$
Para saber cuantos digitos debo tener, simplemente multiplica por 4.
Una forma representación que se le da para un número hexadecimal es 0x. Solo por regla.
El bit (lsb) el más insignificativo está a la derecha. Y el resto está en izquierda.
El lsB va a ser los dos últimos dígitos.
___
En binario la adicion es similar.
Un overflow es cuando te sobrepasa la cantidad de bits cuando el sistema no obtienen la cantidad correcta, y cuando colocas signo pueden ocurrir overflow en manera de dar resultados errores.
El r'imer estándar para represntar signos es sign-mafnitud. Sonde tu tueines una cantidad maxima de bits. En donde reservas, un vir más, en donde el ultimo bit representa solo las dos posibilidades, el posititvo y negativo.
El problema que surge es que si tenemos el valor de 6, diriamos que es + 6, y con -6.  Pero al sumarlo aritmeticamente , no da.
En la cardinalidad del conjunto se define por la fórmula del ppt p.34.
___
La otra forma de representación es de repsentación a dos. 
Endonde al aritmética se sostiene. Lo que se hace para esto , lo que hacemos es desplazar la recta de número, ya que va de infinito a infinito. 
Lo que hago es invertir los bits. ENotnces si fuera 0110 sería 1001 invertido.
Y cuando se suma da exactamente lo que debe dar.
Para saber que número es cuando es negtivo, inviertelo y quitale el signo y ya esta.
