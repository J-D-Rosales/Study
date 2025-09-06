Practicando Verilog;
Código funcional para EDA Playground hacer el MUX 2:1
Diseño
```
// Code your design here
`timescale 1ns/1ns

module mux2_1_s( 
  input a,
  input b,
  input s,
  output y);
  
  assign y = (~s & a) | (s & b);
endmodule
```

Implementación del testbench:
```
// Code your testbench here
// or browse Examples
`timescale 1ns/1ps

module tb_mux2_1;
  reg a,b,s;
  wire y;
  mux2_1_s instanciar_dut (.a(a), .b(b), .s(s), .y(y));
  initial begin 
    $dumpfile("mux2_1.vcd"); 
    $dumpvars(1, tb_mux2_1);
    a=0; b=0; s=0; #10;
    a=0; b=0; s=1; #10;
    a=0; b=1; s=0; #10;
    a=0; b=1; s=1; #10;
    a=1; b=0; s=0; #10;
    a=1; b=0; s=1; #10;
    a=1; b=1; s=0; #10;
    a=1; b=1; s=1; #10;
    
  $finish;
  end
endmodule
```

Por si deseas estructural, cambias eso de assign a:
```
// Si quieres structural:
  // wire ns, w0, w1;
  // not(ns, s);
  // and(w0, a, ns);
  // and(w1, b, s);
  // or(y, w0, w1);
```

Ahora intentaremos hacerlo con un Mux de 4:1.

Lo logramos. Aunque esto se hizo haciendo estrucutral. Aunque igual funciona. Debes tomar en cuenta que se tomará tanto behavioral como structural. 
```
// Code your design here
`timescale 1ns/1ns

module mux2_1_b( 
  input a,
  input b,
  input s,
  output y);
  
  assign y = (~s & a) | (s & b);
endmodule

module mux_4_1_B(
  input a,
  input b,
  input c,
  input d,
  input s1,
  input s2,
  output y);
  
  wire n1;
  wire n2;
  
  mux2_1_b u0 (.a(a),.b(b),.s(s1),.y(n1));
  mux2_1_b u1 (.a(c),.b(d),.s(s1),.y(n2));
  mux2_1_b u2 (.a(n1),.b(n2),.s(s2),.y(y));
  
endmodule
```

OJO CADA INSTANCIA DEL MODULO DEBE TENER SU NOMBRE
```
`timescale 1ns/1ns
module mux4_1_t;
  reg a,b,c,d;
  reg s1,s2;
  wire y;
  
  //instancias a utilizar
  mux_4_1_B chanchito (.a(a),.b(b),.c(c),.d(d),.s1(s1),.s2(s2),.y(y));
  
  initial begin
    $dumpfile("mux_4_1_B.vcd"); 
    $dumpvars(1, mux4_1_t);
    
    a=0;b=0;c=0;d=0;s1=0;s2=1; #10;
    a=0;b=0;c=0;d=0;s1=1;s2=0; #10;
    a=1;b=1;c=1;d=1;s1=0;s2=1; #10;
    a=1;b=1;c=1;d=1;s1=1;s2=0; #10;
  end
endmodule
```

El demux de 16:1, sería así:
Diseño:
```
// Code your design here
// implementando el MUX 16:1

`timescale 1ns/1ns

module mux2_1_b(
  input a,
  input b,
  input s,
  output y
);
  assign y = (~s&a) | (s&b); 
  
endmodule
    
