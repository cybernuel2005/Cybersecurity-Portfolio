## What Is Networking - 13-02-2026
A network simply means devices that are connected
- A private Network - Network only allowed users can use
- A Public Network - Network anyone can use

The Internet - One giant network that consists of many small networks with itself
- ARPANET - First internet in the late 1960s, funded by the United States Department of Defense
- World Wide Web(WWW) - A big part of the internet now, invented by *Tim Berners-Lee* in 1989

## IP Address & MAC Address - 14-02-2026
### IP Address
Internet Protocol (IP) Address - A logical address or digital home address assigned to a device for network communication over the Internet.
- Allows devices to send and receive data across networks
- Follows a set of standards called Protocols
- Changes from device to device
- Two devices can't have the same ip address at the same time

The two Types
IPv4:
- Divided into 4 sets of numbers called Octet
- Each section ranges from 0 - 255
- Each octet/section is separated by a dot
- Uses 32-bit, that's 2^32 producing 4.3 billion unique addresses
- Format - 192.168.1.1

IPv6:
- Uses 128-bit, that's 2^128 producing 340 undecillion unique addresses
- Format - 2001:0db8:85a3:0000:0000:8a2e:0370:7334

Private IP Address
- Used within a local network
- Assigned by your network (router, WiFi, internal network carrier)

Public IP Addresses
- Used directly on the internet
- Assigned by your Internet Service Provider (ISP)

### MAC Address
Media Access Control (MAC) Address - A unique permanent ID number given to a device's network hardware to identify a device on a local network
- A device fingerprint
- Made up of 12 characters
- Letters and numbers from 0 - 9 and A - F respectively
- The characters are written in pairs
- Each pair is separated by a colon, considered as a separator
- The first six characters represent the company that made the network device
- The last six characters are unique for devices to devices
- Can be faked or spoofed in the process of spoofing

To apply this concept practically, I completed a Simple MAC Address spoofing:

- Blue ball wasn't allowed to access the TryHackMe site before its MAC address was blocked
![First step](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/efcafbd20aed865074d59679336ace149fad0061/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-14%20205643.png)
![Second Step](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/1ffbfbee3ff2b853656eb7ceefcbd4c22706c700/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-14%20205522.png)

- MAC Address spoofed To Access the TryHackMe Site
![Third Step](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/a25bdf56500cd14146385ae78b6c7ccc5f6686e4/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-14%20205830.png)
  
## Ping - 15-02-2026
Ping is a command that uses ICMP(Internet Control Message Protocol) packets to determine the performance of a connection between devices over a network or the internet
- Check if a device or website is alive on a network
- The syntax is
  ping id address or website URL

To apply this concept practically, I completed a ping command process

![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/382401d4794aa61c7a3524c170ffc3e42b51a529/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-14%20221042.png)

## Local Area Network(LAN) Topologies - 16-02-2026
Topology is the way devices are arranged or connected to each other in a network

### Star Topology
Devices are connected individually via a central networking device, such as a switch or a hub.
All communication or data flows through the central device
##### Advantages
- Fault isolation is easy
- Scalable
- Centralized management

#### Disadvantages
- Single point of failure
- Higher cost
- Maintenance complexity at scale

### Bus Topology
All devices are connected to a single main cable called the backbone cable.
All communication or data travels along the main cable to reach each device

#### Advantages
- Cost-effective
- Simple to install
- Easy for small networks

#### Disadvantages
- Single point of failure
- Performance bottlenecks
- Difficult troubleshooting
- Limited scalability

### Ring/Token Topology
Devices are connected to each other to form a loop.
All communication or data travels around the ring from one device to the next till date reaches its destination

#### Advantages
- Less cabling required
- Predictable traffic flow
- Structured transmission
- Reduces network or data congestion
- Easy troubleshooting

#### Disadvantages
- Single point of failure
- High data latency
- Device dependency
- Network disruption during changes

To apply this concept practically, I identified ways in which LAN topologies are vulnerable to breaking

![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/4c6a2c0a4eab89e8df156e2f8ea8bf145b8dc597/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-17%20031932.png)
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/74e16c5961ff111209c6e5dcc9fbe8398775c1b7/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-17%20032613.png)

### Note
Bus topology is more cost-effective, followed by ring topology, and then star topology

## What is a Switch?
A networking device that connects multiple devices(hosts) together on a network and sends data to the right device
- Mostly done using Ethernet through switch ports
- Have different ports of 4,8,16,24,32 and 64
- More effective than a hub/repeater
- Reduces data traffic
- Keep track of what device is connected to which port

### What is a Router?
A device that connects different networks together and passes data between them.
- It does it by using routing
- Routing is the process of directing data between different networks using IP addresses to determine the best path
- Routing is useful when devices are connected by many paths

