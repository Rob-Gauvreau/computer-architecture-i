# Lab 4 — CPU Control Unit (Hardwired Instruction Decoder)

**CEG2136 — Computer Architecture I** · University of Ottawa · Spring/Summer 2024

## Overview

Designed the control-logic equations for a **hardwired CPU Control Unit** using register-transfer operations, timing states, opcode decoding, and combinational logic. This builds on the earlier ALU lab to coordinate CPU register updates, memory operations, data-bus routing, and instruction sequencing.

The laboratory's processor model uses an **8-bit datapath**, **256 × 8 memory**, and memory-reference instructions encoded as an opcode byte followed by an address byte. A sequence counter generates control timing states for display, fetch and execute phases.

## Control-signal design

The submitted report derives control equations from the timing/operation table and illustrates their implementation as individual gate-level circuits.

| Function | Control signals |
| --- | --- |
| Register transfers | `AR_Load`, `PC_Load`, `PC_Inc`, `DR_Load`, `DR_Inc`, `IR_Load` |
| Accumulator | `AC_Clear`, `AC_Load`, `AC_Inc` |
| Memory / output | `memwrite`, `OUTD_Load` |
| ALU selection | `ALU_Sel2`, `ALU_Sel1`, `ALU_Sel0` |
| Bus selection | `BusSel2`, `BusSel1`, `BusSel0` |
| Sequencing | `SC_Clear`, `Halt` |

## Diagrams and references

The organized Lab 4 archive includes:

- **19 control-signal schematics** extracted from the editable laboratory report, individually named under `images/control-signals/`
- **Expected/reference waveform** under `images/simulation/`
- **10-page lab report** in PDF and DOCX formats under `report/`
- **Control timing/selection table** in XLS and PDF formats, plus course manual, under `references/`
- **Working control-equation draft** under `notes/`
- **Quartus project header**: [`quartus/lab4.qpf`](quartus/lab4.qpf)

The report discusses the design of register control, ALU selections, and bus selections and includes the derived equations.

## Reported outcome

The report documents the control-signal circuits and equations. It notes that the final waveform simulation did not successfully run in Quartus. The waveform shown in the archive is the **expected reference**, not evidence of a completed simulation.

## Source notes

The files are preserved from the 2024 coursework, with duplicate uploads and ZIP metadata omitted. Student-number references have been redacted from the public-sharing report and working draft.
