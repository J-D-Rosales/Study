# resumen

`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 11/12/2025 10:06:10 PM
// Design Name: 
// Module Name: reg_decode_to_execute_control
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////


module reg_decode_to_execute_control (
    input             clk,
    input             reset,

    // --------- CONTROL (desde etapa D) ---------
    input             RegWriteD,
    input      [1:0]  ResultSrcD,
    input             MemWriteD,
    input             JumpD,
    input             BranchD,
    input      [2:0]  ALUControlD,
    input             ALUSrcD,

    // --------- CONTROL (hacia etapa E) --------
    output reg        RegWriteE,
    output reg [1:0]  ResultSrcE,
    output reg        MemWriteE,
    output reg        JumpE,
    output reg        BranchE,
    output reg [2:0]  ALUControlE,
    output reg        ALUSrcE,
);

    // Registro con reset asíncrono
    always @ (posedge clk or posedge reset) begin
        if (reset) begin
            // CONTROL
            RegWriteE   <= 1'b0;
            ResultSrcE  <= 2'b0;
            MemWriteE   <= 1'b0;
            JumpE       <= 1'b0;
            BranchE     <= 1'b0;
            ALUControlE <= 3'b0;
            ALUSrcE     <= 1'b0;

        end else begin
            // CONTROL
            RegWriteE   <= RegWriteD;
            ResultSrcE  <= ResultSrcD;
            MemWriteE   <= MemWriteD;
            JumpE       <= JumpD;
            BranchE     <= BranchD;
            ALUControlE <= ALUControlD;
            ALUSrcE     <= ALUSrcD;
        end
    end

endmodule





`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 11/12/2025 08:44:52 PM
// Design Name: 
// Module Name: reg_decode_to_execute
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////

// falta agregar lo de hazard unit
module reg_execute_to_memory_control(
    input             clk,
    input             reset,

    // --------- CONTROL desde etapa E ---------
    input             RegWriteE,
    input      [1:0]  ResultSrcE,
    input             MemWriteE,

    // --------- CONTROL hacia etapa M --------
    output reg        RegWriteM,
    output reg [1:0]  ResultSrcM,
    output reg        MemWriteM,

);

    always @ (posedge clk or posedge reset) begin
        if (reset) begin
            // CONTROL
            RegWriteM  <= 1'b0;
            ResultSrcM <= 2'b0;
            MemWriteM  <= 1'b0;

        end else begin
            // CONTROL
            RegWriteM  <= RegWriteE;
            ResultSrcM <= ResultSrcE;
            MemWriteM  <= MemWriteE;

        end
    end

endmodule





`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 11/12/2025 08:44:52 PM
// Design Name: 
// Module Name: reg_decode_to_execute
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////

// falta agregar lo de hazard unit
module reg_memory_to_writeback_control(
    input             clk,
    input             reset,

    // --------- CONTROL desde etapa M ---------
    input             RegWriteM,
    input      [1:0]  ResultSrcM,

    // --------- CONTROL hacia etapa W --------
    output reg        RegWriteW,
    output reg [1:0]  ResultSrcW,
);

    always @ (posedge clk or posedge reset) begin
        if (reset) begin
            // CONTROL
            RegWriteW  <= 1'b0;
            ResultSrcW <= 2'b0;

        end else begin
            // CONTROL
            RegWriteW  <= RegWriteM;
            ResultSrcW <= ResultSrcM;

        end
    end

endmodule}

__________________
`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 11/17/2025 11:16:13 AM
// Design Name: 
// Module Name: datapath
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////


module datapath(input  clk, reset,
//________________ inputs del controller
                input  [1:0]  ResultSrcW, 
                input  PCSrcE, ALUSrcE,
                input  RegWriteW,
                input  [1:0]  ImmSrcD, 
                input  [2:0]  ALUControlE,
                input   MemWriteM,
//inputs de la memeoria
                input  [31:0] ReadDataM,
                input  [31:0] InstrF,
// outputs
                output ZeroE,
                output InstrD,
                output [31:0] PCF,     
                output [31:0] ALUResultM, WriteDataM
                );
  
  
 localparam WIDTH = 32; // Define a local parameter for bus width

