
# Project Highlight

- Designed and developed an optical sensing system using a light source and photodiode to detect very small signals, amplify them, and measure muscle oxygen saturation
- Improved and optimized the performance of a device for measuring cerebral oxygen saturation.
- Implemented design modifications and transferred a battery-free medical IoT device to mass production.
- Optimized power and interface circuits for smart medical devices powered through audio jack, USB Lightning, and USB Type-C.

---

# 1.Wearable Muscle Oxygen Monitoring Device 

This project focused on developing a wearable device that measures muscle oxygen consumption using fNIRS technology.  
The goal was to miniaturize a concept prototype into a compact wearable device capable of real-time monitoring with BLE connectivity and at least 5 hours of battery operation.  
A wireless charging system was integrated to improve usability and enable continuous data transmission to a mobile application.  
The hardware architecture was redesigned using a rigid-flex PCB structure to achieve a smaller form factor and improved reliability compared to the initial prototype.  
The final product was successfully prepared for mass production quality and launched through crowdfunding platforms.

---

## Goal

- Miniaturize a concept device that measures muscle oxygen consumption into a wearable device  
- Enable real-time monitoring with BLE communication  
- Achieve at least **5 hours of battery operation**  
- Integrate **wireless charging capability**  
- Prepare the system for **mass production quality**


---

## Introduction

The device measures muscle oxygen saturation using **functional near-infrared spectroscopy (fNIRS)**.  
Near-infrared light is emitted into muscle tissue, and the reflected light is detected using photodiodes.  
The system analyzes the difference in absorption between oxygenated and deoxygenated hemoglobin to estimate muscle oxygen saturation.  
The processed data is transmitted via BLE to a mobile application for real-time monitoring and performance analysis.

---

## System Architecture

### Sensor Module
- NIR LED light source
- Photodiode detector

### Analog Front End
- Signal amplification
- ADC conversion

### Processing
- MCU signal processing
- SmO₂ calculation algorithm

### Connectivity
- BLE communication
- Mobile application interface

### Power System
- Rechargeable battery
- Wireless charging system

---

## Key Challenges

### Wireless Charging System
- Component selection for wireless charging
- Circuit implementation, tuning, and optimization
- Integration into a compact wearable form factor

### Miniaturization
- Rigid-flex PCB design applied for minimal size
- Improved hardware design compared to the prototype

### Wireless Communication Reliability
- Structural improvements for Wi-Fi radiation performance
- Wireless communication optimization and throughput margin

### Battery Performance
- Power optimization to achieve stable operation for more than 5 hours

### EMI / EMC Considerations
- PCB layout optimization
- Layer stack-up design for EMI/EMC compliance

---

## Proof of Result

The product was successfully launched through crowdfunding platforms and prepared for mass production.

**Kickstarter Launch**  
https://www.kickstarter.com/projects/763656766/repace-the-revolutionary-scientific-workout-solution?ref=discovery&term=repace&total_hits=37&category_id=341  

**Indiegogo Launch**  
https://www.indiegogo.com/en/projects/clomp/clomp-run-easy-burn-more-body-fat

This project demonstrated the successful commercialization of a wearable fNIRS-based muscle oxygen monitoring device.



## 2. 📡 RF Hardware Testing & Validation

Testing and verifying RF performance is a core part of my hardware development process. Below is the S-parameter (S11) measurement result for a 2.4 GHz wireless system, demonstrating my ability to use high-end lab equipment for signal integrity validation.

