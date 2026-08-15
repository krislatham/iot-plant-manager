# iot-plant-manager

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)]()
[![Hardware](https://img.shields.io/badge/Hardware-ESP32%20%7C%20MicroPython-blue.svg)]()
[![AI Engine](https://img.shields.io/badge/AI-OpenCV%20%7C%20YOLO-orange.svg)]()

> An automated IoT & AI-powered plant management system using MicroPython on microcontrollers and edge camera vision to detect foliage health, schedule precision irrigation, and control environmental conditions.

---

## 📌 Overview

**`iot-plant-manager`** is an end-to-end microcontroller and computer vision system designed to automate indoor plant care and greenhouse monitoring. By combining environmental IoT sensors (soil moisture, temperature, ambient light) with AI-enabled cameras (ESP32-CAM, Raspberry Pi Camera, or OpenCV/YOLO models), this project continuously assesses plant foliage health, detects early signs of pest infestation or disease, and controls automated irrigation and lighting systems in real time.

Built as an open educational project for robotics and IoT enthusiasts, this repository provides MicroPython firmware drivers, software domain layers, hardware schematics, computer vision pipelines, and web integration tools.

---

## ✨ Key Features

- **🤖 AI Visual Health Analysis:** Computer vision models classify foliage condition (e.g., leaf discoloration, wilting, blight, or pest damage) via on-device or edge-inferenced image processing.
- **🌱 Environmental Sensing:** Continuous logging of soil moisture, ambient temperature, relative humidity, and PAR light intensity.
- **⚙️ Closed-Loop Actuation:** Dynamic triggers for automated watering pumps, grow-light intensity, and exhaust fan cycles based on combined sensor data and visual health status.
- **📊 Live Video Feed & Telemetry:** Streams camera snapshots, detection bounding boxes, and IoT metrics to a central dashboard via MQTT/WebSockets.
- **🚨 Automated Early Warnings:** Sends instant notifications when visual anomalies (such as leaf yellowing or spotting) or soil dryness exceed configurable confidence thresholds.

---

## 🛠️ Hardware & Software Stack

| Component Category | Technologies & Hardware Modules |
| :--- | :--- |
| **Microcontrollers** | ESP32 / ESP32-CAM, Raspberry Pi (Zero 2 W / 4) |
| **Sensors** | Capacitive Soil Moisture Sensor v1.2, DHT22 (Temp & Humidity), BH1750 (Ambient Light) |
| **Actuators** | 5V Relay Modules, 12V Submersible Water Pump, LED Grow Lights, PWM Fan |
| **Firmware Environment**| MicroPython 1.20+, VSCode with Pymakr Extension |
| **Vision & UI** | Python 3, OpenCV, YOLOv8 Nano, TFLite, MQTT, WebSockets, ThingsBoard |

---

## 📁 Repository Structure

```text
iot-plant-manager/
├── docs/       # Hardware schematics, wiring diagrams, and architecture specs
├── dao/        # Data Access Objects (hardware state persistence, logging drivers)
├── domain/     # Core domain logic & business models (sensor thresholds, status objects)
├── lib/        # External MicroPython libraries & third-party driver modules
├── services/   # Active services (MQTT publisher, vision stream handler, actuation loops)
├── util/       # Helper utilities (Wi-Fi connection manager, pin mappings, logger)
├── LICENSE     # MIT License
└── README.md   # Project documentation
