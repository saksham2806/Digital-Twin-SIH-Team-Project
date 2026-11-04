# AI-Enabled Digital Twin for Aero Piston Engine Health Monitoring

An AI-enabled Digital Twin framework for real-time health monitoring and predictive maintenance of UAV aero-piston engines, integrating physics-informed engine simulation, synthetic sensor telemetry, fault injection, and machine-learning-based diagnostic capabilities.

## Overview

This project focuses on developing a virtual representation of an aero-piston engine to monitor its operating conditions, identify abnormal behaviour, and support predictive maintenance. The system combines a reduced-order physics-informed engine model with simulated sensor data and an interactive monitoring dashboard.

## Key Features

- **Digital Twin Engine Simulation:** Developed a physics-informed aero-piston engine simulator to represent engine behaviour under varying mission and environmental conditions.
- **Real-Time Telemetry:** Generated synthetic engine sensor data at 10 Hz to monitor critical parameters, including RPM, Cylinder Head Temperature (CHT), Exhaust Gas Temperature (EGT), oil pressure, oil temperature, fuel flow, and vibration.
- **Fault Injection & Diagnosis:** Implemented fault simulation for cooling degradation, injector degradation, lubrication degradation, mechanical degradation, misfire, and sensor drift.
- **Engine Health Monitoring:** Integrated health index, fault severity, diagnostic confidence, and engine operating status indicators.
- **Predictive Maintenance:** Incorporated prototype Remaining Useful Life (RUL) estimation and degradation trend monitoring to support maintenance decisions.
- **Interactive Dashboard:** Developed a Streamlit-based dashboard featuring live telemetry visualisation, fault injection controls, engine health indicators, and diagnostic outputs.

## System Architecture

The project follows a modular architecture consisting of:

1. **Engine Model:** Simulates aero-piston engine operating behaviour.
2. **Mission & Environment Model:** Represents mission phases, altitude, ambient temperature, and operating conditions.
3. **Fault Simulation:** Introduces controlled engine degradation and sensor faults.
4. **Sensor Model:** Generates simulated engine measurements and telemetry.
5. **Telemetry Logging:** Records engine parameters for monitoring and analysis.
6. **Health Monitoring Dashboard:** Displays engine status, fault diagnostics, health index, and RUL trends.

## Technologies Used

- Python
- Streamlit
- Pandas
- NumPy
- Matplotlib
- JSON
- CSV-based Telemetry Logging

## Repository Structure

```text
sih26/
│
├── config/
├── data/
├── digital_twin/
├── models/
├── simulator/
│   ├── engine.py
│   ├── environment.py
│   ├── faults.py
│   ├── mission.py
│   ├── sensors.py
│   └── telemetry.py
│
├── dashboard.py
├── main.py
├── generate_dataset.py
├── requirements.txt
└── README.md
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Rishi071056/sih26.git
cd sih26
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Engine Simulator

```bash
python main.py
```

### 4. Launch the Monitoring Dashboard

Open another terminal and execute:

```bash
streamlit run dashboard.py
```

## Future Scope

- Integration of real-world aero-piston engine sensor data.
- Advanced machine learning models for fault classification and anomaly detection.
- Improved virtual sensor modelling.
- Data-driven Remaining Useful Life prediction.
- Integration of real-time hardware telemetry.
- Enhanced Digital Twin synchronisation and predictive maintenance capabilities.

## Project Status

Prototype under development. The current implementation uses synthetic engine telemetry and a physics-informed simulation model. RUL outputs are illustrative estimates and require validation against real engine degradation data before operational use.

## Contributors

**Rishi** | **Saksham**

Collaboratively developed as part of an AI-enabled Digital Twin project for aero-piston engine health monitoring.
