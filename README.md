<div align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=240&section=header&text=NeuroSense-X&fontSize=68&fontColor=ffffff&fontAlignY=36&desc=AI-Assisted%20Cranial%20Mechanical%20Vibration%20Analysis%20Platform&descSize=17&descAlignY=58&animation=fadeIn" width="100%" alt="NeuroSense-X banner"/> <a href="https://git.io/typing-svg"> <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&duration=3200&pause=900&color=22D3EE&center=true&vCenter=true&width=640&lines=Acquire.+Process.+Analyse.+Visualize.;ESP32+%C2%B7+MEMS+Sensing+%C2%B7+Web+Serial+API;Engineering+%C2%B7+Measurement+%C2%B7+Signal+Intelligence" alt="Typing animation"/> </a> <br/> <img src="https://img.shields.io/badge/Domain-Biomedical%20Engineering-0E7490?style=for-the-badge&labelColor=0B1220"> <img src="https://img.shields.io/badge/Platform-Web%20Application-2563EB?style=for-the-badge&labelColor=0B1220"> <img src="https://img.shields.io/badge/Hardware-ESP32-00979D?style=for-the-badge&logo=espressif&logoColor=white&labelColor=0B1220"> <img src="https://img.shields.io/badge/Status-Experimental-F97316?style=for-the-badge&labelColor=0B1220">

<br/><br/>

About · Features · Architecture · Hardware · Signal Processing · Quick Start · Serial Protocol · Limitations · Roadmap · Insights · Credits

</div> <br/> <div align="center">
👤 Conceived, Designed & Built by Katikireddy Tharun
<a href="https://github.com/Tonyteja369"> <img src="https://img.shields.io/badge/Founder%20%26%20Sole%20Owner-Katikireddy%20Tharun-0E7490?style=for-the-badge&logo=github&logoColor=white&labelColor=0B1220"> </a> <img src="https://img.shields.io/badge/Idea%20%26%20Research-Katikireddy%20Tharun-7C3AED?style=for-the-badge&labelColor=0B1220"> <img src="https://img.shields.io/badge/Hardware%20%26%20Firmware-Katikireddy%20Tharun-00979D?style=for-the-badge&labelColor=0B1220"> <img src="https://img.shields.io/badge/Software%20%26%20Analysis-Katikireddy%20Tharun-2563EB?style=for-the-badge&labelColor=0B1220"> </div> <br/>
🔬 About

NeuroSense-X is an experimental biomedical instrumentation and signal-analysis platform that acquires, processes, analyses and visualizes mechanical vibration measurements across multiple cranial positions.

It unites four layers in one workflow:

	Layer	What it does
🔌	Embedded	ESP32 firmware talking to MEMS sensors over I²C
📡	Acquisition	Multi-sensor streaming through serial communication
📈	Processing	Digital signal processing and frequency-domain analysis
🖥️	Visualization	Interactive, real-time web dashboard and reporting
<br/>
✨ Core Features
<table> <tr> <td width="50%" valign="top">
🔵 Hardware Connectivity

ESP32 integration, MEMS sensor communication and serial data acquisition.

</td> <td width="50%" valign="top">
🟢 Live Monitoring

Real-time three-axis acceleration measurements and sensor visualization.

</td> </tr> <tr> <td width="50%" valign="top">
🟣 Signal Processing

Baseline removal, filtering, RMS calculations and FFT analysis.

</td> <td width="50%" valign="top">
🟠 Frequency Analysis

Frequency spectrum visualization and experimental resonance analysis.

</td> </tr> <tr> <td width="50%" valign="top">
🔴 Sensor Comparison

Comparative acceleration analysis across multiple measurement positions.

</td> <td width="50%" valign="top">
⚫ Reporting

Experimental data visualization, analysis summaries and reporting.

</td> </tr> </table> <br/>
⚙️ System Architecture
🔊 Bone-ConductionTransducer
〰️ Mechanical Excitation
📟 MEMS AccelerometerSensors
🔀 TCA9548A I²CMultiplexer
🧠 ESP32 Microcontroller
🔌 Serial Communication
🖥️ NeuroSense-X WebApplication
📈 Signal Processing &Analysis
📊 Visualization &Reporting
<br/>
🔧 Hardware
Component	Function
ESP32-WROOM-32	Microcontroller
MPU6050	Three-axis accelerometer and gyroscope
TCA9548A	I²C multiplexer
Bone-Conduction Transducer	Mechanical excitation
PAM8403	Audio amplification
📍 Sensor Configuration
Sensor	Measurement Position	Multiplexer Channel
S1	Left Temporal	0
S2	Right Temporal	1
S3	Frontal Midline	2
<br/>
📊 Signal Processing & Methods
Method	Application
RMS	Effective acceleration magnitude
FFT	Frequency-domain transformation
Mean	Average signal measurement
Peak Amplitude	Maximum signal magnitude
Peak-to-Peak	Total signal excursion
Filtering	Noise and unwanted frequency suppression
Resonance	Investigation of mechanical response peaks
Damping	Vibration decay characterization
Attenuation	Input-output amplitude comparison
Transfer Function	Frequency-dependent input-output relationship
SNR	Signal quality assessment
<br/>
💻 Technology Stack
<div align="center"> <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"> <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white"> <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white"> <img src="https://img.shields.io/badge/ESP32-00979D?style=for-the-badge&logo=espressif&logoColor=white"> <img src="https://img.shields.io/badge/Web_Serial_API-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white"> </div> <br/>
🚀 Quick Start

