
# 🚀 Portfolio
### Specialized in Wearable Tech, RF Optimization, and EMI/EMC Troubleshooting

## 📑 Executive Summary
I am a Hardware Engineer with expertise in taking complex medical and wearable devices from **initial concept to mass production**. My work focuses on high-density miniaturization, wireless power integration, and proprietary hardware development to ensure an optimal user experience in portable electronics.

* **Key Achievement:** Enhanced user accessibility and device performance of wearable fNIRS technology, overcoming the bulkiness of existing market solutions (e.g., Moxy).
* **Core Competencies:**
    * **Ultra-Miniaturization:** High-density PCB design using **0.4mm pitch WLCSP** components to achieve extreme form-factor reduction.
    * **Power & Charging:** Low-power system architecture and implementation of **Wireless Charging** for enhanced usability.
    * **Stability & RF:** Optimization of wireless signals (RF) and **EMI/EMC troubleshooting** to ensure robust communication and certification.
    * **Intellectual Property:** Contribution to corporate **Hardware IP** through proprietary circuit designs and innovative architectures.
    * **Production & Quality:** **Design for Manufacturing (DFM)** and rigorous quality control for seamless mass production.
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
Optimized 2.4GHz antenna matching using a VNA to ensure maximum signal range and minimize energy loss.

| Measurement Plot | Technical Analysis |
| :--- | :--- |
| ![VNA Return Loss](https://github.com/user-attachments/assets/b7801090-8495-43df-86b6-4f3185360358) | **Result:** **-18.38 dB** Return Loss at 2.45 GHz.<br>**Insight:** Confirms **>98%** power transmission. Ripples above **5 GHz** are **measurement artifacts** from cable/connector limitations, not the antenna's intrinsic performance. |

### 📐 Precision PCB Layout Design
The layout was engineered to maintain a strict 50 $\Omega$ environment to prevent signal loss.

| PCB Design Snapshot | Design Strategy |
| :--- | :--- |
| <img src="https://github.com/user-attachments/assets/85e5ba37-4415-4dbf-b432-09d0055749a2" width="400"> | **Controlled Impedance:** Trace widths calculated based on PCB stack-up.<br>**Shielding:** Implemented a solid reference ground plane to provide a clear return path and reduce noise. |

---

##3. 🛡️ EMI/EMC Troubleshooting & Signal Integrity
**Challenge:** The initial design exhibited harmonic spikes near the **KN32 Class B** limit, risking certification failure and sensitive signal interference in the fNIRS module.

### 🔍 Diagnosis & Mitigation
I implemented high-precision hardware optimizations to stabilize the mixed-signal path and secure a safe EMI margin.

| Status | Radiated Emission (RE) Test Result | Engineering Analysis |
| :--- | :--- | :--- |
| **Before (Old)** | <img src="https://github.com/user-attachments/assets/5bc9edeb-b79a-4988-a19c-0eeb6d53c23a" width="100%"> | Identified noise spikes in the 100-200 MHz range, compromising the SNR of the fNIRS photodiode. |
| **After (New)** | <img src="https://github.com/user-attachments/assets/aafe484b-423c-4c0e-a745-dabe4d648b89" width="100%"> | **PASS:** Successfully suppressed harmonic peaks by optimizing the return path and signal isolation. |

### 🛠 Applied Solutions
1. **Stack-up Optimization (4-Layer Migration):** Upgraded the Photodiode/OP-AMP feedback loop from a 2-layer to a **4-layer stack-up**. By securing a dedicated **Reference Ground Plane**, I minimized loop inductance and stabilized the sensitive analog feedback path against external EMI.
2. **Clock Signal Isolation:** Re-routed high-speed clock lines on the MCU and ASIC boards to ensure maximum physical isolation from power traces, effectively mitigating **cross-talk** and harmonic emissions.
3. **RF Radiation Pattern Optimization:** Relocated the Wi-Fi module to the PCB's top edge and re-oriented the antenna to radiate outward. This eliminated mechanical interference and minimized internal EMI reflections by optimizing the **Radiation Pattern**.

<img src="https://github.com/user-attachments/assets/14caffa5-49e0-42e4-af8f-459b70e8ded9" width="300">
---

## 🛠 Technical Stack Summary
* **Low Power Design:** System-level Power Optimization (**3.7V / 300mAh Li-ion**), Battery Management (BMS).
* **Wireless Tech:** BLE (nRF52 series), Wireless Charging (Qi-standard, 1hr Fast Charge).
* **Hardware Design:** Rigid-Flex PCB, Microstrip/Impedance Control, DFM (Design for Manufacturing).
