<p align="center">
  <strong>VOLAR MARINE SYSTEMS</strong><br>
  <em>Vessel-Optimized Lift, Autonomy & Robotics</em><br>
  Montréal, Québec, Canada
</p>

---

# MK-1 USV

**A 13ft hybrid range-extended surveillance and patrol unmanned surface vessel.**  
Remote-operated today. Training the AI for autonomous operations tomorrow.

🔗 **[View the Interactive Spec Sheet →](https://yourusername.github.io/volar-mk1/)**

---

## What is the MK-1?

The MK-1 is a working ISR (Intelligence, Surveillance, Reconnaissance) platform that delivers persistent maritime patrol capability under remote operator control over LTE/5G. It doesn't wait for autonomy to be useful — it patrols harbours, monitors waterways, inspects infrastructure, and surveys the environment **today**.

While conducting real patrol missions, the MK-1 continuously records every sensor feed, every operator decision, and every environmental condition. This operational dataset is the training corpus for a future autonomous AI program. The MK-1 builds the dataset that makes the autonomous USV possible.

## Key Specifications

| Parameter | Detail |
|---|---|
| **Hull** | 13ft fiberglass, foam-core unsinkable (Boston Whaler 130 SS) |
| **All-up weight** | ~350 kg (with genset and fuel) |
| **Propulsion** | 2× 15kW BLDC electric motors in custom azimuth stern drive pods, 360° steering |
| **Battery** | 2× 51.2V 100Ah LiFePO4 (10.24 kWh total) |
| **Range extender** | DC generator (48V) for hybrid operation |
| **Cruise speed** | ~16 knots |
| **Endurance** | ~4 hrs battery only · 12+ hrs with genset |
| **EO/IR payload** | SIYI ZT30 — 30× optical zoom, 640×512 thermal, 1,200m LRF |
| **Navigation** | Dual u-blox ZED-F9P RTK GNSS, moving baseline heading (compass-free) |
| **Flight controller** | Cube Orange+ running ArduPilot Rover/Boat |
| **Companion computer** | NVIDIA Jetson Orin Nano 8GB — ROS2, MAVROS, H.265 pipeline |
| **Communications** | Sierra Wireless RV55 LTE-A, dual SIM, encrypted VPN tunnel |
| **Data recording** | ROS2 rosbag (all topics), H.265 video, ArduPilot logs, synchronized timestamps |
| **Autonomy** | None (V1) — fully remote-operated by human over LTE |

## Systems Architecture

The MK-1 integrates 11 documented subsystems, each with full BOM, part numbers, interfaces, and assembly instructions:

| # | Subsystem | Summary |
|---|---|---|
| 01 | Hull & Structure | Foam-core fiberglass, marine plywood reinforcement, sensor mast, shock-isolated gimbal mount |
| 02 | Propulsion (ASD) | Dual Flipsky 65161 motors, custom 360° azimuth stern drive pods, VESC 100/250 controllers |
| 03 | Power System | 2× 51.2V 100Ah LiFePO4, DC generator hybrid, F16 relay digital switching, pre-charge circuit |
| 04 | Flight Controller | Cube Orange+, ArduPilot Rover/Boat, dual ZED-F9P RTK GPS with moving baseline heading |
| 05 | Companion Computer | Jetson Orin Nano 8GB, ROS2 Humble, MAVROS, GStreamer video pipeline, rosbag recording |
| 06 | Communications | Sierra Wireless RV55 LTE-A, dual SIM, 4×4 MIMO antenna, OpenVPN encrypted tunnel |
| 07 | EO/IR Payload | SIYI ZT30 4-sensor gimbal, MAVLink control, RTSP video output |
| 08 | Safety & Recovery | RF kill switch, standalone GPS tracker, AIS transponder, COLREGS nav lights, bilge pump |
| 09 | Wiring & Interconnects | Marine-grade tinned copper, Deutsch DT sealed connectors, DIN rail distribution |
| 10 | Ground Control | QGroundControl over LTE, RC transmitter for safety pilot override |
| 11 | Custom Parts | Outsourced CAD + CNC: ASD pods, azimuth gear sets, genset bed, wiring harness |

## Budget

| Category | Amount (CAD) |
|---|---|
| Parts (11 subsystems) | $32,238 |
| Taxes (QC 14.975%) | $3,862 |
| Shipping | $1,100 |
| Consumables | $450 |
| Contingency (15%) | $4,836 |
| **Total all-in prototype** | **$42,486** |

## Economies of Scale

| Production Tier | Units | COGS/unit | MSRP | Gross Margin |
|---|---|---|---|---|
| Pilot batch | 10 | $27,413 | $74,900 | 63.4% |
| Low-rate production | 100 | $19,320 | $52,900 | 63.5% |
| Medium-rate | 550 | $13,931 | $37,900 | 63.2% |
| Full-rate production | 1,000 | $11,706 | $31,900 | 63.3% |

COGS reduction of **72%** from prototype to full-rate production. Gross margins above **63%** at every tier.

## The AI Flywheel

```
 MK-1 Patrols → Data Recorded → AI Trained → Autonomous USV
      ↑                                              |
      └──────────────── more vessels ←───────────────┘
```

Every patrol generates synchronized video, thermal, GPS, IMU, motor telemetry, and operator decisions. At 550 deployed units running daily 6-hour patrols, that's **3,300 vessel-hours of training data per day** — real-world operational data that no competitor can replicate from simulation alone.

## Competitive Position

| | Industry Standard | VOLAR MK-1 |
|---|---|---|
| **MSRP** | $129K – $2M+ | $31.9K – $74.9K |
| **Revenue starts** | After autonomy proven (years) | At first deployment |
| **Capital needed** | $30M – $345M+ (VC-backed) | $43K prototype (non-dilutive grants) |
| **Approach** | Build autonomy first, sell later | Sell surveillance now, train AI from operations |
| **AI training data** | Simulation + controlled tests | Real patrol missions, fleet-scale |
| **Canadian presence** | None in this class | Designed, built, and operated in Canada |

## Mission Applications

- **Harbour & Port Security** — Persistent patrol, 30× optical zoom + thermal for vessel ID day/night
- **Waterway Monitoring** — River, lake, and coastal surveillance for environmental agencies
- **Infrastructure Inspection** — Bridge pilings, dam faces, pipeline crossings, shoreline erosion
- **AI Training Data Generation** — Every patrol feeds the autonomous training pipeline

## Roadmap

| Phase | Timeline | Milestone |
|---|---|---|
| 🟢 **NOW** | Weeks 1–2 | Federal incorporation, IRAP/accelerator applications, pitch materials |
| 🟢 **NOW** | Weeks 3–8 | Zero-cost positioning: LinkedIn, university outreach, hull shopping, COVE intro |
| 🟠 Funded | Weeks 8–12 | IRAP signed, hull acquired, machine shop deposit, build begins |
| 🟠 Build | Weeks 12–20 | Hull prep, battery install, genset mounted, ASD pods fabricated — MK-1 moves |
| 🟠 Build | Weeks 20–24 | FC, dual GPS, Jetson, SIYI ZT30, LTE gateway — full system integration |
| 🟠 Validate | Weeks 24–28 | Water trials, extended genset runs, data quality validation, demo video |
| 🔵 Revenue | Week 28+ | First paid patrol contracts, IDEaS application, SR&ED claim, AI co-founder search |

## Canadian Funding Alignment

The MK-1 is eligible for every major Canadian innovation and defence program:

- **NRC IRAP** — Non-repayable R&D contributions ($50K–$150K)
- **SR&ED** — 35% refundable tax credit (~$12K on prototype alone)
- **IDEaS (DND)** — Competitive projects up to $1.2M for defence innovation
- **BOREALIS / COVE** — Defence innovation consortium, test facilities, Navy partners
- **Investissement Québec** — IMPULSION PME, ESSOR, CRIC 2026
- **Montréal AI Ecosystem** — Mila, ÉTS, McGill robotics — future AI talent pipeline

## Repository Contents

```
├── index.html          ← Interactive MK-1 spec sheet (GitHub Pages)
└── README.md           ← This file
```

## Status

> **Active development.** Solo founder, pre-incorporation, pre-facility.  
> Seeking: funding partners, government collaborators, early customers, and an AI co-founder.

## Contact

**VOLAR Marine Systems**  
Montréal, Québec, Canada  

📧 [Get in touch](mailto:your-email@example.com)

---

<p align="center">
  <sub>© 2026 VOLAR Marine Systems — Confidential</sub>
</p>
