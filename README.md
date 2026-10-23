# CSE 210 — Computer Architecture Sessional (BUET)

Coursework for **CSE 210: Computer Architecture Sessional**, Department of CSE, Bangladesh University of Engineering and Technology (January 2024 term), built and simulated in [Logisim](http://www.cburch.com/logisim/).

**Author:** Shahraz Hussain Siyam (2105023) · Lab group A1, Group 8

## Contents

| Folder | What's inside |
|---|---|
| `ALU/` | Assignment 1 — ALU (`ALU.circ`, submitted as Group 4) built from 7400-series ICs, with the assignment spec; `MAIN_CIRCUIT.circ` is an extended ALU prototype |
| `MIPS_Project/Simulation/` | Final project — single-cycle MIPS datapath (`mips_datapath.circ`): register file, instruction & data memory, ALU, control unit, plus the provided 8-bit ALU module |
| `MIPS_Project/Assembler/` | C++ assembler that turns MIPS assembly (`in.txt`) into machine code for the instruction ROM; `control.txt` holds the control-unit ROM image |
| `MIPS_Project/Report/` | Project report |
| `MIPS_Project/Drafts/` | Earlier register / datapath prototypes |
| `lib/` | 7400-series TTL IC library for Logisim |

## MIPS project

Supported instructions: `add, sub, and, or, nor, sll, srl, addi, subi, andi, ori, lw, sw, beq, bneq, j`.

```bash
cd MIPS_Project/Assembler
g++ -O2 -o assembler assembler.cpp
./assembler            # reads in.txt, writes out.txt
```

Load `out.txt` into the instruction memory and `control.txt` into the control ROM in `mips_datapath.circ`, then step the clock.

## Team (MIPS project)
- 2105022 — Mafruha Islam Aishi
- 2105023 — Shahraz Hussain Siyam
- 2105024 — Ridhwanul Islam
