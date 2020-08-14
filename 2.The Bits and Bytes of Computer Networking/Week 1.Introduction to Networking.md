## Introduction to Computer Networking

### The TCP/IP Five-Layer Network Model

| Layer        | Protocol | Protocol Data Unit | Addressing  |
| :---         | :----:   |          ---:      |  :--:       |
|5.Application | http,smtp|messages            | n/a         |
|4.Transport   | TCP/UDP  | Sengmentation      |Port#'s      |
|3.Network     | IP       | Datagram           |IpAddress    |
|2.Data Link   |Ethernet,WIFI|  Frames         |MACADDRESS   |
|1.Physical    |10 Base t,801.11|Bits          |         n/a |

### Physical Layer
- Represents the physical devices that interconnect computers
- The physical layer consists of devices and means of transmitting bits across computer networks.
-  A bit is the smallest representation of data that a computer can understand. It's a one or a zero


### Data Link Layer -> Protocol -> Ethernet
- Resposible fro defining a common way to interprenting the signals so network devices can communicate.
- The Ethernet standarts also devine a protocol responsible for getting data to nodes on the same network.

### Network Layer(Also Internet Layer)
- Allows different networks to communicate with each other through devices known as routers.
- Internetwork is a collection of networks connected together through routers and the most famous is the Internet.
- IP is the heart of the Internet and most smaller networks around the world.

### Transport Layer
- Sorts out which client and server programs are supposed to get the data.

### Application Layer
- The application layer is the highest abstraction layer of the TCP/IP model that provides the interfaces and protocols needed by the users.
----
## The Basics of Networking Devices
### Cables
- Connecting various devices to eachother and allowning data to transmitted over them.The connection is called point to point.
- We have two categories
    - Copper
        - Are most common used and they changes the voltage from one to zero.The most common forms of copper twisted-pair cables used in networking are Cat5,Cat5e,Cat6.Cat5 is the older and indroduced aproblem name Crosstalk.
        - Crosstalk is when an electrical pulse on one wire is accidentally detected on another wire.
        - Cat5e and 6 are capable or reduce or eliminate the crosstalk.
    - Fiber(Fiber Optic Cables)
        - They contain individual optical fibers,which are tiny tubes made out of glass about the width of a human hair.
        - They uses portions of light to represents the ones and zeros of the data.
        - They are quicker than the Copper cables but more expensive and fragale.
---

### Hubs and Switches
- Hubs and switches are the primary devices used to connect computers on a single network, usually referred to as a LAN, or local area network.They inspect Ethernet data to determine where to send things.
### Hub
- hub is a physical (1) layer device that allows for connections from many computers at once. All the devices connected to a hub will end up talking to all other devices at the same time. It's up to each system connected to the hub to determine if the incoming data was meant for them, or to ignore it if it isn't. This causes a lot of noise on the network and creates what's called a collision domain.
   - Collision Domain, is a network segment where only one device can communicate at a time. If multiple systems try sending data at the same time, the electrical pulses sent across the cable can interfere with each other.

### Switch 
- It is a layer two device very simalar to the hub as it does the same job but the difference is that while a hub is a layer one or physical layer device, a switch is a layer two or data link device.That means that it reduces the the sizes of collision domains in the network because it inspects the contents of the data and understands which system sended the data and  which system is recieving it.

### Routers - Core ISP Routers
- A router is a layer 3 device that knows how to forward data between independent networks. So we can connect to a network lets say in america.
- They inspect IP data to send to the clients.
- The common used are what we have on our home or office.After they connect to the ISP routers that have more sofisticated routing tables.
- Border Gateway Protocol used by routers to send data beetween each other. It let's them learn about the most optimal paths to forward traffic.

### Servers and Clients
- We call all of the network devices that help computers communicate with each other nodes.
- Server is something that provides the data to something that request the data
- Client is something that request the data from a server 
- In most network topographies, each node is primarily either a server, or a client.

