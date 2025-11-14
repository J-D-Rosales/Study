En el examen sí o sí va a haber problemas de nivel hard.
Resolver problemas de leetcode.
## Algoritmo
Definición simple: Conjunto ordenado de pasos o instrucciones a un tal fin.

## Notación asintótica.
Se expresará la complejidad a través de la entrada.
Ejemplo:
- Problemas aritméticos: número de bits
- En grafos: Vértices y aristas.
Y así.

Para representar la complejidad siempre será positivo. No existe algoritmo con tiempo negativo.
Se tomará datos grandes, es así, que las constantes se desprecian.
___
**Primera clase de función**:
>[!note] Definición
>$O(g(n))$ = $\{f(n):$ existen constantes positivas $c \in$ $n_{0}$ ral que $0\leq f(n) \leq cg(n)$, para todo $n \geq n_{0}$.

En pocas palabras, una función $2n^{2} \in O(n^{2})$ 

Informalmente, se dice que $f(n) \in O(g(n))$, en tanto $f(n)$ crece no maximo tan rapidamente cuanto $g(n)$.

En el ejemplo
$\frac{1}{2}n^{2} - 3n \in O(n^{2})$
Entonces, se satisface con
$c = \frac{1}{2}$ y $n_{0} = 7$
# Omega
>[!note] Definicion
>$\Omega(g(n)) = \{f(n):$ existen constantes positivas $c$ y $n_{0}$ tal que $0 \leq cg(n) \leq f(n)$ para todo $n \geq n_{0}$

informalmente decimos que , $f(n) \in \Omega(g(n))$, en tanto  f(n) crece no mínimo tanto lentamente que $g(n)$.
f crece más rápido que g(n).
