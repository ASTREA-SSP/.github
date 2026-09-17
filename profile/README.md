# 🛸 ASTREA SOLO SPACE PROGRAM (ASTREA SSP)

HARDWARE / AVIONICS / FLIGHT GUIDANCE

🛸 Mission `ICARUS-RLV` featuring:
- a Stratospheric Reentry Vehicle
- C++ / FreeRTOS (via ESP32)
- Active GNC (via RCS + Grid Fins)
- RTLS (Return to Launch Site)

DATA SCIENCE / ASTROPHYSICS

🔭 Projct `Joanus` featuring:
- an Exoplanet Discovery Pipeline
- Python / BLS / Signal Processing
- NASA / Roman Data Verification
- Relative-First Science Suite


**Astrea Solo Space Program (Astrea SSP)** is an independent aerospace technology and data science research initiative. It encompasses the design, hardware avionics, and flight software development for autonomous Stratospheric Reusable Launch Vehicles alongside advanced astrophysical data processing pipelines.

---

## 🛠️ Main Projects Overview

### 1. 🛸 Mission ICARUS-RLV (Embedded Systems & Avionics)

- **Objective**
  - Development of an autonomous Balloon-Launched Reentry Vehicle (BLARV) to test Guidance, Navigation, and Control (GNC), Cold-Gas-RCS attitude adjustment, active aerodynamic grid fin control, and Return-To-Launch-Site (RTLS) capabilities

- **Flight Software**
  - Deterministic C++ / FreeRTOS multi-tasking architecture executing on dual-core ESP32 microcontrollers

- **Scientific Payload:**
  - **Radiation Payload:** Interrupt-based Geiger-Müller counter capturing cosmic secondary radiation at the Pfotzer-Maximum (15–20 km altitude)
  - **Astrobiology Testbed:** Servo-actuated biological sample chamber subjecting dry yeast (*Saccharomyces cerevisiae*) to stratospheric UV-C radiation, sub-zero temperatures ($-55^\circ\text{C}$), and near-vacuum conditions
  - **Optical Payload:** Standalone 4K camera payload triggered dynamically via hardware GPIO handshake pulses from the On-Board Computer (OBC)

### 2. 🔭 Projekt JOANUS (Astrophysical Data Science Pipeline)

- **Objective**
  - Autonomous identification, extraction, and validation of exoplanet candidates from NASA space telescope archives (TESS, Kepler) ahead of the 2027 Nancy Grace Roman Space Telescope data drop

- **Architecture**
  - **Relativ-First Metric:** Computes the fundamental radius ratio $\frac{R_p}{R_*} = \sqrt{\delta}$ directly from relative photometry independent of pre-cataloged stellar data
  - **Blind Search:** Automated period identification using Box Least Squares (BLS) periodograms
  - **Validation Suite:** False-positive elimination including Odd/Even transit depth consistency checks ($<15\%$ threshold) and Phase 0.5 secondary eclipse detection
  - **Batch & Persistence:** Multi-target headless execution via `batch_process.py` with structured JSON telemetry exports
  - 
---

## 🗺️ Staged Roadmap

| Phase 0 (Current) | PHASE 1 (LOCAL DROPS) | PHASE 2 (1.600g BALLOON) | PHASE 3 (3.000g TITAN) |
| ----------------- | --------------------- | ------------------------ | ---------------------- | 
| Architectural | controlled 1000m Drop Tests | 35.000m Stratosphere | 40.000m Near-Vacuum |
| Design & Bench | GNC, Grid Fins & Parachute | 1.600g Balloon (250€) | 3.000g Balloon (800€) |
| Testing | Landing-Leg Verification | Full Science Payload | Final Pinnacle Mission |


**Phase 0 (Architecture & Bench Testing)** <br>
  FreeRTOS task scheduling, IMU sensor-fusion loops, hardware interrupt testing for radiation logging, and JOANUS pipeline modularization

**Phase 1 (Low-Altitude Drop Tests)** <br>
  Controlled Drops from 1000m over designated fields to validate flight state machines, grid-fin PID control, and parachute deployment

**Phase 2 (Stratospheric Mission - 1.600g Envelope)** <br>
  High-altitude launch up to ~35,000m targeting Pfotzer-Maximum radiation profiling, biological yeast exposure, 4K stratospheric photography, and active return homing

**Phase 3 (High-Altitude Pinnacle - 3.000g Envelope)** <br>
  Near-space execution up to ~40,000m ($<3\text{ hPa}$ pressure) testing cold-gas RCS attitude stabilization in ultra-thin atmosphere.
