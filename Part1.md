# Creating a Logical Diagram
# Active Directory Project - Lab Diagram  

## Overview  
This project is part of a five-part series where we build a fully functional Active Directory (AD) lab from scratch. The lab includes two servers, two computers, and a network setup. This environment helps you practice installing and configuring AD, Splunk, and related tools, providing practical experience to showcase during interviews.  

## Lab Diagram  
Below is the diagram representing our lab environment:  

![Lab Diagram](path-to-your-diagram-image)  

### Components  
- **Servers**  
  - **Active Directory Server**  
    - IP: `192.168.10.20`  
    - Installed Tools:  
      - Splunk Universal Forwarder  
      - Sysmon (Telemetry collection)  
    - Purpose: Manage the domain and forward logs to the Splunk server.  
  - **Splunk Server**  
    - IP: `192.168.10.10`  
    - Installed Tools:  
      - Splunk Enterprise  
    - Purpose: Collect and analyze logs from the AD server and the target machine.  

- **Computers**  
  - **Target Machine**  
    - OS: Windows 10  
    - IP: DHCP Assigned  
    - Installed Tools:  
      - Splunk Universal Forwarder  
      - Sysmon  
      - Atomic Red Team (for generating test data)  
    - Purpose: Simulate a workstation in the domain.  
  - **Attacker Machine**  
    - OS: Kali Linux  
    - IP: `192.168.10.250`  
    - Purpose: Simulate an attacker attempting to compromise the network.  

- **Network Infrastructure**  
  - **Switch**: Connects all devices.  
  - **Router**: Provides connectivity between the lab and the internet.  
  - **Cloud**: Represents the internet.  

### Network Information  
- **Domain Name**: `mydfir.local`  
- **Network Subnet**: `192.168.10.0/24`  

### Log Forwarding  
- Logs are forwarded to the Splunk server from:  
  - Active Directory Server  
  - Target Machine  
- **Log Forwarding Details**:  
  - Connection: Dotted green lines in the diagram  
  - Tools Used: Splunk Universal Forwarder  

### Potential Enhancements  
To make the lab more advanced, you could add:  
- **Intrusion Detection System (IDS)**  
- **Endpoint Detection and Response (EDR)**  
- **Firewall**  

## Future Steps  
In the next part of this series, we will:  
1. Install all components (servers, virtual machines, tools).  
2. Configure the network to connect all devices.  
3. Begin the exciting process of generating and analyzing telemetry data.  

## Tools Used for Diagram Creation  
The diagram was created using [Draw.io](https://app.diagrams.net/), a free and easy-to-use tool for creating network diagrams.  

## Stay Connected  
Follow along with this series to build your skills, troubleshoot issues, and get hands-on experience for interviews. Let’s stay curious and do things differently!  

