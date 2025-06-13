# System Overview

## Introduction

The FSM Cybersecurity Project aims to emulate Operational Technology (OT) components such as PLCs (Programmable Logic Controllers), communication protocols like OPC UA, Modbus, and Siemens S7-1500. These emulations are accomplished using Docker containers to simulate both the devices and protocols typically found in ICS (industrial control system). Furthermore, the project focuses on testing various cyberattacks that could be executed against these components.

This system allows us to replicate the cyber-physical systems found in the Cyber-Physical Lab (FSM, IIT Delhi), testing security protocols and attack vectors in a controlled, virtual environment.

## Key Components

## Emulated OT Components

The system consists of the following emulated OT components:

- **PLCs (Programmable Logic Controllers)**: These are the main control systems in industrial environments.
- **Communication Protocols**:
  - **OPC UA (Unified Architecture)**: A platform-independent communication protocol for secure data exchange.
  - **Modbus**: A protocol for communication between devices in industrial networks.
  - **Siemens S7**: A proprietary protocol used by Siemens PLCs for industrial automation.

These components will be emulated inside Docker containers to replicate their functioning in a controlled environment, enabling us to simulate interactions and test different cybersecurity strategies.

## Components and Services

- **Docker Containers**: The system is containerized using Docker, ensuring the ease of deployment and isolation of different OT components.
- **Communication Wrappers**: For secure interaction between the PLCs and clients, communication wrappers are developed using protocols like OPC UA.
- **Cyberattack Simulation**: The project aims to simulate various cyberattacks, including sniffing, Man-in-the-Middle (MITM) attacks, Dictionary attacks, and worms, to test the vulnerabilities of these systems. These attacks are simulated within the Docker containers, and the system analyzes the vulnerabilities in real-time.

---