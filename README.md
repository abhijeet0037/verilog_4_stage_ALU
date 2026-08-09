# 16-bit 4-Stage Pipelined ALU

A 16-bit Arithmetic Logic Unit (ALU) implemented in Verilog HDL using a
4-stage pipeline architecture.

This project demonstrates RTL design, synchronous pipelining, register
transfer between pipeline stages, ALU operation execution, and functional
verification using Verilog testbenches and waveform analysis.

---

## 📌 Project Overview

The objective of this project is to design a 16-bit pipelined ALU capable
of performing arithmetic and logical operations while dividing the
datapath into multiple sequential stages.

Instead of performing the complete operation in a single clock cycle,
the design uses four pipeline stages. This allows multiple operations
to be processed concurrently, improving the overall throughput of the
ALU.

---

## ⚙️ Key Features

- 16-bit datapath
- 4-stage pipelined architecture
- Synchronous design using clocked registers
- Arithmetic and logical ALU operations
- Verilog HDL RTL implementation
- Dedicated verification testbenches
- Simulation waveform analysis
- Modular project organization
- Functional verification through simulation

---

## 📁 Project Structure

verilog_4_stage_ALU/
│
├── verilog_ALU/
│   │
│   ├── RTL Design/
│   │   └── ALU_pipe_line.v
│   │
│   ├── Test Benches/
│   │   ├── alu_pl_tb1.v
│   │   └── alu_tb2_pl.v
│   │
│   ├── Images/
│   │   ├── ALU_datapath.png
│   │   └── Block_diagram.png
│   │
│   ├── Waveforms/
│   │   ├── pipe1.vcd
│   │   ├── pipeline.vcd
│   │   ├── waveform_tb1.png
│   │   └── waveform_tb2.png
│   │
│   └── Project Report/
│
└── README.md

---

## 🏗️ Architecture

The ALU is organized as a **4-stage pipeline**:

```text
        Input Operands
              │
              ▼
      ┌─────────────────┐
      │    Stage 1      │
      │ Input / Operand │
      │   Registration  │
      └────────┬────────┘
               │
               ▼
      ┌─────────────────┐
      │    Stage 2      │
      │ ALU / Partial   │
      │   Computation   │
      └────────┬────────┘
               │
               ▼
      ┌─────────────────┐
      │    Stage 3      │
      │  Intermediate   │
      │   Registration  │
      └────────┬────────┘
               │
               ▼
      ┌─────────────────┐
      │    Stage 4      │
      │ Output / Result │
      │   Registration  │
      └────────┬────────┘
               │
               ▼
          ALU Result

