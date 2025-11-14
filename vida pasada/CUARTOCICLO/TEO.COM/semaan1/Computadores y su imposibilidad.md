Teorema H no existe.
Suponga que H exista
-> Sabemos construit 
	N negador
	P duplicador
Construimos X
" Dado input M":
- Simula P con input M
- Simula H con input (m,m)
- Simula N con input con la respuesta de H
___
Repaso de negación:
Usando una proposición contraria a la original, probar una contradicción, un sinsentido. 
La razón razón de utilizar tus premisas es porque cumplen un rol que te hacen llegar a un fin.
Se propondrá modelos de computación.

**Función longitud**: Es una función que recibe una cadena y te devuelve algo.
Empty string: $\epsilon$ 
Las operaciones que tenemos son :
operación reverso: Toma un string y lo asocia con su reverso. carro -> orrac
Concatenación: Función binaria que recibe dos cadenas y devuelve una cadena. 
La concatenación está definida para dos cadenas de distintos alfabetos. Pero, se puede hacer (parcharlo) refactorizar. Implícitamente se definió cuál es el alfabeto.
**Substring, Prefix**: El substring es una subcadena (El órden importa). Sufijo es eleminar letras de la parte derecha y prefijo de la parte izquierda.

La notación de exponenciación se traslada a conjuntos siempre y cuando los conjuntos son los mismos. 
**String**: Son simplemente conjuntos de letras.
$$
\begin{align}
\Sigma^{1}  \{ a \} \\
\Sigma^{2}  \{ ab \}
\end{align}
$$
Para poder tener a todo slos Símbolos.
$\Sigma^{+}: \Sigma^{1} \cup \Sigma^{2}$ y así.
**Lenguaje**:
$L$ es un lenguaje, L es un conjunto de strings.
También se puede definir como $\Sigma^{*}$
