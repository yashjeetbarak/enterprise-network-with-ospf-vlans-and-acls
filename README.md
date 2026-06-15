# Enterprise Network Design with OSPF, VLAN Segmentation, and ACL Security

## Project Overview
This project simulates a headquarters and two branch offices connected through OSPF dynamic routing. The design includes VLAN segmentation, Router-on-a-Stick inter-VLAN routing, DHCP, SSH management, and ACL-based protection for Finance resources.

## Network Topology
![Topology](screenshots/topology.png)

## Technologies Used
- OSPF Area 0
- VLAN Segmentation
- Router-on-a-Stick
- DHCP
- SSH
- ACLs
- 802.1Q Trunking

## Network Design
| Site | VLAN | Department | Network |
|------|------|------------|---------|
| HQ | 10 | HR | 192.168.10.0/24 |
| HQ | 20 | IT | 192.168.20.0/24 |
| Branch 1 | 30 | HR | 192.168.30.0/24 |
| Branch 1 | 40 | IT | 192.168.40.0/24 |
| Branch 2 | 50 | Finance | 192.168.50.0/24 |
| Branch 2 | 60 | IT | 192.168.60.0/24 |

## Validation & Testing
### OSPF
![OSPF](screenshots/ospf-neighbor-state.png)

### Routing
![Routing](screenshots/routing-table.png)

### DHCP
![DHCP](screenshots/dhcp-leases.png)

### SSH
![SSH](screenshots/ssh-login.png)

### ACL
![ACL](screenshots/finance-acl.png)

### Connectivity
![Connectivity](screenshots/connectivity-test.png)
