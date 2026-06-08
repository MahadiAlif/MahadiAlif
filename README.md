```
╔══════════════════════════════════════════════════════════════════════════════╗
║                                                                            ║
║   ███╗   ███╗ █████╗ ██╗  ██╗ █████╗ ██████╗ ██╗     █████╗ ██╗     ██╗  ██████╗  ║
║   ████╗ ████║██╔══██╗██║  ██║██╔══██╗██╔══██╗██║    ██╔══██╗██║     ██║  ██╔═══╝  ║
║   ██╔████╔██║███████║███████║███████║██║  ██║██║    ███████║██║     ██║  █████╗   ║
║   ██║╚██╔╝██║██╔══██║██╔══██║██╔══██║██║  ██║██║    ██╔══██║██║     ██║  ██╔══╝   ║
║   ██║ ╚═╝ ██║██║  ██║██║  ██║██║  ██║██████╔╝██║    ██║  ██║███████╗██║  ██║      ║
║   ╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═════╝ ╚═╝    ╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝      ║
║                                                                            ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

```c
/**
 * @file    runtime.c
 * @brief   System initialization — Engineering Runtime v3.2
 * @author  Mahadi Alif
 * @target  bare-metal | RTOS | edge-compute
 */

#include <firmware.h>
#include <signal_processing.h>
#include <robotics.h>
#include <edge_ml.h>

int main(void) {

    system_init(POLITECNICO_DI_TORINO, ELECTRONICS_TELECOM_ENG);

    while (1) {
        acquire_signals(IMU | ENCODERS | ANALOG_FRONTEND);
        process_dsp_pipeline(FIR | FFT | KALMAN);
        fuse_sensors(CAN_BUS | ROS2_TOPICS);
        deploy_inference(EDGE_ML | INT8_QUANTIZED);
        push_telemetry(UART | SPI | I2C);

        watchdog_feed();  // system alive — shipping production firmware
    }
}
```

---

<div align="center">

### `> SYSTEM IDENTITY`

**Electronics & Telecommunications Engineering** · Politecnico di Torino  
Operating at the intersection of **bare-metal firmware**, **real-time robotics**, and **digital signal processing**.

Building systems where clock cycles matter and latency budgets are measured in microseconds.

</div>

---

## `> RUNTIME TELEMETRY`

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=MahadiAlif&show_icons=true&theme=tokyonight&bg_color=0a0f1d&hide_border=true&title_color=70a5fd&icon_color=38bdae&text_color=a9b1d6&count_private=true&include_all_commits=true" alt="GitHub Stats" height="180"/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=MahadiAlif&theme=tokyonight&background=0a0f1d&hide_border=true&ring=70a5fd&fire=f7768e&currStreakLabel=70a5fd&sideLabels=a9b1d6&dates=565f89" alt="GitHub Streak" height="180"/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=MahadiAlif&layout=compact&theme=tokyonight&bg_color=0a0f1d&hide_border=true&title_color=70a5fd&text_color=a9b1d6&langs_count=8" alt="Top Languages" height="180"/>

</div>

---

## `> HARDWARE & SOFTWARE STACK`

```
┌──────────────────────────────────────────────────────────────────────┐
│                        ENGINEERING STACK TREE                       │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌─── LANGUAGES ─────────────────────────────────────────────────┐   │
│  │  C/C++ (bare-metal, RTOS)  ·  Python  ·  MATLAB/Simulink     │   │
│  └───────────────────────────────────────────────────────────────-┘   │
│                                                                      │
│  ┌─── EMBEDDED TARGETS ─────────────────────────────────────────-┐   │
│  │  STM32 (F4/H7)  ·  ESP32-P4  ·  ARM Cortex-M                 │   │
│  └───────────────────────────────────────────────────────────────-┘   │
│                                                                      │
│  ┌─── RTOS & MIDDLEWARE ─────────────────────────────────────────┐   │
│  │  FreeRTOS  ·  ROS 2 (Humble/Iron)  ·  CAN Bus / DDS          │   │
│  └───────────────────────────────────────────────────────────────-┘   │
│                                                                      │
│  ┌─── SIGNAL PROCESSING ─────────────────────────────────────────┐   │
│  │  FIR/IIR Filtering  ·  FFT/DFT  ·  Kalman Estimation         │   │
│  │  Sensor Fusion (IMU + Encoders)  ·  Biomedical DSP            │   │
│  └───────────────────────────────────────────────────────────────-┘   │
│                                                                      │
│  ┌─── EDGE ML & INFERENCE ───────────────────────────────────────┐   │
│  │  OpenVINO  ·  INT8 Quantization  ·  TFLite Micro             │   │
│  └───────────────────────────────────────────────────────────────-┘   │
│                                                                      │
│  ┌─── PCB & HARDWARE DESIGN ─────────────────────────────────────┐   │
│  │  Altium Designer  ·  KiCad  ·  Analog Frontend Design         │   │
│  └───────────────────────────────────────────────────────────────-┘   │
│                                                                      │
│  ┌─── TOOLCHAIN & CI/CD ─────────────────────────────────────────┐   │
│  │  GCC-ARM  ·  CMake  ·  Git  ·  GitHub Actions  ·  Docker     │   │
│  │  JTAG/SWD Debugging  ·  Logic Analyzers  ·  Oscilloscopes    │   │
│  └───────────────────────────────────────────────────────────────-┘   │
│                                                                      │
│  ┌─── SIMULATION & MODELING ─────────────────────────────────────┐   │
│  │  MATLAB/Simulink  ·  HIL Simulation  ·  LTspice              │   │
│  └───────────────────────────────────────────────────────────────-┘   │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

