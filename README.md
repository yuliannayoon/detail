
# 🚀 Portfolio
### Specialized in Wearable Tech, RF Optimization, and EMI/EMC Troubleshooting

## 📑 Executive Summary
I am a Hardware Engineer with expertise in taking complex medical and wearable devices from **initial concept to mass production**. My work focuses on miniaturization, high-sensitivity sensor integration (fNIRS), and **Low Power Design** to ensure long-term reliability and an optimal user experience in portable devices.

* **Key Achievement:** Enhanced user accessibility and device performance of wearable fNIRS technology, overcoming the bulkiness of existing market solutions (e.g., Moxy).
* **Core Competencies:** Low Power System Design, Rigid-Flex PCB, RF/EMI Optimization, Mass Production Quality Control.

---

## 1. 🏃 Wearable Muscle Oxygen Monitoring Device
**Project Goal:** Miniaturize a bench-top concept into a compact, BLE-enabled wearable device with a focus on power efficiency and ergonomic design.

### 🔋 Low Power Design & Energy Management
To achieve a slim wearable form factor, I optimized the system to operate reliably on a limited battery capacity while maintaining continuous data streaming.

* **Battery Management:** Integrated a **3.7V / 300mAh Lithium-ion (Li-ion) battery**, balancing device weight and capacity.
* **Power Optimization:** Implemented system-wide low-power modes, achieving **≈5 hours of continuous operation** during real-time fNIRS sensing and BLE communication.
* **Efficient Charging:** Designed a **Wireless Charging** system that achieves a full charge in **approximately 1 hour**, significantly enhancing user convenience.

| Phase | Prototype & Development | Engineering Key Points |
| :--- | :--- | :--- |
| **01. Concept** | <img src="https://github.com/user-attachments/assets/3dceb73d-b276-42f3-b70e-b46a8689c06e" width="400"> | **Validation:** Confirmed fNIRS sensor accuracy and initial Wireless Power Consortium (WPC) coil integration. |
| **02. Optimization** | <img src="https://github.com/user-attachments/assets/5f431d1f-eb61-44d4-ad2f-0301b3c3eb6c" width="400"> | **Miniaturization:** Transitioned to **Rigid-Flex PCB** to fit a complex ergonomic housing while maintaining BLE signal integrity. |
| **03. Final Product** | <img src="https://github.com/user-attachments/assets/01b484f3-ced6-4725-bef9-f779a06a443d" width="400"> | **Market Ready:** Successfully launched globally via Kickstarter and Indiegogo after passing all mass production quality checks. |

### 🔍 Engineering Highlights
* **Optical Sensing (fNIRS):** Designed a high-precision Analog Front End (AFE) for detection of minute light absorption changes in muscle tissue.
* **Connectivity:** Tuned nRF52-based BLE for high throughput with minimal power overhead.
* **Launch Platforms:** [Kickstarter](https://www.kickstarter.com/projects/763656766/repace-the-revolutionary-scientific-workout-solution) | [Indiegogo](https://www.indiegogo.com/en/projects/clomp/clomp-run-easy-burn-more-body-fat)

---

## 2. 📡 RF Testing & Layout Optimization
To ensure reliable wireless communication in various environments, I performed deep-dive RF analysis and impedance matching.

### 📡 S11 Parameter Verification (2.4 GHz)
Using a Vector Network Analyzer (VNA), I verified that signal reflections were minimized for maximum power transfer.

| Measurement Plot | Technical Analysis |
| :--- | :--- |
| ![VNA Return Loss](https://github.com/user-attachments/assets/b7801090-8495-43df-86b6-4f3185360358) | **Result:** **-18.38 dB** Return Loss at 2.45 GHz.<br>**Insight:** Confirms that >98% of power is successfully transmitted. Measurement ripples >5GHz were identified as artifacts from the non-chamber environment. |

### 📐 Precision PCB Layout Design
The layout was engineered to maintain a strict 50 $\Omega$ environment to prevent signal loss.

| PCB Design Snapshot | Design Strategy |
| :--- | :--- |
| <img src="https://github.com/user-attachments/assets/85e5ba37-4415-4dbf-b432-09d0055749a2" width="400"> | **Controlled Impedance:** Trace widths calculated based on PCB stack-up.<br>**Shielding:** Implemented a solid reference ground plane to provide a clear return path and reduce noise. |

---

## 3. 🛡️ EMI/EMC Troubleshooting
**Challenge:** The initial design (Old Board) exhibited harmonic spikes near the KN32 Class B limit line, risking certification failure.

### 🔍 Diagnosis & Mitigation
I implemented a series of hardware-level optimizations to secure a safe margin for mass production.

| Status | Radiated Emission (RE) Test Result | Engineering Analysis |
| :--- | :--- | :--- |
| **Before (Old)** | <img src="https://github.com/user-attachments/assets/5bc9edeb-b79a-4988-a19c-0eeb6d53c23a" width="100%"> | Identified noise spikes in the 100-200 MHz range, reducing the safety margin. |
| **After (New)** | <img src="https://github.com/user-attachments/assets/aafe484b-423c-4c0e-a745-dabe4d648b89" width="100%"> | **PASS:** Successfully flattened the emission profile across the 30 MHz - 1 GHz spectrum. |

### 🛠 Applied Solutions
1. **Decoupling Strategy:** Optimized capacitor placement near high-speed switching nodes.
2. **Filtering:** Integrated Ferrite beads and LC filters on sensitive signal paths.
3. **Shielding:** Improved contact resistance of the module's enclosure for enhanced EMI shielding.

---

## 🛠 Technical Stack Summary
* **Low Power Design:** System-level Power Optimization (**3.7V / 300mAh Li-ion**), Battery Management (BMS).
* **Wireless Tech:** BLE (nRF52 series), Wireless Charging (Qi-standard, 1hr Fast Charge).
* **Hardware Design:** Rigid-Flex PCB, Microstrip/Impedance Control, DFM (Design for Manufacturing).
* **Equipment:** VNA (Keysight PNA), EMI Receiver, Spectrum Analyzer.
