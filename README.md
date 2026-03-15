
# Project Highlight

- Designed and developed an optical sensing system using a light source and photodiode to detect very small signals, amplify them, and measure muscle oxygen saturation; successfully transferred the product to mass production.
- Improved and optimized the performance of a device for measuring cerebral oxygen saturation.
- Implemented design modifications and transferred a battery-free medical IoT device to mass production.
- Optimized power and interface circuits for smart medical devices powered through audio jack, USB Lightning, and USB Type-C.

---

# 1.Wearable Muscle Oxygen Monitoring Device (fNIRS-based)

## Project Summary

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

## Overview

The product was successfully launched through crowdfunding platforms.

**Kickstarter Launch**  
https://www.kickstarter.com/projects/763656766/repace-the-revolutionary-scientific-workout-solution?ref=discovery&term=repace&total_hits=37&category_id=341  

**Indiegogo Launch**  
https://www.indiegogo.com/en/projects/clomp/clomp-run-easy-burn-more-body-fat

The device provides real-time monitoring of muscle oxygen saturation for sports performance analysis.

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

https://github.com/yuliannayoon/impedance_matching/issues/2#issue-4079400928


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
