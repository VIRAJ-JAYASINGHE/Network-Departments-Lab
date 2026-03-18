🌐 Network Departments Lab
📝 Overview

This Packet Tracer lab demonstrates VLAN configuration and inter-department communication using Router-on-a-Stick (ROAS).

🖧 1 Router (R1)
🖇️ 1 Switch (SW1)
🟢 3 VLANs: IT, HR, Finance
💻 2 PCs per department

🔗 Trunk port between Switch and Router for inter-VLAN communication

🟢 VLAN Configuration
VLAN ID	Name	Ports
10	IT	Fa0/1, Fa0/2
20	HR	Fa0/3, Fa0/4
30	Finance	Fa0/5, Fa0/6

🔧 Router Configuration (ROAS)
interface g0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0

interface g0/0.20
 encapsulation dot1Q 20
 ip address 192.168.11.1 255.255.255.0

interface g0/0.30
 encapsulation dot1Q 30
 ip address 192.168.12.1 255.255.255.0
 
💻 PC IP Assignment
PC	VLAN	IP Address	Default Gateway
PC0	IT	192.168.10.2	192.168.10.1
PC1	IT	192.168.10.3	192.168.10.1
PC2	HR	192.168.11.2	192.168.11.1
PC3	HR	192.168.11.3	192.168.11.1
PC4	Finance	192.168.12.2	192.168.12.1
PC5	Finance	192.168.12.3	192.168.12.1

✅ Verification Steps

📶 Ping between PCs in different VLANs to confirm inter-VLAN routing
📋 Check VLANs on switch: show vlan brief
🔌 Check trunk port: show interfaces trunk
👤 Author

Viraj Jayasinghe
📅 Date: 18 March 2026
