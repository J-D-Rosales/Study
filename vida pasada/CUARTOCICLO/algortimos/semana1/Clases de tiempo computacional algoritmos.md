# Notación teta
$\Theta(g(n)) = \{$ existen constantes positivas $c_{1},c_{2},y~n_{0}$ tal que $0\leq c_{1}g(n) \leq f(n) \leq c_{2}g(n)$, para todo $n\geq n_{0}$}.
Informalmente decimos que, $f(n) \in \Theta(g(n))$, en tanto $f(n)$ crece tan rapidamente que $g(n)$.
Si pertenecen a los dos clases anteriores, pertencen a theta.
# Notación o
$o(g(n)) = f(n)$ para toda contante c positiva, existe una constante $n_{0} >0$ tal que $0 \leq f(n) <cg(n)$, para todo $n\geq n_{0}$.
INformalmente, decimos que, f(n) $\in o(g(n))$, en tanto que f(n) cresce mas lentamente que g(N).
EN el ejemplo lo resolveríamos:
$f(n)<cg(n)$
$100n^{2}<cn^{3}$
$\frac{1000}{n} < c$
$\frac{1000}{c} < c$ Por que son números positivos.
Luego se colocará la fucnión techo y se el suma 1 porque es el número más mínimo.
# Clase $w$
Definición: $w(g(n)) =  \{$ para toda ocnstante poistiva $c$, exite una constante $n_{0}> 0$ tal que  $0\leq cg(n) < f(n)$, para todo $n\geq n_{0}$.
Informalmente, decimos que , se $f(n) \in w(g(n))$, en tanto $f(n)$ crece mas rapidamente que $g(n)$.

Las definiciones equivalente, se pueden dar con los límites.
Existes propiedades de transitividad en las definiciones. Se recomienda practicarlas.
___
Usaremos $f(n) = O(g(n))$.
Esto está mal, pero por simplicidad , lo realizaremso de esta manera.

En el mejor de los casos puede haber un o, o un omega, porque solo son grupos de funciones.
# Problemas
1) $2^{n} \in O(3^{n})$
2) $\log_{10}n \in \Theta(lg_{2}n)$
3) $n! \in O(n^{n})$


# Punteros
