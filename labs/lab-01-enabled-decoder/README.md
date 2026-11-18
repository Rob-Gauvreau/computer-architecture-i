# Lab 1 — Enabled 2-to-4 Decoder

## Overview

Designed an **enabled 2-to-4 decoder** in Quartus II with enable `A`, selectors `S1` and `S0`, and outputs `B`, `C`, `D` and `E`.

When `A = 0`, all outputs remain low. When `A = 1`, exactly one output is asserted:

| `S1S0` | Active output |
| --- | --- |
| `00` | `B` |
| `01` | `C` |
| `10` | `D` |
| `11` | `E` |

## Verification

The decoder was simulated in Quartus and tested on the **Terasic DE2-115 FPGA board**. The report compares the observed behavior with the eight-entry truth table.

## Folder guide

- [**Quartus**](quartus/) — circuit design and project files.
- [**Images**](images/) — schematics, waveforms and hardware photographs.
- [**Report**](report/) — technical report and supporting details.
