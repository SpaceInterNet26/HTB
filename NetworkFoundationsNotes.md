network consists of nodes, links and data sharing.
importance: resource sharing, communication, data access, collaboration.

Local Area Network (LAN) - connects devices over a short distance.
Characteristics: 
Geographical scope - covers small area.
Ownership - typically owned by a single person or organization.
Speed - high data transfer rate.
Media - uses wired (ethernet) or wireless (Wi-Fi) connection.

Wide Area Network (WAN) - connects multiple LAN's over a large area.
Characteristics: 
Geographical scope - covers a large area. (countries)
Ownership - collective ownership (internet service prov.)
Speed - slower data transfer compared to LAN.
Media -  fiber optics, satellite links, telecommunication lines.

LAN connects to Internet Service Provider's (ISP) WAN.
ISP - company providing internet access.
modem acts as a bridge between LAN and ISP's infrastructure.

OSI Model
Open System Interconnection model - conceptual framework for standardization of computing system functions.
1. Physical layer - transmission of raw bitstreams. Deals with physical connection between devices.
2. Data link layer - node-to-node data transfer. transmission with proper sync, error detection and correction. Switches and Bridges operate here, using MAC (unique identifier for use as a network address) addresses to id network devices.
3. Network layer - packet forwarding. logical addressing and path determination, so data reaches correct destination. Routers operate here, using IP (unique address, that identifies device on internet. handles addressing and packet routing) addresses to determine most efficient path.
4. Transport layer - end-to-end communication services to apps. reliable/unreliable data delivery, segmentation, messages reassembly, flow control, error checking. 
Protocols TCP and UDP operate here:
TCP(Transmission Control Protocol) - reliable, connection-oriented transmission with error recovery.
UDP - fast, connectionless communication.
5. Session layer - sessions(device communications) between apps. establishes, maintains, terminates connections. Essential for session checkpointing and recovery. API's coordinate communication between systems and apps here.
6. Presentation layer - translator between app layer and network format. Data representation, ensuring that info sent by app layer of one system is readable by another. Including encryption and decryption, data compression and converting data formats.
7. Application layer - provides network services directly to end-user apps. Enables resource sharing, remote file access, etc. 
common protocols:
HTTP (Hypertext Transfer Protocol) - web browsing
FTP (File Transfer Protocol) - file transfers
SMTP (Simple Mail Transfer Protocol) - email transmission
DNS (Domain Name System) - resolving domain names to IP addresses. 

TCP/IP Model - condensed version of OSI model.
1. Link layer - (Physical and Data link layers of OSI model)
2. Internet layer -  (Network layer of OSI)
3. Transport layer - (corresponding to OSI)
4. Application layer - (Session, Presentation, Application layers)

Transmission - process of sending data signals over a medium.
Types:
Analog - continuous signals to represent info ( ex.: trad radio broadcasts) 
Digital - employs discrete signals (bits) to encode data (ex.: pc networks)
Modes:
Simplex - allows one-way communication only (keyboard)
Half-duplex - two-way communication but not simultaneously ( walkie-talkies)
Full-duplex - two-way communication simultaneously (phone calls)
Media:
twisted pair cables - ethernet or LAN connections
coaxial cables - TV and early ethernet
fiber optic cables - transmit data as light pulses. High-speed internet backbone.
Radio waves - Wi-Fi and cellular networks
microwaves - satellite communication
infrared - short-range communications

Network Components:
End Devices - PC, phone, IoT
Intermediary Devices - Switches, modems, routers
Network media and software - Cables, protocols, firewalls
Servers - Web servers, File servers, Database servers

End Devices:
also known as host, is any device that sends or receives data within a network.
Intermediary Devices:
facilitates data flow between end devices. Responsible for packet forwarding( Directing data packets to their destinations by reading network address info and determining the most efficient paths).  often incorporates firewalls to protect certain networks form unauthorized access.

Network Interface Card (NIC) - hardware component that allows connection to a network. Each NIC has unique Media Access Control (MAC) address, for devices to identify each other. 

Router - forwards data packets between networks and directs internet traffic. reads network address info in data packets to determine their destinations. uses Open Shortest Path First (OSPF) and Border Gateway Protocol (BGP) to find most efficient path for data. 
A router examines incoming data packets and forwards them to their destinations, based on IP addresses. By connecting multiple networks, it enables devices on different networks to communicate. Manage network traffic by selecting optimal path for data transmission - traffic management . enhance security by having firewalls and access control lists.

Switch - connect multiple devices within the same network. uses MAC addresses to forward data only to the intended recipient.

Network protocols - set of rules of how data is formatted, transmitted, received across a network.
aspects:
- Data Segmentation
-Addressing
-Routing
-Error Checking
-Synchronization

Media Access Control (MAC) address - unique identifier assigned to the Network Interface Card (NIC), allowing it to be recognized on a local network. Used to deliver data frames to the correct physical device.
Address Resolution Protocol (ARP) - maps IP addresses to MAC addresses, allowing devices to find the MAC address associated with a known IP address in the same network.

Internet Protocol (IP) address - numerical label assigned to each device connected to a network that utilizes IP for communication. 
Routers use IP addresses to determine the optimal path for data.

Port - a number assigned to specific processes/services on a network to help computers sort traffic.
Well-Known Ports (0-1023):
reserved for common and universally recognized services and protocols. (HTTP - 80 ; HTTPS - 443)
Registered Ports (1024-49151):
used for external services.
Dynamic/Private Ports (49152-65535):
used by client apps to send and receive data from servers.

Dynamic Host Configuration Protocol (DHCP)
network management protocol used to automate the process of configuring devices on IP networks.

