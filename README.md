AIM: 
To create and configure a suitable network topology involving both LAN and WAN using Cisco Packet Tracer. The setup includes 10-12 computers, switches, and routers, aiming to simulate the transmission of messages from computers in one network to computers in another network, ensuring proper connectivity and communication across different network segments. 
PROCEDURE: 
1. Topology Design 
LAN Configuration: 
1. Designed a network topology with 12 computers connected to 2 switches, ensuring adequate connectivity within the LAN segment. 
2. Implemented WAN configuration to connect the two LANs using 2 routers, establishing a broader network structure for communication. 
2. Network Setup in Cisco Packet Tracer 
Add Devices: 
1. Placed and connected 10 computers in two separate LAN segments: o LAN 1: 5 computers 
o LAN 2: 5 computers 
2. Added 2 switches to manage connections within each LAN. 
3. Introduced 2 routers to facilitate WAN connectivity. 
Configure IP Addresses: 
1. Assigned unique IP addresses to all computers: 
o LAN 1: 192.168.1.1 to 192.168.1.6 
o LAN 2: 192.168.2.1 to 192.168.2.6 
2. Configured router interfaces with appropriate IP addresses: 
o Router 1 (LAN 1 interface): 192.168.1.254 
o Router 2 (LAN 2 interface): 192.168.2.254 
o WAN link: 
▪ Router 1: 10.0.0.1 
▪ Router 2: 10.0.0.2 
3. Set up routing protocols: 
o Router 1: Configured with RIP. 
o Router 2: Configured with OSPF.
3. Configuration Steps 
LAN Configuration: 
1. Connected computers to the switches using appropriate network cables (copper straight-through). 
2. Configured unique IP addresses on each computer, ensuring they were within the same subnet. 
3. Connected the switches to ensure communication across devices within the LAN. WAN Configuration: 
1. Connected the routers to each other using serial cables to establish the WAN connection. 
2. Configured the router interfaces with IP addresses that facilitate communication across the WAN. 
3. Set up routing: 
o On Router 1: 
bash 
Copy code 
enable 
configure terminal 
router rip 
version 1 
network 192.168.1.0 
network 10.0.0.0 
o On Router 2: 
bash 
Copy code 
enable 
configure terminal 
router ospf 1 
network 192.168.2.0 0.0.0.255 area 0 
network 10.0.0.0 0.0.0.255 area 0 
4. Simulation 
Send a Message: 
1. Utilized Cisco Packet Tracer's simulation mode to monitor network activity. 2. Configured and sent a message from a computer in LAN 1 (e.g., PC_123) to a computer in LAN 2 (e.g., PC_127). 
3. Captured and verified the message transmission, ensuring successful delivery to the destination computer. 
RESULT: 
Network Topology and Configuration:
● LAN Setup: 
o Computers: 12 computers were successfully placed and connected. o Switches: 2 switches managed LAN connections. 
o IP Configuration: Unique IP addresses were assigned within the same subnet for all computers. 
● WAN Setup: 
o Routers: 2 routers were configured to connect the two distinct LANs. o Router IP Configuration: Routers were assigned IP addresses to enable connectivity. 
o Routing Protocols: 
▪ RIP was implemented on Router 1. 
▪ OSPF was configured on Router 2. 
Message Transmission: 
● A message was successfully sent from a computer in LAN 1 to a computer in LAN 2. ● Simulation mode in Cisco Packet Tracer confirmed that the message was routed correctly through the WAN and received at the destination computer. 

