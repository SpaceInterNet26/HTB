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