Prerequisites: Node.js, npm and Git.

bash
# 1 · Clone the repository
git clone https://github.com/Tonyteja369/NeuroSense-X-Software.git

# 2 · Enter the project
cd NeuroSense-X-Software

# 3 · Install dependencies
npm install

# 4 · Start the development server
npm run dev

[!TIP] The Web Serial API is available in Chromium-based browsers such as Chrome and Edge.

<br/>
🔌 Serial Protocol

The ESP32 streams sensor measurements over serial communication.

Setting	Value
Baud Rate	115200
Format	CSV, one sample per line
csv
timestamp_us,sensor_id,ax_g,ay_g,az_g
Field	Description
timestamp_us	Timestamp in microseconds
sensor_id	Sensor identification
ax_g	X-axis acceleration (g)
ay_g	Y-axis acceleration (g)
az_g	Z-axis acceleration (g)
<br/>
⚠️ Experimental Limitations

[!IMPORTANT] The current prototype uses an MPU6050-based acquisition architecture with a nominal 100 Hz sampling target. At that rate the theoretical Nyquist frequency is 50 Hz.

[!WARNING] High-frequency cranial vibration characterization requires higher-bandwidth sensors, faster synchronized acquisition, suitable calibration and controlled experimental conditions.

[!NOTE] Resonance, damping, attenuation and transfer-function analysis require appropriate experimental measurements. Their inclusion in the software does not imply that these measurements have been experimentally validated.

[!CAUTION] Medical Disclaimer: NeuroSense-X is an experimental biomedical engineering platform. It is not a clinically validated medical device and is not intended for medical diagnosis or treatment.

<br/>
🔭 Roadmap
[ ] Higher-bandwidth vibration acquisition
[ ] Synchronized multi-channel sensor measurements
[ ] Calibrated mechanical excitation
[ ] Advanced frequency-response characterization
[ ] Experimental damping and attenuation analysis
[ ] Improved signal-quality assessment
[ ] Advanced research visualization and reporting
<br/>
📈 Developer Insights
<div align="center"> <!-- Full dashboard generated by .github/workflows/metrics.yml (see setup notes) --> <img src="./assets/github-metrics.svg" alt="GitHub metrics dashboard" width="100%"/>

<br/><br/>

<img height="170" src="https://github-readme-stats.vercel.app/api?username=Tonyteja369&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0B1220&count_private=true&rank_icon=github" alt="GitHub stats"/> <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Tonyteja369&layout=compact&theme=tokyonight&hide_border=true&bg_color=0B1220" alt="Top languages"/> <img src="https://github-readme-streak-stats.herokuapp.com/?user=Tonyteja369&theme=tokyonight&hide_border=true&background=0B1220" alt="Streak stats"/> <img src="https://github-readme-activity-graph.vercel.app/graph?username=Tonyteja369&theme=tokyo-night&hide_border=true&bg_color=0B1220&area=true" width="100%" alt="Contribution activity graph"/> </div> <br/>
🧑‍🔬 Ownership & Credits
Area	Owner
💡 Concept, research idea & experimental design	Katikireddy Tharun
🔧 Hardware design, wiring & sensor placement	Katikireddy Tharun
📟 ESP32 firmware & serial protocol	Katikireddy Tharun
💻 Web application, UI & signal-processing software	Katikireddy Tharun
📝 Documentation & project direction	Katikireddy Tharun

NeuroSense-X is the original work of Katikireddy Tharun — every idea, hardware design and line of software in this project.

<br/> <div align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2C5364,50:203A43,100:0F2027&height=140&section=footer&text=Engineering%20·%20Measurement%20·%20Signal%20Intelligence&fontSize=20&fontColor=ffffff&fontAlignY=62" width="100%" alt="footer"/>
NeuroSense-X

An Experimental Biomedical Instrumentation Initiative

© 2026 Katikireddy Tharun · All rights reserved

</div>
