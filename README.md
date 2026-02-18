# 🤖 Team CEAR - Robocon 2026 Submission

![Robocon Team CEAR](https://img.shields.io/badge/Team-CEAR-blue?style=for-the-badge&logo=robotframework&logoColor=white)
![Status](https://img.shields.io/badge/Status-Submission%20Ready-green?style=for-the-badge)

Welcome to the official repository for **Team CEAR**'s Robocon 2026 submission. This repository contains the CAD models, technical documentation, design calculations, and the machine learning modules developed for the competition.

---

## 📂 Project Overview

### 🏛️ 1. CAD Designs & Visuals
Detailed 3D models and assembly views of our robots.
- **Root Files**: 
  - `Final.STEP`: The master assembly file for the robot design.
  - `Lifting-Mechanism .mp4`: Video demonstration of our custom lifting system.
- **R1_Views/**: High-resolution renders and technical views of Robot 1 (R1).
- **R2_Views/**: High-resolution renders and technical views of Robot 2 (R2).

### 🧠 2. Deep Learning: Box Detection
A specialized vision module to identify and classify game elements.
- **Location**: `FakeReal-box-detection/`
- **Features**: 
    - Convolutional Neural Network (CNN) built with TensorFlow/Keras.
    - Classifies boxes into "Real" and "Fake" categories.
    - Optimized for low-latency inference on edge devices.
    - Includes a full training pipeline and dataset management.

### 📊 3. Engineering & Calculations
Scientific grounding for our mechanical designs.
- **Location**: `Calculations/`
- **Contents**:
    - `Calculations.pdf`: Detailed stress analysis, torque requirements, and stability factors.
    - `linear actuators calculation.jpeg`: Selection criteria and stroke analysis for our actuator systems.

### 📄 4. Technical Documentation
- **`Stage I Document – CEAR.pdf`**: Our comprehensive project report detailing the strategy, mechanical design, electronics, and software architecture.

---

## 🛠️ Technological Stack

- **Mechanical Design**: SolidWorks / CAD Software (STEP, MP4 Exports)
- **Deep Learning**: Python, TensorFlow, Keras, NumPy
- **Documentation**: LaTeX/Markdown, Engineering Analysis

---

## 🚀 Key Features

- **Robust Vision System**: High-accuracy real/fake box classification for autonomous tasks.
- **Optimized Lifting Mechanism**: Custom-engineered system for efficient object handling.
- **Multi-Robot Coordination**: Designed for seamless integration between R1 and R2.

---

## 👥 Team CEAR

| Role | Details |
| :--- | :--- |
| **Team Name** | **CEAR** |
| **Project** | ABU Robocon 2026 |
| **Focus** | Robotics, AI Vision, Mechanical Excellence |

---

## 📜 License
This project is for Robocon 2026 submission purposes. All rights reserved by Team CEAR.
