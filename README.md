# Enterprise Campus Network Design

## Overview

This project demonstrates the design and implementation of a secure enterprise campus network using Cisco Packet Tracer. The network was built using a hierarchical design consisting of Core and Access layers. The project focuses on network segmentation, redundancy, high availability, security, and centralized management.

## Topology

The topology consists of:

* Core1 (3560 Layer 3 Switch)
* Core2 (3560 Layer 3 Switch)
* Building-A Access Switch
* Building-B Access Switch
* Building-C Access Switch
* End-user PCs

The core switches provide routing, gateway redundancy, DHCP services, and security policies. Access switches provide end-device connectivity.

## VLAN Design

| VLAN | Name       | Subnet        |
| ---- | ---------- | ------------- |
| 10   | Students   | 10.10.10.0/24 |
| 20   | Faculty    | 10.20.20.0/24 |
| 30   | Library    | 10.30.30.0/24 |
| 99   | Management | 10.99.99.0/24 |

## Technologies Implemented

### VLAN Segmentation

Created separate VLANs for Students, Faculty, Library, and Management traffic.

### Trunking

Configured IEEE 802.1Q trunk links between access and core switches to transport multiple VLANs.

### Inter-VLAN Routing

Implemented Switch Virtual Interfaces (SVIs) on Layer 3 switches to enable communication between VLANs.

### Spanning Tree Protocol (STP)

Configured STP root bridge election and verified failover by simulating link failures.

### EtherChannel (LACP)

Bundled multiple physical links into a single logical Port-Channel using LACP to increase bandwidth and redundancy.

### HSRP Version 2

Configured gateway redundancy using HSRP Version 2.

Virtual Gateways:

* VLAN 10: 10.10.10.254
* VLAN 20: 10.20.20.254
* VLAN 30: 10.30.30.254
* VLAN 99: 10.99.99.254

### DHCP

Configured centralized DHCP services on Core1 to automatically assign IP addresses to clients.

### Access Control Lists (ACLs)

Implemented security policies to restrict communication between specific departments.

Example:

* Students VLAN denied access to Faculty VLAN.

### SSH

Configured SSH Version 2 for secure remote device management.

### Port Security

Configured sticky MAC addressing and violation protection on access ports.

### Management VLAN

Created VLAN 99 for switch management and remote administration.

## Verification

The following tests were successfully completed:

* VLAN communication verification
* Inter-VLAN routing verification
* STP failover testing
* EtherChannel verification
* HSRP failover testing
* DHCP address assignment verification
* ACL filtering verification
* SSH connectivity verification
* Port security verification

## Files Included

* Packet Tracer topology (.pkt)
* Device configurations
* Verification screenshots
* Project report

## Skills Demonstrated

* VLAN Configuration
* Trunking
* Inter-VLAN Routing
* STP
* EtherChannel
* HSRP
* DHCP
* ACLs
* SSH
* Port Security
* Network Troubleshooting

## Author

Karri Hemanth Reddy

Aspiring Network Engineer | CCNA Candidate
