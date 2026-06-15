# Enterprise Network Design with OSPF, VLAN Segmentation, and ACL Security

## Project Overview

This project simulates a company with a headquarters location and two branch offices connected through OSPF dynamic routing.

The objective was to provide communication between all locations while maintaining departmental separation through VLANs and restricting access to Finance resources using access control lists (ACLs).

The network was built and validated in Cisco Packet Tracer and includes dynamic routing, DHCP services, SSH-based management, inter-VLAN routing, and security controls.

---

## Network Design

| Site | VLAN | Department | Network |
|------|------|------------|---------|
| HQ | 10 | HR | 192.168.10.0/24 |
| HQ | 20 | IT | 192.168.20.0/24 |
| Branch 1 | 30 | HR | 192.168.30.0/24 |
| Branch 1 | 40 | IT | 192.168.40.0/24 |
| Branch 2 | 50 | Finance | 192.168.50.0/24 |
| Branch 2 | 60 | IT | 192.168.60.0/24 |

WAN Links:
- HQ ↔ Branch 1: 192.168.70.0/24
- HQ ↔ Branch 2: 192.168.80.0/24

---

## Technologies Used

- Cisco Packet Tracer
- OSPF Area 0
- VLANs
- Router-on-a-Stick
- DHCP
- SSH
- ACLs
- 802.1Q Trunking

---

## Security Implementation

An extended ACL named Finance-Protect was configured to prevent HR departments from accessing Finance resources while allowing legitimate business traffic.

The ACL was verified through successful and unsuccessful connectivity tests.

---

## Validation & Testing

- OSPF neighbor verification
- Routing table validation
- DHCP lease verification
- VLAN verification
- Trunk verification
- SSH login testing
- ACL validation
- End-to-end connectivity testing

See the screenshots folder for verification evidence.

---

## Challenges Encountered

One of the primary challenges involved verifying OSPF neighbor relationships between locations.

The issue was approached by validating WAN connectivity first, followed by routing protocol verification using Cisco IOS troubleshooting commands.

---

## Key Takeaways

- Troubleshooting OSPF adjacencies
- Enterprise VLAN design
- Router-on-a-Stick implementation
- ACL deployment and validation
- DHCP deployment across multiple locations
- Structured network troubleshooting

---

## Author

Yash Barak
