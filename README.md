# Enterprise-office-Network-using-VLAn-s-and-DHCP
Project Overview

This project demonstrates the design and implementation of an enterprise office network using Cisco Packet Tracer. The network consists of three departments: HR, Finance, and IT. VLANs were used to logically separate departments, while Router-on-a-Stick was implemented to enable inter-VLAN communication. DHCP was configured to automate IP address allocation.

Objectives
Design a scalable enterprise network.
Implement VLAN segmentation for different departments.
Configure IEEE 802.1Q trunking.
Enable inter-VLAN routing using Router-on-a-Stick.
Configure DHCP for automatic IP address assignment.
Verify network connectivity through testing and troubleshooting.
Network Topology
                    Router0
                  Gig0/0
                      |
                 Trunk Link
                      |
                Switch0 Fa0/7
      __________________________________
      |               |                |
   VLAN 10         VLAN 20         VLAN 30
      HR           Finance            IT

  PC1  PC2       PC3  PC4       PC5  PC6
Devices Used
Device	Quantity
Cisco 2911 Router	1
Cisco 2960 Switch	1
PCs	6
Copper Straight Through Cables	7
VLAN Configuration
VLAN ID	Department	Network
10	HR	192.168.10.0/24
20	Finance	192.168.20.0/24
30	IT	192.168.30.0/24
Switch Port Assignment
Switch Port	VLAN	Department
Fa0/1	10	HR
Fa0/2	10	HR
Fa0/3	20	Finance
Fa0/4	20	Finance
Fa0/5	30	IT
Fa0/6	30	IT
Fa0/7	Trunk	Router Connection
Technologies and Concepts Used
Cisco Packet Tracer
VLAN (Virtual Local Area Network)
IEEE 802.1Q Trunking
Router-on-a-Stick
DHCP (Dynamic Host Configuration Protocol)
TCP/IP Addressing
Inter-VLAN Routing
Network Troubleshooting
Router Configuration
VLAN 10 Gateway
interface g0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
VLAN 20 Gateway
interface g0/0.20
encapsulation dot1Q 20
ip address 192.168.20.1 255.255.255.0
VLAN 30 Gateway
interface g0/0.30
encapsulation dot1Q 30
ip address 192.168.30.1 255.255.255.0
DHCP Configuration

Three DHCP pools were configured:

HR
ip dhcp pool HR
network 192.168.10.0 255.255.255.0
default-router 192.168.10.1
Finance
ip dhcp pool FINANCE
network 192.168.20.0 255.255.255.0
default-router 192.168.20.1
IT
ip dhcp pool IT
network 192.168.30.0 255.255.255.0
default-router 192.168.30.1
Verification and Testing

The following tests were performed:

VLAN Verification
show vlan brief
Trunk Verification
show interfaces fa0/7 switchport
Interface Verification
show ip interface brief
Connectivity Testing
ping 192.168.20.2
ping 192.168.30.2

Successful ping responses confirmed proper inter-VLAN communication.

Results
Successfully created and configured VLANs for HR, Finance, and IT departments.
Configured trunking between switch and router.
Implemented Router-on-a-Stick for inter-VLAN routing.
Configured DHCP for dynamic IP address allocation.
Verified communication between all VLANs.
Demonstrated network troubleshooting and validation techniques.
Skills Demonstrated
Network Design
VLAN Configuration
Layer 2 Switching
Layer 3 Routing
DHCP Configuration
Cisco IOS CLI
TCP/IP Networking
Network Troubleshooting
Cisco Packet Tracer