DHCP Server - network device that manages IP address allocation.
DHCP Client - device that connects to the network and requests network configuration parameters from DHCP server.

How DHCP works:
1.Discover - device broadcasts a DHCP Discover msg to find available DHCP servers.
2. Offer - servers respond with DHCP Offer msg, proposing an IP address lease.
3.Request - client replies with DHCP Request msg, indicating it accepts.
4.Acknowledge - serve sends DHCP Acknowledge msg, confirming that client has been assigned the IP address.


Network Address Translation (NAT)
allows multiple devices on a private network share a single public IP address.
Public IP - globally unique
Private IP - used within LANS.

Types of NAT:
Static - each private IP corresponds to public IP.
Dynamic - assigns public IP from a pool of available addresses to a private IP.
Port Address Translation (PAT) - multiple private IP's share a single public IP.


Domain Name System (DNS)
provides a domain name for IP address.

DNS  Hierarchy:
1. Root Servers
2. Top-Level Domains (TLD's)
3. Second-Level Domains
4. Subdomains

DNS Resolution (Domain Translation):

Step 1: domain name typed in browser.

Step 2: pc checks DNS cache.

Step 3: if not found, queries recursive DNS server. Provided by ISP.

Step 4: recursive DNS server contacts root server, which points to TLD name server.

Step 5: TLD name server directs to authoritative name server.

Step 6: authoritative name server responds with IP address.

Step 7: recursive server returns IP address to pc.


Internet Architecture - describes how data is organized, transmitted and managed across networks.

Peer-to-Peer (P2P) Architecture - each node acts as both a client and a server.

Advantages:
Scalability - more nodes can increase total resources.
Resilience - if one node is offline, others still function.
Cost distribution -  distributed among peers.

Disadvantages:
management - harder to control and manage.
potential reliability issues.
Security challenges.

Client-Server Architecture - clients, which are user devices, send requests and servers respond.

Tiers:
Single-Tier - client, server and database on the same machine.

Two-Tier - splits application environment into client and server.  client - presentation layer , server - data layer.

Three-Tier - adds a third layer - application server.

N-Tier - multiple levels of application servers.

Advantages:
Centralized control - easier to manage and update.
Security - Central security policies can be applied.
Performance - Dedicated servers can be optimized.

Disadvantages:
Single point of failure - central server down = clients lose access.
High cost.
Network congestion.

Hybrid Architecture - Client-Server and P2P combined.

Advantages:
Efficiency - relieves workload from server by letting peers share data.
Control - Central server manages authentication, services.

Disadvantages:
Implementation - requires sophisticated design.
Single point of failure.

Cloud Architecture - virtualized client-server model.

SaaS (Software as a service) model - application accessibility without managing underlying hardware.
 
Characteristics:
1. On-demand self-service
2. Broad network access
3. Resource pooling
4. Rapid elasticity
5. Measured service

Advantages:
Scalability.
Reduced cost.
Flexibility.

Disadvantages:
Vendor lock-in.
Security/Compliance.
Connectivity.

Software-Defined Networking Architecture (SDN)
separates control plane from data plane.
control plane - makes decisions about where traffic is sent.
data plane - forwards the traffic.

Advantages:
Centralized control.
Programmability & Automation.
Scalability & Efficiency.

Disadvantages:
Controller vulnerability
Complex implementation.


Wireless Networks
Communication system, that employs radio waves or other signals allowing devices to connect to the internet, share files and access services. 

Advantages:
Mobility
Ease of installation
Scalability

Disadvantages:
Security
Interference
Speed Limitations

wireless router components:
WAN, LAN, antennae, processor & memory.

mobile hotspot - uses cellular data.

cell tower - structure to create cellular network cell.
cell - area of coverage provided by a single cell tower.
Towers managed by Base Station Controller (BSC).

Macro cells - large towers, extensive coverage.
Micro/small cells - towers fill coverage gaps left by macro cells.

Frequency bands:
1. 2.4 GHz - better at penetrating walls, prone to interference.
2. 5 GHz - faster speeds, shorter range.
3. Cellular bands - For 4G & 5G. range from lower to mid frequencies.


Network Security
CIA triad:
- Confidentiality - only authorized user can view info.
- Integrity - info remains accurate and unaltered.
- Availability - network resources are accessible when needed.

Firewall
network security device (software/hardware/both), that monitors incoming and outgoing network traffic.

firewall policies (access control lists) determine whether to allow or block specific traffic.

traffic filtering - firewall operate packets of data according to firewall policies .

1. Packet Filtering firewall
Layer 3 and 4 of OSI model.
examines source/destination IP, port and protocol type.

2. Stateful Inspection firewall
Tracks the state of network connections.
understand entire convos unlike packet filters.

3. Application Layer firewall (Proxy firewall)
up to layer 7 of OSI model.
inspect actual content of traffic and block malicious requests.

4. Next-gen firewall (NGFW)
stateful inspection with advanced features, intrusion detection/prevention and application control combo.

Intrusion Detection and Prevention Systems (IDS/IPS)

security solutions to monitor and respond to suspicious network or system activity.

IDS - observes traffic, generates alerts but doesnt block.
IPS - observes traffic, rejects malicious traffic.

Signature-based detection - matches traffic to database of known exploits.
Anomaly-based detection - detects anything unusual compared to normal activity.

1. Network-based IDS/IPS (NIDS/NIPS)
hardware/software device placed at strategic points int network to inspect all traffic.

2. Host-based IDS/IPS (HIDS/HIPS)
runs on individual hosts, monitors inbound/outbound traffic and  system logs for suspicious behavior.

Best practices:
Define clear policies.
Regular updates.
Monitor and log events.
layered security.
periodic penetration testing.

localhost/loopback address - allows a device to communicate with itself.

