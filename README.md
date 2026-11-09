# Cisco-Packet-Tracer-Labs
# Enterprise Network Configuration — Cisco Packet Tracer

**NGT Academy | Full Stack Network Associate (FSNA)**

## Project Overview

Completed a hands-on enterprise networking lab using Cisco Packet Tracer, configuring a simulated network infrastructure consisting of Cisco routers, switches, wireless devices, workstations, IP phones, and external network services.

The project focused on implementing network segmentation, secure device management, inter-VLAN routing, IP address allocation, and end-to-end connectivity.

## Network Topology

![Enterprise Network Topology](network-topology.png)

## Technologies & Configurations

### 1. Cisco Switch Configuration
- Configured two Cisco switches with hostnames and management IP addresses.
- Implemented SSHv2 for secure remote administration and disabled Telnet access.
- Applied access control lists to restrict remote management access.
- Configured Spanning Tree root bridge priority and PortFast.
- Configured access and trunk ports between switches and the router.

### 2. VLAN Configuration

| VLAN | Purpose | Network |
|---|---|---|
| 100 | Management | 192.168.100.0/24 |
| 150 | Voice | 192.168.150.0/24 |
| 200 | Data | 192.168.200.0/24 |

- Segmented management, voice, and data traffic.
- Configured 802.1Q VLAN trunking.
- Assigned access and voice VLANs to switch ports.

### 3. Inter-VLAN Routing
- Configured router-on-a-stick using Cisco router subinterfaces.
- Implemented 802.1Q encapsulation for VLANs 100, 150, and 200.
- Assigned gateway addresses to each VLAN.

### 4. DHCP and External Connectivity
- Configured a DHCP pool for the data VLAN.
- Defined DHCP address exclusions, default gateway, and DNS settings.
- Configured a static default route toward the simulated ISP.
- Configured NAT inside interfaces.

### 5. Voice over IP (VoIP)
- Configured Cisco IP phones using dedicated voice VLANs.
- Assigned directory numbers 1001 and 1002.
- Configured phone registration and calling functionality.

### 6. Wireless Networking
- Configured a wireless access point with an SSID and WPA2-PSK authentication.
- Connected a wireless tablet to the network.
- Verified wireless client IP addressing and connectivity.

## Network Verification

Completed the lab's connectivity and configuration verification tasks, including:

- DHCP address assignment
- Connectivity to VLAN gateways
- External DNS and web server connectivity
- Wireless network connectivity
- IP phone registration and calling

## Tools & Technologies

Cisco Packet Tracer, Cisco IOS CLI, VLANs, 802.1Q, SSHv2, ACLs, DHCP, DNS, Static Routing, Spanning Tree Protocol, VoIP, WPA2-PSK, and network troubleshooting.

## Project Outcome

Successfully completed the FSNA networking lab, demonstrating hands-on experience with Cisco network configuration, secure device administration, network segmentation, routing, and troubleshooting in a simulated enterprise environment.
## Configuration Verification

The following Cisco IOS commands were used to verify the completed network configuration:

| Command | Verification Result |
|---|---|
| `show vlan brief` | Confirmed Management, Voice, and Data VLANs are active |
| `show interfaces trunk` | Verified three operational 802.1Q trunk interfaces |
| `show ip interface brief` | Confirmed router subinterfaces and WAN interface are operational |
| `show ip route` | Verified connected VLAN networks and static default route |
| `show ip dhcp binding` | Confirmed five DHCP address assignments across Voice and Data VLANs |

### Verification Screenshots

![VLAN Configuration](verification-screenshots/01-vlan-configuration.png)

![Trunk Configuration](verification-screenshots/02-trunk-configuration.png)

![Router Routing Table](verification-screenshots/04-routing-table.png)

![Router Interface Status](verification-screenshots/05-router-interface-status.png)

![DHCP Bindings](verification-screenshots/06-dhcp-bindings.png)
