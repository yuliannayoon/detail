
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


# 🏃 Wearable Muscle Oxygen Monitoring Device (SmO₂ Monitor)

This project showcases the end-to-end hardware development process of an fNIRS-based wearable device, evolving from a functional engineering prototype to a mass-produced consumer product.

## 🚀 Phase 1: Engineering Prototype & Hardware Validation

In the early stages, the focus was on validating the fNIRS (Functional Near-Infrared Spectroscopy) sensor accuracy and power delivery.

| Engineering Prototype (Internal View) | Hardware Analysis |
| :--- | :--- |
| ![Image](https://github.com/user-attachments/assets/cf8ba69c-62fe-44d4-ab09-b9655ad20ba0) | **[Validation Focus]** <br><br> • **Core Tech:** Integration of NIR LED source and PD detectors. <br> • **Architecture:** Rigid PCB for initial signal processing validation. <br> • **Testing:** Wireless charging coil integration and battery discharge testing. |

### 🔍 Engineering Highlights:
* **Signal Integrity:** Designed the Analog Front End (AFE) for high-sensitivity detection of reflected NIR light from muscle tissue.
* **Early Miniaturization:** Prototyped the wireless charging system (WPC) within a limited footprint.

---

## 📐 Phase 2: Hardware Optimization & Development

To achieve a wearable form factor, I transitioned the design to a **Rigid-Flex PCB** structure, significantly reducing the device volume while improving mechanical reliability.

| Developed Hardware & Tuning | Development Specs |
| :--- | :--- |
| ![Image](https://github.com/user-attachments/assets/5f431d1f-eb61-44d4-ad2f-0301b3c3eb6c) | **[Optimization Keys]** <br><br> • **Form Factor:** Transitioned to Rigid-Flex PCB for 3D fit. <br> • **RF Performance:** BLE antenna tuning and Wi-Fi radiation optimization. <br> • **Power Management:** Achieved >5 hours of continuous operation via BLE. |

### 🔍 Engineering Highlights:
* **Antenna Optimization:** Conducted VNA measurements (as seen in my RF verification section) to ensure stable BLE connectivity despite the compact enclosure and proximity to the human body.
* **WPC Tuning:** Fine-tuned the wireless charging resonant frequency for high power-transfer efficiency through the enclosure.

---

## 📦 Phase 3: Final Product & Mass Production

The project culminated in a successful global launch through Kickstarter and Indiegogo, meeting all mass-production quality standards.

| Final Commercial Product | Launch Details |
| :--- | :--- |
| <img src="https://github.com/user-attachments/assets/INSERT_IMG_6507_URL" width="450"> | **[Commercial Success]** <br><br> • **Certification:** Passed EMI/EMC (KN32) and RF certifications. <br> • **Mass Production:** Optimized DFM (Design for Manufacturing) to reduce assembly error. <br> • **Platform:** Launched as "REPACE" / "CLOMP". |

### 🔍 Engineering Highlights:
* **Reliability Engineering:** Designed the system to withstand motion artifacts during high-intensity exercise.
* **Regulatory Compliance:** Implemented shielding and decoupling strategies to ensure a clear margin below EMI limit lines.

---

## 🛠 Tech Stack Summary
* **Hardware:** Rigid-Flex PCB Design, BLE (nRF52 series), fNIRS Sensor Integration.
* **Power:** Wireless Charging (Qi standard), Li-Po Battery Management.
* **Tools:** VNA (Keysight PNA), EMI Receiver, EasyEDA/Altium.



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

## 4.🛡️ EMI/EMC Troubleshooting: Radiated Emission (RE) Reduction

This section demonstrates the process of diagnosing and mitigating Radiated Emission (RE) issues to meet **KN32 Class A/B** regulatory standards. The goal was to reduce noise peaks and ensure a stable operating margin for the LD PD module.

### 🔍 1. Initial Status (Old Board)
The initial testing showed several noise spikes, particularly in the lower frequency range, which reduced the overall margin against the KN32 Class B limit.

| Pre-Mitigation RE Test (Old) | Technical Analysis |
| :--- | :--- |
| <img src="https://github.com/user-attachments/assets/aafe484b-423c-4c0e-a745-dabe4d648b89" width="100%"> | **[Baseline Issues]** <br><br> • **Limit Standard:** KN32 Class A/B <br> • **Observation:** Unstable noise floor with multiple harmonic spikes. <br> • **Risk:** Insufficient margin for mass production reliability. |

---

### 🔍 2. Optimized Status (New Board)
By implementing hardware-level mitigation strategies, the emission profile was significantly flattened, securing a much wider margin across the 30 MHz - 1 GHz spectrum.

| Post-Mitigation RE Test (New) | Improvements & Results |
| :--- | :--- |
| <img src="https://github.com/user-attachments/assets/5bc9edeb-b79a-4988-a19c-0eeb6d53c23a" width="100%"> | **[Key Improvements]** <br><br> • **Status:** **PASS** (Stable Compliance) <br> • **Result:** Significant reduction in broadband noise and harmonic peaks. <br> • **Margin:** Achieved a reliable safety margin below the Class B limit. |

### 🛠 Applied Mitigation Techniques
To achieve these results, the following hardware optimizations were performed:
1. **Decoupling Strategy:** Optimized capacitor placement and values near the high-speed switching nodes to suppress noise at the source.
2. **Filtering:** Integrated ferrite beads and LC filters on sensitive signal paths to block unintended RF radiation.
3. **Grounding & Shielding:** Enhanced the PCB ground plane integrity and improved the contact resistance of the module's shielding enclosure.

### 🛠 Tools & Expertise
* **Equipment:** EMI Receiver, Anechoic Chamber, Spectrum Analyzer
* **Skills:** EMI/EMC Troubleshooting, Noise Path Analysis, PCB Layout Optimization for Signal Integrity
