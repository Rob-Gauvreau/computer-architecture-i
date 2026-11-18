# Lab 0 — 1-Bit Full Adder

## Overview

Implemented a **1-bit full adder** using a Quartus II gate-level schematic. Inputs `A`, `B` and `Cin` produce sum `S` and carry-out `Cout`.

- **Sum:** `S = A XOR B XOR Cin`
- **Carry:** `Cout = (A AND B) OR (Cin AND (A XOR B))`

## Verification

The circuit was simulated and tested on the **Terasic DE2-115 FPGA board**, using switches as inputs and LEDs as outputs. The report documents correct results for all eight input combinations.

## Folder guide

- [**Quartus**](quartus/) — circuit design and project files.
- [**Images**](images/) — schematics, waveforms and hardware photographs.
- [**Report**](report/) — technical report and supporting details.
