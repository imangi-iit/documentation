# Concepts Used

## 1. Introduction to PLCs

- What is a PLC?
- PLC Applications in Industry
- PLC Programming Languages

## 2. Docker and Containerization

- Docker Basics

  - What is Docker?
  - Docker Containers and Images
  - Docker Networking (Bridge, Host, Overlay)

- Docker Compose

  - Defining Multi-container Applications
  - Configuration Management

- Networking in Docker

  - Bridge Network
  - Virtual Ethernet (veth) Interfaces

## 3. OpenPLC

- Introduction to OpenPLC

  - What is OpenPLC?
  - OpenPLC Software Stack and Runtime
  - OpenPLC Code Examples

- Configuring OpenPLC in Docker

  - Installing OpenPLC on Docker
  - Running OpenPLC Containers
  - Configuring Communication Between Containers

## 4A. OPC UA Protocol

- Introduction to OPC UA

  - What is OPC UA?
  - OPC UA Security Features

    - Authentication
    - Encryption
    - Data Integrity

- Implementing OPC UA in Docker Containers

  - OPC UA Servers and Clients
  - Configuring OPC UA Communication

## 4B. Modbus Protocol | [link](https://www.advantech.com/en/resources/white-papers/5d094a3b-9c70-48fa-ae48-580d351fa42d)

- Introduction to Modbus Protocol
  - Default communication protocol behind OpenPLC.
- Format and content of Modbus data

  - Different types of data storage locations within a slave device.
  - **Coils** are single-bit, discrete outputs that can be read and written, while **registers** are 16-bit values that can also be read and written, or read-only depending on the register type.

### Coils

- Represent discrete (boolean), on/off (binary) values, like the state of a switch or a relay.
- Can be read to determine their current state (on or off).
- Can be written to change their state (e.g., turn a relay on or off).
- Modbus function codes for coils include reading multiple coils (01), reading a single coil (05), and writing a single coil (05).

### Registers

- Represent numerical values, typically 16-bit integers.
- Can be read to retrieve the current value.
- Can be written to change the value (with some registers being read-only).
- Modbus function codes for registers include reading multiple holding registers (03), reading multiple input registers (04), writing a single holding register (06), and writing multiple holding registers (16).
- Two types of registers:

  - Holding Registers (4x): These are general-purpose registers that can be both read and written. They are often used to store configuration parameters or setpoints.
  - Input Registers (3x): These registers are read-only and typically used to store sensor readings or other measured values.

### Addressing

- Each coil or register has a unique address within the Modbus slave device.
- These addresses are used in Modbus messages to specify which data element is being accessed.
- The specific addressing scheme (e.g., the starting address for coils or registers) is defined by the Modbus slave device.

## 5. Networking and Communication in PLC Emulation

- Docker Bridge Networking

  - How Docker Bridge Works
  - Container-to-Container Communication

- Ethernet Communication (eth0)

  - Connecting Containers to External Networks

## 6. Cybersecurity for PLC Systems

- PLC Vulnerabilities

  - Common PLC Security Threats
  - Known Cyberattacks on PLCs

- Types of Attacks

  - Man-in-the-Middle (MITM) Attacks
  - Dictionary Attacks
  - Worms and Malware

- Securing PLC Communications

  - OPC UA Security Features (Authentication, Encryption, Data Integrity)
  - Best Practices for Securing Industrial Networks

## 7. Cybersecurity Emulation Setup

- Simulating Cyber Attacks

  - Setting Up MITM Attacks
  - Brute Force and Dictionary Attacks on PLC Systems
  - Worm Simulation in Docker Containers

- Emulation Infrastructure

  - Configuring Docker Containers for Attack Simulations
  - Secure Configuration of Ports and Network Settings

## 8. Docker Container Security

- Securing Docker Containers

  - User Permissions
  - Network Isolation
  - Image Security Best Practices

- Using Docker Compose for Secure Configurations

  - Multi-Container Security Considerations
  - Managing Exposed Ports

## 9. Future Work and Optimizations

- Enhancements in Cybersecurity Emulation

  - Adding New Attack Scenarios
  - Enhancing Security Protocols

- System Optimization

  - Scaling Docker Containers for Larger Systems
  - Performance Tuning for Docker and OpenPLC

<!--

# Concepts Applied | Other Generated

## Containerization and Virtualization

- **Docker**: The entire system is virtualized using Docker containers, allowing the simulation of multiple devices (PLCs) and communication protocols in a controlled environment. Containers provide isolation, which is ideal for testing and security purposes.

## OPC UA and Industrial Protocols

- **OPC UA (Unified Architecture)**: A secure and scalable communication protocol widely used in industrial systems. It provides mechanisms for authentication, encryption, and integrity, ensuring secure data exchange.
- **Modbus**: A simple protocol for serial communication in industrial control systems. It is used to simulate interactions between PLCs and connected devices.
- **Siemens S7**: A proprietary industrial protocol for Siemens PLCs, commonly used in automation environments.

## Cybersecurity

- **Cyberattack Simulation**: Various cyberattacks, including MITM (Man-in-the-Middle) and dictionary attacks, are simulated to test the vulnerabilities of OT systems.
- **Encryption and Data Integrity**: Ensures that the communication remains secure from unauthorized access or modification. -->
