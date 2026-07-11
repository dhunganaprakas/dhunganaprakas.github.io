<!-- NOTE: To update the resume, edit resume/resume.tex and push. GitHub Actions (.github/workflows/build-resume.yml) recompiles it to assets/resume/Resume_PD.pdf automatically. Do not edit the PDF directly. -->
# Prakash Dhungana

**Embedded Software Engineer** — Safety-Critical Firmware · Embedded Linux & RTOS · TinyML

📍 Lexington, KY, USA &nbsp;·&nbsp; 📧 [prakash.dhungana@uky.edu](mailto:prakash.dhungana@uky.edu) &nbsp;·&nbsp; [LinkedIn](https://linkedin.com/in/dhunganaprakas) &nbsp;·&nbsp; [GitHub](https://github.com/dhunganaprakas) &nbsp;·&nbsp; 📄 [**Download Resume (PDF)**](/assets/resume/Resume_PD.pdf)

---

## About

I am an embedded software engineer with production experience in safety-critical automotive firmware and a Ph.D. (expected August 2026) focused on real-time machine learning for resource-constrained embedded platforms.

At **TTTech Auto** (now TrustMotion), I integrated NVIDIA DriveOS Safety Services (3LSS) into the MotionWise autonomous-driving middleware under ISO 26262, and implemented low-level C/C++ PCIe and DMA drivers on multicore SoCs enabling deterministic communication between safety and performance hosts. In my Ph.D. research at the **University of Kentucky**, advised by Dr. Sayed Ahmad Salehi at the [Computing with Unconventional Technologies (CUT) lab](https://salehi.engr.uky.edu/cut-lab), I design integer-only inference engines and on-device continual learning systems that bring real-time ML to ARM Cortex-M microcontrollers — 41 ms end-to-end latency in a 13.5 kB memory footprint.

My path into embedded software started on the hardware side: after earning a B.E. in Mechanical Engineering (Tribhuvan University, 2016), I spent three years diagnosing engines, ECUs, and powertrain control logic as an automotive service engineer in Nepal. That hands-on grounding led me to an M.Sc. in Automotive Computing and Communications (University of Osijek, Croatia, 2021) and into embedded software for ADAS and autonomous driving. I am comfortable on both sides of the hardware-software boundary — with a schematic and a logic analyzer, or a debugger and a driver stack.

## Experience

| Role | Organization | Period |
|---|---|---|
| Graduate Research Assistant — Embedded AI & Real-Time Systems | University of Kentucky, USA | 2023 – 2026 |
| Embedded Software Engineer | TTTech Auto (now TrustMotion), Croatia | 2021 – 2022 |
| Graduate Student Intern — ADAS Embedded Software | TTTech Auto, Croatia | 2019 – 2021 |
| Automotive Service Engineer | IME Motors / Goldfish International, Nepal | 2016 – 2019 |

## Core Skills

- **Languages:** C, C++, Python, Bash, Assembly
- **Platforms & OS:** Embedded Linux (Yocto, Buildroot, systemd), NVIDIA DriveOS/Jetson/Xavier, QNX, RTOS, bare-metal, ARM Cortex-M/A, Aurix TriCore
- **Low-level:** Kernel and device driver development (PCIe, DMA, Ethernet NIC, USB, MIPI camera), board bring-up
- **Protocols:** CAN, Automotive Ethernet, TCP/IP, UDP, SPI, I2C, UART
- **Safety & Standards:** ISO 26262, AUTOSAR, ASPICE, MISRA-C/C++
- **Debug & Test:** TRACE32 (Lauterbach/JTAG), GDB, logic analyzers, VectorCAST, profiling
- **Embedded AI:** TensorFlow Lite, integer-arithmetic optimization, on-device continual learning

## Projects

### RTKWS: Real-Time Keyword Spotting on Microcontrollers

Designed and implemented an efficient real-time keyword spotting architecture for edge devices, comprising data acquisition, silence detection, feature extraction, and binary classification units. To minimize memory footprint and computational complexity, the pipeline operates entirely on 8-bit integer voice data — all computation is integer-only. Feature extraction converts audio into 2-D feature maps via short-time Fourier transform, classified by a compact CNN (three convolutional layers, one fully connected) quantized with a new approach based on the TensorFlow Lite quantization method. The architecture is written in pure C with no external dependencies for portability, and was deployed on a low-cost TI TM4C123GXL microcontroller, achieving real-time operation.

![RTKWS deployment setup on TI TM4C123GXL](/assets/publications/rtkws_deployment.jpg "RTKWS Deployment Setup")

### PCIe Backbone Communication for Automotive ECUs

Ethernet switches have dominated inter-ECU communication architectures in vehicles. Replacing Ethernet with PCIe offers a faster, hardware-efficient alternative, and Non-Transparent Bridges (NTB) enable separate memory systems to share the same PCIe bus. This project developed multi-host PCIe communication between two or more automotive ECUs. (I handed the project over before completion when I left for graduate study.)

### Three-Layered Safety Supervision (3LSS) Framework Integration

3LSS is a safety extension implemented by NVIDIA for [DriveOS](https://developer.nvidia.com/drive/os), compliant with ASPICE, ISO 26262, and ISO/SAE 21434. It monitors hardware safety through a wide range of built-in tests for heterogeneous redundancy, reporting over SPI to the safety host of the automotive ECU, which analyzes the reports and triggers safety reactions on error. I integrated the 3LSS framework into the MotionWise middleware platform.

### Brightness and Color Equalization (BCE) on a Real ADAS Platform

Implemented and evaluated four brightness and color equalization methods — combinations of basic linear transformation and gamma correction — for multi-camera panoramic imaging on a production ADAS platform (ALPHA development board). Added blending based on improved gradual fusion for smooth brightness/color transitions in overlapping regions, with subjective testing to select the preferred method.

![Inputs provided to the BCE algorithm](/assets/publications/bce_input.jpg "Inputs to BCE Algorithm")

![Outputs from the BCE algorithm](/assets/publications/bce_output.jpg "Outputs from BCE Algorithm")

- a — Gamma correction for both color and brightness equalization
- b — Gamma correction for brightness, linear transformation for color
- c — Gamma correction for color, linear transformation for brightness
- d — Linear transformation for both color and brightness equalization

## Publications

- P. Dhungana and S. A. Salehi, "Exploring the Effect of Kernel Depth in Compact Keyword Spotting Models," *2024 International Congress on Human-Computer Interaction, Optimization and Robotic Applications (HORA)*, Istanbul, Türkiye, 2024, pp. 1–6. [doi:10.1109/HORA61326.2024.10550542](https://ieeexplore.ieee.org/document/10550542)
- P. Dhungana and S. A. Salehi, "RTKWS: Real-Time Keyword Spotting Based on Integer Arithmetic for Edge Deployment," *2024 25th International Symposium on Quality Electronic Design (ISQED)*, San Francisco, CA, USA, 2024, pp. 1–7. [doi:10.1109/ISQED60706.2024.10528680](https://ieeexplore.ieee.org/document/10528680)
- S. A. Salehi and P. Dhungana, "A Low-Cost Keyword Spotting Architecture Based on Wavelet Packets Feature Extraction for Edge Devices," *2024 25th International Symposium on Quality Electronic Design (ISQED)*, San Francisco, CA, USA, 2024, pp. 1–1. [doi:10.1109/ISQED60706.2024.10528719](https://ieeexplore.ieee.org/document/10528719)
- P. Dhungana, M. Herceg, R. Grbić and V. Marinković, "Implementation of Brightness and Color Equalization Methods to Create a Smooth Panoramic Image on a Real ADAS Platform," *2022 International Symposium ELMAR*, Zadar, Croatia, 2022, pp. 185–190. [doi:10.1109/ELMAR55880.2022.9899793](https://ieeexplore.ieee.org/document/9899793)

## Get in Touch

I am currently seeking full-time embedded software engineering roles in **autonomous systems, robotics, and automotive** (available from **August 2026**). The fastest way to reach me is by email: [prakash.dhungana@uky.edu](mailto:prakash.dhungana@uky.edu), or connect on [LinkedIn](https://linkedin.com/in/dhunganaprakas).