| Measurement Plot | Technical Analysis |
| :--- | :--- |
| ![VNA Return Loss](https://github.com/user-attachments/assets/b7801090-8495-43df-86b6-4f3185360358) | **[Key Performance Indicators]** <br><br> • **Target Frequency:** 2.4 GHz ISM Band <br> • **Return Loss (S11):** **-18.38 dB** at 2.45 GHz <br> • **Status:** Excellent impedance matching (<-10 dB threshold met) |

### 🔍 Technical Insights & Analysis

* **Impedance Matching Success:** The device under test (DUT) shows a strong resonance at 2.45 GHz with a return loss of -18.38 dB. This confirms that the impedance matching network is well-optimized, ensuring minimal signal reflection and maximum power transfer efficiency.

* **Analysis of High-Frequency Ripples:** The periodic fluctuations (ripples) observed above 5 GHz are identified as **measurement artifacts** caused by the testing environment. 
    * **Root Cause:** Since the measurement was conducted in a non-shielded laboratory setting (Non-Chamber), these ripples result from multipath reflections off nearby objects and phase interference at the cable/connector interfaces.
    * **Conclusion:** These effects do not impact the functional performance of the 2.4 GHz band, confirming the reliability of the core design.

### 🛠 Engineering Tools & Skills
* **Equipment:** Keysight PNA Network Analyzer (N5227A, 10 MHz - 67 GHz)
* **Expertise:** RF Circuit Design, VNA Calibration, PCB Stack-up Optimization, and Impedance Control.


## 3.📐 RF Layout Design for Impedance Matching

This section details the PCB layout strategy implemented to achieve optimal impedance matching at 2.4 GHz. The design focuses on minimizing parasitic effects and maintaining a controlled impedance transmission path.

| PCB Design Snapshot | Design Specifications |
| :--- | :--- |
| <img src="https://github.com/user-attachments/assets/85e5ba37-4415-4dbf-b432-09d0055749a2" width="450" alt="RF Layout Design"> | **[Design Parameters]** <br><br> • **Target Frequency:** 2.4 GHz ISM <br> • **Trace Type:** Microstrip Line <br> • **Characteristic Impedance ($Z_0$):** 50 ohm Controlled <br> • **Substrate:** FR-4 |

### 🔍 Engineering Highlights

* **Controlled Impedance Traces:** Trace widths and gaps were precisely calculated based on the PCB stack-up to ensure a continuous 50 $\Omega$ characteristic impedance. This minimizes signal reflection at impedance discontinuities.
* **Parasitic Minimization:** Component placement and transition points (e.g., from connector to trace) were optimized to reduce parasitic inductance and capacitance, critical for maintaining signal integrity at microwave frequencies.
* **Ground Plane Integrity:** A solid, unbroken reference ground plane was maintained directly beneath the RF signal traces to provide a clear return path and improve shielding.

## 🛡️ EMI/EMC Troubleshooting & Radiated Emission Reduction

This section demonstrates my ability to diagnose EMI issues and implement effective hardware mitigation strategies to meet regulatory standards (KN32 Class A/B). The project involved reducing radiated emissions from a fully assembled LD PD (Laser Diode Photodiode) module.

### 🔍 Challenge: Non-Compliant Emission Levels

Initially, the fully assembled LD PD module exhibited radiated emission levels dangerously close to the **KN32 Class B** limit line in the 100-200 MHz range. To ensure product reliability and regulatory compliance, emission reduction was critical.

| Pre-Mitigation RE Test Plot | Initial Performance Analysis |
| :--- | :--- |
| ![Pre-Mitigation EMI Plot](https://github.com/user-attachments/assets/PLEASE_INSERT_PRE_MITIGATION_IMAGE_URL_HERE) | **[Baseline Measurements]** <br><br> • **Standard:** KN32 Class A/B RE_QP <br> • **Frequency Range:** 30 MHz - 1 GHz <br> • **Issue:** High emissions (>20 dBµV/m) highlighted in the 100-200 MHz band, approaching Class B limit. |

### 🛠 Mitigation Strategy

To address the identified emission peaks, I implemented the following noise suppression techniques:

1.  **Shielding Enhancement:** Verified and improved the grounding contact of the module's metallic enclosure to enhance Faraday cage effectiveness against radiated coupling.
2.  **Filtering & Decoupling:** Added decoupling capacitors close to the noise-generating components and introduced ferrite beads on signal lines to suppress common-mode and differential-mode noise.
3.  **Layout Optimization:** Adjusted critical high-speed signal traces to minimize loop areas and reduce unintended loop antenna effects.

### 🔍 Results: Successful Compliance & Noise Reduction

After implementing the mitigation strategies, the module was re-tested. The post-mitigation plot shows a significant reduction in emission levels, ensuring compliance with a generous margin.

| Post-Mitigation RE Test Plot | Post-Performance Analysis |
| :--- | :--- |
| ![Post-Mitigation EMI Plot](https://github.com/user-attachments/assets/PLEASE_INSERT_POST_MITIGATION_IMAGE_URL_HERE) | **[Final Measurements]** <br><br> • **Status:** **PASS** (Compliant with KN32 Class A & B) <br> • **Improvement:** Effective suppression of peaks across the entire 100-200 MHz band. <br> • **Margin:** Achieved a substantial margin below all limits, guaranteeing stable operation. |

### 🛠 Tools & Expertise
* **Equipment:** EMI Receiver / Spectrum Analyzer, Anechoic Chamber, Biconical Antenna, Log-Periodic Antenna
* **Skills:** EMI Diagnosis, Noise Source Identification, PCB Shielding/Filtering Design, EMC Troubleshooting


