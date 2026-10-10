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

