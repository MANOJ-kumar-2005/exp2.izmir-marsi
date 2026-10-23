
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
<img width="1920" height="1080" alt="Screenshot 2026-10-23 184750" src="https://github.com/user-attachments/assets/b553eb64-c5ed-4717-adf5-fc16419a71f3" />

<img width="1920" height="1080" alt="Screenshot 2026-10-23 184800" src="https://github.com/user-attachments/assets/51e77000-9ac6-4015-899b-28d1db8bd15c" />

<img width="1920" height="1080" alt="Screenshot 2026-10-23 184813" src="https://github.com/user-attachments/assets/13d5a654-e51c-48ad-af51-e85dda6a7b69" />

<img width="1920" height="1080" alt="Screenshot 2026-10-23 184829" src="https://github.com/user-attachments/assets/c3a31280-e2a8-4952-976b-a999d97d5ff2" />

<img width="1920" height="1080" alt="Screenshot 2026-10-23 184841" src="https://github.com/user-attachments/assets/1e13570c-ac5b-4407-8480-1226ac99f7b3" />

<img width="1920" height="1080" alt="Screenshot 2026-10-23 185044" src="https://github.com/user-attachments/assets/cb977ce0-c60e-4f65-8a02-1fee6192f928" />

<img width="1920" height="1080" alt="Screenshot 2026-10-23 185057" src="https://github.com/user-attachments/assets/9184bf4e-4ce3-4887-831f-abae9c2ccc86" />





________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>

<img width="1920" height="1080" alt="Screenshot 2026-10-23 184733" src="https://github.com/user-attachments/assets/71576d6e-b771-4dd2-a45c-e717b5142781" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

