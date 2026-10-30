# 6T-SRAM-Cell-Design-and-Analysis

This repository contains the **design, simulation, and functional analysis of a 6-Transistor (6T) SRAM cell** implemented at the **transistor level** using **GPDK 180 nm CMOS technology** in **Cadence Virtuoso**.  
The project was carried out as a **personal learning initiative** to gain hands-on understanding of SRAM cell operation and stability considerations.

---

## Project Overview

- Designed a standard **6T SRAM cell** using cross-coupled CMOS inverters and access transistors  
- Performed **functional verification** for:
  - Hold ‘0’ and Hold ‘1’
  - Write ‘0’ and Write ‘1’
  - Read ‘0’ and Read ‘1’
- Analyzed SRAM behavior using **transient simulations**
- Justified transistor sizing using **Cell Ratio (CR)** and **Pull-up Ratio (PR)**

---

## Tools and Technology

- **EDA Tool:** Cadence Virtuoso  
- **Process Technology:** GPDK 180 nm CMOS  
- **Design Level:** Transistor-level schematic  
- **Simulations:** Transient analysis  

---

## Transistor Sizing

| Transistor Type | Width |
|-----------------|-------|
| Access NMOS (WA) | 2 µm |
| Pull-up PMOS (WP) | 2.4 µm |
| Pull-down NMOS (WN) | 3 µm |

- **Cell Ratio (CR) = 1.5** → Ensures read stability  
- **Pull-up Ratio (PR) = 1.2** → Ensures write ability  

---

## Simulation Methodology

- Internal storage nodes **Q and QB were initialized** to define logic ‘0’ or logic ‘1’
- Word line (WL) was asserted to observe read and write behavior
- Bit-line response (**BL / BLB**) was monitored during read operations
- Hold mode was verified with WL disabled  

---

## Key Observations

- Correct functional behavior observed for **hold, write, and read operations**
- No unintended data flipping during read operations
- Internal nodes remained stable, confirming **non-destructive read**
- Simulation waveforms were clean, consistent, and repeatable

---

## Repository Structure

6T-SRAM-Cell-Design-and-Analysis/
- results/
   - 6T_SRAM_Transistor_Level_Schematic.png
   - Hold_0_and_Hold_1_Waveforms.png
   - Read_0_Waveform.png
   - Read_1_Waveform.png
   - Write_0_and_Write_1_Waveforms.png
- 6T_SRAM_Cell_Design_and_Analysis.pdf
- README.md

---

## Future Work

- Static Noise Margin (SNM) extraction using butterfly curves  
- SRAM array-level implementation 

---