## A Primer of Subnetting - 17-02-2026
Subnetting is dividing one big network into smaller, organized networks

A subnet mask  is a 32-bit number used to determine the network and host portion of an IPv4 address for routing and network segmentation

Subnets use IP Addresses in three different ways
- Network Address - Used to identify a network existence
- Host Address - Used to identify a device on a subnet
- Default Gateway - A special address assigned to a device on the network capable of sending information to another network

## ARP & DHCP - 18-02-2026
### ARP (Address Resolution Protocol)
It is a protocol on local networks used to map a device's IP address to its MAC address so data can be delivered to the right device

How it works
- Checks ARP table/cache - To check if the IP address already has a known MAC address
- ARP broadcast Request - Sends to every device on the local network, "Who has this IP address? Tell me your MAC?"
- ARP Reply - Device responds to the broadcast with its MAC address
- Update ARP table/cache - The computer stores this mapping in its ARP table for a short time
- Data Delivery - With the MAC address known, the computer sends the frame to the correct device on the LAN.

ARP cache/table is a temporary storage on a device that keeps a list of known IP addresses and their corresponding MAC addresses

### DHCP (Dynamic Host Configuration Protocol)
It is a protocol that automatically assigns IP addresses and other communication parameters to devices when they join a network using a client-server architecture

How it works
- DHCP Discover - A broadcast message sent by the device to DHCP servers asking for an IP address
   - Sent to all devices on the local network because the device doesn’t know where the DHCP server is.
   - Starts the process.
- DHCP Offer - The DHCP server replies to the device.
  - The offer is temporary until the device accepts it.
  - Multiple DHCP servers could technically offer addresses; the device picks one.
- DHCP Request - The device responds to the server
  - Confirms to one DHCP server that it accepts the IP.
  - Prevents conflicts if multiple servers make offers.
- DHCP Ack(Acknowledgement) - The DHCP server replies back to finalize the process
  - This finalizes the lease.
  - The device can now communicate on the network with this IP.

## Open systems Interconnection(OSI) Model - 19-02-2026
A model that provides a framework of how all networked devices send, recieve and interpret data. It is arranged from Layer 7 to 1.
Note: Encapsulation - A term for when pieces of information are added to data in the OSI model

### Physical Layer(1st)
Responsible for physically transmitting raw bits{Data unit (0s and 1s-binary numbering system)}  using electrical, optical, or radio(wireless) signals between devices through networking hardware.
##### Layer 1 Devices
- Cables (Transmission media)
- Hub
- Repeater
- Antennas (wireless)
- Network Interface Card(NIC)

### Data Link Layer(2nd)
Packages bits into frames(Data unit), uses *MAC addresses* to send data to the correct device on the local network, and handles error detection and flow controls 
#### Layer 2 Devices
- Switch
-  Bridge
-  NIC

### Network Layer(3rd)
Responsible for using *IP addresses* to route packets(Data unit) between networks and chooses the best path for them to reach their destination.

Routing is choosing the best path for packets to travel from one network to another.

Some common routing protocols are
- OSPF( Open Shortest Path First)
- RIP ( Routing Information Protocol)

Factors that determine the Best path
- What path is the shortest? - The least number of devices that the packets need to travel across
- What path is mostly reliable? - Have packets been lost on that path before
- Which path has the faster physical connection? - Is the path using a copper connection (slower) or a fiber connection(faster)

Router - Layer 3 device

### Transport Layer(4th)
Plays a vital part in transmitting segments/datagrams(Data unit) across a network using *port numbers*, getting data to the correct app.
Uses TCP and UDP protocols

#### Transmission Control Protocol(TCP)
Provides reliable data transfer(segment), flow control, and congestion control. Higher-level protocols such as HTTP, POP3, IMAP, and SMTP use TCP

###### Advantages
- Data accuracy
- Reliable
- Requires three way handshake to establish a connection
- Make sure the sender does not send data faster or larger than the receiver can handle
- Reserves a constant connection between two devices for the amount of time it takes for the data transmission
- Incorporate error checking into its design

###### Disadvantages
- Requires all data segments to arrive correctly; if not data can't be used
- Reserves system resources for the duration of a connection, so a slow connection may reduce overall performance or cause bottlenecks
- Significantly slower because more work has to be done by the device using this protocol

Use in file sharing, internet browsing, sending emails, etc.

#### User Datagram Protocol(UDP)
It's a connectionless, fast query(datagram), prioritise real time communications, such as audio and video conferencing, and broadcasts

###### Advantages
- Much faster than TCP
- Does not control the transmission speed; it lets the application decide
- Does not reserve a continuous connection on a device, reducing resource usage and improving efficiency

