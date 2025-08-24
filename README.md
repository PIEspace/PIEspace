<h1 align="center">🚀 PIEspace — Pioneering VTVL Rockets & Autonomous Aerospace 🚀</h1>

<p align="center">
  <img src="Logo%20Two.jpeg" alt="PIEspace Logo" width="280"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?color=%23FF5733&size=26&center=true&vCenter=true&width=900&lines=Revolutionizing+Space+Travel;Electric+VTVL+Rocket+Development;MarsShip+Program+Underway;Building+Aerospace+Grade+Flight+Computers;Next+Stop:+Mars!"/>
</p>

<p align="center">
  <a href="https://github.com/PIEspace?tab=followers">
    <img src="https://img.shields.io/github/followers/PIEspace?label=Follow&style=social"/>
  </a>
  <a href="https://visitor-badge.laobi.icu/badge?page_id=PIEspace.PIEspace">
    <img src="https://visitor-badge.laobi.icu/badge?page_id=PIEspace.PIEspace"/>
  </a>
  <a href="mailto:pie.space12@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact%20Us-blue?style=flat&logo=gmail"/>
  </a>
  <img src="https://img.shields.io/badge/License-Apache--2.0-green"/>
  <img src="https://img.shields.io/badge/QA-Flight%20Ready%20Process-8A2BE2"/>
</p>

---

## 📖 Table of Contents
- [🚀 Mission](#-mission)
- [🛰️ Programs & Projects](#️-programs--projects)
- [🧠 Systems Architecture](#-systems-architecture)
- [🛡️ Quality Assurance](#️-quality-assurance)
- [📡 Telemetry Schema](#-telemetry-schema)
- [🧰 Developer Guide](#-developer-guide)
- [⚙️ CI/CD Automation](#️-cicd-automation)
- [📊 Metrics](#-metrics)
- [🤝 Contributing](#-contributing)
- [🔒 Security](#-security)
- [📜 License](#-license)
- [🔗 Connect](#-connect)
- [📎 Appendices](#-appendices)

---

## 🚀 Mission

At **PIEspace**, we believe **Vertical Take-Off and Vertical Landing (VTVL)** is the gateway to **reusable rockets** and eventually, **Mars colonization**.

🌍 **Current Focus**  
- **MarsShip V1** — electric VTVL demonstrator (200–500 m hop + belly-flop + precision landing).  
- **Agni Flight Computer v3** — aerospace-grade avionics with sensor fusion.  
- **SkyVoyager CanSat v3** — testbed for atmospheric data & telemetry.  

✨ *“We are not just building rockets. We are building the future.”*

---

## 🛰️ Programs & Projects

### 🚀 MarsShip V1 — Electric VTVL Rocket
- **Goal:** Hop to 500 m, belly-flop, return to pad.  
- **Tech Stack:**  
  - STM32H7VIT6 Flight Computer + Raspberry Pi 4/5 onboard AI  
  - Sensors: BNO055 IMU, BMP388 baro, GNSS, distance sensors  
  - Actuators: Dual ESC motors, 2-axis TVC, grid fins, RCS  
  - Comms: LoRa, NRF24, Wi-Fi, Bluetooth, 4G (Quectel EC200U-CN)  
  - Structure: Carbon fiber  

### 🤖 Robotics Program
- Autonomous robots for **in-space assembly & planetary exploration**.  
- Focus: **Swarm AI, adaptive control, machine learning**.  

### 💻 GCS — Ground Control System
- Python (PySide6) + Processing + Web GUI.  
- Real-time telemetry, replay, maps, 3D visualization.  

---

## 🧠 Systems Architecture

```mermaid
flowchart TD
  GCS[Ground Control Station] <--->|LoRa/4G| COMMS[Comms Hub]
  COMMS <-->|UART| FC[Flight Controller STM32H7VIT6]
  OC[Onboard Computer RPi4/5] <-->|USB| FC
  FC -->|PWM| ACT[TVC Servos, ESCs, Grid Fins]
  SENS[IMU BNO055, Baro BMP388, GNSS] -->|I2C/SPI| FC
  PWR[Battery + BMS] --> FC
