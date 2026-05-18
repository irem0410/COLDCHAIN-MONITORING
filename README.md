# Cold-Chain Logistics Monitoring Simulation using OMNeT++, INET, and FLoRa

Final Project for CNG 476 – System Simulation  
Middle East Technical University Northern Cyprus Campus (METU NCC)

## Group Members
- Ali Murat Chatkha
- Irem Dede

---

# Project Description

This project models a simplified IoT-based cold-chain monitoring system using discrete-event simulation in OMNeT++. The system simulates environmental monitoring during transportation/storage using LoRaWAN communication.

Three wireless sensor nodes periodically generate temperature and humidity measurements and transmit them through a LoRa gateway to a backend server. The simulation evaluates communication reliability, packet delivery behaviour, collisions, and alarm generation under stochastic environmental conditions.

The project was implemented using:
- OMNeT++
- INET Framework
- FLoRa Framework

---

# Main Features

- LoRaWAN-based wireless communication
- Periodic environmental monitoring
- Temperature and humidity generation
- Alarm triggering when thresholds are exceeded
- Packet forwarding through gateway/server architecture
- Randomized sensor behaviour using stochastic distributions
- Repeated simulation runs using different random seeds
- Statistical analysis of simulation outputs

---

# Repository Structure

## src/

Contains the main C++ application implementation.

### Files
- `ColdChainApp.cc`
  - Main application logic
  - Sensor value generation
  - Packet creation and transmission
  - Alarm generation
  - Scheduling periodic events

- `ColdChainApp.h`
  - Header definitions for the simulation application

---

## ned/

Contains OMNeT++ network topology definitions.

### Files
- `ColdChainNetwork.ned`
  - Main network topology definition

- `SensorNode.ned`
  - Sensor node structure

- `Gateway.ned`
  - LoRa gateway module

- `BackendServer.ned`
  - Backend/application server definition

---

## ini/

Contains simulation configuration files.

### Files
- `omnetpp.ini`
  - Main simulation configuration
  - Simulation duration
  - Number of runs
  - Random seeds
  - Module parameters

- `coldchain.ini`
  - Additional scenario configuration parameters

- `energyConfig.xml`
  - Energy-related configuration settings

- `General.anf`
  - OMNeT++ analysis configuration file

---

## results/

Contains generated simulation output files.

### Files
- `results.vec`
  - Vector results from simulations

- `results.vci`
  - Indexed vector result file

- Scalar outputs generated from repeated simulation runs

---

### Included Figures
- System topology
- Temperature time-series plots
- Humidity time-series plots
- Histograms
- Q-Q plots
- Packet delivery ratio plots
- Collision analysis plots
- Alarm result figures
- Console execution screenshots

---

# Simulation Parameters

| Parameter | Value |
|---|---|
| Number of Sensor Nodes | 3 |
| Simulation Duration | 3600 seconds |
| Communication Technology | LoRaWAN |
| Simulation Type | Discrete-Event Simulation |
| Temperature Distribution | Normal Distribution |
| Humidity Distribution | Normal Distribution |
| Number of Repeated Runs | 10 |

---

# Performance Metrics

The project evaluates:
- Packet Delivery Ratio (PDR)
- Collision Count
- Alarm Frequency
- Environmental Variability
- Communication Reliability

---

# Statistical Modelling

The simulation includes:
- Random number generation
- Normally distributed environmental values
- Monte Carlo repeated simulation runs
- Histogram analysis
- Q-Q plot analysis
- Confidence interval estimation

---

# Running the Project

1. Open OMNeT++
2. Import the project folder
3. Build the project
4. Run the simulation using:
   - `omnetpp.ini`

Framework requirements:
- INET Framework
- FLoRa Framework

---

# Notes

This project was developed for educational purposes as part of the CNG 476 System Simulation course.

The implementation focuses on demonstrating discrete-event simulation concepts, stochastic modelling, wireless communication behaviour, and IoT-based monitoring systems.

---
