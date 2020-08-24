# Google IT Support
### My notes from the lectures for study.


## 1. Technical Support Fundamentals

<details>
<summary>Week 1. Introduction to IT</summary>

# History of Computing

### From Abacus to Analytical Engine
- A computer is a device that stores and processes data by performing calculations.

- Abacus is one of the earliest known computers

- The first major step forward was the invention of the mechanical calculator in the 17th by Blaise Pascal. It was limited to addition, subtraction, multiplication and division for pretty small numbers. 
- In the 1800s, a man by the name of Joseph Jacquard invented a programmable loom.
-  Babbage built what was called a difference engine. Babbage's follow up to the difference engine was a machine he called the Analytical Engine. It took the powerful insights of a mathematician named Ada Lovelace to realize the true potential of the analytical engine. She was the first person to recognize that the machine could be used for more than pure calculations. She developed the first algorithm for the engine. It was the very first example of computer programming. 
- An algorithm is just a series of steps that solves specific problems.


### The Path to Modern Computers
- Cryptography is the art of writing and solving codes
- A magnetic tape worked by magnetizing data onto a tape
- The ENIAC was one of the earliest forms of general purpose computers
- The very first compiler was invented by Admiral Grace Hopper.Compilers made it possible to translate human language via a programming language into machine code
- Eventually, the industry gave way to the first hard disk drives and microprocessors
- Then in the 1970s, a young engineer named Steve Wozniak invented the Apple I, a single-board computer MIT for hobbyists. With his friend Steve Jobs, they created a company called Apple Computer.
-  In the 1980s, IBM introduced its personal computer. It was released with a primitive version of an operating system called MS DOS or Microsoft Disk Operating System.
- With huge players in the market like Apple Macintosh and Microsoft Windows taking over the operating systems space, a programmer by the name of Richard Stallman started developing a free Unix-like operating system. Unix was an operating system developed by Ken Thompson and Dennis Ritchie, but it wasn't cheap and wasn't available to everyone.
- Stallman created an OS that he called GNU. It was meant to be free to use with similar functionality to Unix. Unlike Windows or Macintosh, GNU wasn't owned by a single company, its code was open source which meant that anyone could modify and share it. GNU didn't evolve into a full operating system, but it set a foundation for the formation of one of the largest open source operating system, Linux, which was created by Linus Torvalds

## Digital Logic
### Computer Language
- The communication that a computer uses is referred to as binary system, also known as base-2 numeral system.This means that it only talks in 1s and 0s.
- In computing terms, we group binary into 8 numbers, or bits. Technically, a bit is a binary digit
-  A group of 8 bits is referred to as a byte. A byte of zeroes and ones could look like 10011011. Each byte can store one character, and we can have 256 possible values, thanks to the base-2 system, 2 to the 8th. In computer talk, this byte could mean something like the letter C.

### Character Encoding
-  Character encoding is used to assign our binary values to characters so that we as humans can read them.
- The oldest character encoding standard used this ASCII
- Then came UTF 8. The most prevalent encoding standard used today

### Binary
- Imagine we have a light bulb and a switch that turns the state of the light on or off. If we turn the light on, we can denote that state is one. If the light bulb is off, we can represent the state is zero. Now imagine eight light bulbs and switches, that represents eight bits with a state of zero or one.

