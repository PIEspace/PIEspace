# 🚀 PIEspace — Pioneering the Future of VTVL & Autonomous Aerospace

![Logo](Logo%20Two.jpeg)

[![GitHub Followers](https://img.shields.io/github/followers/PIEspace?label=Follow&style=social)](https://github.com/PIEspace?tab=followers)
![Visitors](https://visitor-badge.laobi.icu/badge?page_id=PIEspace.PIEspace)
[![Contact](https://img.shields.io/badge/Email-Contact%20Us-blue?style=flat&logo=gmail)](mailto:pie.space12@gmail.com)
![QA](https://img.shields.io/badge/QA-Flight%20Ready%20Process-8A2BE2)
![License](https://img.shields.io/badge/License-Apache--2.0-green)

---

## 📖 Table of Contents
- [🚀 Mission](#-mission)
- [🛰️ Programs & Projects](#️-programs--projects)
- [🧠 Systems Architecture](#-systems-architecture)
- [🛡️ Quality Assurance & Safety](#️-quality-assurance--safety)
- [📡 Telemetry & Data Schema](#-telemetry--data-schema)
- [🧰 Developer Guide](#-developer-guide)
- [⚙️ CI/CD & Automation](#️-cicd--automation)
- [📊 Metrics & Dashboards](#-metrics--dashboards)
- [🤝 Contributing](#-contributing)
- [🔒 Security](#-security)
- [📜 License](#-license)
- [🔗 Connect](#-connect)
- [📎 Appendices](#-appendices)

---

## 🚀 Mission

At **PIEspace**, our mission is to master **electric VTVL (Vertical Take-Off, Vertical Landing)** and autonomous rockets as a stepping stone to interplanetary spacecraft.

**2025–2026 Goals**
- Develop **MarsShip V1** (200–500 m hop → belly-flop → precision landing).
- Establish a robust **flight-safety & QA process**.
- Publish **open telemetry formats**, **control stacks**, and **GCS tooling**.

---

## 🛰️ Programs & Projects

### 🔹 MarsShip V1 — Electric VTVL Rocket
- **Goal:** Hop to 200–500 m, belly-flop, land on pad.  
- **Status:** Integration & Hardware-in-the-Loop (HIL) testing.  
- **Tech:** STM32H7VIT6 + Raspberry Pi, BNO055, BMP388, GNSS, LoRa/NRF/4G, carbon-fiber body, TVC gimbal, grid fins.

### 🔹 Agni Flight Computer
- Aerospace-grade avionics stack with **sensor fusion (Madgwick + Kalman)**, **deterministic control**, and **fail-safes**.

### 🔹 Ground Control System (GCS)
- Professional **dashboard** for pre-flight, live telemetry, command uplink, and replay.  
- Stack: Python (PyQt), Processing/JavaFX, or WebSerial GUI.

### 🔹 SkyVoyager CanSat V3
- Atmospheric sensing & telemetry to derisk rocket avionics.

---

## 🧠 Systems Architecture

```mermaid
flowchart LR
  GCS[Ground Control Station] <---> COMMS[Comms: LoRa/NRF/4G]
  COMMS <-->|UART/SPI| FC[Flight Controller STM32H7VIT6]
  OC[Onboard Computer RPi 4/5] <-->|UART| FC
  FC -->|PWM| ACT[TVC, ESCs, Grid Fins]
  SENS[IMU BNO055, Baro BMP388, GNSS] -->|I2C| FC
  PWR[Power & BMS] --> FC
