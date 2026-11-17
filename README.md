# NeuroSense-X
### AI-Assisted Cranial Mechanical Vibration Analysis Platform

**NeuroSense-X** is an experimental biomedical instrumentation and signal-analysis platform designed to acquire, process, analyse and visualize mechanical vibration measurements across multiple cranial positions.

The platform integrates embedded hardware communication, real-time sensor data acquisition, digital signal processing and interactive visualization to support experimental investigation of cranial mechanical vibration characteristics.

---

## Project Overview

NeuroSense-X aims to provide an integrated environment for studying mechanical vibration measurements using MEMS accelerometers positioned at multiple cranial locations.

The software is designed to support:

- Real-time sensor data acquisition.
- Multi-sensor monitoring.
- Three-axis acceleration visualization.
- RMS-based signal analysis.
- FFT-based frequency analysis.
- Signal preprocessing and filtering.
- Comparative sensor analysis.
- Experimental data visualization.
- Report generation.

## System Architecture

```text
Bone-Conduction Transducer
          |
          v
Mechanical Excitation
          |
          v
MEMS Accelerometer Sensors
          |
          v
TCA9548A I2C Multiplexer
          |
          v
ESP32 Microcontroller
          |
          v
Serial Data Communication
          |
          v
NeuroSense-X Web Platform
          |
          v
Signal Processing & Analysis
          |
          v
Visualization & Reporting
```

## Key Features

### 1. Overview Dashboard
Provides a centralized interface for accessing system modules, experimental status and measurement summaries.

### 2. Hardware Connectivity
Supports serial communication with the ESP32-based acquisition system through the Web Serial API.

### 3. Live Monitoring
Designed to display real-time three-axis acceleration measurements and sensor information.

### 4. Experiment Management
Provides an interface for organizing experimental sessions and measurement datasets.

### 5. Signal Processing Laboratory
Provides tools for signal preprocessing, baseline removal, filtering and frequency-domain analysis.

### 6. RMS Analysis
Calculates Root Mean Square values to quantify the effective magnitude of acquired acceleration signals.

### 7. FFT Analysis
Uses Fast Fourier Transform methods to investigate frequency components in acquired signals.

### 8. Resonance Analysis
Provides an experimental analysis interface for investigating frequency-dependent mechanical responses.

### 9. Mechanical Resonance Mapping
Visualizes comparative measurements across defined cranial sensor positions.

### 10. Sensor Comparison
Supports comparison of measurements from multiple sensor locations.

### 11. Reporting
Provides an interface for presenting experimental measurements, analysis results and visualizations.

### 12. Diagnostics and Calibration
Supports system diagnostics, measurement-quality checks and calibration-related workflows.

---

## Hardware Integration

The current prototype architecture includes:

| Component | Purpose |
|---|---|
| ESP32-WROOM-32 | Microcontroller and data acquisition |
| MPU6050 | Three-axis accelerometer and gyroscope |
| TCA9548A | I2C sensor multiplexing |
| Bone-Conduction Transducer | Mechanical vibration excitation |
| PAM8403 | Audio amplification |

### Sensor Configuration

| Sensor | Measurement Position | I2C Channel |
|---|---|---|
| S1 | Left Temporal | 0 |
| S2 | Right Temporal | 1 |
| S3 | Frontal Midline | 2 |

## Signal Processing Methods

The platform's analytical framework includes:

| Method | Purpose |
|---|---|
| Mean | Average signal value |
| RMS | Effective signal magnitude |
| FFT | Frequency-domain transformation |
| Peak Amplitude | Maximum absolute signal magnitude |
| Peak-to-Peak | Total signal excursion |
| Filtering | Suppression of unwanted frequency components |
| Damping Analysis | Investigation of vibration decay |
| Attenuation Analysis | Comparison of input and output amplitudes |
| Transfer Function | Frequency-dependent input-output relationship |

*Advanced damping, attenuation and transfer-function measurements require appropriate calibrated input/output measurements and suitable acquisition hardware.*

---

## Technology Stack

- React
- TypeScript
- Vite
- Tailwind CSS
- shadcn/ui
- Web Serial API
- JavaScript-based signal processing
- IndexedDB for local experimental data storage

---

## Installation and Setup

### Prerequisites

- Node.js
- npm
- Git
- A Chromium-based browser supporting Web Serial API for hardware connectivity.

### Clone Repository

```bash
git clone https://github.com/Tonyteja369/NeuroSense-X-Software.git
```

### Navigate to Project

```bash
cd NeuroSense-X-Software
```

### Install Dependencies

```bash
npm install
```

### Start Development Server

```bash
npm run dev
```

Open the local development URL displayed in the terminal.

---

## Data Communication

The ESP32 communicates with the web application through serial data transmission.

Expected CSV format:

```csv
timestamp_us,sensor_id,ax_g,ay_g,az_g
```

Where:

- `timestamp_us`: Measurement timestamp in microseconds.
- `sensor_id`: Sensor identification number.
- `ax_g`: X-axis acceleration.
- `ay_g`: Y-axis acceleration.
- `az_g`: Z-axis acceleration.

Serial baud rate: `115200`

---

## Experimental Limitations

NeuroSense-X is currently an experimental biomedical instrumentation and signal-analysis platform.

Important considerations:

- The MPU6050 acquisition configuration has a nominal sampling target of 100 Hz.
- The theoretical Nyquist frequency at 100 Hz sampling is 50 Hz.
- The three sensors are read sequentially through the I2C multiplexer.
- High-frequency vibration characterization requires higher-bandwidth sensors and faster acquisition hardware.
- Accurate attenuation analysis requires calibrated mechanical input measurements.
- Damping analysis requires suitable vibration-decay measurements.
- Experimental results require controlled conditions and validation.

**NeuroSense-X is not a clinically validated medical device and is not intended for diagnosis or treatment of medical conditions.**

---

## Future Development

- Higher-bandwidth vibration acquisition.
- Synchronized multi-channel measurements.
- Calibrated mechanical excitation.
- Advanced frequency-response analysis.
- Experimental damping characterization.
- Frequency-dependent attenuation analysis.
- Improved signal-quality assessment.
- Research-oriented data export and visualization.

---

## Project Information

**Project:** NeuroSense-X  
**Domain:** Biomedical Engineering | Biomedical Instrumentation | Signal Processing  
**Platform:** Web-Based Experimental Analysis System  
**Hardware:** ESP32 and MEMS Accelerometers  
**Repository:** NeuroSense-X Software

---

## Disclaimer

This project is intended for educational, experimental and research-development purposes. Measurements and analytical outputs should not be interpreted as clinical findings or diagnostic results.
