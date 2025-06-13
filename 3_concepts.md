# Concepts Used

## **1. Introduction to PLCs**

* **What is a PLC?**
* **PLC Applications in Industry**
* **PLC Programming Languages**

## **2. Docker and Containerization**

* **Docker Basics**

  * What is Docker?
  * Docker Containers and Images
  * Docker Networking (Bridge, Host, Overlay)
* **Docker Compose**

  * Defining Multi-container Applications
  * Configuration Management
* **Networking in Docker**

  * Bridge Network
  * Virtual Ethernet (veth) Interfaces

## **3. OpenPLC**

* **Introduction to OpenPLC**

  * What is OpenPLC?
  * OpenPLC Software Stack and Runtime
  * OpenPLC Code Examples
* **Configuring OpenPLC in Docker**

  * Installing OpenPLC on Docker
  * Running OpenPLC Containers
  * Configuring Communication Between Containers

## **4. OPC UA Protocol**

* **Introduction to OPC UA**

  * What is OPC UA?
  * OPC UA Security Features

    * Authentication
    * Encryption
    * Data Integrity
* **Implementing OPC UA in Docker Containers**

  * OPC UA Servers and Clients
  * Configuring OPC UA Communication

## **5. Networking and Communication in PLC Emulation**

* **Docker Bridge Networking**

  * How Docker Bridge Works
  * Container-to-Container Communication
* **Ethernet Communication (eth0)**

  * Connecting Containers to External Networks

## **6. Cybersecurity for PLC Systems**

* **PLC Vulnerabilities**

  * Common PLC Security Threats
  * Known Cyberattacks on PLCs
* **Types of Attacks**

  * Man-in-the-Middle (MITM) Attacks
  * Dictionary Attacks
  * Worms and Malware
* **Securing PLC Communications**

  * OPC UA Security Features (Authentication, Encryption, Data Integrity)
  * Best Practices for Securing Industrial Networks

## **7. Cybersecurity Emulation Setup**

* **Simulating Cyber Attacks**

  * Setting Up MITM Attacks
  * Brute Force and Dictionary Attacks on PLC Systems
  * Worm Simulation in Docker Containers
* **Emulation Infrastructure**

  * Configuring Docker Containers for Attack Simulations
  * Secure Configuration of Ports and Network Settings

## **8. Docker Container Security**

* **Securing Docker Containers**

  * User Permissions
  * Network Isolation
  * Image Security Best Practices
* **Using Docker Compose for Secure Configurations**

  * Multi-Container Security Considerations
  * Managing Exposed Ports

## **9. Future Work and Optimizations**

* **Enhancements in Cybersecurity Emulation**

  * Adding New Attack Scenarios
  * Enhancing Security Protocols
* **System Optimization**

  * Scaling Docker Containers for Larger Systems
  * Performance Tuning for Docker and OpenPLC