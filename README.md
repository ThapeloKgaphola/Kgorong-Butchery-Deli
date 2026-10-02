# Kgorong-Butchery-Deli
computer networks project
# CMPG 325 Computer Networks

# Project Information

- Project ID: CMPG325-2026-019
- Client ID: CLI-019
- Organisation: Kgorong Butchery and Deli (Vryburg)
- Industry: Retail
- Addressing Block: 10.17.0.0/16

## Project Objective

The objective of this project is to design and simulate a computer
network for Kgorong Butchery and Deli (Vryburg) using Cisco Packet Tracer.

The network is designed to provide reliable connectivity while
implementing network segmentation and controlled routing.

## Assigned Networking Challenge

Static Routing (multi-router path control)

The network will use multiple routers and static routes to provide
controlled paths between different network segments.

## Design Constraint

After-hours cleaning and security contractors require limited
wireless access to the network.

## Change Request

CR7 requires four CCTV cameras to be added to the network.
The CCTV traffic must be segmented from the other network traffic.

## Network Segmentation

| VLAN | Name | Network |
|---|---|---|
| 10 | Administration | 10.17.10.0/24 |
| 20 | POS | 10.17.20.0/24 |
| 30 | Staff | 10.17.30.0/24 |
| 40 | Contractor Wi-Fi | 10.17.40.0/24 |
| 50 | CCTV | 10.17.50.0/24 |
| 60 | Management | 10.17.60.0/24 |

## Technologies

- Cisco Packet Tracer
- IPv4 addressing
- VLANs
- Static routing
- Network segmentation
- Wireless networking
- Access control

## Project Evidence

This repository contains the project requirements, physical and
logical topology diagrams, IP addressing plan, Packet Tracer
implementation and supporting documentation.


## Milestone 2 - Client Implementation Review

Milestone 2 focused on implementing, testing and verifying the proposed network design for Kgorong Butchery and Deli in Cisco Packet Tracer.

### Implementation Completed

The following network components and features were successfully implemented:

- Six VLANs for Administration, POS, Staff, Contractor Wi-Fi, CCTV and Network Management.
- Router-on-a-stick inter-VLAN routing using R1.
- Three-router topology consisting of R1, R2 and R3.
- Static routing between the routers.
- Multi-router path control using configured static routes.
- Dedicated contractor wireless network using VLAN 40.
- Extended ACL named `CONTRACTOR_LIMIT` to restrict contractor access to protected internal networks.
- Four CCTV cameras connected to the dedicated VLAN 50 CCTV network in accordance with Change Request CR7.
- Trunk links configured to carry the required VLAN traffic between network devices.

### Static Routing - Assigned Networking Feature

The assigned networking feature for this project is **Static Routing (multi-router path control)**.

Three routers were configured using the following transit networks:

| Router Link | Network |
|---|---|
| R1 - R2 | 10.17.254.0/30 |
| R2 - R3 | 10.17.254.4/30 |
| R1 - R3 | 10.17.254.8/30 |

Static routes were configured on R1, R2 and R3 to provide connectivity to remote networks and control the paths used between routers.

Routing tables were verified using `show ip route`, while `ping` and `traceroute` were used to confirm connectivity and forwarding paths.

### Change Request CR7 - CCTV Segmentation

Change Request CR7 required four CCTV cameras to be added to the network and their traffic to be segmented from other network traffic.

A dedicated CCTV network was implemented using:

- VLAN: 50
- Network: 10.17.50.0/24
- Default Gateway: 10.17.50.1
- Camera 1: 10.17.50.11
- Camera 2: 10.17.50.12
- Camera 3: 10.17.50.13
- Camera 4: 10.17.50.14

Testing confirmed that the CCTV devices could communicate with their gateway and that authorised internal devices could reach the CCTV network.

### Contractor Wireless Access

A dedicated contractor wireless network was implemented using VLAN 40 and the SSID `Kgorong-Contractor`.

The `CONTRACTOR_LIMIT` extended ACL was applied inbound on R1 interface GigabitEthernet0/2.40. The ACL prevents contractor devices from accessing protected Admin, POS, Staff, CCTV and Management networks while allowing permitted traffic.

Testing confirmed that contractor devices could reach permitted destinations while access to protected internal networks was blocked.

### Testing and Verification

The completed implementation was tested using:

- `ping` for end-to-end connectivity testing.
- `traceroute` for static-routing path verification.
- `show ip route` for routing-table verification.
- `show access-lists` for ACL verification.
- `show ip interface` for interface and ACL verification.

Testing confirmed successful VLAN connectivity, CCTV operation, contractor wireless connectivity, ACL enforcement and multi-router static path control.

### Milestone 2 Files

The following Milestone 2 deliverables are included in this repository:

- `milestone2_FINAL.pkt` - Completed Cisco Packet Tracer implementation.
- `milestone2 testing evidence.docx` - Testing evidence, screenshots, troubleshooting and final test results.

### Milestone 2 Status

**Implementation:** Complete  
**Assigned Feature - Static Routing:** Implemented and tested  
**CR7 - Four CCTV Cameras:** Implemented and tested  
**Contractor Wireless Access:** Implemented and tested  
**Testing Evidence:** Completed  
**Packet Tracer File:** Completed