---

## `> DEPLOYMENT LOG — FIELD OPERATIONS`

<details>
<summary><b>⚡ ACTIVE — Kram Studio · Hardware & Software Development Intern</b></summary>
<br>

```
SUBSYSTEM:    Firmware & Analog Electronics
TARGET:       ESP32-P4
DOMAIN:       Edge ML Deployment · Analog Frontend · Production Firmware
```

- Architecting **ESP32-P4 firmware** for production-grade embedded systems
- Designing **analog electronics** and signal conditioning circuits
- Deploying **edge ML inference pipelines** on resource-constrained microcontrollers
- Full-stack hardware-software co-design from schematic capture to firmware bring-up

</details>

<details>
<summary><b>🔧 ARCHIVED — PIC4SeR Mechatronics Lab · Embedded Systems & Robotics Intern</b></summary>
<br>

```
SUBSYSTEM:    Sensor Fusion & Telemetry
TARGET:       STM32 + FreeRTOS
DOMAIN:       ROS 2 Integration · CAN Bus Telemetry · Real-Time Control
```

- Developed **STM32/FreeRTOS firmware** for real-time sensor acquisition and motor control
- Implemented **ROS 2 ↔ CAN bus** telemetry bridge for autonomous robot platforms
- Engineered **sensor fusion algorithms** (IMU + wheel encoders) for state estimation
- Designed hardware abstraction layers for multi-sensor data ingestion at deterministic rates

</details>

---

## `> INTERACTIVE PROJECT VAULT`

<details>
<summary><b>🧬 Biomedical Signal Processing Platform</b> — STM32 · MATLAB · Python</summary>
<br>

```
TARGET:       STM32 Microcontroller + Host PC
PIPELINE:     Analog Acquisition → ADC → FIR Filtering → FFT Validation
PRECISION:    0.53 Hz frequency resolution
STACK:        Embedded C · MATLAB · Python · DSP Toolchain
```

End-to-end biomedical DSP pipeline from analog signal acquisition on STM32 hardware through real-time FIR/IIR filtering to frequency-domain validation via FFT. Achieved **0.53 Hz filtering resolution** — critical for isolating physiological signal bands (ECG, EMG, EEG). Python post-processing layer for automated spectral analysis and clinical-grade signal quality metrics.

</details>

<details>
<summary><b>✈️ H2Fly — Hybrid Electric Flight Control System</b> — MATLAB/Simulink · Embedded C</summary>
<br>

```
TARGET:       Hybrid Electric Aircraft Powertrain
SIMULATION:   MATLAB/Simulink · Hardware-in-the-Loop (HIL)
CONTROLLERS:  PID · State-Space · Embedded C Implementation
DOMAIN:       Aerospace Control Systems · Power Electronics
```

