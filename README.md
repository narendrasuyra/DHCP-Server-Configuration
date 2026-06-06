# DHCP Configuration in Cisco Packet Tracer

## 📌 Project Overview
This project demonstrates the configuration of a Cisco router as a DHCP (Dynamic Host Configuration Protocol) server in Cisco Packet Tracer. The router automatically assigns IP addresses to client PCs, reducing manual configuration and improving network management.

## 🎯 Objective
Configure a Cisco router as a DHCP server to automatically provide IP addresses to hosts connected through a switch.

## 🛠️ Network Topology

### Devices Used
- 1 Router
- 1 Switch
- 4 PCs (PC0, PC1, PC2, PC3)

### Connections
- Router → Switch
- PC0 → Switch
- PC1 → Switch
- PC2 → Switch
- PC3 → Switch

## 🌐 Network Addressing

| Parameter | Value |
|------------|---------|
| Network Address | 192.168.10.0 |
| Subnet Mask | 255.255.255.0 |
| Router IP | 192.168.10.1 |
| DHCP Pool Name | LAN |

## ⚙️ Router Configuration

```bash
enable
configure terminal

interface fa0/0
ip address 192.168.10.1 255.255.255.0
no shutdown
exit

ip dhcp excluded-address 192.168.10.1 192.168.10.5

ip dhcp pool LAN
network 192.168.10.0 255.255.255.0
default-router 192.168.10.1
exit
```

## 🔍 Verification

1. Configure all PCs to obtain IP addresses automatically.
2. Verify that each PC receives an IP address from the DHCP server.
3. Perform ping tests between PCs to confirm connectivity.

### Expected DHCP Range
```
192.168.10.6 - 192.168.10.254
```

## ✅ Results

- Successfully configured a Cisco router as a DHCP server.
- All PCs received IP addresses automatically.
- Network connectivity was verified using ping tests.
- Demonstrated practical knowledge of DHCP, IP addressing, and Cisco router configuration.

## 🧠 Skills Demonstrated

- DHCP Configuration
- Cisco Packet Tracer
- TCP/IP Networking
- IP Address Management
- Network Troubleshooting
- Router Configuration
- LAN Setup

## 👨‍💻 Author

**Narendra Achari**

Cybersecurity & Networking Enthusiast  
CompTIA Security+ Certified
