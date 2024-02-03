# Processor Simulation Project

Welcome to the Spicy Von Neumann Fillet with Extra Shifts processor simulation project! This project involves simulating a fictional processor design and architecture using Java. Below you will find details on the memory architecture, instruction set architecture, datapath, program flow, and printing requirements for this package.

## Memory Architecture

- **Architecture:** Von Neumann
  - Program and data stored in the same memory.
- **Memory Size:** 2048 * 32
  - Main Memory:
    - Addresses from 0 to 1023: Program Instructions
    - Addresses from 1024 to 2047: Data
- **Registers:** 33
  - 31 General-Purpose Registers (R1 to R31)
  - 1 Zero Register (R0)
  - 1 Program Counter (PC)

## Instruction Set Architecture

- **Instruction Size:** 32 bits
- **Instruction Types:** R-Format, I-Format, J-Format
- **Instruction Count:** 12

| Name              | Mnemonic | Type | Format | Operation                         |
|-------------------|----------|------|--------|-----------------------------------|
| Add               | ADD      | R    | R      | R1 = R2 + R3                     |
| Subtract          | SUB      | R    | R      | R1 = R2 - R3                     |
| Multiply Immediate| MULI     | I    | I      | R1 = R2 * IMM                    |
| Add Immediate     | ADDI     | I    | I      | R1 = R2 + IMM                    |
| Branch if Not Equal| BNE      | I    | I      | IF(R1 != R2) { PC = PC+1+IMM }  |
| And Immediate     | ANDI     | I    | I      | R1 = R2 & IMM                    |
| Or Immediate      | ORI      | I    | I      | R1 = R2 \| IMM                   |
| Jump              | J        | J    | J      | PC = PC[31:28] \| ADDRESS        |
| Shift Left Logical| SLL      | R    | R      | R1 = R2 << SHAMT                 |
| Shift Right Logical| SRL     | R    | R      | R1 = R2 >>> SHAMT                |
| Load Word         | LW       | I    | I      | R1 = MEM[R2 + IMM]               |
| Store Word        | SW       | I    | I      | MEM[R2 + IMM] = R1               |

## Datapath

- **Stages:** 5 (IF, ID, EX, MEM, WB)
- **Pipeline:** 4 instructions (maximum) running in parallel

## Program Flow

1. Write the program in assembly language in a text file.
2. Read instructions from the text file and parse them.
3. Store parsed instructions in memory.
4. Start execution by fetching the first instruction at Clock Cycle 1.
5. Continue execution following the provided pattern in the Datapath section.
6. Simulate clock cycles by incrementing a variable.

## Printings

- Print Clock Cycle number.
- Print Pipeline stages: Which instruction is at each stage, input parameters/values.
- Print updates to registers and memory.
- Print content of all registers and memory after the last clock cycle.

---

This README provides comprehensive information on the Spicy Von Neumann Fillet with Extra Shifts processor simulation project. Follow the instructions carefully to successfully implement the simulated processor and meet project requirements.