--- 
### The Physical Layer
### Twisted Pair Cabling and Duplexing
- Modulation in the Copper cable is the way of varying the voltage across this cable.
- When used for computer networks, this kind of modulation is more specifically known as line coding. 
- Line coding allows devices on either end of a link to understand that an electrical charge in a certain state is a zero, and in another state is a one. Through this seemingly simple techniques, modern networks are capable of moving 10 billion ones and zeros across a single network cable every second.
- Duplex communication is the concept that information can flow in both directions across the cable.
- Simplex communication is unidirectional.
- A phone call on the other hand is duplex since both parties can listen and speak.
- So, devices on either side of a networking link can both communicate with each other at the exact same time. This is known as full duplex
- Half-duplex means that, while communication is possible in each direction, only one device can be communicating at a time.

### Network Ports and Patch Panels
- The most common port is the RJ45.

---
## The Data Link Layer
### Ethernet and MAC Addresses
- Ethernet and Wifi
- Ethernet is old technology from back in the 80's.Back then we have not any switches so only hubs thats why collision domain was a big problem.
- Ethernet as a protocol solved this problem by using a technique known as a carrier sense multiple access with collision detection.The CSMA/CD.
- CSMA/CD Used to determine when the communications channels are clear,and whern a device is free to transmit data.
- MAC Address or Media Access Control Address is something that identifies for whice node the data trasmition is ment for.A MAC Address is a globally unique indentifier attached to an individual network interface.Its a 48-bit number normally represented by 6 groupings of two hexadecimal numbers.
- Octet in computer networking is that any number that can be represented by 8 bits.
- The mac address is split in two sections.The first is called (OUI) Organizationally Unique Identifire and it is the first 3 octets of the MAC address.
- Ethernet uses MAC addresses to ensure that the data it sends has both has both the address for the machine that sent the transition,as well the one the transmission was sended for.

### Unicast, Multicast, and Broadcast
- The way for one device to transmit data to one other device is known as unicast.
- A unicast transmission is always meant for just one receiving address.
- At the Ethernet level, this is done by looking at a special bit in the destination MAC address. If the least significant bit in the first octet of a destination address is set to zero, it means that Ethernet frame is intended for only the destination address. This means it would be sent to all devices on the collision domain, but only actually received and processed by the intended destination.
- If the least significant bit in the first octet of a destination address is set to one, it means you're dealing with a multicast frame.
- A multicast frame is similarly set to all devices on the local network signal. What's different is that it will be accepted or discarded by each device depending on criteria aside from their own hardware MAC address. Network interfaces can be configured to accept lists of configured multicast addresses for these sort of communication.
- The third type of Ethernet transmission is known as broadcast. An Ethernet broadcast is sent to every single device on a LAN. This is accomplished by using a special destination known as a broadcast address. The Ethernet broadcast address is all Fs. 
- Ethernet broadcasts are used so that devices can learn more about each other. 

### Dissecting an Ethernet Frame
- Data Packet is an all-encompassing term that represents any single set of binary data sent across a network link. It just represents a concept it does not specific to a layer.
- Data packets ate the point of ethernet level are known as Ethernet Frames.
- Ethernet Frame is a highly structured collention of information presented in a specific order.The first part of this frame called Preamble.
- Preamble is 8 bytes (64 bits) long,and it can itself be split into two sections
- The last section (SFD) Start Frame Delimiter sgnals to a receiving device that the preamble is over and that the actual frame contents will now follow.
- After comes the Destination MAC address.This is the hardware address of the intended recipient.
- Ether type field is 16 bits long nad used to describe the protocol of the contents of the frame.
- VLAN Header indicates that the frame itself is whats called a VLAN frame.If a VLAN frame is present the Ether type field follows it.
- VLAN or Virtual LAN is a technique that lets you have multiple logical LANs operating on the same physical equipment.
- Next is the Payload .In networking terms,is the actual data being transported ,which is everything that is not a header.
- FCS (Frame Check Sequence) A 4byte or 32-bit number that represents a checksum value for the entire frame.This checksume value is calculated by performing what is known as a cyclical redundancy check against the frame.     







