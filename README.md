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
