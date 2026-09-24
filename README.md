# 🏨 Hotel Network Design

A secure and scalable **Hotel Network Management System** designed and simulated using **Cisco Packet Tracer**. The project integrates VLAN segmentation, OSPF dynamic routing, ACL-based security, centralized network services, wireless connectivity, and IoT automation.

---

## 📌 Project Overview

This project presents a multi-floor hotel network connecting guest floors, Reception, Accounts, a central server room, wireless devices, and IoT systems.

The network is designed to provide reliable communication, network segmentation, centralized services, security, and smart-room automation.

---

## 🏗️ Network Architecture

The network consists of **five routers**, switches, wireless access points, centralized servers, hotel departments, and IoT devices.

```mermaid
flowchart TB

    R1[Router 1]
    R2[Router 2]
    R3[Router 3]
    R4[Router 4]
    R5[Router 5]

    R1 <-->|OSPF| R2
    R2 <-->|OSPF| R3
    R3 <-->|OSPF| R4
    R4 <-->|OSPF| R5

    R1 --> Reception[Reception]
    R2 --> Floor1[Guest Floor 1]
    R3 --> Floor2[Guest Floor 2]
    R4 --> Floor3[Guest Floor 3]
    R5 --> Accounts[Accounts]

    R1 --> Servers[Server Room]

    Servers --> DHCP[DHCP]
    Servers --> DNS[DNS]
    Servers --> WEB[Web Server]
    Servers --> EMAIL[Email Server]
    Servers --> IOT[IoT Server]

    Floor1 --> AP1[Wireless AP]
    Floor2 --> AP2[Wireless AP]
    Floor3 --> AP3[Wireless AP]

    IOT --> RFID[RFID Door Lock]
    IOT --> Motion[Motion Sensor]
    IOT --> CCTV[CCTV]
    IOT --> Light[Smart Light]
    IOT --> Temp[Temperature Sensor]
    IOT --> Fire[Fire Sensor]

🔑 Key Features
- Multi-floor hotel network
- VLAN-based network segmentation
- Inter-VLAN routing using router-on-a-stick
- OSPF dynamic routing
- ACL-based network security
- DHCP automatic IP assignment
- DNS name resolution
- Hotel Web Server
- Internal Email Server
- Centralized IoT Server
- Wireless guest connectivity
- RFID-based door access
- Motion-based lighting and CCTV automation
- Temperature and AC automation
- Fire detection and emergency response
🖥️ Network Services
Service	Purpose
DHCP	Automatic IP address assignment
DNS	Domain name resolution
Web Server	Hotel website hosting
Email Server	Internal communication
IoT Server	Smart device management and automation


🤖 IoT Automation
The project integrates smart devices to automate hotel operations.
Motion Detected
      ↓
Light ON + Camera Activated


RFID Card
      ↓
Authorization
      ↓
Door Unlock


Fire Detected
      ↓
Alarm + Sprinkler Activated

🔐 Security
VLANs separate Guest, Reception, Accounts, Server, and IoT traffic.
ACLs are used to restrict unauthorized communication. For example:
Guest VLAN ────────► Accounts VLAN
                       ❌ BLOCKED

🧰 Tools & Technologies
- Cisco Packet Tracer
- Cisco Routers & Switches
- VLAN
- OSPF
- ACL
- 802.1Q
- DHCP
- DNS
- Web Server
- Email Server
- IoT Server
- Wireless Networking
- RFID and IoT Automation
📊 Results
The simulated network successfully demonstrates:
- Network connectivity between hotel departments
- VLAN segmentation
- OSPF-based dynamic routing
- Automatic IP configuration
- DNS and Web Server access
- Internal email communication
- ACL-based traffic restriction
- IoT device communication and automation
