# Lab 2 — Sequential Logic: Synchronous Counters

**CEG2136 Computer Architecture I** · University of Ottawa · Spring/Summer 2024

## Project overview

Designed **synchronous counters with JK flip-flops** and derived their excitation equations using state tables and Karnaugh maps. The laboratory covers a **BCD (modulo-10) counter**, a **modulo-6 counter**, and their cascade into a **modulo-60 counter**. The original report includes Quartus II 13.0 SP1 schematics, simulation results and discussion of implementation challenges.

| Circuit | State sequence | Key logic |
| --- | --- | --- |
| BCD (modulo-10) counter | 0–9 | Four JK flip-flops, enable, reset, rollover |
| Modulo-6 counter | 0–5 | Three JK flip-flops, enable, reset, rollover |
| Cascaded modulo-60 counter | 0–59 | Connected BCD and modulo-6 counter symbols |

### Design and simulation images

The organized archive contains five distinct image files; duplicate PNGs have been removed:

| File in `images/` | Content |
| --- | --- |
| `bcd-counter-schematic.png` | Four-flip-flop BCD counter schematic |
| `bcd-counter-waveforms.png` | BCD counter waveform simulation |
| `modulo-6-counter-schematic.png` | Three-flip-flop modulo-6 schematic |
| `modulo-60-counter-schematic.png` | Hierarchical BCD/modulo-6 design |
| `modulo-60-counter-waveforms.png` | Cascaded counter waveform simulation |

## Available editable Quartus sources

| File | Purpose |
| --- | --- |
| `quartus/bcd-counter/FunctionalSimulationBCDCounterLab2.bdf` | BCD counter gate-level schematic |
| `quartus/bcd-counter/FunctionWaveformLab2BCDCounter.vwf` | BCD waveform stimuli |
| `quartus/modulo-6-counter/WaveformLab2Modulo6.vwf` | Modulo-6 waveform stimuli |
| `quartus/modulo-6-counter/Modulo6Counter.qpf` | Quartus project header, renamed from `Lab2 - Copy.qpf` to match its revision |

**Project completeness:** These uploads do **not** comprise a complete independently compilable Quartus project. The original modulo-6 `.qsf` and `.bdf`, counter symbol files (`.bsf`), and the top-level modulo-60 source schematic were not provided. The corresponding designs are visible in the PDF and screenshot evidence, but they are not substituted with invented source files.

## Documentation

The accompanying **10-page lab report** includes a JK flip-flop excitation table, counter state/excitation tables, Karnaugh maps, counter diagrams, and the author's discussion of simulations. The public-sharing PDF has the student number redacted from the first page.

The report and five images are preserved in the companion Lab 2 ZIP and are **not yet uploaded to GitHub**. Their target paths are `report/lab-02-synchronous-counters-report.pdf` and `images/` respectively.

## Verification notes

The report states that the sequential circuits were successfully designed and simulated. This repository is an archival copy of those materials; **no new simulation, compilation or hardware test was performed**.

The ZIP originally supplied contained only a duplicate PDF and `.qpf`; the other files were uploaded separately. Two pairs of screenshot images were visually identical and were deduplicated. The schematic and waveform filenames remain unchanged to avoid breaking potential Quartus references.
