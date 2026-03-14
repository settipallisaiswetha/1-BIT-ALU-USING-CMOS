# 1-Bit ALU Using CMOS in NI Multisim

## Project Overview
This project implements a **1-bit Arithmetic Logic Unit (ALU)** using **CMOS logic design** in **NI Multisim**.  
The ALU performs multiple logical and arithmetic operations using CMOS transistor-level circuits, and the required output is selected through an **8:1 Multiplexer**.

## Features
The ALU supports the following operations:

- AND
- OR
- XOR
- CARRY
- DIFFERENCE
- BORROW
- INVERTER
- PASSTHROUGH

These outputs are connected to an **8:1 MUX**, and the selected output is displayed through an **LED**.

## Software Used
- **NI Multisim**

## Components Used
- NMOS transistors
- PMOS transistors
- Interactive digital constants for inputs
- 8:1 Multiplexer
- LED
- 220Ω resistor
- VDD supply (5V)
- Ground

## Inputs
The circuit uses the following inputs:

- **A**
- **B**
- **Select lines:** `S2, S1, S0`
- **Enable pin** for MUX (`~G`)

## Output
- Final ALU output is taken from the **MUX output**
- Output is observed using an **LED**

## Functional Blocks
The CMOS ALU is divided into multiple transistor-level blocks:

1. **AND block**
2. **OR block**
3. **XOR block**
4. **Carry block**
5. **Difference block**
6. **Borrow block**
7. **Inverter block**
8. **Passthrough block**

Each block generates one output, and all outputs are connected to the **MUX_8TO1**.

## MUX Selection Table

| S2 | S1 | S0 | Selected Output |
|----|----|----|-----------------|
| 0  | 0  | 0  | AND             |
| 0  | 0  | 1  | OR              |
| 0  | 1  | 0  | XOR             |
| 0  | 1  | 1  | CARRY           |
| 1  | 0  | 0  | DIFFERENCE      |
| 1  | 0  | 1  | BORROW          |
| 1  | 1  | 0  | INVERTER        |
| 1  | 1  | 1  | PASSTHROUGH     |

## Circuit Operation
- CMOS transistor networks generate individual logic/arithmetic outputs.
- These outputs are connected to the data inputs `D0` to `D7` of the **8:1 multiplexer**.
- The select lines choose which function appears at the MUX output.
- The selected output is indicated by an LED.

## Power Supply
- **VDD = 5V**
- Proper ground connections are used for all CMOS stages.

## How to Simulate
1. Open the project in **NI Multisim**.
2. Verify all VDD and GND connections.
3. Set input values for **A** and **B** using interactive digital constants.
4. Set select lines `S2, S1, S0`.
5. Ensure MUX enable `~G = 0`.
6. Run the simulation.
7. Observe the result on the LED.

## Notes
- The MUX enable pin must be active low (`~G = 0`) for proper operation.
- Long wires should be checked carefully to avoid accidental junction errors.
- Each CMOS block should be tested individually before testing the full ALU.

## Applications
- Digital system design
- Arithmetic and logic unit study
- CMOS logic implementation
- VLSI and transistor-level learning

## Conclusion
This project demonstrates the design of a **1-bit ALU using CMOS logic** in NI Multisim.  
It combines transistor-level logic design with multiplexer-based function selection, making it useful for understanding both **digital electronics** and **CMOS circuit implementation**.

