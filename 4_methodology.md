# Methodology Followed

## 1. Literature Review and Insights from AI

The first step involved conducting a thorough literature review on the cybersecurity of OT components. This helped in understanding the current state of the domain, identifying key challenges, and gathering insights into potential security issues faced by OT systems. AI-based methodologies and modern threat detection techniques were also explored for integration into the project.

## 2. Collection and Accumulation of Resources

A comprehensive collection of resources was accumulated, including:
- Articles, white papers, and journals on cybersecurity and OT components.
- GitHub repositories with relevant code, tools, and frameworks for OT emulation and cybersecurity.
- Documentation on industrial protocols (OPC UA, Modbus, Siemens S7), Docker containers, and attack simulation techniques.

These resources laid the foundation for the next steps in the project.

## 3. Deciding Upon the Stages of the Project and Components/Infrastructure

### Initial Stage: Understanding OPC UA Communication
- **Protocol Selection**: The project started with **OPC UA** protocol due to its widespread use in industrial environments and its built-in security features.
- **Sample Client-Server Setup**: A sample client-server setup was created using `opc.tcp://localhost:4840` port to understand the basics of OPC-UA and TCP-based communication.
    - A simple, manually coded PLC program was used to test this communication.
    - The focus was on connecting the OPC UA client (a GUI-based software) to the server and visualizing the PLC’s working, including reading and modifying values.

### Docker Containerization
- **Developing Docker Containers**: Docker containers were created to emulate the client and server components. The containers were configured to expose ports `4840` (OPC UA) and `502` (Modbus) for open communication within the network.
- **Custom PLC Program with OpenPLC**: A custom PLC program was developed using OpenPLC Editor. The program contained three variables, one of which was mutable (input), and was then run in the server container.
    - The client container was able to read and modify the values in the server container, allowing further experimentation with scripts for interaction.

## 4. Progressing to Additional Protocols

After successfully implementing OPC UA, the next step was to extend the system to support other protocols:
- **Siemens S7 Protocol**: The same approach was followed for the Siemens S7 protocol, where a custom PLC program was used to emulate the communication between the client and server containers.
- **Modbus Protocol**: Similarly, Modbus protocol was integrated into the system to test communication with additional types of OT devices.

## 5. Development of Attack Simulation

- **Creating Attacker Docker Container**: An attacker container was developed to simulate a cyberattack on the emulated OT components. Initially, the attacker container was set up to sniff network packets between the client and server containers.
    - This initial phase focused on basic packet sniffing to identify communication vulnerabilities.
    - **Advanced Attack Techniques**: Future work will involve a more sophisticated approach to enter the Docker network without leaving traces in the Docker logs. Research on this advanced method will be explored.

## 6. Simulation of MITM Attack

- **MITM Attack Simulation**: A basic MITM attack was simulated by intercepting the communication between the client and server. 
    - This was implemented using packet sniffing tools, and future work will enhance this by including more complex attack techniques, such as **IP address spoofing** and modifying the intercepted communication.

## 7. Future Goals

The future goals for the project include:
- **Advanced Attack Scenarios**: Implementing more nuanced attack types, such as **Ransomware** or **Denial of Service (DoS)** attacks, to test the resilience of the system under different types of threats.
- **Attack Evasion Techniques**: Exploring more advanced methods to bypass security measures in Docker containers, potentially integrating **AI-based intrusion detection systems**.
- **Scalability**: Extending the emulation to handle larger industrial networks with multiple devices and communication protocols.
- **Optimization**: Refining the system for better performance, enhancing the speed and efficiency of both emulation and attack simulations.
