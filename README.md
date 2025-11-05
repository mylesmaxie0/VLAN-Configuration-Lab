# VLAN Configuration Lab

This lab demonstrates how to configure multiple VLANs on a single Cisco switch. Each VLAN represents a department within an organization and provides network segmentation for improved performance and security.

There is no trunking or inter-VLAN routing in this scenario — each VLAN operates as an isolated broadcast domain.

#

Devices used:
- 1 Cisco Switch
- 8 PCs (2 per VLAN)

### Topology
<img width="1728" height="775" alt="Screenshot 2025-11-05 at 1 24 39 PM" src="https://github.com/user-attachments/assets/043edd41-8f14-4350-95ee-0abd0f117a33" />

##  Network Layout

| VLAN | Department | Network | Subnet Mask | Hosts | 
|------|-------------|----------|--------------|--------|
| 10 | Sales | 192.168.10.0/27 | 255.255.255.224 | 30 | 
| 20 | Marketing | 192.168.20.0/26 | 255.255.255.192 | 42 | 
| 30 | Finance | 192.168.30.0/27 | 255.255.255.224 | 25 |
| 40 | IT | 192.168.40.0/28 | 255.255.255.240 | 14 | 
