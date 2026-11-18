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

The laboratory archive includes five design and waveform images:

| File in `images/` | Content |
| --- | --- |
| `bcd-counter-schematic.png` | Four-flip-flop BCD counter schematic |
| `bcd-counter-waveforms.png` | BCD counter waveform simulation |
| `modulo-6-counter-schematic.png` | Three-flip-flop modulo-6 schematic |
| `modulo-60-counter-schematic.png` | Hierarchical BCD/modulo-6 design |
| `modulo-60-counter-waveforms.png` | Cascaded counter waveform simulation |

## Quartus source files

| File | Purpose |
| --- | --- |
| `quartus/bcd-counter/FunctionalSimulationBCDCounterLab2.bdf` | BCD counter gate-level schematic |
| `quartus/bcd-counter/FunctionWaveformLab2BCDCounter.vwf` | BCD waveform stimuli |
| `quartus/modulo-6-counter/WaveformLab2Modulo6.vwf` | Modulo-6 waveform stimuli |
| `quartus/modulo-6-counter/Modulo6Counter.qpf` | Quartus project header, renamed from `Lab2 - Copy.qpf` to match its revision |

## Documentation

The accompanying **10-page lab report** includes a JK flip-flop excitation table, counter state/excitation tables, Karnaugh maps, counter diagrams, and the author's discussion of simulations. The public-sharing PDF has the student number redacted from the first page.

The report and five images are preserved in the companion Lab 2 ZIP and are **not yet uploaded to GitHub**. Their target paths are `report/lab-02-synchronous-counters-report.pdf` and `images/` respectively.

## Results

The laboratory report documents the counter designs, state tables, excitation equations, and functional simulation results. The BCD and modulo-6 designs were combined into a modulo-60 counter.
