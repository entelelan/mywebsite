# HomeLab Network Project – Version 1
## Project Overview
This project documents the design, implementation, and validation of a small enterprise-style network built in a home lab environment. The lab is intentionally structured to reflect real-world network engineering practices while serving as a hands-on platform for reinforcing core networking concepts. Although implemented in a home lab, the network design emphasizes professional standards, clear documentation, and iterative improvement. All configurations are validated using a combination of physical Cisco hardware and Cisco Packet Tracer to support repeatability, experimentation, and long-term documentation.

## Project Objectives
The primary objectives of this project are to:
* Design and implement a functional routed and switched network
* Practice VLAN segmentation and inter-VLAN routing
* Establish basic Internet edge connectivity and NAT
* Integrate wireless and VoIP into the LAN design
* Document design decisions, configurations, and validation steps
* Create a foundation that can be expanded into CCNP-level and multivendor studies

## Design Scope (Version 1)
Version 1 of this project focuses on foundational connectivity and services. The scope includes:
* Router-on-a-stick inter-VLAN routing
* Core and access layer switching
* VLAN segmentation for data, voice, management, and unused ports
* DHCP and basic IP services
* Internet edge routing with NAT
* Wireless LAN integration
* Basic VoIP phone registration and call flow simulation
Advanced redundancy, dynamic routing, centralized services, and security hardening are intentionally deferred to later versions of the project.

## Logical Network Design
VLAN Allocation
VLAN ID	Purpose
10	Data
20	Voice
99	Management
88	Native
404	Unused / Inactive
IP Addressing Strategy
* Internal LAN networks use private IPv4 addressing from the 192.168.0.0/16 range.
* WAN and point-to-point links use the 203.0.113.0/24 RFC 5737 test network to avoid overlap with real public address space.
Inter-VLAN routing is provided via router-on-a-stick using an integrated services router connected to an access switch via an 802.1Q trunk.

## Tools & Platforms
* Cisco 2811, 1921 Integrated Services Routers
* Cisco Catalyst 2960 and 3560 switches
* Cisco IP Phone
* Cisco Packet Tracer for network simulation and documentation parity
Physical and simulated environments are kept as closely aligned as possible.

## Versioning & Future Growth
This project follows a versioned implementation model. Each version introduces new technologies or architectural changes without retroactively modifying prior versions.
Planned future versions include:
* Migration to multilayer switching
* Dynamic routing protocols
* Redundancy and high availability
* Centralized network services
* Layer 2 and Layer 3 security controls
* Multivendor network implementations using EVE-NG or GNS3

## Documentation Approach
Each major implementation phase is documented as a milestone post. Milestone posts focus on:
* Design intent
* Configuration highlights
* Validation and testing
* Observed behavior and limitations
This approach creates a clear record of both technical progress and design decision-making over time.