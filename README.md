# Enterprise Multi-Routing Protocol Network Integration
### OSPF • EIGRP • RIP v2 • Route Redistribution • Cisco Packet Tracer

[ Project Status Completed ] [ Network Simulator Cisco Packet Tracer ] [ Protocol Integration OSPF EIGRP RIP ] [ Security Level Encrypted SSH ]

This project is a professional network simulation demonstrating the design configuration and integration of a corporate network structure. It bridges three distinct routing domains (OSPF, EIGRP, and RIP) using a central core router.

## Table of Contents

*   Project Overview
*   Why This Project
*   Network Architecture Description
*   Network Statistics
*   IP Addressing Scheme and Subnet Allocation
*   Route Redistribution Logic
*   Sample Routing Table
*   Device Security Configuration
*   Skills Demonstrated
*   Why Not VXLAN
*   Project Structure
*   Getting Started Guide
*   Future Improvements
*   Author Information
*   License

## Project Overview

The objective of this project is to simulate a modern corporate infrastructure that integrates legacy network segments and modern high-speed branches. By establishing communication between disparate routing protocols, this network achieves seamless connectivity across distinct departments, ensuring business continuity and efficient resource sharing.

## Why This Project

In enterprise environments, companies often undergo mergers, acquisitions, or infrastructure upgrades. During these transitions, different parts of the company run different routing protocols. This project demonstrates how to connect these separate networks, translate their routing languages, and secure their administrative access to maintain operational continuity.

## Network Architecture Description

The network is composed of a central core routing device that connects three major routing zones:

*   OSPF Domain: Represents the high-speed corporate core network, divided into a backbone area and a regular area connected by an Area Border Router.
*   EIGRP Domain: Simulates a modern branch office configured for fast route convergence.
*   RIP Domain: Represents a legacy network segment integrated into the corporate intranet.
*   Core Gateway: The central router that connects to all three domains and translates routing updates.

## Network Statistics
| Component | Quantity |
|-----------|---------:|
| Routers | 10 |
| Switches | 10 |
| End Devices | 20+ |
| Routing Protocols | 3 |
| Routing Domains | 3 |
| Central Router | 1 |


## Sample Routing Table
| Route Type | Destination | Next Hop | AD |
|------------|------------|----------|---:|
| O IA | 192.168.1.0/24 | 70.0.0.1 | 110 |
| O | 192.168.2.0/24 | 70.0.0.1 | 110 |
| D | 192.168.5.0/24 | 90.0.0.1 | 90 |
| R | 192.168.9.0/24 | 80.0.0.1 | 120 |
| C | 192.168.10.0/24 | Directly Connected | 0 |
## Route Redistribution Logic

The central router runs all three routing protocols. It translates OSPF cost metrics into EIGRP composite vector metrics (bandwidth and delay) and RIP hop counts. It also translates EIGRP vector metrics into OSPF costs and RIP hop counts, and RIP hop counts into OSPF costs and EIGRP vector metrics. This prevents unreachable route advertisements due to default metric differences.


## Device Security Configuration

Administrative terminal lines are protected using encrypted Secure Shell access, a local username and secret password database, and a warning Message of the Day banner.

## Skills Demonstrated

*   Enterprise Network Design
*   Cisco IOS Configuration
*   OSPF Multi-Area Deployment
*   EIGRP Configuration
*   RIP Version Two Configuration
*   Route Redistribution
*   Routing Table Analysis
*   SSH Secure Management
*   Network Troubleshooting
*   ICMP and Traceroute Testing
*   Enterprise Documentation

## Why Not VXLAN

Cisco Packet Tracer does not support modern data center technologies such as VXLAN, EVPN, or Cisco ACI. This project demonstrates how a centralized redistribution architecture can simulate communication between isolated routing domains using technologies available in Packet Tracer while preserving enterprise networking concepts.

## Project Structure

*   project.pkt: Cisco Packet Tracer simulation file containing the active network topology.
*   Multi-Routing Protocols.docx: Technical report outlining the configurations and parameters.
*   README.md: Project documentation overview.

## Getting Started Guide
1. Clone the repository.
2. Open `project.pkt` using Cisco Packet Tracer 8.x or later.
3. Wait until all interfaces reach the UP/UP state.
4. Verify routing using:
   - show ip route
   - ping
   - traceroute
5. Test SSH connectivity to the Central Router.

## Future Improvements

*   IPvsix Deployment
*   HSRP Redundancy
*   EtherChannel
*   SNMP Monitoring
*   Syslog Server
*   NetFlow Analysis
*   MP-BGP
*   VXLAN Migration using GNSthree or CML
*   Python Network Automation
*   Ansible Configuration Management

## Author

**Mahmoud Bahnsey**

Network and Cybersecurity Student

*   GitHub: github.com/mahmoudbahnsey
*   LinkedIn: www.linkedin.com/in/mahmoud-bahnsey-4731963a6

## License

This project is licensed under the MIT License.

If you use this project for educational purposes, please provide appropriate attribution.

Developed with passion for Network and Cybersecurity Engineering. Copyright Mahmoud Bahnsey. All rights reserved.
