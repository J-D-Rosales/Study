Haremos los códigos de
- D-flip flop
- Enable-flip-flop
- Reset-flip-flop
- T-flip-flop
- JK flip-flop
Previamente se realizó la tabla característica para saber la tabla de verdad. Es así, que podemos realizarlo en verilog. Cualquier error se comentará por aquí. Los códigos serán pegados aquí. 
<span style="color:	#87CEEB">Recomendaciones:</span>
- Siempre al trabajar con verilog colocar wire en los inputs y reg en los outputs. 
- Dentro de los paréntesis de always tiene que ir lo que afecta sí o sí, osea asíncrono. 
- colcoar begin y end en always, porque simboliza una operación en ese bloque. 
always @(posedge clk)
Significa: este bloque se ejecuta una vez, exactamente en cada flanco de subida de clk

Realizando las pruebas pertinentes aquí está el código de D-flip-flop
```verilog
// design

`timescale 1ns/1ns

module dff(clk,d,q);
  input wire d,clk;
  output reg q;
  
  // usaremos el always
  always @ (posedge clk)
    begin
      q <= d;// q+ = D en el flanco
    end
endmodule
```

```verilog
// Code your testbench here
// or browse Examples
`timescale 1ns/1ns

module tb_dff();
  reg clk, d;
  wire q;
  
  // instanciamos el module
  dff test_1 (.clk(clk),.d(d),.q(q));
  
  // solo en eda playground, colocamos los files
  initial begin
    $dumpfile("wave.vcd"); 
    $dumpvars(0, tb_dff.test_1);        
  end
  
  // realizamos las pruebas
  always #5 clk = ~clk;
  initial begin
  clk = 0; d = 0; #5;
  d = 1; #5;
  d = 0; #5;
  d = 1; #5;

  $finish;
  end
  
endmodule
```
Usando el enable, tendríamos:
```verilog
// design 
// se realizará con el D-flip-flop con el enable

`timescale 1ns/1ns

module dffe(d,en,clk,q);
// definimos los inputs, colocar con reg y wire, porque 
  // estaremos usando wire
  input wire d,en,clk;
  output reg q;
  // forma 1
  /*
  always @ (posedge clk)
    begin
      if(en)
        q <= d;
    end
    */
   // segunda forma
  wire d_next = en ? d : q;
  always @(posedge clk)
    begin
      q <= d_next;
    end
    
endmodule

```

```verilog
// testbench

`timescale 1ns/1ns

module tb_dffe();
  reg d,en,clk;
  wire q;
  
  // instanciamos el module
  dffe test_1(.d(d),.en(en),.clk(clk),.q(q));
  
  // realizamos el export de files (solo en eda)
  initial begin
  $dumpfile("wave.vcd"); 
  $dumpvars(0, tb_dffe.test_1); 
  end
  // realizamos los test cases
  always #5 clk = ~clk;
  initial begin
  clk = 0; d = 0; en = 0; #10;
  d = 0; en = 0; #10;
  d = 0; en = 1; #10;
  d = 1; en = 0; #10;
  d = 1; en = 1; #10;
  $finish;
  end
endmodule
```

El código con el reset es interesante, porque si solo colocas r en el posedge, entonces, cuando se dispare hara eso, lo qeu esta en begin end. Por ello tienes que colocarle un if. Es decir if(r) q <= 0. SI reset entonces cambiar el valor a 0.
```verilog
// design

`timescale 1ns/1ns

module dfftr(d,en,r,clk,q);
  input wire d,en,r,clk;
  output reg q;
  // usamos el always, haremos el asyn
  wire d_next = en ? d : q;
  always @(posedge clk or posedge r)
  begin
    if(r)
      q <= 1'b0;
    else
    q<= d_next;
  end
endmodule

```

```verilog
// testbench

`timescale 1ns/1ns

module tb_dfftr();
  reg d,en,r,clk;
  wire q;
  // instanciamos nuestro test becnh
  dfftr test_1(.d(d),.en(en),.r(r),.clk(clk),.q(q));
  // hacemos el exit de files (solo apra eda playground
  initial begin
  $dumpfile("wave.vcd"); 
    $dumpvars(0, tb_dfftr.test_1); 
  end
  always #5 clk = ~clk;
  
  //realizamos los test
  initial begin
  clk = 0; d = 0; en = 0; r = 0; #10;
  d = 0; en = 0; r = 0; #10;
  d = 1; en = 1; r = 0; #10;
  d = 0; en = 1; r = 0; #10;
  d = 1; en = 1; r = 1; #10;
  d = 0; en = 0; r = 1; #10;
  d = 0; en = 1; r = 1; #10;
  d = 1; en = 0; r = 1; #10;
  $finish;
  end
endmodule`timescale 1ns/1ns

module dff(d,en,clk,q);
  input wire clk,en,d;
  output reg q;
  // realizar el always
  
  wire n1 = en ? d : q;
  always @(posedge clk)
    begin
      q <= n1;
    end
endmodule
```
NOw let's do the T-flip-flop

