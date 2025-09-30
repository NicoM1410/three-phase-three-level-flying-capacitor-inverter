# Design and Analysis of a Three-Phase Three-Level Flying Capacitor Inverter

This repository contains the design and analysis of a **three-phase three-level flying capacitor inverter (FCI)**, developed for railway applications operating at non-standard frequencies (16.7 Hz, German railway system).  
The project includes simulations, efficiency analysis, thermal evaluation, and spectral studies carried out using **PLECS**.

---

## Abstract
The main objective of this work is to design a power conversion system that combines **energy efficiency, waveform quality, and thermal reliability**.  
The inverter topology reduces voltage stress on switching devices and improves output waveform quality.  
The analysis includes:
- Phase-shifted sinusoidal PWM (PS-SPWM) control  
- Flying capacitor voltage balancing  
- Thermal modeling of SiC MOSFETs  
- Efficiency curve evaluation and harmonic distortion analysis  

---

## Specifications
- **Topology:** Three-phase three-level flying capacitor inverter  
- **DC-Link Voltage:** 1000 V  
- **Output Power:** 15 kW  
- **Line-to-Line Voltage:** 400 V (RMS)  
- **Switching Frequency:** 20 kHz  
- **Power Factor:** 0.9  
- **Semiconductors:** SiC MOSFET ABB/Hitachi 5SFG0780B12000x + body diode  
- **ON Resistance (Ron):** ~10 mΩ (simulation model)  
- **Ambient Temperature:** 40 °C (max junction temp 100 °C)  
- **DC-Link Capacitors:** 2 × 100 µF (split to 500 V each)  
- **Flying Capacitor:** 100 µF  

---

## Results
- Maximum efficiency: **97.45% full load**  
- Four-point efficiency: **96.17%**  
- European efficiency: **94.80%**  
- Low THD on phase current due to R–L load filtering (no external output filter)  
- Spectral analysis: PS-SPWM with two carriers phase-shifted by 180° → only **even harmonics of fsw** (40 kHz, 80 kHz…) in voltage spectrum; phase current remains nearly sinusoidal  
- Thermal performance within safe operating margins (switching losses dominate conduction losses)  

---

## Repository Content
- `Final_Project.pdf` → Full project report with figures and explanations  
- `FinalProject.plecs` → Simulation model in PLECS  
- `README.md` → Project documentation (this file)  

---

## How to Run the Simulation
1. Open `FinalProject.plecs` with **PLECS 4.9 or later**.  
2. Run the time-domain simulation.  
3. View plots of voltages, currents, THD, and efficiency.  

---

## Authors
- **Niccolò Mazzocchi** – University of Bologna  
- **Riccardo Salvardi** – University of Bologna  

---

## License
This project is provided for academic and educational purposes.  
No commercial use without permission.  
