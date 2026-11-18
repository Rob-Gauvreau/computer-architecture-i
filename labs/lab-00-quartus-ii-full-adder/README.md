# Lab 0 — Quartus II Introduction: 1-Bit Full Adder

## Overview

Implemented and verified a **1-bit full adder** as a gate-level block diagram using **Altera Quartus II 13.0 SP1** and a **Terasic DE2-115** FPGA development board (Cyclone IV E, `EP4CE115F29C7`). The exercise covers Boolean minimization, waveform simulation, pin assignment, compilation, and hardware verification.

## Logic

Three inputs (`A`, `B`, `Cin`) generate a sum (`S`) and carry-out (`Cout`):

- **Sum:** `S = A XOR B XOR Cin`
- **Carry-out:** `Cout = (A AND B) OR (Cin AND (A XOR B))`

The report derives the truth table/Karnaugh maps and documents all eight input combinations.

## Board mapping

| Signal | DE2-115 interface | FPGA pin |
| --- | --- | --- |
| `A` | `SW0` | `PIN_AB28` |
| `B` | `SW1` | `PIN_AC28` |
| `Cin` | `SW2` | `PIN_AC27` |
| `S` | `LEDR0` | `PIN_F19` |
| `Cout` | `LEDR1` | `PIN_G19` |

## Results

The submitted report documents agreement between theoretical and experimental full-adder outputs for **all 8 input combinations**. Quartus compilation succeeded on May 16, 2024. The design is combinational and uses no dedicated logic registers.

### FPGA verification

| Test inputs `(A, B, Cin)` | Expected `(S, Cout)` |
| --- | --- |
| `(1, 0, 0)` | `(1, 0)` |
| `(1, 1, 0)` | `(0, 1)` |
| `(1, 1, 1)` | `(1, 1)` |

The original screenshot evidence, hardware photographs, and PDF report are organized in the downloadable Lab 0 archive. Their binary uploads to this repository are still pending.

## Project files

Editable Quartus sources are under [`quartus/`](quartus/):

| File | Purpose |
| --- | --- |
| `LAB0REBUILT.qpf` | Quartus project and revision |
| `LAB0REBUILT.qsf` | Device selection, pin assignments and design sources |
| `LAB0REBUILT.bdf` | Editable gate-level schematic |
| `Waveform001.vwf` | Waveform stimulus and simulation setup |

To open the design, launch **Quartus II 13.0 SP1**, then open `quartus/LAB0REBUILT.qpf`. The original filenames are preserved because Quartus references them internally. A workstation-specific absolute waveform path in the `.qsf` was converted to a relative path. The project has not been recompiled after packaging.

## Source notes

The design and results are from May 2024. Duplicate files and macOS metadata were removed from the organized archive. For public sharing, student numbers were redacted from the report cover. The original report is retained separately in the uploaded source materials.
