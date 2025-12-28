# High-Efficiency 1.8 GHz RF Wireless Power Transfer System

This repository presents the complete design and simulation of a **1.8 GHz RF Wireless Power Transfer (WPT) system**, developed as part of an academic research project. The work focuses on achieving **high RF-to-DC conversion efficiency** through careful co-design of the antenna, impedance matching network, and nonlinear rectifier.

The proposed system achieves a **peak RF-to-DC Power Conversion Efficiency (PCE) of 88.23%**, verified using combined electromagnetic (EM) and nonlinear circuit simulations. The design targets **low-power wireless energy harvesting and IoT applications**, where efficiency, compactness, and practical implementation are key requirements.

This project was jointly carried out by **Harish Arjun** and **Avinash Tanti** as part of their postgraduate studies.

---

## 1. Motivation and Scope

Wireless Power Transfer (WPT) enables the delivery of electrical energy without physical interconnections, offering a promising alternative to conventional battery-powered systems. Among various WPT approaches, RF-based techniques provide flexibility in transmission distance, system integration, and scalability. However, the overall efficiency of RF-WPT systems is strongly influenced by antenna characteristics, impedance matching accuracy, and the nonlinear behavior of RF rectifiers.

The scope of this project is to design and simulate a **far-field RF WPT system operating at 1.8 GHz**, with emphasis on:
- Efficient microstrip patch antenna design
- Accurate characterization of nonlinear rectifier impedance
- Smith-chart-based impedance matching at low input power levels
- End-to-end system integration and performance evaluation

---

## 2. System Overview

The implemented WPT system consists of the following functional blocks:

1. **RF Excitation Source**  
   A continuous-wave RF signal at 1.8 GHz representing the transmitting stage.

2. **Transmitting and Receiving Antennas**  
   Identical rectangular microstrip patch antennas designed on an FR-4 substrate to ensure consistent impedance behavior and stable radiation characteristics.

3. **Impedance Matching Network**  
   A lumped-element network synthesized using Smith chart techniques to transform the nonlinear rectifier input impedance to 50 Ω at the operating frequency.

4. **RF Rectifier**  
   A Schottky-diode-based voltage doubler circuit that converts the received RF signal into DC power.

5. **Load Interface**  
   A resistive load optimized to maximize RF-to-DC conversion efficiency.

All subsystems are evaluated together to accurately capture electromagnetic effects, impedance interactions, and nonlinear rectification behavior.

---

## 3. Key Design Specifications

| Parameter | Value |
|---------|------|
| Operating Frequency | 1.8 GHz |
| Antenna Type | Rectangular microstrip patch |
| Substrate Material | FR-4 |
| System Impedance | 50 Ω |
| Input RF Power | 5 dBm |
| Optimal Load Resistance | 2.7 kΩ |
| Antenna Gain | ≈ 3 dBi |
| Peak RF-to-DC Efficiency | **88.23%** |

---

## 4. Design Methodology

### 4.1 Antenna Design and Electromagnetic Analysis
The transmitting and receiving antennas were designed using classical microstrip antenna theory and refined through electromagnetic simulation. Key parameters such as patch dimensions, substrate properties, and feed offset were optimized to achieve resonance at 1.8 GHz with acceptable return loss.

The antenna analysis includes:
- S11 and input impedance characteristics
- Radiation pattern and gain evaluation
- Surface current distribution analysis

---

### 4.2 Rectifier Modeling
A nonlinear Schottky diode model was developed to accurately represent high-frequency junction behavior. This model forms the core of the RF rectifier and directly influences RF-to-DC conversion efficiency.

Harmonic Balance (HB) simulations were used to analyze:
- Diode conduction intervals
- Harmonic generation
- Steady-state DC output power

---

### 4.3 Input Impedance Characterization
Due to the nonlinear nature of the rectifier, its input impedance varies with both frequency and input power. Large-Signal S-Parameter (LSSP) and source-pull simulations were performed to extract the power-dependent impedance characteristics, which serve as the foundation for impedance matching design.

---

### 4.4 Smith-Chart-Based Impedance Matching
A lumped-element matching network was synthesized using Smith chart techniques to transform the rectifier impedance to the 50 Ω reference at the operating point. The matching network was iteratively optimized to maximize power delivery to the rectifier under nominal excitation conditions.

---

### 4.5 System Integration
A full end-to-end system simulation was performed by integrating the antenna, matching network, rectifier, and load. Antenna S-parameters obtained from EM simulations were imported into the circuit environment, enabling accurate co-simulation of electromagnetic and nonlinear circuit effects.

---

## 5. Results and Performance

The integrated WPT system demonstrates the following key results:

- Antenna return loss below −10 dB at 1.8 GHz  
- Effective impedance transformation using Smith-chart matching  
- Stable rectifier operation at low RF input power  
- **Peak RF-to-DC Power Conversion Efficiency of 88.23%**

These results highlight the importance of co-optimizing antenna performance, impedance matching, and rectifier design, even when using a lossy FR-4 substrate.

---

## 6. Repository Organization

The repository is organized to reflect the logical progression of the system design, from individual subsystem development to full system integration.

- `antenna/`  
  Antenna design and electromagnetic simulation results, including S-parameters, radiation patterns, impedance plots, and current distribution.

- `diode_model/`  
  Nonlinear Schottky diode model used in the rectifier and matching network simulations.

- `impedance_analysis/`  
  Results from LSSP and source-pull simulations used to characterize the rectifier input impedance.

- `matching_network/`  
  Smith-chart synthesized impedance matching networks and associated simulation results.

- `rf_rectifier/`  
  Voltage doubler rectifier schematics and RF-to-DC efficiency plots prior to full system integration.

- `system_integration/`  
  Complete WPT system schematics and final end-to-end performance results.

- `results/`  
  Curated set of key plots summarizing final system performance.

- `workspace_view/`  
  Screenshots and visual references of the ADS workspace and simulation setup.

- `docs/`  
  Formal project documentation, including the detailed project report.

---

## 7. Tools and Simulation Environment

- **MATLAB Antenna Designer** – Antenna modeling and EM analysis  
- **Keysight Advanced Design System (ADS)** – Circuit design and nonlinear simulation  
- Harmonic Balance (HB) and Large-Signal S-Parameter (LSSP) analyses  

---

## 8. Publication Status

The results presented in this repository form the basis of a **conference paper** that has been prepared for submission.  
To maintain publication integrity, the manuscript is **not included in this repository at this stage** and will be made available following the completion of the review and acceptance process.

---

## 9. Applications

- RF energy harvesting systems  
- Battery-less IoT sensor nodes  
- Wireless sensor networks  
- Short-range wireless charging modules  

---

## 10. License and Usage

This repository is intended for **academic and research reference**.  
Reuse of the material should be accompanied by appropriate attribution to the original authors.

---

## 11. Future Work

Potential extensions of this work include:
- Adaptive or tunable impedance matching networks  
- Multi-stage rectifier architectures  
- Antenna arrays for improved link range  
- Fabrication and experimental validation  
- Integration with energy storage elements  
---

## Author
**Avinash Tanti and Harish Arjun**