MATLAB/Simulink modeling of hybrid electric aircraft powertrain dynamics with embedded C controller implementation. Full **Hardware-in-the-Loop (HIL) simulation** pipeline validating control law performance against plant models before deployment to target hardware. Designed for safety-critical flight control certification workflows.

</details>

<details>
<summary><b>👁️ OpenVINO Multimedia Processing Platform</b> — Intel OpenVINO · Python · C++</summary>
<br>

```
TARGET:       Intel CPU/iGPU/VPU Inference Engines
PERFORMANCE:  34 FPS real-time video analytics
OPTIMIZATION: INT8 Quantization · Model Pruning
STACK:        OpenVINO · Python · C++ · OpenCV
```

Real-time video analytics pipeline achieving **34 FPS** throughput with **INT8 quantized** neural network inference on Intel hardware. Implemented model optimization through quantization-aware training and post-training calibration. Multi-backend support across CPU, integrated GPU, and VPU accelerators with dynamic workload scheduling.

</details>

<details>
<summary><b>🛰️ CubeSat Attitude Control System</b> — C · Python · CI/CD</summary>
<br>

```
TARGET:       CubeSat On-Board Computer
SUBSYSTEM:    Attitude Determination & Control (ADCS)
ALGORITHMS:   Quaternion Kinematics · PD Control · Magnetorquer Actuation
PIPELINE:     C Firmware · Python Simulation · GitHub Actions CI/CD
```

Attitude determination and control system for CubeSat platforms. Quaternion-based orientation estimation with PD control laws driving magnetorquer actuation. **CI/CD automation** via GitHub Actions for continuous build verification, unit testing, and simulation regression across control parameter sweeps.

</details>

---

## `> RESEARCH OUTPUT`

```
┌──────────────────────────────────────────────────────────────────────┐
│  PUBLICATION                                                         │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  "Comparative Analysis of Brain-Computer Interfaces                  │
│   and Electromyography Prosthetics"                                  │
│                                                                      │
│  DOI:  zenodo.org/records/17456364                                   │
│  SCOPE: BCI signal acquisition · EMG decoding · Prosthetic control   │
│  VENUE: Zenodo (Open Access)                                         │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

🔗 **Read the full paper:** [zenodo.org/records/17456364](https://zenodo.org/records/17456364)

---

## `> ECOSYSTEM LEADERSHIP`

<table>
<tr>
<td align="center" width="33%">

**🔷 Intel Student Ambassador**

Evangelizing edge compute, OpenVINO inference optimization, and Intel architecture across academic communities.

</td>
<td align="center" width="33%">

**🟦 IBM Z Student Ambassador**

Bridging mainframe computing paradigms with modern engineering workflows and enterprise-scale reliability patterns.

</td>
<td align="center" width="33%">

**🏛️ Elected Student Council Member**

Politecnico di Torino — representing engineering student interests in institutional governance and academic policy.

</td>
</tr>
</table>

---

## `> CONTACT INTERFACE`

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a0f1d?style=for-the-badge&logo=linkedin&logoColor=70a5fd)](https://linkedin.com/in/mahadi-alif)
[![Email](https://img.shields.io/badge/Email-0a0f1d?style=for-the-badge&logo=gmail&logoColor=f7768e)](mailto:mahadi.alif@studenti.polito.it)
[![Zenodo](https://img.shields.io/badge/Zenodo-0a0f1d?style=for-the-badge&logo=zenodo&logoColor=38bdae)](https://zenodo.org/records/17456364)

</div>

---

## `> CONTRIBUTION GRID`

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/MahadiAlif/MahadiAlif/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/MahadiAlif/MahadiAlif/output/github-snake.svg" />
  <img alt="github-snake" src="https://raw.githubusercontent.com/MahadiAlif/MahadiAlif/output/github-snake-dark.svg" />
</picture>

</div>

---

<div align="center">

```
┌──────────────────────────────────────────────────────────────────┐
│  SYSTEM STATUS:  OPERATIONAL                                     │
│  UPTIME:         CONTINUOUS                                      │
│  NEXT DEPLOY:    ALWAYS SHIPPING                                 │
└──────────────────────────────────────────────────────────────────┘
```

*Firmware compiled. Registers configured. Interrupts armed. Shipping production code.*

</div>
