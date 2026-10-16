# Intro to Networking
Uniform Resource Locator (URL) = Fully Qualified Domain Name (FQDN)

## Network Types
### Common Terminology
- Wide Area Network (WAN) | Internet.
- Local Area Network (LAN)  | Internal Network.
- Wireless Local Area Network (WLAN) | Internal Network accessible via Wi-Fi.
- Virtual Private Network (VPN) | Connects multiple networks to one LAN.

### WAN
a large number of LANs joined together.
### LAN / WLAN
typically assign IP addresses designated for local use.
### VPN
goal - making user feel as if they were in a different network.
#### Site-To-Site VPN
client and server are Network Devices (Routers or Firewalls) and share entire network ranges.
#### Remote Access VPN
clients pc creates a virtual interface that behaves as if it is on clients network.
#### SSL VPN
VPN in web browser. Streams applications or desktop sessions.

## Book Terms
### Network Type
- Global Area Network (GAN) | Global network (Internet)
- Metropolitan Area Network (MAN) | Regional network (multiple LANs)
- Wireless Personal Area Network (WPAN) | Personal Network (Bluetooth)
### GAN
International companies maintain isolated networks that span several WANs and connects company computers. worldwide network, like, Internet.
- uses the glass fibers infrastructure of WANs.
### MAN
broadband telecommunications network that connect LANs in geographical proximity.
### PAN / WPAN
enables data exchange between end devices.
Bluetooth, cable form.
## Networking Topologies
typical arrangement and physical / logical connection of devices in a network. It determines the components to be used and the access methods to the transmission media.
The transmission medium layout used to connect devices is the physical topology of the network.
> topology is a structure of a network.
### 1. Connections
#### Wired connections
- Coaxial cabling
- Glass fiber cabling
- Twisted-pair cabling
- and others
#### Wireless connections
- Wi-Fi
- Cellular
- Satellite
- and others
### 2. Nodes - Network Interface Controller (NICs)
- Repeaters
- Hubs
- Bridges
- Switches
- Router/Modem
- Gateways
- Firewalls
Nodes are the transmission medium's connection points to transmitters and receivers of signals in the medium.
### 3. Classifications
#### Point-to point
dedicated connection between two hosts. Direct and straightforward physical link exists only between two hosts.
> basic model of traditional telephony
#### Bus
All hosts are connected via a transmission medium. Every hosts has access to the medium. No central network component.
Only one host can send, and the others only receive.
#### Star
a network components maintains a connection to all hosts via separate link (Central network component). Handles data packet forwarding.
#### Ring
Physical topology is such that host is connected with to cables :
- One for incoming signals.
- One for outgoing signals.

transmission medium is accessed sequentially using a token. A token is a bit pattern that continually passes through a ring network in one direction, which works according to claim token process.
#### Mesh
many nodes decide about connection on a physical level and routing on a logical.
##### Fully meshed structure
- Each host is connected to every host.

primarily used in WAN or MAN to ensure high reliability and bandwidth.
##### Partially meshed structure
- endpoints are connected by only one connection.
#### Tree
extended star topology.
#### Hybrid
combines two or more topologies.
#### Daisy Chain
multiple hosts are connected by placing a cable from one node to another (chain of connections).
## Proxies
when a device/service sits in the middle of a connection and acts as a mediator. The mediator - the device must be able to inspect the contents of the traffic.  Almost always operates at Layer 7 of OSI model.
### Dedicated Proxy / Forward Proxy
when a client makes a request to a computer, and that computer carries out the request (filters outgoing requests).
### Reverse Proxy
filter incoming requests.
common - Web Application Firewall (WAF). It inspects web requests for malicious content and blocks the request if its malicious.
### (Non-) Transparent Proxy
proxy services act either transparently or not.
#### Transparent proxy
Client doesnt know about its existence.
#### Non-Transparent proxy
Client must be informed.
## Networking Models
Two networking models describe communication and data transfer from one host to another.
### OSI Model
reference model that can be used to describe and define the communication between systems. Has 7 layers.
### TCIP/IP Model
the protocols are responsible for the switching and transferring of data packets on the internet. The internet is entirely based on TCP/IP  protocol family. For example UDP or ICMP belongs to the family.
### OSI vs. TCP/IP
1. TCP/IP
- communication protocol that lets hosts connect to the internet.
- allows a lightening of rules.
2. OSI
- communication gateway between the network and end-users.
- strict protocols and limitations.
### Packet Transfers
Protocol Data Unit (PDU) - devices in a layer exchange data in a different format. 
Encapsulation - during transmission, each layer adds a header to the PDU from the upper layer, which controls and identifies the packet.
## OSI Model
#### Layer
##### 7. Application
- controls input and output od data and provides application functions.
##### 6. Presentation
- transfers the system-dependent presentation of data into a form independent of the application.
##### 5. Session
- controls the logical connection between two systems and prevents connection breakdowns or other problems.
##### 4. Transport
- end-to-end control of the transferred data. It can detect and avoid congestion and segment data streams.
##### 3. Network
- connections are established in circuit-switched networks, and data packets are forwarded in packet-switched networks.
- Data is transmitted over the entire network form the sender to receiver.
##### 2. Data Link
- enable reliable and error-free transmission on medium.
##### 1. Physical
- electrical signals, optical signals, electromagnetic waves.
- transmission takes place on wired or wireless transmission lines.
## TCP/IP Model
#### Layer
##### 4. Application
- allows applications to use other layers' services and defines the protocols application can use to exchange data.
##### 3. Transport
- provides TCP session and UDP services for the application layer.
##### 2. Internet
- host addressing, packaging and routing functions.
##### 1. Link
- places TCP/IP packets on the network medium and receives corresponding packets from medium. 
### Most Important Tasks
##### Logical Addressing
- IP protocol
##### Routing
- IP protocol
##### Error & Control Flow
- TCP
##### Application Support
- TCP
##### Name Resolution
- DNS
## IP Addresses
### IPv4 Structure
32-bit binary number combined into 4 bytes consisting of 8-bit groups (octets) ranging from 0-255.
IP address is divided into host and network parts. router assigns the host part, network administrator assigns the network part. IANA - allocates and manages unique IPs on the internet. IP network blocks divided into classes A-E.
### Subnet Mask
subnetting helps further separate classes into small networks. Separation is done using netmasks. It describes which bit positions within the IP address act as network or host part.
### Network and Gateway Addresses
default gateway - name for the IPv4 address of the router.
### Broadcast Address
connects all devices in the network with each other. 
broadcast - message transmitted to all hosts of a network.
It is the last IPv4 address that is used for the broadcast.
### CIDR
Classless Inter-Domain Routing (CIDR) - method of representation and replaces that fixed assignment between IPv4 address and network classes.
The division is based on subnet mask or CIDR suffix, which allows the division into subnets. CIDR suffix - indicates how many bits from the beginning of the address belong to network.
## Subnetting
The division of IPv4 address into several smaller address ranges.
> subnet is a logical segment of a network that uses IP addresses with the same network address.
for example: 
IPv4 - 192.168.12.160/26
Subnet Mask - 255.255.255.192 (because /26)

- Network part is not changeable
- Host part changeable
