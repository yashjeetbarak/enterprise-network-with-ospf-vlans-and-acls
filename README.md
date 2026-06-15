# Enterprise Network Design with OSPF, VLAN Segmentation, and ACL Security

## Network Topology

![Topology](<img width="959" height="418" alt="topology" src="https://github.com/user-attachments/assets/fefa271f-e589-4b76-849d-122b53cd15ae" />
)

## Project Overview

This project simulates a headquarters and two branch offices connected using OSPF dynamic routing. The network was designed to provide secure inter-site connectivity, departmental segmentation through VLANs, centralized DHCP services, SSH administration, and ACL-based protection for Finance resources.

## Project Scenario

A growing organization required secure communication between headquarters and remote offices while maintaining departmental separation and protecting sensitive Finance systems from unauthorized access.

## Technologies Used

- OSPF Area 0
- VLAN Segmentation
- Router-on-a-Stick
- DHCP Services
- SSH Remote Administration
- Extended ACLs
- 802.1Q Trunking
- Cisco Packet Tracer

## Network Design

| Site | VLAN | Department | Network |
|------|------|------------|---------|
| HQ | 10 | HR | 192.168.10.0/24 |
| HQ | 20 | IT | 192.168.20.0/24 |
| Branch 1 | 30 | HR_B2 | 192.168.30.0/24 |
| Branch 1 | 40 | IT_B2 | 192.168.40.0/24 |
| Branch 2 | 50 | Finance | 192.168.50.0/24 |
| Branch 2 | 60 | IT_B3 | 192.168.60.0/24 |

## Security Implementation

A Finance-Protect ACL was configured to deny access from HR networks to the Finance VLAN while permitting legitimate business traffic.

## Validation & Testing

### OSPF Neighbor Verification
![OSPF](screenshots/ospf-neighbor-state.png)

### Routing Table Verification
![Routing](screenshots/routing-table.png)

### DHCP Verification
![DHCP](screenshots/dhcp-leases.png)

### VLAN Verification
![HQ VLANs](screenshots/hq-vlans.png)

![Branch 1 VLANs](screenshots/branch1-vlans.png)

![Branch 2 VLANs](screenshots/branch2-vlans.png)

### Trunk Verification
![HQ Trunk](screenshots/trunk-status-hq.png)

![Branch1 Trunk](screenshots/trunk-status-branch1.png)

![Branch2 Trunk](screenshots/trunk-status-branch2.png)

### SSH Verification
![SSH](screenshots/ssh-login.png)

### Connectivity Testing
![Connectivity](screenshots/connectivity-test.png)

## Challenges Encountered

OSPF adjacency verification and route propagation validation required systematic troubleshooting using WAN connectivity checks, OSPF neighbor verification, and routing table analysis.

## Key Takeaways

- OSPF troubleshooting
- Enterprise VLAN design
- ACL implementation and validation
- DHCP deployment
- Secure SSH administration
- Structured network troubleshooting

## Repository Structure

packet-tracer-file/

screenshots/

README.md

## Author

Yash Barak
