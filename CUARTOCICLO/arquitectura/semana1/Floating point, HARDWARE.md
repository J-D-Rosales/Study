El formato es 
-> Signo , exponente y fraccion
El formato es
$(-1)^{s} \times 1 \cdot Fr \times 2^{\exp-bias}$
# LENGUAJE DE PROGRAMACION EN HARDWARE
Vamos a intentar estructurar al hacerp rogramación en hardware. 
Todo va a partir de los transistores. Que puede tener dos formas, que genera puertas lógicas. Dónde el más sencillo es el not.
Después de unir las puertas lógicas.  Y podemos hacer un 
**MUX**: una módulo que tiene un selector, que va a decidir cual es la salida. 
Con los módulos grandes puedo armar coasas más grandes. 
Estos serán los **flip flop**, Aritméticas, etc. Que va a ser la tarea del CPU.
Y si puedes hacerlo de manera paralela, es decir que puedan generarse más operaciones de cada lata de cpu pasa a ser un GPU.
Etapas de nuestro proceso
**1era etapa**: Simulación.
Aquí vamos a crear nuestro diseño, y lo vamos a ver nuestro resultado, que lo vamos a llamar waveform.
Trabajamos con waveform porque vamos a tener señales, no variables, simplemente van a ser señales eléctricas. Vamos a Tner A, b , Y el output será Y. La idea es poder leer esas señales eléctricas.
**2.-** Implementación.
Todo el diseño que lo haz crad en un archivo. Ahora vamos a generar un archivo que se llamada nellits, (archivo en binario) que va a permitir mapear las variables que vamos a usar.
La dos partes son desafiantes. 
## Tipos de dispositivos
**Procesador**:
Tenemos un fabricación general del circuito y vamos a meter la lógica o magia en la programación. Pero es ineficaz, porque no es específico.
**ASIC** **Circuitos integrados de algún tipo de aplicación específica** : Aquí lo que vamos a hacer es programar antes de fabricar. Un circuito que prácticamente solo sirva para eso. Vamos a programar sobre máscaras. Las máscaras permiten crear esos circuitos quemando sus placas. 
Solo le colocaríamos dato y tendríamos el resultado.
Aquí estaremos **(FPGA)** Dispositivos de hardware reconfigurable: Nos van a permitir mapear las conexiones que tiene.Por medio de archivos Bit file. 
# Hardware design
Vamos a manejar un lenguaje HDL. 
Vamos a usar el Verilog. Que es más usado, la versión europea.
## General processor 
La diferencia principal de programar. 
Cuando programamos, estamos tendidos a usar paralelismo y concurrencia. Y para poder usar eso necesitamos varios núcleos o threads.
En cambio concurrencia, es optimizar procesos, en dónde se aprovecha las tareas en segundo plano, para aprovechar los tiempos muertos del otro.
Lo que vamos a hacer es programar sobre señales eléctricas. Es decir, sobre los inputs. NO HAY MANERA DE SEPARAR LOS DOS PROCESOS.
Osea se vam hacer en paralelo. Es decir está óptimo.
Estamos hablando ya no de variables sino de objetos reales.
Se puede hacer concurrencia parchando ciertas cantidades de electricidad.
En el Basys 3 (chip)
Solo tenemos 15 entradas, entonces hay formas de solucionarlo. Porque queremos meter 32 bits, que hacemos, podría ser comprimirlo o hacerlo de tiempo en tiempo.
No es todo es simulación sino también implementación. Por eso no podemos usar cuántos inputs queramos.
El software que usaremos será Vivado.
# Basic syntax
Sintaxis del Vivado.
No se puede empezar por un número. No se puede colocar Mayúsculas y minúsculas sin casi nada.
Doble eslash para comentarios, y /* para multiple comentario.
EN la ppt, están todas las operaciones.
### Numebr representation in Verilog
El formato que vamos a usar es N'Bxx: O'b''''-0001
Veremos:
que el formato es N el n´mero de bits, B es la base, y xx es el número ejemplo
5'b01111
Esto no es two complement ni unsigned. Lo importante no es lo que colocas adentro sino como lo interpretas. Es cómo decir a un lenguaje de programación que es lo que quieres leer.
Vamos a tener también el X y el Z, como valores.
Lo normal en las funciones de onda o lo correcto es
```bash
a---
b---
y---
```
SI la señal está en verde, está correcto. Pero si sale en rojo, significa que el x no está bien definido.
El azul es Z. que es definitivamente que algo está mal. Nos indica que hay algo mal conectado. 
## Definir un módulo en Verilog
Tenemos que definir un modulo, un ejemplo es así.
```cpp
module example(a,b,c,y);
input a;
input b;
input c;
output y;
// como propgramar
endmodule
```
Tener en cuenta los puntos y las comas.
Hay otra manera d eoccoarlo.
```cpp
module example(input a;
input b;
input c;output y;);
// como propgramar
endmodule
```
Vamos a poder definir inputs y autputs, con más vantiad de variables, cómo arrays.
Algunas formas de manipulación de bits.
```bash
// bit slicing
wire [15:0] longbus;
assing shortbus = longbus[12:5];
//concatenacion
assing y = {a[2],a[1],a[0],a[0];
// duplication
}
```

## Tipos de estilos a utilizar.
Implementaciones reales requieren los dos.
### Estructural
Lo que dice es que va a ser una descripción fiel del circuito. "cómo funciona".
### Behavioral
Va a ser una descripción de la lógica del circuito. ¿Qué hace el circuito?
En la imagen del strucural HDL.
Podemos definir el modulo small de la siugiente manera
```bash
module small(A,B,Y):
input A,B;
output Y;
// logica
endmodule
```
Luego definiría el módulo grande.
La variable de tipo wire, irá en structural porque vamos a definir todos los circuitos.
Se podría definir de las siguientes amneras, tal como se ve en el ppt.
Practicando
Primero se ponde el autput

```verilog
and m1(n1,a,b);
```
Vamos a tener por un lado el diseño y por el otro lado el testing. 
Tendremos un emulador para placas. 
Como el tester es un emulador par aalgo real. DEBE DEfinir una escala de tiempo.
- Diseño
- Variables
- Señales
- Waveform