###### Disadvantages
- Doesn't care if the data is received or not
- UPD's flexibility requires developers to implement their own reliability and control mechanisms, increasing complexity
- Unstable connections result in a terrible experience for the user

### Session Layer(5th)
Manages and controls communication sessions between applications using *session id/token*.
A session is an ongoing exchange between two applications.

Responsible for:
- Session creation
- Session maintenance
- Session termination
- Session isolation
- Session recovery

### Presentation Layer(6th)
Responsible for standardizing data, that's translating, formatting, encrypting, and compressing  so the receiving application understands it securely and efficiently. It handles three main things
- Translation(format converwion)
- Encryption/Decryption
- Compression

### Application Layer(7th)
Provides the interface and *protocols* that allow software applications to communicate with the user.

To apply this concept practically, I completed an OSI model game
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/d640b4ee8fbf47db5c761496dd80a578adda48e7/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-21%20152650.png)
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/d87424f22c3980422627ef817e91680479f2cafa/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-21%20153047.png)

## Packets & Frames - 23-02-2026
Packets and Frames are small pieces of data that, when combined, form a larger piece of information or message. However, they are two different things in the OSI model 

A packet is a piece of data from layer 3(network layer) of the OSI model, containing information such as IP header and payload.

IP header is the metadata, not the actual message that contains the instruction of how the data should travel.
##### What's Inside an IP header
- Source IP Address - Who sent the data
- Destination IP Address - Where data is going
- TTL(Time To Live) - Prevent infinite routing loops
- Protocol - What protocol is the packet using
- Total Length - Size of the entire packet
- Header Length - Size of the IP header
- Fragmentation Info - If packets were split
- Checksum - Detect header corruption

Payload is the real content or message being carried

A frame is used in the layer 2(Data Link) of the OSI model, which encapsulates the packet and adds additional information such as MAC address

Note this - Data travels in frames on the local network, and travels in packets across networks

### TCP/IP (Three-way handshake)
It's a connection - based protocol that requires a connection

TCP/IP protocol consists of 4 layers and is the summarized version of the OSI model.
These layers are
- Application
- Transport
- Internet
- Network Interface

TCP packets contain various sections of information known as the header and work in the transport layer. The header contains;
- Source port - Port opened by the sender to send a TCP packet from. Chosen randomly from 0 - 65535 ports that aren't already in use at that time
- Destination Port - The port number that an application or service is running on the remote host to receive the data. Not chosen randomly
- Source IP - IP Address of the device that is sending the packet
- Destination IP - IP Address of the device that is receiving the packet
- Sequence Number - Random number that is given to the first data transmitted when a connection occurs
- Acknowledge Number - Indicates the next byte of data the receiver expects, confirming receipt of all previous bytes has been sucessful
- Checksum - A value used to verify that the TCP header and data were not corrupted during transmission
- Data - where the message to transmit is stored
- Flag - Determine how the packet should be handled by either device during the handshake process

#### Three-Way Handshake
It's the term given for the process used to establish a connection between two devices. It communicates using a few special messages(STEP-MESSAGE-DESCRIPTION)
- STEP1 - SYN(Synchronize) - It's the initial packet sent by a client. It's used to initiate a connection
- STEP2 - SYN/ACK - Packet is sent by the server to acknowledge the synchronization attempt from the client
- STEP3 - ACK(Acknowledge) - Either by a client or server, an acknowledge packet is sent  to show the connection has been successfully established
- STEP4 - DATA - Once the connection has been established, data(such as byte of file)  is sent via a "DATA" message
- STEP5 - FIN(Finish) - This packet is used to close the connection after data transfer is completed
- RST(Reset) - This packet happens when there is a problem during the handshake proccess which ends communication to reset it

TCP Closing a connection - Once a device has determined that the other device has successfully received all the data

To apply this concept practically, I completed a TCP handshake
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/abb8e13c5b2621e2a019a2c32ecde13aad54f931/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-25%20010452.png)
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/6973541f6e8dc6c5f86e670369bb49d5e7d09aaa/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-25%20010605.png)

### UDP/IP
It's a stateless protocol that doesn't require a connection

UDP packets have fewer header details.
- Time To Live(TTL) - Set an expiry timer for the packet
- Source Address
- Destination Address
- Source Port
- Destination Port
- Data

### Ports 101 - 25-02-2026
Ports are an essential point at which data can be exchanged. Networking devices also use ports to enforce strict rules when communicating with one another. 

