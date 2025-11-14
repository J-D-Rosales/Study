>[!note] Definición
>Es un contenedor secuencial, el cual permite tener datos en espacios de almacenamiento no relacionados (memoria).

Usa un nodo. Y tien en resumen las siguientes funciones.
- push front
- push back
- pop front
- pop back
- clear
## Diferencias de forward list vs array
Ubicación en la memoria:
Tiempos de acceso
Tamaño
Dimensiones
Preguntas que te pueden servir. Si las demuestras chévere.
1. ¿Cuánto se demora encontrar un elemento al comienzo? ¿Al final? ¿En cualquier posición? O(1), O(n) y O(n) 2. ¿Y para insertar un elemento después del primer nodo? ¿Después del último nodo? ¿Después de cualquier nodo? O(1), O(n) y O(n) 3. ¿Cómo sería el caso 2 pero antes del nodo? O(1), O(n) y O(n)
En resumen:
![[Automatic_door.png]]
# Clase
Sea $f(n)$ y $g(n)$ funciones asintóticamentes no negativas, usando la definción básica de la notación $\Theta$ Pruebe:
$$
max(f(n),g(n)) = \Theta (f(n) + g(n))
$$
2.-  Encuentra el orden de $T(n) = \sum_{2}^{n} \frac{1}{K\ln k}$
Integralo, y te dras cuenta que es ln(ln n) luego eso esta en $\Theta(\ln \ln(n))$.
