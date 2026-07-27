# -Enterprise-network-using-packet-tracer

# Overview

This project demonstrates the design and implementation of a scalable enterprise campus network using Cisco Packet Tracer. The topology is divided into three logical enterprise zones—Access Zone, Core Operations Zone, and Distribution Zone—to emulate a real-world organizational network.

The implementation integrates multiple dynamic routing protocols, centralized network services, access control mechanisms, and secure communication technologies to provide efficient, secure, and highly available connectivity between different departments.

The project was designed as a practical implementation of CCNA networking concepts while following enterprise network design principles.

# Project Objectives
Design a scalable enterprise network architecture.
Implement multiple dynamic routing protocols.
Provide centralized IP address management.
Enable secure inter-department communication.
Simulate enterprise WAN connectivity.
Implement access control policies.
Configure network address translation.
Demonstrate VPN communication.
Validate complete end-to-end connectivity.
# Enterprise Architecture
                          ENTERPRISE NETWORK

                    +-----------------------------+
                    |        Access Zone          |
                    |-----------------------------|
                    | HR Department              |
                    | IT Department              |
                    | Training Department        |
                    | Development Department     |
                    +-------------+--------------+
                                  |
                             RIP Routing
                                  |
               =======================================
                                  |
                    +-------------+--------------+
                    |    Core Operations Zone    |
                    |----------------------------|
                    | Finance Department         |
                    | R&D Department             |
                    | Data Center               |
                    +-------------+--------------+
                                  |
                            EIGRP Routing
                                  |
               =======================================
                                  |
                    +-------------+--------------+
                    |   Distribution Zone        |
                    |----------------------------|
                    | Sales Department           |
                    | Supply Chain               |
                    | Remote Office             |
                    +---------------------------+
                           OSPF Routing
# Network Zones
# 1. Access Zone

The Access Zone represents the user-facing portion of the enterprise network where employee workstations connect to departmental routers through Layer-2 switches.

Departments :
Human Resources
Information Technology
Training
Development

Technologies :
RIP Version 2
DHCP Relay
ACL
GRE VPN
Functions
End-user connectivity
Dynamic IP allocation
Department segmentation
Gateway services

# 2. Core Operations Zone

The Core Operations Zone acts as the backbone of the enterprise network. It connects all departments and provides high-speed packet forwarding between the Access and Distribution layers.

Departments :
Finance
Research & Development
Enterprise Services

Technologies :
EIGRP
DHCP Relay
Static NAT
Functions
High-speed routing
Inter-zone communication
Centralized services

# 3. Distribution Zone
The Distribution Zone aggregates enterprise services and external connectivity while enforcing security policies.

# Departments :
Sales & Marketing
Supply Chain
Remote Operations

# Technologies :
OSPF
NAT
ACL

# Functions :
Policy enforcement
Enterprise applications
WAN connectivity

# Network Devices :
| Device              |               Quantity |
| ------------------- | ---------------------: |
| Cisco 2811 Routers  |                     12 |
| Cisco 2960 Switches |                      7 |
| DHCP Servers        |                      2 |
| End Devices         | Multiple PCs & Laptops |
| Servers             |               Multiple |


# ** Technologies Implemented ** :
# Dynamic Routing :
RIP Version 2
EIGRP
OSPF
# Network Services  :
DHCP Relay
Static NAT
GRE Tunnel
# Security :
Standard ACL
Extended ACL

# Network Infrastructure  :
Layer 2 Switching
Layer 3 Routing
IPv4 Addressing
Department Segmentation
Routing Protocol Design

# RIP
Implemented within the Access Zone to provide simple and efficient routing between departmental routers.
Configured on:

HR Router
IT Router
Training Router
Development Router


# **EIGRP**
Used in the Core Operations Zone due to its fast convergence and efficient bandwidth utilization.
Configured on:

Finance Router
R&D Router
Core Router
Enterprise Services Router

**OSPF**
Implemented in the Distribution Zone to support scalable routing and hierarchical network expansion.
Configured on:

Sales Router
Supply Chain Router
Remote Operations Router

# DHCP Relay :
Instead of deploying a DHCP server in every subnet, centralized DHCP servers provide IP address allocation.
Routers forward DHCP requests using:
ip helper-address

Benefits:
Centralized management
Reduced administrative overhead
Efficient IP allocation
Easier scalability

# NAT -
Static Network Address Translation is configured on edge routers to allow communication between private enterprise networks and external networks.

Features :
Static NAT
Inside Interfaces
Outside Interfaces
Public IP Mapping

Benefits :
Conserves public IP addresses
Hides internal addressing
Improves security

# Access Control Lists
* ACLs are implemented to restrict unauthorized communication between selected departments.

Implemented ACLs :
Standard ACL
Extended ACL

 Example Policies :
Restrict specific hosts
Permit required traffic
Block unauthorized inter-department access

# GRE Tunnel (VPN Simulation) :
A GRE tunnel is configured between enterprise routers to simulate secure communication across separate network segments.

Benefits :

Secure logical connectivity
Encapsulation of routed traffic
Simulated site-to-site VPN

# ****Enterprise Departments ****:
# 1)Access Zone:
Human Resources
IT Department
Training Department
Development Department

# 2)Core Operations
Finance
Research & Development
Enterprise Services

# 3)Distribution Zone
Supply Chain
Sales & Marketing
Remote Operations

# ***Network Features*** :
Enterprise Multi-Zone Architecture
Department-Based Segmentation
Dynamic Routing
Multiple Routing Protocols
DHCP Relay
Static NAT
ACL Security
GRE Tunnel
Layer-3 Routing
Centralized Services
Enterprise Backbone
High Availability Design

# Testing Performed :
The network was validated using:
End-to-End Ping
Traceroute
DHCP Lease Verification
Routing Table Verification
OSPF Neighbor Verification
EIGRP Neighbor Verification
RIP Route Advertisement
NAT Translation Testing
ACL Policy Verification
GRE Tunnel Connectivity

# Skills Demonstrated :
Enterprise Network Design
Cisco IOS Configuration
IPv4 Addressing & Subnetting
RIP Configuration
EIGRP Configuration
OSPF Configuration
DHCP Relay Configuration
Static NAT
ACL Implementation
GRE Tunnel Configuration
Layer-3 Routing
Network Troubleshooting
Enterprise Documentation

# Future Enhancements :
VLAN Implementation
Inter-VLAN Routing
HSRP Gateway Redundancy
EtherChannel
IPv6 Deployment
Dynamic NAT/PAT
SNMP Monitoring
Syslog Server
AAA Authentication
Active Directory Integration
DNS Services
QoS
Firewall Policies

# Learning Outcomes :
This project strengthened practical knowledge of:

Enterprise network architecture
Cisco routing technologies
Dynamic routing protocols
Enterprise security
Centralized IP management
WAN connectivity
Network troubleshooting
Infrastructure scalability
Campus network design

# About the Author :

# Ramanand Patharwalkar
Bachelor of Engineering (Computer Engineering)
PG-DAC (CDAC)
Cisco Certified Network Associate (CCNA)
