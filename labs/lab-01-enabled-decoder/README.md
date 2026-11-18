# Lab 1 — Simple Logic Design: Enabled 2-to-4 Decoder

## Overview

Designed and verified a **3-input, 4-output combinational logic circuit** using **Altera Quartus II 13.0 SP1** and the **Terasic DE2-115 FPGA development board** (Cyclone IV E, `EP4CE115F29C7`). The circuit behaves as a **2-to-4 decoder with an active-high enable (`A`)**: when `A = 0`, all four outputs stay low; when `A = 1`, the selector inputs (`S1`, `S0`) assert exactly one output.

The design is built from **two NOT gates and four 3-input AND gates**. The original laboratory report includes the truth table, Karnaugh maps, simulated waveforms, and hardware verification photographs.

## Boolean equations

| Output | Boolean expression | Active when |
| --- | --- | --- |
| `B` | `A · ~S1 · ~S0` | `A=1, S1S0=00` |
| `C` | `A · ~S1 · S0` | `A=1, S1S0=01` |
| `D` | `A · S1 · ~S0` | `A=1, S1S0=10` |
| `E` | `A · S1 · S0` | `A=1, S1S0=11` |

### Truth table

| `A` | `S1` | `S0` | `B` | `C` | `D` | `E` |
| --- | --- | --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 | 1 | 0 | 0 |
| 1 | 1 | 0 | 0 | 0 | 1 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 | 1 |

## FPGA pin assignments

| Signal | DE2-115 interface | FPGA pin |
| --- | --- | --- |
| `A` | `SW0` | `PIN_AB28` |
| `S0` | `SW1` | `PIN_AC28` |
| `S1` | `SW2` | `PIN_AC27` |
| `B` | `LEDR0` | `PIN_G19` |
| `C` | `LEDR1` | `PIN_F19` |
| `D` | `LEDR2` | `PIN_E19` |
| `E` | `LEDR3` | `PIN_F21` |

## Verification

The lab report states that the simulated and observed outputs matched the theoretical truth table in all **8 input combinations**. Its supporting evidence includes waveform simulations and three DE2-115 photographs:

| Inputs `(A, S1, S0)` | Expected outputs | Evidence file |
| --- | --- | --- |
| `(1, 1, 1)` | `E = 1` | `images/hardware-test-111-output-e.jpg` |
| `(1, 0, 0)` | `B = 1` | `images/hardware-test-100-output-b.jpg` |
| `A = 0` | All outputs = 0 | `images/hardware-test-enable-low.jpg` |

### Schematic and simulation

- `images/enabled-decoder-schematic.png`: gate-level Quartus block diagram
- `images/functional-simulation-waveforms.png`: simulated inputs and outputs

**Asset availability:** The screenshots, photographs, and PDF/DOCX reports are included in the separate downloadable Lab 1 archive. They have not yet been committed to GitHub through the available connector; upload the binary assets into the matching `images/` and `report/` folders to complete the online portfolio.

## Editable Quartus project

| File | Description |
| --- | --- |
| `quartus/Lab1Trial1.qpf` | Quartus project file |
| `quartus/Lab1Trial1.qsf` | Target FPGA, pin assignments, and design source settings |
| `quartus/Lab1Trial1.bdf` | Editable schematic for enabled decoder |
| `quartus/Lab1Waveform1.vwf` | Waveform stimuli used for functional simulation |

To open, use **Quartus II 13.0 SP1** and load `quartus/Lab1Trial1.qpf`. The source filenames are intentionally unchanged because they are referenced by Quartus. The absolute waveform path in `.qsf` was changed to a relative path for portability. No recompilation or hardware test was performed during repository preparation.

## Source and archive notes

- Original lab date: **May 23, 2024**; original report submitted **June 2, 2024**.
- The original ZIP duplicated the standalone Quartus files and PDF, so only one copy of each was retained.
- The redundant `.vwf.temp` waveform copy and macOS `__MACOSX` metadata were excluded.
- Student ID was removed from the public-sharing copies of the PDF and editable DOCX; technical content was not intentionally changed.
