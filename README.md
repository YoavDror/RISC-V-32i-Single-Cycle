# RISC-V 32I Single-Cycle Processor

This repository contains a complete **single-cycle RISC-V 32I processor**, designed and implemented in **SystemVerilog**.

---

## Project Goals

- Understand the RISC-V 32I ISA at the bit level  
- Translate instruction formats into real hardware  
- Design a clean, modular CPU datapath  
- Run real assembly programs on a custom processor  
- Demonstrate how software and hardware connect end-to-end  

---

## What This Processor Supports

- **ISA:** RISC-V RV32I  
- **Instruction Types:**
  - R-type  
  - I-type (Arithmetic, Load, JALR)  
  - S-type  
  - B-type  
  - U-type (LUI, AUIPC)  
  - J-type (JAL)  
- **Execution Model:** Single-cycle  
- **Memory:**
  - Byte-addressable instruction memory  
  - Byte-addressable data memory  
- **Simulation:** ModelSim / Questa  

---

## Architecture Overview

The processor is built from clearly separated, reusable blocks:

- Instruction Memory  
- Fetch  
- Decode  
- Register File  
- ALU
- Data Memory 
- Branch Control
- Control Unit  
- Top-Level Integration  

All shared definitions (opcodes, ALU operations, memory sizes, control signals) are centralized in a **SystemVerilog package**, keeping the design clean, readable, and scalable.

---

## Programs Executed on This Processor

The processor successfully runs the following programs end-to-end:

### Maximum Value Finder
Iterates through an array and stores the maximum value.

### Fibonacci Sequence Generator
Computes Fibonacci numbers iteratively and stores them in memory.

### Bubble Sort Algorithm
Sorts an array using nested loops, comparisons, branches, and swaps.

Each program includes: 
- Pseudocode  
- RISC-V assembly  
- 32-bit machine-code encoding in hexadecimal 

---

## How to Run the Simulation

### Requirements
- All RTL source files  
- A testbench  
- `machine_code.mem` file with hexadecimal instructions  

### Steps
1. Paste the desired program’s hex machine code into `machine_code.mem`.
2. Open **ModelSim / Questa**.
3. Change directory to the project folder.
4. Compile all files.
5. Run the testbench.
6. Inspect:
   - Program Counter  
   - Register File  
   - Data Memory contents  
   - ALU and control signals  

---

## Author

**Yoav Dror**  
Design Verification Engineer  
B.Sc Electrical Engineering  