//_________________ fase de fetch
 wire [31:0] PCNextF, PCPlus4F; 
 wire [31:0] PCD, PCPlus4D; 
 // INstrD is an output for the ocntrol
  
  // next PC logic -- falta el enable
  flopr #(WIDTH) pcreg(
    .clk(clk), 
    .reset(reset), 
    .d(PCNextF), 
    .q(PCF)
  ); 

  // 
  adder       pcadd4(
    .a(PCF), 
    .b({WIDTH{1'b0}} + 4), // Using WIDTH parameter for constant 4
    .y(PCPlus4F)
  ); 
  
  reg_fetch_to_decode reg_fetch_to_decode_instance(
   .clk(clk),
   .reset(reset),

    // --------- ENTRADAS DESDE FETCH (F) ---------
    .InstrF(InstrF),      // instrucción leída de la memoria
    .PCF(PCF),         // PC actual en F
    .PCPlus4F(PCPlus4F),    // PC+4 en F

    // --------- SALIDAS HACIA DECODE (D) ---------
    .InstrD(InstrD),      // instrucción latcheada para D
    .PCD(PCD),         // PC en D
    .PCPlus4D(PCPlus4D)     // PC+4 en D
  );


//_____________________________________
// fase del decode
//_________________________________________-
 
 wire [31:0] ImmExtD; 

 // parte de decode
 wire [31:0] RD1D,RD2D;  

// varuables para execute
wire [31:0] RD1E,RD2E, PCE, RdE, ImmExtE, PCPlus4E;
   // register file logic
   
  regfile     rf(
    .clk(clk), 
    .we3(RegWriteW), 
    .a1(InstrD[19:15]), 
    .a2(InstrD[24:20]), 
    .a3(RdW), // falata implementar la señal 
    .wd3(ResultW), 
    
    .rd1(RD1D), 
    .rd2(RD2D)
  ); 
 
 
 
  extend      ext(
    .instr(InstrD[31:7]), 
    .immsrc(ImmSrcD), 
    .immext(ImmExtD)
  ); 

        
  reg_decode_to_execute reg_decode_to_execute_instance(
    .clk(clk),
    .reset(reset),

    // --------- DATOS (desde etapa D) ----------
    .RD1D(RD1D),
    .RD2D(RD2D),
    .PCD(PCD),
    .RdD(InstrD[11:7]),
    .ImmExtD(ImmExtD),
    .PCPlus4D(PCPlus4D),

    // --------- DATOS (hacia etapa E) ----------
    .RD1E(RD1E),
    .RD2E(RD2E),
    .PCE(PCE),
    .RdE(RdE),
    .ImmExtE(ImmExtE),
    .PCPlus4E(PCPlus4E)
);

//_____________________________________________
//-fase de Execution
//_____________________________-

 wire [31:0] SrcAE, SrcBE, WriteDataE,ALUResultE; 
    
 assign SrcAE = RD1E;
 assign WriteDataE = RD2E;
 wire [31:0] PCTargetE;


// wires que salen de los registros // aluresultM,WriteDataM es un output
wire [31:0] RdM, PCPlus4M;
  
  mux2 #(WIDTH)  AluSrcE_mux(
    .d0(RD2E), 
    .d1(ImmExtE), 
    .s(ALUSrcE), 
    .y(SrcBE)
  ); 
 
   alu         alu(
    .a(SrcAE), 
    .b(SrcBE), 
    .alucontrol(ALUControlE), 
    .result(ALUResultE), 
    .zero(ZeroE)
  ); 
 
  // para eso del branch
  adder       pcaddbranch(
    .a(PCE), 
    .b(ImmExtE), 
    .y(PCTargetE)
  ); 

    reg_execute_to_memory reg_execute_to_memory_instance(
        .clk(clk),
        .reset(reset),
    
        // --------- DATOS desde etapa E ----------
        .ALUResultE(ALUResultE),
        .WriteDataE(WriteDataE),
        .RdE(RdE),
        .PCPlus4E(PCPlus4E),
    
        // --------- DATOS hacia etapa M ----------
        .ALUResultM(ALUResultM),
        .WriteDataM(WriteDataM),
        .RdM(RdM),
        .PCPlus4M(PCPlus4M)
    );

//_____________________
// fase de Write Back
//_______________________________________
    // wire RdM and PCPlus4M are done.

    wire [31:0] ReadDataW,PCPlus4W,ALUResultW;
    
    wire [31:0] RdW;
    wire [31:0] ResultW;
    
    
    reg_memory_to_writeback reg_memory_to_writeback_instance(
        .clk(clk),
        .reset(reset),
    
        // --------- DATOS desde etapa M ----------
        .ReadDataM(ReadDataM),
        .ALUResultM(ALUResultM),
        .PCPlus4M(PCPlus4M),
        .RdM(RdM),
    
        // --------- DATOS hacia etapa W ----------
        .ReadDataW(ReadDataW),
        .ALUResultW(ALUResultW),
        .PCPlus4W(PCPlus4W),
        .RdW(RdW)
    );
    

   mux3 #(WIDTH)  resultmux(
    .d0(ALUResultW), 
    .d1(ReadDataW), 
    .d2(PCPlus4W), 
    .s(ResultSrcW), 
    .y(ResultW)
  ); 

  mux2 #(WIDTH)  pcmux(
    .d0(PCPlus4F), 
    .d1(PCTargetE), 
    .s(PCSrcE), 
    .y(PCNextF)
  ); 

