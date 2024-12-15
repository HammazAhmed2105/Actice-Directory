# Active Directory Home Lab Project Series

## Overview

Majority of organizations use **Active Directory** (AD) to manage resources such as users, computers, and groups. In this project series, we will build a **home lab** that is beneficial for both **blue teamers** and IT professionals in general. By the end of this five-part series, you will have:

- A fully functioning **Active Directory environment** to learn about AD administration and domain functionality.
- A **Splunk instance** ingesting events from your Windows Server (with AD) and a target Windows machine.
- Insights into **red team** and **blue team** activities, including generating and detecting attacks.

This project is hands-on and requires some time investment. 

---

## Key Highlights

1. **Learn by Doing:**
   - Set up and manage an Active Directory environment.
   - Configure and use **Splunk** to monitor your environment.
   - Use **Kali Linux** for red team attacks and **Atomic Red Team** for testing telemetry.

2. **Diagram First Approach:**
   - Build a network diagram at the start to visualize your environment. Diagrams are crucial during job interviews, where you may need to explain your setup and discuss security measures.

3. **Virtualized Setup:**
   - Use **VirtualBox** to set up the lab environment.
   - Take snapshots of virtual machines for experimentation without fear of permanent errors.

4. **Interactive Learning:**
   - Experiment with attacks and defenses.
   - Learn about logging, monitoring, and alert creation using **Splunk**.

---

## Project Breakdown

### **Part 1: Network Diagram and Environment Planning**
- Create a basic network diagram.
- Understand the purpose of each component in the lab environment.

### **Part 2: Asset Installation and Configuration**
- Download and install the following:
  - **Windows Server 2022**
  - **Windows 10** (Target Machine)
  - **Kali Linux** (Attack Machine)
  - **Splunk** (on Ubuntu Server)
- Configure the lab using **VirtualBox**.

### **Part 3: Logging and Monitoring Setup**
- Install and configure **Sysmon** for detailed logging.
- Set up Splunk to query telemetry.
- Experiment with creating your own alerts, dashboards, and reports.

### **Part 4: Active Directory Configuration**
- Configure Active Directory on Windows Server.
- Promote the server to a **Domain Controller**.
- Create and manage domain users.
- Join the target Windows machine to the domain.

### **Part 5: Attack Simulation and Telemetry Analysis**
- Perform a **brute force attack** on a domain user using Kali Linux.
- Analyze telemetry generated in Splunk.
- Use **Atomic Red Team** to simulate attacks and monitor results.

---

## Learning Outcomes

- **Red Team Skills:**
  - Launch attacks using Kali Linux.
  - Understand how attacks work in an Active Directory environment.

- **Blue Team Skills:**
  - Detect and analyze telemetry from servers and endpoints.
  - Configure Splunk to monitor and alert on suspicious activities.

- **Beginner-Friendly Environment:**
  - Experiment with configurations and learn without fear of breaking systems.

---

## Troubleshooting

A separate troubleshooting guide will be provided to address common errors encountered during the project.

---

## Additional Resources

- **Splunk Documentation & Training Videos:** Learn how to build alerts, reports, and dashboards.
- **GitHub Portfolio Setup:** If you don't know how to showcase your project on GitHub, refer to [this video tutorial](#) (link to your video).

---

## Bonus Content

I am working on a comprehensive **SOC Analyst Course**, which includes additional attack scenarios, alert creation, and dashboard building using Splunk. If you're interested, stay tuned for more details.

---

## Showcase Your Work

Feel free to include this project in your portfolio! Use GitHub or any free site to highlight your work and demonstrate your skills to potential employers.

---

Thank you for following along, and remember to stay curious and always do things differently!
