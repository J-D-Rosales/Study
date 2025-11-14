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

endmodule