endmodule
____
# pipeline
`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 11/17/2025 10:50:00 AM
// Design Name: 
// Module Name: pipeline
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////


module pipeline(input  clk, reset,
                   output [31:0] PCF,
                   input  [31:0] InstrF,
                   output MemWriteM,
                   output [31:0] DataAdr, 
                   output [31:0] WriteDataM,
                   input  [31:0] ReadDataM);
  
  wire [31:0] ALUResult; 
  
  wire       ALUSrcE, RegWriteW, ZeroE; 
  wire [1:0] ResultSrcW, ImmSrcD; 
  wire [2:0] ALUControlE; 
  wire       PCSrcE; 
  wire [31:0] InstrD;  
  // DataAdr is connected to ALUResult
  assign DataAdr = ALUResultM;
    // controler terminado
  controller c(
    .clk(clk), // el main decoder sigue siendo combinatciona pero esto es para los registros
    .reset(reset), // lo mismo
    
    .op(InstrD[6:0]), 
    .funct3(InstrD[14:12]), 
    .funct7b5(InstrD[30]), 
    
    //------------outputs
    .ZeroE(ZeroE),
    .ResultSrcW(ResultSrcW), 
    .MemWriteM(MemWriteM), 
    .PCSrcE(PCSrcE),
    .ALUSrcE(ALUSrcE), 
    .RegWriteW(RegWriteW), 
    .ImmSrcD(ImmSrcD), 
    .ALUControlE(ALUControlE)
  ); 
  
  
// vamos con el datapath

    datapath dp(
        .clk(clk), 
        .reset(reset), 
        
        .ResultSrcW(ResultSrcW),    // Mapeo: ResultSrcW -> ResultSrc
        .PCSrcE(PCSrcE),            // Mapeo: PCSrcE -> PCSrc
        .ALUSrcE(ALUSrcE),          // Mapeo: ALUSrcE -> ALUSrc
        .RegWriteW(RegWriteW),      // Mapeo: RegWriteW -> RegWrite
        .ImmSrcD(ImmSrcD),          // Mapeo: ImmSrcD -> ImmSrc
        .ALUControlE(ALUControlE),  // Mapeo: ALUControlE -> ALUControl
        .ReadDataM(ReadDataM),
        .MemWriteM(MemWriteM),
        
        .ZeroE(ZeroE), 
        .PCF(PCF),                  // Mapeo: PCF -> PC
        .InstrF(InstrF),            // Mapeo: InstrF -> Instr
        
        .InstrD(InstrD),
        .ALUResultM(ALUResultM),    // Mapeo: ALUResultM -> ALUResult
        .WriteDataM(WriteDataM)    // Mapeo: WriteDataM -> WriteData
    );
    
  
  
endmodule
____
testbench
module testbench;
  reg          clk;
  reg          reset;
  wire [31:0]  WriteData;
  wire [31:0]  DataAdr;
  wire         MemWrite;
  
  // instantiate device to be tested
  top dut(
    .clk(clk), 
    .reset(reset), 
    .WriteData(WriteData), 
    .DataAdr(DataAdr), 
    .MemWrite(MemWrite)
  );

  // initialize test
  initial begin
    reset = 1; # 22;
    reset = 0;
  end

  // generate clock to sequence tests
  always begin
    clk = 1;
    # 5; clk = 0; # 5;
  end

  // check results
  always @(negedge clk) begin
    if(MemWrite) begin
      if(DataAdr === 100 & WriteData === 25) begin
        $display("Simulation succeeded");
        $stop;
      end else if (DataAdr !== 96) begin
        $display("Simulation failed");
        $stop;
      end
    end
  end
endmodule
____
00500113
00C00193
FF718393
0023E233
0041F2B3
004282B3
02728863
0041A233
00020463
00000293
0023A233
005203B3
402383B3
0471AA23
06002103
005104B3
008001EF
00100113
00002337
00910133
0221A023
00210063

____
mi pipeline
`timescale 1ns / 1ps

