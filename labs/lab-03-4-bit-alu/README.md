# Lab 3 — 4-Bit Arithmetic Logic Unit (ALU)

**CEG2136 — Computer Architecture I** · University of Ottawa · Spring/Summer 2024

## Overview

Developed a hierarchical **4-bit arithmetic logic unit** using Quartus II schematic blocks and functional waveform simulation. The ALU combines arithmetic, bitwise logic, and shifting functions from reusable 1-bit building blocks, then extends them to a 4-bit design.

The project demonstrates:
- **Arithmetic:** addition/subtraction using multiplexer-selected inputs and full-adder stages
- **Logic:** bitwise AND, OR and XOR with operation selection
- **Shifting:** 1-bit and 4-bit shift configurations
- **Status flags:** carry, zero, negative and overflow
- **Top-level verification:** input generation, integrated ALU and checker logic

## Design hierarchy and results

| Component | Design screenshot | Waveform screenshot |
| --- | --- | --- |
| 1-bit shift unit | `shift-1bit-schematic.png` | `shift-1bit-waveforms.png` |
| 4-bit shift unit | `shift-4bit-schematic.png` | `shift-4bit-waveforms.png` |
| 1-bit logic unit | `logic-1bit-schematic.png` | `logic-1bit-waveforms.png` |
| 4-bit logic unit | `logic-4bit-schematic.png` | `logic-4bit-waveforms.png` |
| 1-bit arithmetic unit | `arithmetic-1bit-schematic.png` | `arithmetic-1bit-waveforms.png` |
| 4-bit arithmetic unit | `arithmetic-4bit-schematic.png` | `arithmetic-4bit-waveforms.png` |
| Integrated 4-bit ALU | `alu-4bit-schematic.png` | `alu-4bit-waveforms.png` |
| Top-level simulation | `top-level-simulation-schematic.png` | `top-level-simulation-waveforms.png` |

An additional top-level checker schematic and expanded checker waveform image document the simulation and verification sequence.

## Laboratory observations

The simulated individual ALU components and combined datapath are presented in the laboratory report. The report also documents **intermittent nonzero `chk` values** in the top-level checker where zero was expected; these observations are preserved as originally reported.

## Files

- [`quartus/ALU1.qpf`](quartus/ALU1.qpf) — original Quartus project file
- `images/diagrams/` — nine circuit and checker diagrams
- `images/waveforms/` — nine waveform screenshots
- `report/lab-03-4-bit-alu-report.pdf` — 12-page lab report
- `report/lab-03-4-bit-alu-report.docx` — editable report

**Source files and image/report organization:** The 18 PNGs and PDF/DOCX report are bundled in the separate Lab 3 ZIP for upload into the paths shown above. The available GitHub connection has published the README and Quartus project file.

**Software:** Altera Quartus II 13.0 Service Pack 1. The original lab report also lists the Terasic DE2-115 development board.
