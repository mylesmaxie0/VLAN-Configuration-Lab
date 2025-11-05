# VLAN Configuration Lab

This lab demonstrates how to configure multiple VLANs on a single Cisco switch. Each VLAN represents a department within an organization and provides network segmentation for improved performance and security.

There is no trunking or inter-VLAN routing in this scenario — each VLAN operates as an isolated broadcast domain.

#

Devices used:
- 1 Cisco Switch
- 10 PCs 

### Topology
<img width="1728" height="775" alt="Screenshot 2025-11-05 at 1 24 39 PM" src="https://github.com/user-attachments/assets/043edd41-8f14-4350-95ee-0abd0f117a33" />

##  Network Layout

| VLAN | Department | Network | Subnet Mask | Hosts | 
|------|-------------|----------|--------------|--------|
| 10 | Sales | 192.168.10.0/27 | 255.255.255.224 | 30 | 
| 20 | Marketing | 192.168.20.0/26 | 255.255.255.192 | 42 | 
| 30 | Finance | 192.168.30.0/27 | 255.255.255.224 | 25 |
| 40 | IT | 192.168.40.0/28 | 255.255.255.240 | 14 | 

#

### VLAN Configuration Steps

1. Create VLANS
<img width="850" height="505" alt="Screenshot 2025-11-05 at 1 31 07 PM" src="https://github.com/user-attachments/assets/10a62e27-7879-4c94-95e7-db919f7e90cc" />

2. Assign Ports to VLANs
<img width="850" height="505" alt="Screenshot 2025-11-05 at 1 39 12 PM" src="https://github.com/user-attachments/assets/26a7e80b-fbd2-4156-af6c-f56627170c9a" />

3. Verify VLAN Configuration
<img width="850" height="505" alt="Screenshot 2025-11-05 at 1 40 51 PM" src="https://github.com/user-attachments/assets/29260d1e-da99-4c00-a263-0b7bcc018ca1" />

4. Running Configuration
<img width="850" height="631" alt="Screenshot 2025-11-05 at 1 43 16 PM" src="https://github.com/user-attachments/assets/dd22bb35-fbc6-462f-a97d-8ec5512a66fa" />

#

### Test Connectivity

#### Ping PC inside VLAN 10 (Success!)
<img width="1152" height="536" alt="Screenshot 2025-11-05 at 1 54 21 PM" src="https://github.com/user-attachments/assets/51d0dc8d-70c4-4edc-9351-619d500fad41" />

#### Ping PC from VLAN 10 -> VLAN 20 (Failed!)
<img width="1209" height="560" alt="Screenshot 2025-11-05 at 1 57 16 PM" src="https://github.com/user-attachments/assets/10df9d18-96d0-4700-854d-95ddf1d0a439" />

## Summary

This VLAN lab successfully demonstrated how to configure and verify multiple VLANs on a single Cisco switch using Cisco Packet Tracer.  

Through this exercise, the following key objectives were achieved:

- **VLAN Creation:**  
  VLANs 10 (Sales), 20 (Marketing), 30 (Finance), and 40 (IT) were created and properly named.

- **Port Assignment:**  
  Specific switch ports were configured as access ports and assigned to their respective VLANs.

- **IP Addressing:**  
  Each VLAN was allocated its own subnet with appropriate IP addresses for connected devices.

- **Connectivity Verification:**  
  - Devices **within the same VLAN** communicated successfully using `ping`.  
  - Devices **in different VLANs** were unable to communicate, confirming VLAN isolation.

- **Concept Reinforcement:**  
  The lab reinforced key concepts of network segmentation, broadcast domain isolation, and access port configuration at Layer 2.

### Key Takeaways
- VLANs separate broadcast traffic, improving security and network performance.  
- Access ports belong to a single VLAN and are used for end devices.  
- Inter-VLAN communication requires a Layer 3 device (e.g., router-on-a-stick or Layer 3 switch).  
- Proper IP addressing and port mapping are critical for successful VLAN design.


This foundational VLAN lab provides a baseline for understanding how Layer 2 segmentation works before progressing to more advanced multi-switch and routing configurations.
