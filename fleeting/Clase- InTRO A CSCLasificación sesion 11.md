-> Ya se hizo el análisis de componentes principales, es así que se continua con clasificadores.
CLasificar: A un nuevo dato se le clasifica con el dato más próximo.

Se puede predecir distintas varibales dependiendo de otras. 
En base a las columnas y un indentificador se puede predecir ciertas observaciones.
PPor ejemplo, si esa paersona sigue a pereda, podiblemente le guste el futboly  lo clasificamos allí.

La forma de leerlo con python es:

```python
pd.read

```
Teniedo una gran cantidad de datos, e ingresa un nuevo dato, entonces se puede predecir a grandes rasgos la edad que tiene o si le gusta tal par cual.
ejemplo clasificar por mayor de 45 o menro de 45

LA inteligencia artificial se puede definir en 2 ramas, la predicibilidad, y la IA generativa. 
La intelegencia artifical generativa es la más popular.

**Actviidad de clase**: De los daots, lo que se va a hacer es entrenar el modelo con los datos de 80%, y después el  20% se usa para ver si vlasifca bien. Se compara con las etiquetas reales y veremos que tan bien lo hizo.
El paquete que permite partirlo en 2 partes una para entrenar el modelo y el otro para testearlo es el sktlearn.

AL querer ordenar el csv, genramos un problema, porque pueden existir grupos desbalanceados, por ejemplo un grupo de datos que son solo de 60 años, entonces si viene un niño de 4, el modelo nunca se entreno con esos datos.

La estratificación es un concepto que se usa para poder hacer que la variable a la cual queremos aplicarle la clasficación, en dónde cómo sabemos quue existe la probabilidad que quede desbalanceado, así que la estratificación ayuda a que esa probailidad no sea posible.

Cómo esxisten 3 etapas, lo que se hace es cortar a los dsaot de 20 para validar y 20% para prueba.
entonces, al final quedaría 60, 20, 20.

