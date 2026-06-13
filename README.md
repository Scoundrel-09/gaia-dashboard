# 🌍 Gaia — Urban Water Quality Monitoring System

**Live Dashboard:** [https://scoundrel-09.github.io/gaia-dashboard](https://scoundrel-09.github.io/gaia-dashboard)

---

## Overview

Gaia is a three-phase environmental monitoring system designed to investigate how urbanization affects local water quality in Central Florida. The system collects real-time water quality data, analyzes it across seven key parameters, and publishes the results to a live, publicly accessible dashboard — enabling direct comparison between urban, suburban, and rural water sources.

This project was built independently by a high school student as part of an ongoing research initiative into the relationship between urban development and freshwater ecosystem health.

---

## The Three Phases

### Phase 1 — Gaia Collector *(in development)*
A solar-powered robotic sampling arm that autonomously collects water samples from monitoring sites using a peristaltic pump and GPS-tagged location logging.

### Phase 2 — Gaia Dashboard *(live)*
A cloud-connected web dashboard that visualizes live sensor data, historical trends, and urbanization comparison analysis across multiple sampling sites in real time.

### Phase 3 — Gaia Analyzer *(simulation complete, hardware in progress)*
A stationary water quality testing station built on the ESP32 platform that measures seven water quality parameters and uploads results to a cloud database every 10 seconds.

---

## Sensors & Parameters Measured

| Parameter | Sensor | Unit |
|-----------|--------|------|
| Temperature | DS18B20 Waterproof Probe | °C |
| pH | DFRobot Gravity pH Sensor | pH |
| Total Dissolved Solids (TDS) | DFRobot Gravity TDS Sensor | ppm |
| Turbidity | DFRobot Gravity Turbidity Sensor | NTU |
| Dissolved Oxygen | Analog DO Sensor | mg/L |
| Conductivity | Analog EC Sensor | µS/cm |
| Oxidation-Reduction Potential (ORP) | Analog ORP Sensor | mV |

Each reading is evaluated against EPA water quality benchmarks and assigned a **Safety Score (0–100)** that reflects overall water quality health.

---

## Tech Stack

**Hardware**
- ESP32-WROOM-32D (38-pin)
- DS1307 RTC Module
- 7-sensor analog/digital array

**Firmware**
- Arduino C++ (ESP32 Core)
- OneWire / DallasTemperature
- RTClib
- ArduinoJson
- WiFi + HTTPClient

**Backend**
- Supabase (PostgreSQL, REST API)

**Frontend**
- HTML / CSS / JavaScript
- Chart.js (data visualization)
- Leaflet.js (interactive mapping)
- Hosted on GitHub Pages

---

## Urbanization Comparison Layer

Gaia's dashboard includes a unique research feature: a side-by-side comparison of water quality across sites with varying levels of urbanization, using metrics including:

- Population density
- Impervious surface percentage
- Distance to urban centers and highways
- Presence of nearby construction

This allows direct visual and statistical correlation analysis between urban development indicators and water quality parameters.

---

## Project Status

- ✅ Full sensor suite simulated and validated
- ✅ Real-time cloud database integration (Supabase)
- ✅ Live public dashboard with charts, map, and urbanization analysis
- ✅ RTC-based timestamping and WiFi failover logic
- 🔄 Physical hardware assembly in progress
- 🔄 Field deployment and real data collection — Summer 2026
- 🔄 Robotic sampling arm (Phase 1) — in development

---

## About

Built by Luca Cristancho, a rising senior at Lake Howell High School in Winter Park, FL, as an independent research and engineering project exploring the intersection of urban development and environmental health.

---

*Project Gaia — © 2026*
