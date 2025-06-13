---
# Documentation for FSM Cybersecurity Project | Methodology Followed
---

## Steps Followed
1. Literature Review and Insights from AI about the past developments in this domain (cybersecurity of OT components).
2. Collection and accumulation of resources (articles, GitHub repositories, etc).
3. Deciding upon the stages of the project and the components/infrastructure to be used at each stage.
    - Starting with **OPC UA** protocol and implementing the idea of a sample client-server using the `ocp.tcp://localhost:4840` port. This used a manually coded sample PLC program, because the aim was to understand and implement OPC-UA and TCP based communication.
    - Running and configuring the OPCUA Client (a GUI based software for visualising a PLC and its working), connecting it to the port, reading values, changes, etc.
    - Development of Docker containers to emulate clients and server, exposing the 4840 and 502 ports for open communication in the network.
    <!-- - Now, the base was set for development of more advanced and a complex setup, which was again, closer to a real life lab emulation.  -->
    - Now, a custom PLC program was made using OpenPLC editor with simple three variables, one of which was the input and hence mutable. This was ran in the server Docker container, with the client being able to read the values (developing scripts of different kinds to read the values).
4. Move on to the next protocols - Siemens S7 and Modbus and follow a similar approach for them.
5. Developing an attacker Docker container to initially sniff the packets (there exist an advanced and a more nuanced approach to enter the Docker network without being inside the Docker logs, explore that).
6. Simulation of MITM attack (advanced implementation would include IP address spoofing, etc).
7. Future Goals ...