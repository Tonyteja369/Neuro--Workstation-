<div align="center">

# 🧠 NeuroSense-X

### AI-Assisted Cranial Mechanical Vibration Analysis Platform

**Biomedical Instrumentation · Signal Processing · Mechanical Vibration Analysis**

<img src="https://img.shields.io/badge/Domain-Biomedical%20Engineering-007C91?style=for-the-badge">
<img src="https://img.shields.io/badge/Platform-Web%20Application-2563EB?style=for-the-badge">
<img src="https://img.shields.io/badge/Hardware-ESP32-00979D?style=for-the-badge">
<img src="https://img.shields.io/badge/Status-Experimental-orange?style=for-the-badge">

</div>

---

## 🔬 About the Project

NeuroSense-X is an experimental biomedical instrumentation and signal-analysis platform designed to acquire, process, analyse and visualize mechanical vibration measurements across multiple cranial positions.

It integrates embedded hardware communication, multi-sensor data acquisition, digital signal processing and interactive visualization.

---

## ✨ Core Features

<table>
<tr>
<td width="50%" valign="top">

<h3>🔵 Hardware Connectivity</h3>
ESP32 integration, MEMS sensor communication and serial data acquisition.

</td>
<td width="50%" valign="top">

<h3>🟢 Live Monitoring</h3>
Real-time three-axis acceleration measurements and sensor visualization.

</td>
</tr>
<tr>
<td width="50%" valign="top">

<h3>🟣 Signal Processing</h3>
Baseline removal, filtering, RMS calculations and FFT analysis.

</td>
<td width="50%" valign="top">

<h3>🟠 Frequency Analysis</h3>
Frequency spectrum visualization and experimental resonance analysis.

</td>
</tr>
<tr>
<td width="50%" valign="top">

<h3>🔴 Sensor Comparison</h3>
Comparative acceleration analysis across multiple measurement positions.

</td>
<td width="50%" valign="top">

<h3>⚫ Reporting</h3>
Experimental data visualization, analysis summaries and reporting.

</td>
</tr>
</table>

---

## ⚙️ System Architecture

```text
Bone-Conduction Transducer
          ↓
Mechanical Excitation
          ↓
MEMS Accelerometer Sensors
          ↓
TCA9548A I2C Multiplexer
          ↓
ESP32 Microcontroller
          ↓
Serial Communication
          ↓
NeuroSense-X Web Application
          ↓
Signal Processing & Analysis
          ↓
Visualization & Reporting
```

## 🔧 Hardware Components

| Component | Function |
|---|---|
| ESP32-WROOM-32 | Microcontroller |
| MPU6050 | Three-axis accelerometer and gyroscope |
| TCA9548A | I2C multiplexer |
| Bone-Conduction Transducer | Mechanical excitation |
| PAM8403 | Audio amplification |

### Sensor Configuration

| Sensor | Measurement Position | Channel |
|---|---|---|
| S1 | Left Temporal | 0 |
| S2 | Right Temporal | 1 |
| S3 | Frontal Midline | 2 |

---

## 📊 Signal Processing & Mathematical Methods

| Method | Application |
|---|---|
| RMS | Effective acceleration magnitude |
| FFT | Frequency-domain transformation |
| Mean | Average signal measurement |
| Peak Amplitude | Maximum signal magnitude |
| Peak-to-Peak | Total signal excursion |
| Filtering | Noise and unwanted frequency suppression |
| Resonance | Investigation of mechanical response peaks |
| Damping | Vibration decay characterization |
| Attenuation | Input-output amplitude comparison |
| Transfer Function | Frequency-dependent input-output relationship |
| SNR | Signal quality assessment |

---

## 💻 Technology Stack

<div align="center">

<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB">
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
<img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white">
<img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white">
<img src="https://img.shields.io/badge/ESP32-00979D?style=for-the-badge">
<img src="https://img.shields.io/badge/Web_Serial_API-4285F4?style=for-the-badge">

</div>

---

## 🚀 Installation

**Prerequisites:** Node.js, npm and Git.

**1. Clone the repository**

```bash
git clone https://github.com/Tonyteja369/NeuroSense-X-Software.git
```

**2. Navigate to the project**

```bash
cd NeuroSense-X-Software
```

**3. Install dependencies**

```bash
npm install
```

**4. Start development server**

```bash
npm run dev
```

---

## 🔌 Serial Communication

The ESP32 transmits sensor measurements through serial communication.

**Baud Rate:** `115200`

**CSV Data Format:**

```csv
timestamp_us,sensor_id,ax_g,ay_g,az_g
```

| Parameter | Description |
|---|---|
| timestamp_us | Timestamp in microseconds |
| sensor_id | Sensor identification |
| ax_g | X-axis acceleration |
| ay_g | Y-axis acceleration |
| az_g | Z-axis acceleration |

---

## ⚠️ Experimental Limitations

> [!IMPORTANT]
> The current prototype uses an MPU6050-based acquisition architecture with a nominal 100 Hz sampling target. Its theoretical Nyquist frequency at that sampling rate is 50 Hz.

> [!WARNING]
> High-frequency cranial vibration characterization requires higher-bandwidth sensors, faster synchronized acquisition, suitable calibration and controlled experimental conditions.

> [!NOTE]
> Resonance, damping, attenuation and transfer-function analysis require appropriate experimental measurements. Their inclusion in the software does not imply that these measurements have been experimentally validated.

**Medical Disclaimer:** NeuroSense-X is an experimental biomedical engineering platform. It is not a clinically validated medical device and is not intended for medical diagnosis or treatment.

---

## 🔭 Future Development

- Higher-bandwidth vibration acquisition.
- Synchronized multi-channel sensor measurements.
- Calibrated mechanical excitation.
- Advanced frequency-response characterization.
- Experimental damping and attenuation analysis.
- Improved signal-quality assessment.
- Advanced research visualization and reporting.

---

<div align="center">

### NeuroSense-X

**Engineering · Measurement · Signal Intelligence**

*An Experimental Biomedical Instrumentation Initiative*

</div>
