# Other References and Auxiliary Stuff

## Detailed Documentation for Softwares and Protocols Used

- **Docker Documentation**: [https://docs.docker.com/](https://docs.docker.com/)
- **OpenPLC Runtime & Editor**: [https://autonomylogic.com/](https://autonomylogic.com/)
- **OPC UA Specifications**: [https://www.opcfoundation.org/about/opc-technologies/opc-ua/](https://www.opcfoundation.org/about/opc-technologies/opc-ua/)
- **Modbus Protocol**: [https://modbus.org/](https://modbus.org/)
- **Siemens S7 Protocol**: [https://support.industry.siemens.com/cs/document/109746613](https://support.industry.siemens.com/cs/document/109746613)

## Research Papers
- [OPC UA Security](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5514836)
- [PLC Network Security](https://doi.org/10.1016/j.ijcip.2018.05.004)
- [OpenPLC for Cyber Attack (Case Studies) on Smart Substation Systems](/assets/research-papers/Compatible_OpenPLC.pdf)
- [Digital Twin Based Cyber Attack Detection Framework for Cyber Physical Manufacturing Systems](/assets/research-papers/Digital_Twin-Based_Cyber-Attack_Detection_Framework_for_Cyber-Physical_Manufacturing_Systems.pdf)
- [Evaluation of OPC UA Secure Communication in Web Browser Applications](/assets/research-papers/Evaluation_of_OPC_UA_secure_communication_in_web_browser_applications.pdf)
- [Investigating the Security of OpenPLC Vulnerabilities Attacks and Mitigation Solutions](/assets/research-papers/Investigating_the_Security_of_OpenPLC_Vulnerabilities_Attacks_and_Mitigation_Solutions.pdf)
- [On PLC Network Security](/assets/research-papers/On_plc_network_sec.pdf)
- [OpenPLC based control system testbed for PLC whitelisting system](/assets/research-papers/OpenPLC.pdf)
- [OPC UA Based on Electronic Device Description](/assets/research-papers/Research_on_OPC_UA_based_on_electronic_device_description.pdf)
- [Research on OPC UA Security](/assets/research-papers/Research_on_OPC_UA_security.pdf)
- [Security Challenges in Industry 4.0](/assets/research-papers/security_challenges_in_industry_4.pdf)
- [MITM Attack Research Paper](/assets/research-papers/mitm-attack-research-paper.pdf)

## Articles & Documents
- [Detailed blog on OPC UA Protocol Cyber Threats](https://www.txone.com/blog/opc-ua-protocol-cyber-threats/)
- [Docker networking explained](https://indumathimanivannan.medium.com/docker-network-modes-explained-bridge-host-and-overlay-comparisons-d691857f9d30)
- [Rogue Certificate](https://www.thesslstore.com/blog/what-is-a-rogue-certificate/)
- [Idea behind SSL Certificate](https://aws.amazon.com/what-is/ssl-certificate/)
- [Structure of OPC UA message](https://reference.opcfoundation.org/Core/Part6/v105/docs/7.1.2)
- [Publisher Subscriber model for OPC UA](https://prosysopc.com/blog/opc-ua-pubsub-explained/)
- [Stuxnet - Real life worm attack on Iran Nuclear Base by USA](https://www.trellix.com/en-in/security-awareness/ransomware/what-is-stuxnet/)
- [OPC UA (OPC Day) Based Communication (PubSub & Server-Client)](/assets/research-papers/13_opc_day.pdf)
- [DEFCON 2025 | S7 Communication Breaking](/assets/research-papers/DEFCON-2025.pdf)
- [Understanding Linux real-time with PREEMPT_RT training](/assets/research-papers/preempt-rt-slides.pdf)
- 

## Data Visualisation and Logging Software
- [Prometheus](https://prometheus.io/) - Open source metrics and monitoring for your systems and services
- [Grafana](https://grafana.com/) - Monitoring system (seems to be advanced and famous)
- [Kibana](https://www.elastic.co/kibana)

## GitHub Links

### Primary Usage
- [AsyncIO Library for OPC UA](https://github.com/FreeOpcUa/opcua-asyncio)
  - Installed using `pip`. Command: `pip install asyncua` or `pip3 install asyncua`
- [OpenPLC v3 Library](https://github.com/thiagoralves/OpenPLC_v3)
- [OPC UA GUI Based Client](https://github.com/FreeOpcUa/opcua-client-gui)
  - Installed using `pip`. Command: `pip install opcua-client` or `pip3 install opcua-client`
### OPC UA Libraries
- [C# Language Based Library](https://github.com/OPCFoundation/UA-.NETStandard)
- [Python Language Based Library](https://github.com/FreeOpcUa/python-opcua) - this is what we are using in the project
  - A few of the examples are not working for the given repository.
  - The structure of the code is not correct for some updated libraries like UTC time etc.
- [C Language Based Library](https://open62541.org/)
- [Java Based Library](https://github.com/eclipse/milo)
### Future Prospects
- [Emulates exploits and attacks on OPC UA based systems](https://github.com/claroty/opcua-exploit-framework)
- [Reinforcement Learning Based Attacker and Defender system on IT Infrastructure](https://github.com/Limmen/csle) | (Previous Intern developments based on CSLE: [link](https://github.com/Artifex2002/csle))
### Auxilliary/Derived Libraries
- [Runs OPC UA emulation on 2 Raspberry Pi - Rudimentary](https://github.com/FHatCSW/OPCUA-Sample)
- [Docker container for OpenPLC Server](https://github.com/jpaffrath/docker-openplc)
- [Previous Documentation by Ashutosh on Notion](https://www.notion.so/e179a310d01c4af39e249d1d50d2935c?v=b8f2151dcac7432aa148bf22530eabf1)
- [OPCUA as a base communication protocol - not supported](https://github.com/andiburger/OpenPLC_v3_Opcua)

## Tools Used | Explore them

- **Wireshark**: For network traffic analysis during attack simulations.
- **Metasploit**: For simulating cyberattacks.
- **Ghidra**: For analyzing and debugging security vulnerabilities in the system.

## Glossary

- **MITM (Man-in-the-Middle)**: An attack where an attacker intercepts and potentially alters communication between two parties.
- **OPC UA**: Open Platform Communications Unified Architecture, a protocol used for secure data exchange in industrial control systems.
- **PLC**: Programmable Logic Controller, used in industrial automation for controlling machines and processes.