### Supplemental Reading on Logic Gates
For more information about logic gates, check out the [link here.](https://simple.wikipedia.org/wiki/Logic_gate)
### How to Count in Binary
- Imagine that we have the following binary number 00001010 and we want to convert it to a decimal number.We check to see what ones are switched on.2+8 = 10.

## Computer Architecture Layer
### Abstraction
- We use the concept of abstraction to take a relatively complex system and simplify it for our use.
- One other simple example of abstraction in an IT role that you might see a lot is an error message. We don't have to dig through someone else's code and find a bug.
### Computer Architecture Overview
-  A computer can be cut into four main layers, hardware, operating system, software, and users.
- The hardware layer is made up of the physical components of a computer
-  The operating system allows hardware to communicate with the system
-  The software layer is how we as humans interact with our computers
- The last layer may not seem like it's part of the system, but it's an essential layer of the computer architecture, the user.

[Back to main](/README.md)

</details>



## 2. The Bits and Bytes of Computer Networking
<details>
<summary>Week 1. Introduction to Computer Networking</summary>

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


## The Physical Layer
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

[Back to main](/README.md)

</details>



<details>

<summary>Week 2. The Network Layer</summary>

### IP Addresses
- IP addresses are a 32 bit long numbers made up of four octets, and each octet is normally described in decimal numbers. 8 bits of data or a single octet can represent all decimal numbers from 0 to 255. For example, 12.30.56.78 is a valid IP address, but 123.456.789.100 would not be.
-  IP addresses belong to the networks, not the devices attached to those networks.
- Your laptop will always have the same MAC address no matter where you use it, but it will have a different IP address assigned to it at an Internet cafe than it would when you're at home.
- Any LAN whould provide different IP beacause its a different local network.
- The protocol that provide us an automaticly IP is the 'dynamic host configuration protocol'.
- An IP address assigned this way is known as a dynamic IP address.
- Static IP address is the opposite which must be configured on a node manually.
- In most cases static IP addresses are reserved for servers and network devices, while dynamic IP addresses are reserved for clients

### IP Datagrams and Encapsulation
- Generally we talk about networking in terms of layers. Each layer is needed for the one above it.
- An IP datagram is a highly structured series of fields that are strictly defined. It's the payload section of the Ethernet frame.
- The proccess that follows below its called "encapsulation".
- The entire contents of an IP datagram are encapsulated as the payload of an Ethernet frame.
-  IP datagram also has a payload section. The contents of this payload are the entirety of a TCP or UDP packet.
- First field is called Version (4bits).
It indicates what version of Internet protocol is being used. The most common version of IP is version four or IPv4. Version six or IPv6 is rapidly seeing more widespread adoption.
- Next is the Header Length field. It is almost always 20 bytes in length when dealing with IPv4. In fact, 20 bytes is the minimum length of an IP header.
- Next is the Service Type field.(8bits) This field can be used to specify details about quality of service or QoS technologies. The important takeaway about QoS is that there are services that allow routers to make decisions about which IP datagram may be more important than others.
- Next is  the Total Length field,(16bits) and its indicate the total length of the IP datagram it's attached to.
- Next is the identification field(16bits) and its used to to group messeges together.If the total amount of data is larger than what can fit in asingle datagram,the IP layer needs to split the data  into many individual packets. In this case the identification field understands that every packete with the same value is part of the same splitted transmission.
- Next is the flag field and its used to indicate if a datagram is allowed to be fragmented, or to indicate that the datagram has already been fragmented.
- After this the next field the fragmentation field takes a single IP datagram and splitting it uo into several smaller datagrams. If a datagram has to cross from a network allowing a larger datagram size to one with a smaller datagram size, the datagram would have to be fragmented into smaller ones. The fragmentation offset field contains values used by the receiving end to take all the parts of a fragmented packet and put them back together in the correct order.
- Next is 'The Time to Live or TTL' field. It's an 8bit field that indicates how many router hops a datagram can traverse before it's thrown away.  Every time a datagram reaches a new router, that router decrements the TTL field by one. Once this value reaches zero, a router knows it doesn't have to forward the datagram any further. It prevends from an endless loop that could happen when router A thinks router B is the next hop, and router B thinks router A is the next hop.
- Next is the Protocol field. It is an 8bit field that contains data about what transport layer protocol is being used.The most common transport layer protocols are TCP and UDP.
- Next is the header checksum field.This field is a checksum of the contents of the entire IP datagram header.Since the TTL field has to be recomputed at every router that a datagram touches, the checksum field necessarily changes, too.
- Next are the source and destination IP address fields(32bits).
- Next is the IP Options field.This is an optional field and is used to set special characteristics for datagrams primarily used for testing purposes. The IP options field is usually followed by a padding field. Since the IP options field is both optional and variable in length, the padding field is just a series of zeros used to ensure the header is the correct total size.

### IP Address Classes
- IP addresses can be split into two sections, the network ID and the host ID.
- If we take an example IP address of 9.100.100.100, the network ID would be the first octet, and the host ID would be the second, third and fourth octets.
- There are three primary types of address classes. Class A, Class B and Class C.
- Class A addresses are those where the first octet is used for the network ID and the last three are used for the host ID. 
- Class B addresses are where the first two octets are used for the network ID, and the second two are used for the host ID. 
- Class C addresses, as you might have guessed, are those where the first three octets are used for the network ID, and only the final octet is used for the host ID.
-  In practical terms, this class system has mostly been replaced by a system known as CIDR or classless inter-domain routing.

### Address Resolution Protocol
- Remember that Mac addresses are used in the datalink layer and IP address are used in the network layer.
- These two seperate address types are related to each other with the address resolution protocol or ARP.
- ARP is a protocol used to discover the hardware address of a node with a certain IP address.
- Once it IP datagram has been fully formed, it needs to be encapsulated inside an Ethernet frame. This means that the transmitting device needs a destination MAC address to complete the Ethernet frame header. Almost all network connected devices will retain a local ARP table. An APR table is just a list of IP addresses an the Mac addresses associated with them.
- The kinds of broadcasts ARP messages are delivered to all computers on the local network. When the network interface that's been assigned an IP of 10.20.40 receives this ARP broadcast, it sends back what's known as an ARP response. This response message will contain the MAC address for the network interface in question. Now, the transmitting computer knows what MAC address to put in the destination hardware address field, and the Ethernet frame is ready for delivery. It'll also likely store this IP address in its local ARP table, so that it won't have to send an ARP broadcast the next time it needs to communicate with this IP, handy. ARP table entries generally expire after a short amount of time to ensure changes in the network are accounted for.

## Subnetting
### Subnetting
- With subnets you can split your large network up into many smaller ones. These individual subnets will all have their own gateway routers serving as the ingress and egress point for each subnet.

### Subnet Masks
- An IP address is just a 32-bit number. In a world without subnets, a certain number of these bits are used for the network ID, and a certain number of the bits are used for the host ID. In a world with subnetting, some bits that would normally comprise the host ID are actually used for the subnet ID. With all three of these IDs representable by a single IP address, we now have a single 32-bit number that can be accurately delivered across many different networks.
- Subnet masks are 32-bit numbers that are normally written now as four octets in decimal.
-  A subnet mask is a binary number that has two sections. The beginning part, which is the mask itself is a string of ones just zeros come after this, the subnet mask, which is the part of the number with all the ones, tells us what we can ignore when computing a host ID. The part with all the zeros tells us what to keep.

### Basic Binary Math
-  You can represent all whole numbers in binary in the same way you can in decimal.
-  You start with zero, which is the same as zero in decimal. Then you increment once. Now you have one, which is the same as one in decimal since we've already run out of numerals to use. It's time to add a new column. So now we have the number one zero which is the same as two in decimal. One one is three, one zero zero is four, one zero one is five, one one zero is six, one one one is seven, etc. It's the exact same thing we do with decimal, just with fewer numerals at our disposal.
- Binary is base two and decimal base 10.
-  Two of the most important operators are OR and AND. In computer logic, a one represents true and a zero represents false.
- The way the or operator works is you look at each digit, and if either of them is true, the result is true. The basic equation is X or Y equals Z.
-  if either X or Y is true then Z is true, otherwise, it's false.
- One or zero equals one, but zero or zero equals zero.
- The operator AND does what it sounds like it does, it returns true if both values are true. Therefore, one and one equals one, but one and zero equals zero, and zero and zero equals zero.

### CIDR
- CIDR or classless inter-domain routing comes into play. CIDR is an even more flexible approach to describing blocks of IP addresses. It expands on the concept of subnetting by using subnet masks to demarcate networks. To demarcate something means to set something off.
- Demarcation point to describe where one network or system ends and another one begins .
- With CIDR, the network ID and subnet ID are combined into one. CIDR is where we get this shorthand slash notation that we discussed in the earlier video on subnetting. This slash notation is also known as CIDR notation. CIDR basically just abandons the concept of address classes entirely, allowing an address to be defined by only two Individual IDs.
- CIDR allows for networks themselves to be differing sizes.

## Routing
### Basic Routing Concepts
- A router is a network device that forwards traffic depending on the destination address of that traffic.
- A router is a device that has at least two network interfaces, since it has to be connected to two networks to do its job.
- Basic routing has just a few steps. 
    - One, a router receives a packet of data on one of its interfaces. 
    - Two, the router examines the destination IP of this packet. 
    - Three, the router then looks up the destination network of this IP in its routing table. Four, the router forwards that out though the interface that's closest to the remote network. As determined by additional info within the routing table.
- Remember, IP addresses belong to networks, not individual nodes on a network.

### Routing Tables
- The most basic routing table will have four columns.
    - Destination network, this column would contain a row for each network that the router knows about, this is just the definition of the remote network, a network ID, and the net mask. These could be stored in one column inside a notation, or the network ID and net mask might be in a separate column. Either way, it's the same concept, the router has a definition for a network and therefore knows what IP addresses might live on that network. When the router receives an incoming packet, it examines the destination IP address and determines which network it belongs to. A routing table will generally have a catchall entry, that matches any IP address that it doesn't have an explicit network listing for.
    - Hop, this is the IP address of the next router that should receive data intended for the destination networking question or this could just state the network is directly connected and that there aren't any additional hops needed.
    - Total hops,it's just important to know that for each next hop and each destination network, the router will have to keep track of how far away that destination currently is.
    -  Interface, the router also has to know which of its interfaces it should for traffic matching the destination network out of.

    ### Interior Gateway Protocols
    - Routing protocols fall into two main categories, interior gateway protocols, and exterior gateway protocols.
    - Interior gateway protocols are further split into two categories, link state routing protocols and distance-vector protocols.
    - Interior gateway protocols are used by routers to share information within a single autonomous system. In networking terms, an autonomous system is a collection of networks that all fall under the control of a single network operator
        - Distance-vector protocols are an older standard. A router using a distance-vector protocol basically just takes its routing table, which is a list of every network known to it and how far away these networks are in terms of hops.Then the router sends this list to every neighboring router, which is basically every router directly connected to it. In computer science, a list is known as a vector. This is why a protocol that just sends a list of distances to networks is known as a distance-vector protocol. With a distance-vector protocol, routers don't really know that much about the total state of an autonomous system, they just have some information about their immediate neighbors.
        Distance vector protocols are pretty simple, but they don't allow for a router to have much information about the state of the world outside of their own direct neighbors.
        - Link state protocols get their name because each router advertises the state of the link of each of its interfaces. These interfaces could be connected to other routers, or they could be direct connections to networks. The information about each router is propagated to every other router on the autonomous system. This means that every router on the system knows every detail about every other router in the system. Each router then uses this much larger set of information and runs complicated algorithms against it to determine what the best path to any destination network might be.
        Link state protocols require both more memory in order to hold all of this data and also much more processing power. This is because it has to run algorithms against this data in order to determine the quickest path to update the routing tables

### Exterior Gateway Protocols
- Exterior gateway protocols are used to communicate data between routers representing the edges of an autonomous system.
- Since routers sharing data using interior gateway protocols are all under control of the same organization. Routers use exterior gateway protocols when they need to share information across different organizations.
- The IANA or the Internet Assigned Numbers Authority, is a non-profit organization that helps manage things like IP address allocation.
- Along with managing IP address allocation, the IANA is also responsible for ASN, or Autonomous System Number allocation. ASNs are numbers assigned to individual autonomous systems
- Unlike IP addresses, they're normally referred to as just a single decimal number.
-  An ASN, never needs to change in order for it to represent more networks or hosts. Its just the core Internet routing tables that need to be updated to know what the ASN represents

### Non-Routable Address Space
- The IPv4 standard doesn't even have enough IP addresses available for every person on the planet.
- In 1996, RFC 1918 was published. RFC stands for Request for Comments, and has a long standing way for those responsible for keeping the internet running to agree upon the standard requirements to do so.
-  RFC 1918, outlined a number of networks that would be defined as non-routable address space. 
- Non-routable address space are ranges of IPs set aside for use by anyone that cannot be routed to.
- Non-routable address space allows for nodes on such a network to communicate with each other but no gateway router will attempt to forward traffic to this type of network.
-  RFC 1918 defined three ranges of IP addresses that will never be routed anywhere by co-routers.
 Non-routable address space are :
    - 10.0.0.0/8
    - 172.16.0.0/12
    - 192.168.0.0/16

        
[Back to main](/README.md)

</details>

<details>
<summary>Week 3. The Transport and Application Layers</summary>

## Introduction to the Transport and Application Layers
- Transport layer allows traffic to be directed to specific network applications
- Application layer allows these applications to communicate in a way they understand.

## The Transport Layer
### The Transport Layer
- The transport layer has the ability to multiplex and demultiplex, which sets this layer apart from all others.
- Multiplexing in the transport layer means that nodes on the network have the ability to direct traffic toward many different receiving services.
- Demultiplexing is the same concept, just at the receiving end, it's taking traffic that's all aimed at the same node and delivering it to the proper receiving service.
- The transport layer handles multiplexing and demultiplexing through ports.
A port is a 16-bit number that's used to direct traffic to specific services running on a networked computer.
- Different network services run while listening on specific ports for incoming requests.
- A socket address or socket number (10.1.1.100:80) its the Ports which are normally denoted with a colon after the IP address.
- FTP is an older method used for transferring files from one computer to another, but you still see it in use today.
FTP traditionally listens on port 21, so if you wanted to establish a connection to an FTP server running on the same IP that our example web server was running on, you direct traffic to 10.1.1.100 port 21.

### Dissection of a TCP Segment
- An IP datagram encapsulates a TCP segment.
    1. An Ethernet frame has a payload section which is really just the entire contents of an IP datagram.
    2. An IP datagram has a payload section and this is made up of what's known as a TCP segment.
    3. So the TCP segment will also have a payload section that ,as athe others before it,will include the contents of the Application Layer.
- A TCP segment is made up of a TCP header and a data section.
    - This data section,is just another payload area for where the application layer places its data.

    - TCP header.
        - Source port and the Destination port fields.
        - The destination port is the port of the service the traffic is intended for.
        - A source port is a high numbered port chosen from a special section of ports known as ephemeral ports.
        -  the sequence number. This is a 32-bit number that's used to keep track of where in a sequence of TCP segments this one is expected to be. The sequence number in a header is used to keep track of which segment out of many this particular segment might be.
        - The acknowledgment number is the number of the next expected segment. A sequence number of one and an acknowledgement number of two could be read as this is segment one, expect segment two next. 
        - The data offset field comes next. This field is a four-bit number that communicates how long the TCP header for this segment is.
        - Then, we have six bits that are reserved for the six TCP control flags.
        - A TCP window (16-bits) specifies the range of sequence numbers that might be sent before an acknowledgement is required.
        -  A 16-bit checksum. It operates just like the checksum fields at the IP and Ethernet level.The checksum is calculated across the entire segment and is compared with the checksum in the header to make sure that there was no data lost or corrupted along the way.
        - The Urgent pointer field is used in conjunction with one of the TCP control flags to point out particular segments that might be more important than others.
        - Options field.
        - Padding which is just a sequence of zeros to ensure that the data payload section begins at the expected location.


### TCP Control Flags and the Three-way Handshake
- The way TCP establishes a connection, is through the use of different TCP control flags, used in a very specific order.

- 6 TCP control flags
    - The first flag is URG, this is short for Urgent. A value of one here indicates that the segment is considered urgent and that the urgent pointer field has more data about this
    - The second flag is ACK, short for acknowledge. A value of one in this field means that the acknowledgment number field should be examined. 
    - The third flag is PSH, which is short for Push. The transmitting device wants the receiving device to push currently- buffered data to the application on the receiving end as soon as possible. (A buffer is a computing technique, where a certain amount of data is held somewhere, before being sent somewhere else).
    - The Fourth flag is RST, short for Reset. This means, that one of the sides in a TCP connection hasn't been able to properly recover from a series of missing or malformed segments.
    - The fifth flag is SYN, which stands for Synchronize. It's used when first establishing a TCP connection and make sure the receiving end knows to examine the sequence number field.
    - The six flag is FIN, which is short for Finish. When this flag is set to one, it means the transmitting computer doesn't have any more data to send and the connection can be closed.
- Transmition example
    - To start the process off, computer A, sends a TCP segment to computer B with this SYN flag set.
    - Computer B then responds with a TCP segment, where both the SYN and ACK flags are set.
    - Then computer A responds again with just the ACK flag set.
    - This is known us the three way handshake. A handshake is a way for two devices to ensure that they're speaking the same protocol and will be able to understand each other. Once the three way handshake is complete, the TCP connection is established.
    - Since both sides have now sent SYN/ACK pairs to each other, a TCP connection in this state is operating in full duplex
    -  To close the connection, the four way handshake happens. The computer ready to close the connection, sends a FIN flag, which the other computer acknowledges with an ACK flag. Then, if this computer is also ready to close the connection, which will almost always be the case. It will send a FIN flag. This is again responded to by an ACK flag.

### TCP Socket States
- A socket is the instantiation of an endpoint in a potential TCP connection. An instantiation is the actual implementation of something defined elsewhere. TCP sockets require actual programs to instantiate them. You can contrast this with a port which is more of a virtual descriptive thing. In other words, you can send traffic to any port you want, but you're only going to get a response if a program has opened a socket on that port.

- Sockets States (Are naming different in each OS)
    - LISTEN. Listen means that a TCP socket is ready and listening for incoming connections. You'd see this on the server side only. 

    - SYN_SENT. This means that a synchronization request has been sent, but the connection hasn't been established yet. You'd see this on the client side only. 
    - SYN_RECEIVED. This means that a socket previously in a listener state, has received a synchronization request and sent a SYN_ACK back. But it hasn't received the final ACK from the client yet. You'd see this on the server side only. 
    - ESTABLISHED. This means that the TCP connection is in working order, and both sides are free to send each other data. You'd see this state on both the client and server sides of the connection. This will be true of all the following socket states, too. So keep that in mind. 
    - FIN_WAIT. This means that a FIN has been sent, but the corresponding ACK from the other end hasn't been received yet. 
    - CLOSE_WAIT. This means that the connection has been closed at the TCP layer, but that the application that opened the socket hasn't released its hold on the socket yet. 
    - CLOSED. This means that the connection has been fully terminated, and that no further communication is possible.

### Connection-oriented and Connectionless Protocols
-  TCP is a connection-oriented protocol. A connection-oriented protocol is one that establishes a connection, and uses this to ensure that all data has been properly transmitted.
- At the IP or Ethernet level, if a checksum doesn't compute, all of that data is just discarded. It's up to TCP to determine when to resend this data
- TCP expects an ack for every bit of data it sends, it's in the best position to know what data successfully got delivered and can make the decision to resend a segment if needed.
- UDP, or User Datagram Protocol. Unlike TCP, UDP doesn't rely on connections, and it doesn't even support the concept of an acknowledgement. With UDP, you just set a destination port and send the packet.UDP, or User Datagram Protocol.

### Firewalls
-  A firewall is just a device that blocks traffic that meets certain criteria.
- Firewalls here is that they're most commonly used at the transportation layer.
- There are firewalls that can perform inspection of application layer traffic, and firewalls that primarily deal with blocking ranges of IP addresses.
- Firewalls that operate at the transportation layer will generally have a configuration that enables them to block traffic to certain ports while allowing traffic to other ports.

## The Application Layer

### The Application Layer
- For web traffic, the application layer protocol is known as HTTP.

### The Application Layer and the OSI Model
- The OSI or Open Systems Interconnection model has seven layers, and introduces two additional layers between our transport layer and our application layer.
- The fifth layer in the OSI model is the session layer. The concept of a session layer is that it's responsible for things like facilitating the communication between actual applications and the transport layer. It's the part of the operating system that takes the application layer data that's been unencapsulated from all the layers below it, and hands it off to the next layer in the OSI model, the presentation layer.
- The presentation layer is responsible for making sure that the unencapsulated application layer data is actually able to be understood by the application in question. This is the part of an operating system that might handle encryption or compression of data.

### All the Layers Working in Unison
- 







[Back to main](/README.md)