module pipeline(input  clk, reset,
                   output [31:0] PCF,
                   input  [31:0] InstrF,
                   output MemWriteM,
                   output [31:0] DataAdr, 
                   output [31:0] WriteDataM,
                   input  [31:0] ReadDataM);
  
  // ✅ DECLARAR TODAS LAS SEÑALES WIRE
  wire [31:0] ALUResultM;
  wire [31:0] InstrD;
  
  wire       ALUSrcE, RegWriteW,RegWriteM, ZeroE; 
  wire [1:0] ResultSrcW, ImmSrcD; 
  wire [2:0] ALUControlE; 
  wire       PCSrcE; 
  
  // wires para el hazard
  wire [4:0] Rs1E,Rs2E, RdM,RdW;
  wire [1:0] ForwardAE,ForwardBE;
  // DataAdr is connected to ALUResultM
  assign DataAdr = ALUResultM;
  
  // Controller
  controller c(
    .clk(clk),
    .reset(reset), 
    
    // Entradas desde Decode
    .op(InstrD[6:0]),
    .funct3(InstrD[14:12]),
    .funct7b5(InstrD[30]),
    
    // Entrada desde Execute
    .ZeroE(ZeroE),
    
    // Outputs - señales de control
    .ResultSrcW(ResultSrcW),
    .MemWriteM(MemWriteM),
    .PCSrcE(PCSrcE),
    .ALUSrcE(ALUSrcE),
    .RegWriteW(RegWriteW),
    .ImmSrcD(ImmSrcD),
    .ALUControlE(ALUControlE),
    
    // output para el hazard unit
    .RegWriteM(RegWriteM)
  ); 
  
  // Datapath
  datapath dp(
    .clk(clk), 
    .reset(reset), 
    
    // ========== SEÑALES DE CONTROL ==========
    .ResultSrcW(ResultSrcW),
    .PCSrcE(PCSrcE),
    .ALUSrcE(ALUSrcE),
    .RegWriteW(RegWriteW),
    .ImmSrcD(ImmSrcD),
    .ALUControlE(ALUControlE),
    
    // ========== DATOS DE MEMORIA ==========
    .ReadDataM(ReadDataM),
    
    // ========== ENTRADAS ==========
    .InstrF(InstrF),
    
    // ========== SALIDAS ==========
    .ZeroE(ZeroE),
    .PCF(PCF),
    .InstrD(InstrD),
    .ALUResultM(ALUResultM),
    .WriteDataM(WriteDataM),
    // ❌ NO INCLUIR .MemWriteM aquí - solo va al controller
    // hazardunit
    .Rs1E(Rs1E),
    .Rs2E(Rs2E),
    .RdM(RdM),
    .RdW(RdW),
    .ForwardAE(ForwardAE),
    .ForwardBE(ForwardBE)
    
      );
  
  // hazard unti
  hazard_unit hu (
    // Entradas desde el Datapath (Direcciones de registros)
    .Rs1E(Rs1E),
    .Rs2E(Rs2E),
    .RdM(RdM),
    .RdW(RdW),
    
    // Entradas desde el Controller (Señales de control)
    .RegWriteM(RegWriteM), 
    .RegWriteW(RegWriteW),
    
    // Salidas hacia el Datapath (Selectores de Mux)
    .ForwardAE(ForwardAE),
    .ForwardBE(ForwardBE)
  );
    
endmodule



