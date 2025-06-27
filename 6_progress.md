# Current Progress and Future Goals

## Current Progress

- **System Design**: The architecture for the PLC emulation and cyberattack simulation is complete.
- **Docker Setup**: Docker containers for OPC UA, Modbus, and Siemens S7 protocols have been created.
- **Cyberattack Simulation**: MITM and dictionary attack simulations have been implemented and tested successfully.
- **Security Implementation**: Authentication and encryption mechanisms have been configured for secure communication.

## Future Goals

- **Advanced Attack Scenarios**: Simulating more complex attacks, such as ransomware or denial of service (DoS) attacks.
- **Scalability**: Expanding the emulation to simulate larger industrial networks with more devices.
- **Optimization**: Improving system performance by optimizing container configurations and network settings.

## Types of Cyberattacks that can be performed

### 1. Basic and Common Implementation
* **Setup**: For a legit pair of server and client, communicating with each other via the OPC-UA protocol.
* Each of the devices have their own sets of MAC Addresses mapped to their respective IP Addresses. (ARP Cache Table)
* The attacker can perform ARP spoofing (ARP Cache table poisoning) and include its own IP Address to the requested MAC Address. The same can be done on both the ends (attacker <-> server and attacker <-> client).
* For a better understanding of the same, check out the attached image. (More details of the attack have been highlighted <here>). 
* !(query) Can you manually trigger the re-configuration of the MAC Address?
* Based on the concept when you use in the **testing** environment (otherwise, OPC UA is a secure protocol which has encryption, authentication and authorization).

### 2. IO-Link based Communication (need to explore this more)
* IO Link is used to connect smart sensors (SS) or IIoT components to the PLC for enabling wireless (sure?) communication.
* The older protocols like Ethernet and Profinet are under use in this case.
* 

### 3. Value mismatch between SCADA Representation and Real Life Implementation
* SCADA simply `GETS` the value from the web server where the respective protocols publish them. (`opc.tcp://localhost:4840` for OPC-UA; `502` for Modbus-TCP, etc).
* These values can be modified before they are shown upon the screen, and manipulated commands can be sent from SCADA. 