module mux16_1_b #(parameter W=8)(
  input [W-1:0] a1,
  input [W-1:0] a2,
  input [W-1:0] a3,
  input [W-1:0] a4,
  input [W-1:0] a5,
  input [W-1:0] a6,
  input [W-1:0] a7,
  input [W-1:0] a8,
  input [W-1:0] a9,
  input [W-1:0] a10,
  input [W-1:0] a11,
  input [W-1:0] a12,
  input [W-1:0] a13,
  input [W-1:0] a14,
  input [W-1:0] a15,
  input [W-1:0] a16,
  input s1,
  input s2,
  input s3,
  input s4,
  output [W-1:0] y
); 
  
  // necesitamos wires 
  wire [W-1:0] n1;
  wire [W-1:0] n2;
  wire [W-1:0] n3;
  wire [W-1:0] n4;
  wire [W-1:0] n5;
  wire [W-1:0] n6;
  wire [W-1:0] n7;
  wire [W-1:0] n8;
  wire [W-1:0] n21;
  wire [W-1:0] n22;
  wire [W-1:0] n23;
  wire [W-1:0] n24;
  wire [W-1:0] n31;
  wire [W-1:0] n32;
  
  // logica estrucutral
  
  mux2_1_b u0 (.a(a1),.b(a2), .s(s1), .y(n1));
  mux2_1_b u1 (.a(a3),.b(a4),.s(s1), .y(n2));
  mux2_1_b u2 (.a(a5),.b(a6),.s(s1), .y(n3));
  mux2_1_b u3 (.a(a7),.b(a8),.s(s1), .y(n4));
  mux2_1_b u4 (.a(a9),.b(a10),.s(s1), .y(n5));
  mux2_1_b u5 (.a(a11),.b(a12),.s(s1), .y(n6));
  mux2_1_b u6 (.a(a13),.b(a14),.s(s1), .y(n7));
  mux2_1_b u7 (.a(a15),.b(a16),.s(s1), .y(n8));
  
  mux2_1_b u8 (.a(n1),.b(n2),.s(s2), .y(n21));
  mux2_1_b u9 (.a(n3),.b(n4),.s(s2), .y(n22));
  mux2_1_b u10 (.a(n5),.b(n6),.s(s2), .y(n23));
  mux2_1_b u11 (.a(n7),.b(n8),.s(s2), .y(n24));
  
  mux2_1_b u12 (.a(n21),.b(n22),.s(s3), .y(n31));
  mux2_1_b u13 (.a(n23),.b(n24),.s(s3), .y(n32));
  
  mux2_1_b u14 (.a(n31),.b(n32),.s(s4), .y(y));
  
endmodule  
```

eL TEST
```
// Code your testbench here
// or browse Examples
`timescale 1ns/1ns

module tb_mux_41;
  reg a1,a2,a3,a4,a5,a6,a7,a8,a9,a10,a11,a12,a13,a14,a15,a16;
  reg s1,s2,s3,s4;
  wire y;
  
  mux16_1_b chanchito (.a1(a1),.a2(a2),.a3(a3),.a4(a4),.a5(a5),.a6(a6),.a7(a7),.a8(a8),.a9(a9),.a10(a10),.a11(a11),.a12(a12),.a13(a13),.a14(a14), .a15(a15),.a16(a16), .s1(s1),.s2(s2),.s3(s3),.s4(s4), .y(y));
  initial begin
    $dumpfile("mux_16_1.vcd"); 
    $dumpvars(1, tb_mux_41.chanchito);  
    
    a1=0;a2=0;a3=0;a4=0;a5=0;a6=0;a7=0;a8=0;a9=0;a10=0;a11=0;a12=0;a13=0;a14=0;a15=0;a16=0;s1=0;s2=0;s3=0;s4=0; #10;
  end
endmodule
  
```

¡genial! 🙌 Lo que te conviene tener para el examen es un **kit de plantillas básicas** de Verilog para los bloques de combinacional más comunes: **MUX, DEMUX, comparador, codificador/decodificador**. Te los dejo con la versión **structural** (si piden compuertas/submódulos) y la **behavioral** (si piden operadores/always). Así puedes armar cualquier cosa rápido.

---

# 🔹 1. MUX 2:1 (1 bit)

### Structural (con compuertas)

```verilog
module mux2_1_struct(
  input  a, b, s,
  output y
);
  wire ns, w0, w1;
  not (ns, s);
  and (w0, a, ns);
  and (w1, b, s);
  or  (y, w0, w1);
endmodule
```

### Behavioral (operador `?:`)

```verilog
module mux2_1_beh(
  input  a, b, s,
  output y
);
  assign y = s ? b : a;
endmodule
```

---

# 🔹 2. MUX N:1 (ej. 4:1)

### Structural (usando mux2_1 como submódulo)

