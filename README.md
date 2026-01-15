# IOTDF-Accelerator: 128-bit High-Throughput Data Filtering Engine

![HDL](https://img.shields.io/badge/HDL-Verilog%20%2F%20SystemVerilog-orange)
![Tools](https://img.shields.io/badge/Tools-VCS%20%7C%20Verdi%20%7C%20SpyGlass-blue)
![Award](https://img.shields.io/badge/Award-1st%20Place-gold)

## 📋 Project Overview
This repository contains the hardware implementation of a high-performance **128-bit IoT Data Filtering (IOTDF)** engine. The accelerator is optimized for real-time processing of massive sensor data, supporting 7 application functions including data extraction, exclusion, and arithmetic analysis.

### 🏆 Key Achievements
* **1st Place** among 37 teams in the Practical Digital System Design (PDSD) course.
* **Total Score: 108/100** (Full marks in Algorithm, Architecture, and Functionality + bonus points for hardware performance).

## 🚀 Technical Highlights
* **128-bit Wide Datapath:** Designed for maximum throughput in data-intensive IoT environments.
* **Timing Optimization:** Implemented a **Kogge-Stone Adder (KSA)** to break critical path bottlenecks, ensuring stable operation at high frequencies.
* **Single-Cycle Logic:** Optimized FSM and parallel comparator arrays to achieve minimal cycle counts for filtering operations.
* **RTL Quality:** Achieved a **perfect 5/5 score in SpyGlass Lint & CDC** checks, ensuring a clean, industry-standard synthesizable design.

## 🏗 Hardware Architecture
### Block Diagram
*(Recommend: Replace the placeholder below with your actual architecture diagram image)*

![IOTDF Architecture Placeholder]


**Data Flow:**
`Host Interface` ➔ `128-bit Input Buffer` ➔ `KSA-based Filtering Logic` ➔ `Output Formatter` ➔ `Valid Out`

### PPA (Power, Performance, Area) Specifications
| Parameter | Value |
| :--- | :--- |
| **Technology** | TSMC 0.13um (Generic Library) |
| **Clock Period** | 4.0 ns (250 MHz) |
| **Total Area** | ~44,563 um² (~44k gates) |
| **Total Power** | 3.376 mW |
| **Sim. Time (Gate-level)** | 43,112 ns |

## 🛠 EDA Tools & Verification Flow
* **Functional Simulation:** Synopsys VCS / Verdi, ModelSim
* **Static Analysis:** Synopsys **SpyGlass** (Linting & CDC)
* **FPGA/ASIC Synthesis:** Vivado, Quartus Prime, Design Compiler
* **Verification Methodology:** * Developed a self-checking SystemVerilog testbench.
    * Integrated **Python-based Golden Models** for automated result comparison.
    * Validated against 100% of hidden test cases provided by the PDSD course.

## 📁 Repository Structure
* `rtl/` : Verilog source files (Top-level, Datapath, Control Unit, KSA).
* `sim/` : Testbench, file-I/O scripts, and simulation logs.
* `syn/` : Synthesis constraints (SDC) and area reports.
* `scripts/` : Python modeling and verification scripts.
* `doc/` : Design report and architectural analysis.

## 👤 Author
**Mi-Ya Yeh, HUNG,HAN-LIN** - National Sun Yat-sen University (NSYSU)
* **Role:** Team Leader
* **Responsibilities:** System architecture, KSA implementation, timing closure, and SpyGlass Lint/CDC verification.
