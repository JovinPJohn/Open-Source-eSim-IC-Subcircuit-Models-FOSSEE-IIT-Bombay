# Open Source eSim IC Subcircuit Models — FOSSEE, IIT Bombay

Contributor: Jovin P. John
Program: Semester-Long Internship, Autumn 2025
Title: Designing Integrated Circuit in eSim
Institute: Albertian Institute of Science and Technology, Kalamassery, Kerala
Guide: Prof. Prabhu Ramachandran, Aerospace Engineering Department, IIT Bombay
Mentors: Mr. Sumanto Kar, Mr. Varad Patil, Ms. Shanthi Priya K, Mr. Aditya M

## About FOSSEE and eSim: Building on Open Source

FOSSEE (Free/Libre and Open Source Software for Education) is an initiative based at IIT Bombay, established to reduce dependency on proprietary software in engineering education and research by promoting free, open-source alternatives. FOSSEE offers documentation, tutorials, and hands-on training to help students and professionals adopt open-source tools in place of costly commercial software.

eSim, developed by FOSSEE, is a fully open-source EDA (Electronic Design Automation) platform that combines schematic creation, circuit simulation, and PCB design into one integrated tool — free to use, with no licensing cost, unlike proprietary EDA suites. eSim integrates several open-source technologies under one roof:

- NgSpice — an open-source SPICE simulator for analog, digital, and mixed-signal circuits
- KiCad — used for schematic-to-netlist conversion and PCB design within eSim
- Makerchip — an open-source-integrated platform for Verilog/SystemVerilog simulation
- GHDL — an open-source VHDL simulator integrated into the eSim ecosystem

By combining these tools into a single, free, and accessible platform, eSim directly addresses a gap in the open-source EDA space, where most existing tools are either simulation-only or design-only, and rarely both, and almost never free.

## Project Objective

The objective of this internship was to design and develop analog and digital integrated circuit models as sub-circuits using device model files already present in the eSim library, so that they could be integrated into the open-source eSim subcircuit library for free use by future developers, students, and researchers.

## Methodology (Open Source Design Workflow)

Each IC was developed following a systematic, fully open-source workflow:

1. Datasheet Analysis — Reviewed official datasheets from manufacturers (Texas Instruments, Fairchild Semiconductor, National Semiconductor) to identify ICs not yet available in the open-source eSim library
2. Subcircuit Creation — Modeled each IC as a subcircuit in eSim using open-source device model files, strictly adhering to datasheet specifications, including accurate symbol and pin diagrams
3. Test Circuit Design — Built test circuits in eSim to verify each subcircuit's functionality against expected datasheet behavior
4. Schematic Testing — Used KiCad (open source) to convert designs into NgSpice (open source) netlists, then ran simulations to validate outputs, iterating until results matched datasheet specifications

This entire pipeline — from schematic capture to simulation to verification — was carried out using free and open-source tools exclusively, with zero dependency on proprietary EDA software.

## The 10 ICs Contributed to the Open-Source eSim Library

| # | IC | Description |
|---|----|-----------  |
| 1 | 74HC283 | High-speed CMOS 4-bit binary full adder with fast carry, used in ALUs and high-speed computing systems |
| 2 | 74LS352 | Dual 4-line to 1-line data selector/multiplexer with independent enable inputs |
| 3 | 74F521 | 8-bit identity comparator for high-speed comparison of two 8-bit words |
| 4 | CD4519BM | CMOS 4-bit AND/OR selector for logic operations on two 4-bit words |
| 5 | 74S140 | Dual 4-input NAND gate with Schottky-clamped transistors for high-speed operation |
| 6 | SN7444A | Gray-to-Decimal decoder converting 4-bit Gray code into 1-of-10 decimal output |
| 7 | SN7443A | Excess-3-to-Decimal decoder for self-complementing binary arithmetic systems |
| 8 | 74F64 | 4-2-3-2-input AND-OR-INVERT gate for efficient sum-of-products logic |
| 9 | 74133 | 13-input NAND gate for detecting simultaneous presence of multiple status signals |
| 10 | 74S51 | Dual 2-wide 2-input AND-OR-INVERT gate with Schottky-clamped transistors |

Each IC in this list was designed as a subcircuit, verified through a dedicated test circuit, and validated using input/output waveform simulation in NgSpice, with results cross-checked against manufacturer datasheets from Texas Instruments and Fairchild Semiconductor.

## Why This Matters for Open Source

Every one of these 10 IC models is released back into the eSim open-source subcircuit library, meaning they are freely available for any student, researcher, or developer worldwide to use in their own circuit designs, at zero licensing cost. This directly supports FOSSEE's mission of reducing dependency on proprietary EDA software in engineering education. Prior to this contribution, none of these ICs existed in the open-source eSim library — this work expands what is freely available to the global open-source hardware design community, one verified, datasheet-accurate model at a time.
