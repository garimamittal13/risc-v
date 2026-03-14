# RISC-V Processor Design in Verilog

A Verilog-based implementation of **RISC-V processor architectures**, including both **sequential** and **pipelined** designs.

## Overview

This repository contains two implementations of a RISC-V processor:

- a **sequential processor**
- a **pipelined processor**

The project focuses on understanding how instruction execution differs between a non-pipelined and a pipelined CPU design, and how pipelining improves throughput by overlapping instruction stages.

## Repository Structure

```text
risc-v/
├── pipelined/
│   └── src/
├── seqential/
│   └── src/
├── README.md
└── project_report_team_10.pdf
```

> Note: The folder is currently named `seqential/` in the repository.

## Implementations

### 1. Sequential RISC-V Processor
The sequential design executes one instruction at a time, completing all stages of execution before starting the next instruction.

This implementation helps in understanding:
- the instruction execution cycle
- datapath and control flow
- how registers, ALU, memory, and control logic interact in a simple CPU

### 2. Pipelined RISC-V Processor
The pipelined design overlaps instruction execution across multiple stages to improve throughput.

This implementation focuses on:
- stage-wise instruction flow
- improved execution efficiency
- modular datapath organization
- architectural comparison with the sequential baseline

## Project Goals

- implement RISC-V processor logic in Verilog
- compare sequential and pipelined execution models
- understand datapath/control design in CPU architecture
- study how pipelining affects performance and throughput

## Tech Stack

- **Language:** Verilog
- **Domain:** Computer Architecture / Digital Design

## How to Use

### 1. Clone the repository

```bash
git clone https://github.com/garimamittal13/risc-v.git
cd risc-v
```

### 2. Open the source folders

Sequential design:
```text
seqential/src/
```

Pipelined design:
```text
pipelined/src/
```

### 3. Simulate the design

Use your preferred Verilog simulator, such as:
- Icarus Verilog
- ModelSim
- Vivado Simulator

A typical Icarus Verilog flow looks like this:

```bash
iverilog -o cpu_sim *.v
vvp cpu_sim
```

If your design includes a dedicated testbench file, compile it together with the relevant source files.

### 4. Inspect outputs
Use simulation output and waveform viewers such as GTKWave to debug and analyze processor behavior.

Example:

```bash
gtkwave dump.vcd
```

## Report

The repository includes a project report:

```text
project_report_team_10.pdf
```

This report documents the architecture, implementation details, and comparison between the two processor designs.

## Why this project matters

This project demonstrates:

- processor design from scratch in Verilog
- understanding of RISC-V instruction execution
- comparison of sequential vs pipelined architectures
- modular digital system design
- practical application of computer architecture concepts

## Future Improvements

Potential extensions include:

- hazard detection and forwarding analysis
- branch handling improvements
- better testing and automated testbenches
- waveform examples in the repository
- support for more RISC-V instructions

## Repository

GitHub: [garimamittal13/risc-v](https://github.com/garimamittal13/risc-v)
