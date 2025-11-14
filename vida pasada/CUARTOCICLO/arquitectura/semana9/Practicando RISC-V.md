1) Hacer un array de 10 elementos:
1- código de c++
2.- Cósigo de assembly y cómo se movería el stack.

```cpp
// realizar un vector o array de 10 elementos  
  
# include <iostream>  
# include <vector>  
  
  
using namespace std;  
  
vector<int> crear_vector(int n) {  
    vector<int> v(n);  
    for (int i = 0; i < n; i++) {  
        v.push_back(i);  
    }  
    return v;  
}  
  
  
int main() {  
    vector<int> v = crear_vector(10);  
    return 0;  
}
```

código de risc five:
```RV
.global _start
_start:
	# esta es la funcion principal, llamaremos a la funcion de main.
	addi s0, x0, 10 # guardamos el n que queremos pasar a la función.
	mv a0, s0; ## copiamos a a0 el s0 que al final es el n
	jal _crear_array
	# tenemos a a0 como el base addres
	# se ha completado todo lo que queriamos
	
_final:
	j _final
	
_crear_array: ## retornar el base addres de mi array
	# tendremos que reservar el espacio en la memria
	# guardamos el main addres
	addi sp, sp, -4 # guardo un word para guardar el s0 pasado
	sw s0, 0(sp) # guardo el valor
	addi sp, sp, -40 ## guardo 40 porque 10*4 = 40
		# a0 sera el resultado a enviar, es decir e lbase addres
	add t0, x0, a0 ## el temporal de t0 sera n
	add a0, sp, x0 ## a0 tiene el base addres
	
#___________________________________________________
	# hacemos el loop para crear el array
	addi t1, x0, 0 # hacemos el contador i =0
	addi t3, x0, 4
	c_for:  bge t1, t0, end # si i >=n va a end 
		sub t2, t0, t1
		addi t2, t2, -1
		mul t2, t2, t3
		add t2, t2, sp;
		sw t1, 0(t2)
		addi t1,t1, 1;
		j c_for
	end:
	#_____ recuperacion de valores
		
	mv a0, sp ## returno el base addres
	addi sp, sp, 40
	lw s0, 0(sp) ## respetar las convenciones de call y callee
	addi sp, sp, 4
	
	jr ra
```