In networking, ports are numerical values between 0 and 65535. Every port between 0 and 1024 is known as *a common port*.
Some ports, port number, and description;
- File transfer protocol(FTP) - 21 - Used by a file sharing application built on a client-server model
- Secure Shell(SSH) - 22 - Used to secure login to systems via a text - based interface for management
- HyperText Transfer Protocol(HTTP) - 80 - Powers the www, used to access web pagesusing browsers
- HyperText Transfer Protocol Secure(HTTPs) - 443 - Secure version of HTTP using encryption
- Server Message Block(SMB) - 445 - Similar to FTP, but allows you to share devices like printers
- Remote Desktop Protocol(RDP) - 3389 - Secure means of logging into a system using a visual desktop interface

To apply this concept practically, I completed a simple port connection
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/7b6f8ae6e094c81ea533accc4e4d91267c506a4f/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-26%20005733.png)

### Port Forwarding - 26-02-2026
It maps an external port on a router to an internal device's port, allowing outside access to internal services.
It is configured at the *router* of a network

### Firewall 101
A security tool, hardware, or software that is used to filter network traffic by stopping unauthorized incoming and outgoing traffic

Factors a firewall can be configured to follow;
- where the traffic is coming from
- where the traffic is going to
- What port is the traffic for
- What protocol is the traffic using
Firewalls perform these packet inspection

Firewalls can be categorised into 2 to 5 categories.
The 2 categories are;
- Stateful - A stateful firewall tracks active connections and makes decisions based on the entire connection.
- Stateless - A stateless firewall checks each packet individually using fixed rules and does not remember past traffic.

Firewall operates at the Network layer(layer 3) and transport layer(layer 4) of the OSI model

To apply this concept practically, I completed a simple firewall filtering
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/ca5da6096097a342287ebf1434a30bf94e2b4097/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-27%20005347.png)
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/ca5da6096097a342287ebf1434a30bf94e2b4097/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-27%20005407.png)
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/ca5da6096097a342287ebf1434a30bf94e2b4097/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-27%20005223.png)

### VPN Basics - 27-02-2026
A Virtual Private Network(VPN) is a technology that allows devices on separate networks to communicate securely by creating a dedicated path between each other over the Internet (known as a tunnel). Devices connected within this tunnel form their own private network.

Benefits
- Allows networks in different geographical locations to be connected.
- Offers privacy - Encrypts traffic, hides your IP and prevents your ISP from seeing browsing details
- Offers Anonymity - The level of anonymity a VPN provides is only as much as how other devices on the network respect privacy. For example, a VPN that logs all of your data/history is essentially the same as not using a VPN in this regard.

#### VPN Technology
- Point-to-Point Protocol(PPP) - A layer 2 protocol that manages authentication, IP assignment and data encapsulation between a client and VPN server before encryption is applied
- Point-to-Point Tunneling Protocol(PPTP) - A VPN protocol that allows PPP data to travel across the internet by creating a tunnel between a client and a server. PPTP is very easy to set up and is supported by most devices. It is, however, weakly encrypted in comparison to alternatives.
- Internet Protocol Security(IPSec) - encrypts data(IP traffic) operating at the network layer using the existing Internet Protocol (IP) framework. IPSec is difficult to set up in comparison to alternatives; however, if successful, it boasts strong encryption and is also supported on many devices.

### LAN Networking Devices
##### What's a Router
- Its job is to connect networks and pass data between them.
- It does this by using routing (hence the name router!).
- Routing is the process of data traveling across networks. Routing involves creating a path between networks so that this data can be successfully delivered.
- Operate at Layer 3 of the OSI model.
- They often feature an interactive interface (such as a website or a console) that allows an administrator to configure various rules, such as port forwarding or firewalling.

Factors for Routing
- What path is the shortest?
- What path is the most reliable?
- Which path has the faster medium (e.g., copper or fibre)?

##### What's a Switch
- It is a dedicated networking device responsible for providing a means of connecting to multiple devices. 
- It can facilitate many devices (from 3 to 63) using Ethernet cables.
- It can operate at both layer 2 and layer 3 of the OSI model.
- But layer 2 switches can't operate at layer 3.
- Layer 3 switches can perform some of the responsibilities of a router

VLAN(Virtual Local Area Network) - Split a single switch into multiple virtual networks, so devices behave as if they are in separate networks

It provides
- Security - Because devices on separate networks can't communicate, even though they are all on one switch
- Reduce broadcast traffic - Broadcasts stay inside their VLAN
- Network organization
- Access control - Can apply firewall rules between VLANs

- To apply this concept practically, I completed an experiment with the network simulator.
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/46f758c64b7e5e281e094d484250c9a4efe26626/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-28%20204544.png)
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/46f758c64b7e5e281e094d484250c9a4efe26626/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-28%20204733.png)


### Go Back
[Pre Security](https://github.com/cybernuel2005/Cybersecurity-Portfolio/tree/main/TryHackMe/Pre%20Security)

