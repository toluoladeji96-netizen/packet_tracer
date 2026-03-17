# Multi-Network VLAN Project

## Project Overview
This project demonstrates inter-network communication between three separate networks using a router and VLANs in Cisco Packet Tracer. 
The setup includes multiple PCs, switches, and a router with subinterfaces configured for VLAN routing.

[PC1] --- [Switch1] ---+
[PC2] --- [Switch1] |
[PC3] --- [Switch1] +--- [Router] --- Internet/Other Network
[PC4] --- [Switch2] ---+
[PC5] --- [Switch2] |
[PC6] --- [Switch2] +--- [Router]

## Network Topology

- **Network 1:** 192.168.1.0/24 (PC1, PC2, PC3)
- **Network 2:** 192.168.2.0/24 (PC4, PC5)
- **Network 3:** 192.168.3.0/24 (PC6)

---

## Devices Used
- Router: GigabitEthernet0/0/1 subinterfaces configured with 802.1Q encapsulation
- Switches: Layer 2 switches with VLAN assignment
- PCs: End devices connected to switches with static IP addresses

---

## Key Configurations

### Router
- Subinterfaces configured for VLAN routing
- IP addresses assigned per VLAN
- Example:
```text
interface g0/0/1.2
 encapsulation dot1Q 2
 ip address 192.168.2.1 255.255.255.0

Switches

VLANs created and assigned to ports:
vlan 2
 name Network2
vlan 3
 name Network3

interface fa0/1
 switchport mode access
 switchport access vlan 2

**How to Open
Download the .pkt file from the pkt_files/ folder.
Open Cisco Packet Tracer.
Open the downloaded .pkt file.
Use the simulation mode to test connectivity between devices.

Learning Outcomes
Understanding of VLAN configuration and routing between VLANs.
Inter-network communication setup using a router with subinterfaces.
Practical experience with IP addressing and subnetting.


