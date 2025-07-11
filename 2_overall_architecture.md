# Overall Architecture

## System Architecture

The architecture for the FSM Cybersecurity project is designed to emulate real-world industrial automation systems using Docker containers. Below is a high-level view of the architecture:

### Docker Containers

- **PLC Client and Server Containers**: Emulates the communication between PLCs using protocols like OPC UA, Modbus, and Siemens S7.
- **OpenPLC**: The software that runs inside the Docker containers to simulate PLC behavior.
- **Cyberattack Simulation**: A set of tools and scripts to simulate attacks like MITM and dictionary attacks on the emulated PLC systems.

### Communication Flow:

1. **PLC Runtime**: Emulated PLC code executes control logic in Docker containers. (In simple terms, it is a compiler for the PLC program)
2. **Network Layer**: Uses Docker’s bridge network for secure communication between containers. (emulates a switch and how the OT components are on the same network)
3. **Attack Simulation**: Cyberattacks are launched via a dedicated attack container, interacting with PLC systems to test vulnerabilities.
4. **Sniffing Containers**: These containers would not be detected by the Docker logger if they are programmed accordingly (advanced application). But, they _are_ visible at the low end (like in the Address Resolution Protocol (ARP) Table, etc).

### Communication Protocols

- **OPC UA**: Used for secure communication between PLCs and clients.
- **Modbus and Siemens S7**: Other communication protocols used to emulate real industrial systems.

### Network Design

- **Docker Bridge Network**: Ensures that all containers can communicate securely, isolated from the host machine.
- **veth Interfaces**: Virtual Ethernet interfaces are used for container-to-container communication within the Docker network.

### Security Measures

- **Encryption**: All communication over OPC UA is encrypted to prevent unauthorized interception.
- **Authentication**: Only authorized devices can communicate within the system.

### Cyberattack Detection

- **Intrusion Detection System (IDS)**: Monitors the network traffic for suspicious activity, indicating potential cyberattacks.
- **Log Analysis**: Logs all activities for analysis after an attack is simulated to understand the impact.

### Docker Network Topology:

The containers communicate via Docker bridge networks, allowing for secure inter-container communication and exposure of ports to simulate real-world industrial communication. The server and client (official containers and parts of the network) lie on the network. An attacker has been added (for initial and naive implementation). An attacker can be programmed to sniff the network without it being an official part of the Docker bridge.

### Presentation Link

Check out the following presentation to get a brief, holistic idea about the project. [Link](https://drive.google.com/file/d/1rhEc1GYZic-qcUvPH_W2J9dXcxn2OWyw/view?usp=sharing).