```verilog
module mux4_1_struct(
  input  a,b,c,d,
  input  s1,s2,
  output y
);
  wire n1, n2;
  mux2_1_beh u0 (.a(a), .b(b), .s(s1), .y(n1));
  mux2_1_beh u1 (.a(c), .b(d), .s(s1), .y(n2));
  mux2_1_beh u2 (.a(n1), .b(n2), .s(s2), .y(y));
endmodule
```

### Behavioral (con `case`)

```verilog
module mux4_1_beh(
  input  a,b,c,d,
  input  s1,s2,
  output reg y
);
  always @(*) begin
    case ({s2,s1})
      2'b00: y = a;
      2'b01: y = b;
      2'b10: y = c;
      2'b11: y = d;
    endcase
  end
endmodule
```

---

# 🔹 3. DEMUX 1:2 (N bits, por ejemplo 8)

### Structural

```verilog
module demux1_2 #(parameter W=8)(
  input  [W-1:0] I,
  input          s,
  output [W-1:0] Y0, Y1
);
  assign Y0 = s ? {W{1'b0}} : I; // {W{1'b0}} = cero de W bits
  assign Y1 = s ? I          : {W{1'b0}};
endmodule
```

### Behavioral

```verilog
module demux1_2_beh #(parameter W=8)(
  input  [W-1:0] I,
  input          s,
  output reg [W-1:0] Y0, Y1
);
  always @(*) begin
    Y0 = 0; Y1 = 0;
    case (s)
      1'b0: Y0 = I;
      1'b1: Y1 = I;
    endcase
  end
endmodule
```

---

# 🔹 4. Comparador de 2 bits

### Structural (ecuaciones booleanas)

```verilog
module cmp2_struct(
  input  [1:0] A, B,
  output F_eq, F_lt, F_gt
);
  assign F_eq = (A[1]~^B[1]) & (A[0]~^B[0]);    // igual
  assign F_gt = (A[1]&~B[1]) | ((A[1]~^B[1]) & A[0] & ~B[0]); 
  assign F_lt = (~A[1]&B[1]) | ((A[1]~^B[1]) & ~A[0] & B[0]); 
endmodule
```

### Behavioral (más directo)

```verilog
module cmp2_beh(
  input  [1:0] A, B,
  output F_eq, F_lt, F_gt
);
  assign F_eq = (A==B);
  assign F_lt = (A< B);
  assign F_gt = (A> B);
endmodule
```

---

# 🔹 5. Decoder 2:4 (de 2 bits a 4 salidas one-hot)

### Structural

```verilog
module decoder2_4(
  input  a, b,
  output y0,y1,y2,y3
);
  assign y0 = ~a & ~b;
  assign y1 = ~a &  b;
  assign y2 =  a & ~b;
  assign y3 =  a &  b;
endmodule
```

### Behavioral

```verilog
module decoder2_4_beh(
  input  [1:0] s,
  output reg [3:0] y
);
  always @(*) begin
    y = 4'b0000;
    y[s] = 1'b1;
  end
endmodule
```

---

# 🔹 6. Encoder (ejemplo: 4:2)

```verilog
module encoder4_2(
  input  [3:0] x,
  output [1:0] y
);
  assign y = (x[3]) ? 2'b11 :
             (x[2]) ? 2'b10 :
             (x[1]) ? 2'b01 : 2'b00;
endmodule
```

---

## 🧩 Cómo usarlos en examen

- **Si piden structural:**  
    – Usa compuertas (`and, or, not`) o tus propios submódulos básicos (como el mux2_1).
    
- **Si piden behavioral:**  
    – Usa `assign` con operadores (`?:`, `==`, `<`, `>`), o un bloque `always @(*)` con `case`/`if`.
    
- **Si piden N bits en vez de 1:**  
    – Declara entradas/salidas como `[N-1:0]`.  
    – Para forzar ceros: `{N{1'b0}}` (cero de N bits).
    
- **Si N no es potencia de 2 (ej. 1:13):**  
    – Implementa el siguiente más grande (ej. 1:16) y deja salidas sobrantes sin usar.
    

---

¿quieres que te arme un **archivo con todas estas plantillas juntas** (un “chuletario” de Verilog), listo para copiar en EDA Playground y probar?