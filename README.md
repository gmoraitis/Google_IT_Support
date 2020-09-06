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

[Top](#Google-IT-Support)

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

[Top](#Google-IT-Support)

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

        
[Top](#Google-IT-Support)

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
- This is the exactly video script.
"Five Layer Network

Imagine three networks, network A will contain address space 10.1.1.0/24. Network B Will contain address space 192.168.1.0/24, and network C will be 172.16.1.0/24. Router A sits between network A and network B. With an interface configured with an IP of 10.1.1.1 on network A, and an interface at 192.168.1.254 on network B. There's a second router, router B, which connects networks B and C. It has an interface on network B with an IP address of 192.168.1.1, and an interface on network C with an IP address of 172.16.1.1. Now let's put a computer on one of the networks. Imagine it's a desktop, sitting on someone's desk at the workplace. It'll be our client in this scenario, and we'll refer to it as computer 1. It's part of Network A and has been assigned an IP address of 10.1.1.100. Now, let's put another computer on one of our other networks.

This one is a server in a data center, it'll act as our server in this scenario, and we'll refer to it as computer 2. It's part of network C, and has been assigned an IP address of 172.16.1.100, and has a web server listening on port 80. An end user sitting at computer 1 opens up a web browser and enters 172.16.1.100 into the address bar, let's see what happens. The web browser running on computer 1 knows it's been ordered to retrieve a web page from 172.16.1.100. The web browser communicates with the local networking stack, which is the part of the operating system responsible for handling networking functions. The web browser explains that it's going to want to establish a TCP connection to 172.16.1.100, port 80. The networking stack will now examine its own subnet. It sees that it lives on the network 10.1.1.0/24, which means that the destination 172.16.1.100 is on another network. At this point, computer 1 knows that it'll have to send any data to its gateway for routing to a remote network. And it's been configured with a gateway of 10.1.1.1. Next, computer 1 looks at its ARP table to determine what MAC address of 10.1.1.1 is, but it doesn't find any corresponding entry. Uh-oh, it's okay, computer A crafts an ARP request for an IP address of 10.1.1.1, which it sends to the hardware broadcast address of all Fs. This ARP discovery request is sent to every node on the local network.

When router A receives this ARP message, it sees that it's the computer currently assigned the IP address of 10.1.1.1. So it responds to computer 1 to let it know about its own MAC address of 00:11:22:33:44:55. Computer 1 receives this response and now knows the hardware address of its gateway. This means that it's ready to start constructing the outbound packet.

Computer 1 knows that it's being asked by the web browser to form an outbound TCP connection, which means it'll need an outbound TCP port. The operating system identifies the ephemeral port of 50000 as being available, and opens a socket connecting the web browser to this port.

Since this is a TCP connection, the networking stack knows that before it can actually transmit any of the data the web browser wants it to, it'll need to establish a connection. The networking stack starts to build a TCP segment. It fills in all the appropriate fields in the header, including a source port of 50000 and a destination port of 80. A sequence number is chosen and is used to fill in the sequence number field. Finally, the SYN flag is set, and a checksum for the segment is calculated and written to the checksum field.

Our newly constructed TCP segment is now passed along to the IP layer of the networking stack. This layer constructs an IP header. This header is filled in with the source IP, the destination IP, and a TTL of 64, which is a pretty standard value for this field.

Next, the TCP segment is inserted as the data payload for the IP datagram. And a checksum is calculated for the whole thing. Now that the IP datagram has been constructed, computer 1 needs to get this to its gateway, which it now knows has a MAC address of 00:11:22:33:44:55, so an Ethernet Datagram is constructed. All the relevant fields are filled in with the appropriate data, most notably, the source and destination MAC addresses.

Finally, the IP datagram is inserted as the data payload of the Ethernet frame, and another checksum is calculated.

Now we have an entire Ethernet frame ready to be sent across the physical layer.

The network interface connected to computer 1 sends this binary data as modulations of the voltage of an electrical current running across a CAT6 cable that's connected between it and a network switch.

This switch receives the frame and inspects the destination MAC address. The switch knows which of its interfaces this MAC address is attached to, and forwards the frame across only the cable connected to this interface.

At the other end of this link is router A, which receives the frame and recognizes its own hardware address as the destination.

Router A knows that this frame is intended for itself. So it now takes the entirety of the frame and calculates a checksum against it. Router A compares this checksum with the one in the Ethernet frame header and sees that they match. Meaning that all of the data has made it in one piece. Next, Router A strips away the Ethernet frame, leaving it with just the IP datagram. Again, it performs a checksum calculation against the entire datagram. And again, it finds that it matches, meaning all the data is correct. It inspects the destination IP address and performs a lookup of this destination in its routing table. Router A sees that in order to get data to the 172.16.1.0/24 network, the quickest path is one hop away via Router B, which has an IP of 192.168.1.1. Router A looks at all the data in the IP datagram, decrements the TTL by 1, calculates a new checksum reflecting that new TTL value, and makes a new IP datagram with this data.

Router B knows that it needs to get this datagram to router B, which has an IP address of 192.168.1.1. It looks at its ARP table, and sees that it has an entry for 192.168.1.1. Now router A can begin to construct an Ethernet frame with the MAC address of its interface on network B as the source. And the MAC address on router B's interface on network B as the destination. Once the values for all fields in this frame have been filled out, router A places the newly constructed IP datagram into the data payload field. Calculates a checksum, and places this checksum into place, and sends the frame out to network B.

Just like before, this frame makes it across network B, and is received by router B. Router B performs all the same checks, removes the the Ethernet frame encapsulation, and performs a checksum against the IP datagram.

It then examines the destination IP address. Looking at its routing table, router B sees that the destination address of computer 2, or 172.16.1.100, is on a locally connected network. So it decrements the TTL by 1 again, calculates a new checksum, and creates a new IP datagram. This new IP datagram is again encapsulated by a new Ethernet frame. This one with the source and destination MAC address of router B and computer 2. And the whole process is repeated one last time. The frame is sent out onto network C, a switch ensures it gets sent out of the interface that computer 2 is connected to. Computer 2 receives the frame, identifies its own MAC address as the destination, and knows that it's intended for itself. Computer 2 then strips away the Ethernet frame, leaving it with the IP datagram. It performs a CRC and recognizes that the data has been delivered intact. It then examines the destination IP address and recognizes that as its own.

Next, computer 2 strips away the IP datagram, leaving it with just the TCP segment. Again, the checksum for this layer is examined, and everything checks out. Next, computer 2 examines the destination port, which is 80. The networking stack on computer 2 checks to ensure that there's an open socket on port 80, which there is. It's in the listen state, and held open by a running Apache web server. Computer 2 then sees that this packet has the SYN flag set. So it examines the sequence number and stores that, since it'll need to put that sequence number in the acknowledgement field once it crafts the response.

After all of that, all we've done is get a single TCP segment containing a SYN flag from one computer to a second one. Everything would have to happen all over again for computer 2 to send a SYN-ACK response to computer 1. Then everything would have to happen all over again for computer 1 to send an ACK back to computer 2, and so on and so on."

[Top](#Google-IT-Support)
</details>

<details>
<summary>Week 4. Networking Services</summary>


## Introduction to Network Services
- At the end of the day, the main purpose of computer networking is so network services can be available to answer requests for the data from clients. The sheer number and variety of things that might comprise a network service makes it impossible to cover all of them.

## Name Resolution
### Why do we need DNS?
- IP address is really just a 32-bit binary number.
- MAC addresses are just 48-bit binary numbers that are normally written out in 6 groupings of 2 hexadecimal digits each.
- DNS, or domain name system, is a global and highly distributed network service that resolves strings of letters into IP address for you.
- The IP address for a domain name can also change all the time for a lot of different reasons. A domain name is just the term we use for something that can be resolved by DNS.
- So, not only does DNS make it easier for humans to remember how to get to a website, It also lets administrative changes happen behind the scenes without an end user having to change their behavior.
- Because of its global structure, DNS lets organizations decide, if you're in the region, resolve the domain name to this IP. If you're in this other region, resolve this domain to this other IP.

### The Many Steps of Name Resolution
- DNS is a system that converts domain names into IP addresses.
- This process of using DNS to turn a domain name into an IP address is known as name resolution.
- DNS servers, are one of the things that need to be specifically configured at a node on a network.
- The standard modern network configuration needs
    - MAC addresses are hard coded and tied to specific pieces of hardware.
    - IP address, subnet mask, and gateway.
    - a DNS server, is the fourth and final part of the standard modern network configuration.
- There are five primary types of DNS servers.
    - Caching Name servers
    - Recursive Name servers, 
    - Root Name servers, 
    - TLD Name servers,
    - Authoritative Name servers.
- Caching and recursive name servers are generally provided by an ISP or your local network.
    - Their purpose is to store domain name lookups for a certain amount of time.
    -  ISP or local network will generally have a caching name server available. Most caching name servers are also recursive name servers. Recursive name servers are ones that perform full DNS resolution requests.
    - **EXAMPLE**: You and your friend are both connected to the same network and you both want to check out Facebook.com, your friend enters www.facebook.com into a web browser, which means that their computer now needs to know the IP of www.facebook.com in order to establish a connection. Both of your computers are on the same network which usually means, that they both been configured with the same name server. So your friends computer ask the name server for the IP of www.facebook.com which it doesn't know, this name server now performs a fully recursive resolution to discover the correct IP for www.facebook.com. This involves a bunch of steps we'll cover in just a moment. This IP is then both delivered to your friend's computer and stored locally in a cache. A few minutes later you enter www.facebook.com into a web browser. Again, your computer needs to know the IP for this domain, so your computer asks the local name server it's been configured with, which is the same one your friend's computer was just talking to. Since the domain name www.Facebook.com had just been looked up, the local name server still has the IP that it resolved to stored and is able to deliver that back to your computer without having to perform a full lookup. **Caching** This is how the same servers act as a caching server. All domain names in the global DNS system have a **TTL or time to live. This is a value in seconds, that can be configured by the owner of a domain name for how long a name server is allowed to cache in entry before it should discard it and perform a full resolution again.** 
    Several years ago, it was normal for these TTL's to be really long, sometimes a full day or more. This is because the general bandwidth available on the Internet was just much less, so network administrators didn't want to waste what bandwidth was available to them by constantly performing full DNS lookups. As the Internet has grown and gone faster, these TTL's for most domains have dropped to anywhere from a few minutes to a few hours. But it's important to know that sometimes you still run into a domain names with very lengthy TTL's, it means that it can take up to the length of a total TTL for a change in DNS record to be known to the entire Internet. 
    Now, let's look at what happens when your local recursive server needs to perform a full recursive resolution. The first step is always to contact a root named server, there are **13 total root name servers** and they're responsible for directing queries toward the appropriate TLD name server.
    In the past, these 13 root servers were distributed to very specific geographic regions, but today, they're mostly distributed across the globe via anycast. **Anycast is a technique that's used to route traffic to different destinations depending on factors like location, congestion, or link health. Using anycast, a computer can send a data gram to a specific IP but could see it routed to one of many different actual destinations depending on a few factors.** This should also make it clear that there aren't really only 13 physical route name servers anymore. It's better to think of them as **13 authorities** that provide route name lookups as a service. The root servers will respond to a DNS lookup with the TLD name server that should be queried. **TLD stands for top level domain and represents the top of the hierarchical DNS name resolution system. A TLD is the last part of any domain name, using www.facebook.com as an example again, the dot com portion should be thought of as the TLD.** We'll go into more details about the different components of a domain name in an upcoming lesson. For each TLD in existence, there is a TLD name server, but just like with root servers, this doesn't mean there's only physically one server in question, it's most likely a global distribution of any cast accessible servers responsible for each TLD. The TLD name servers will respond again with a redirect, this time informing the computer performing the name lookup with what authoritative name server to contact. Authoritative name servers are responsible for the last two parts of any domain name which is the resolution at which a single organization may be responsible for DNS lookups. Using www.weather.com as an example, the TLD name server would point a lookup at the authoritative server for Weather.com, which would likely be controlled by the Weather Channel, the organization itself that runs the site. Finally, the DNS lookup could be redirected at the authoritative server for weather.com which would finally provide the actual IP of the server in question. This strict hierarchy is very important to the stability of the internet, making sure that all full DNS resolutions go through a strictly regulated and controlled series of lookups to get the correct responses, is the best way to protect against malicious parties redirecting traffic. Your computer will blindly send traffic to whatever IP it's told to. So by using a hierarchical system controlled by trusted entities in the way DNS does, we can better ensure that the responses to DNS lookups are accurate. Now that you see how many steps are involved, it should make sense why we trust our local name servers to cache DNS lookups, its so that full lookup path doesn't have to happen for every single TCP connection. In fact, your local computer from your phone to a desktop will generally have its own temporary DNS cache as well, that way, it doesn't have to bother its local name server for every TCP connection either.

### DNS and UDP
- DNS is a great example of an application layer service that uses UDP for the transport layer instead of TCP.
- The biggest difference between TCP and UDP is that UDP is connectionless.DNS with UDP takes fewer steps than TCP.
- DNS traffic is just a precursor to actual traffic.
- *EXAMPLE WITH UDP* The original computer sends a UDP packet to its local name server on port 53 asking for the IP for food.com, that's one packet. The local name server acts as a recursive server and sends up a UDP packet to the root server which sends a response containing the proper TLD name server, that's three packets. The recursive name server sends a packet to the TLD server and receives back a response containing the correct authoritative server. We're now at five packets. Next, the recursive name server sends its final request to the authoritative name server which sends a response containing the IP for food.com. That's seven packets. Finally, the local name server responds to the DNS resolver that made the request in the first place with the IP for food.com. That brings us to a grand total of eight packets. See, way less packets. You can see now how much overhead TCP really requires. And for something as simple as DNS, it's just not needed. It's the perfect example for why protocols like UDP exist in addition to the more robust TCP. You might be wondering how error recovery plays into this, since UDP doesn't have any. The answer is pretty simple. The DNS resolver just asks again if it doesn't get a response. Basically, the same functionality that TCP provides at the transport layer is provided by DNS at the application layer in the most simple manner. A DNS server never needs to care about doing anything but responding to incoming lookups, and a DNS resolver simply needs to perform lookups and repeat them if they don't succeed. A real showcase of the simplicity of both DNS and UDP. I should call out that DNS over TCP does in fact exist and is also in use all over. As the Web has gotten more complex, it's no longer the case that all DNS lookup responses can fit in a single UDP datagram. In these situations, a DNS name server would respond with a packet explaining that the response is too large. The DNS client would then establish a TCP connection in order to perform the lookup.

## Name Resolution in Practice
### Resource Record Types
- DNS is one of the most important technologies that an IT support specialist needs to know in order to troubleshoot networking issues.
- DNS in practice operates with a set of defined resource record types. These allow for different kinds of DNS resolutions to take place.
- The most common resource record is known as an A record. An A record is used to point a certain domain name at a certain IPv4 IP address.A single A record is configured for a single domain name. But, a single domain name can have multiple A records, too. This allows for a technique known as DNS round robin to be used to balance traffic across multiple IPs. Round robin is a concept that involves iterating over a list of items one by one in an orderly fashion. The hope is that this ensures a fairly equal balance of each entry on the list that's selected. Let's say we're in charge of a domain name www.microsoft.com. Microsoft is a large company and their website likely sees a lot of traffic. To help balance this traffic across multiple servers. We configure four A records for www.microsoft.com at the authoritative name server for the microsoft.com domain. We'll use the IPs 10.1.1.1, 10.1.1.2, 10.1.1.3, and 10.1.1.4. When the DNS Resolver performs a look-up of www.microsoft.com, all four IPs would be returned in the order first configured: 10.1 1.1, followed by 10.1.1.2, followed by 10.1.1.3, and finally, 10.1.1.4. The DNS resolving computer would know that it should try to use the first entry, 10.1.1.1, but it knows about all four just in case a connection to 10.1.1.1 fails. The next computer to perform a look up for www.microsoft.com would also receive all four IPs in the response, but the ordering will have changed. The first entry would be 10.1.1.2, followed by 10.1.1.3, followed by 10.1.1,4, and finally, 10.1.1.1 would be last on that list. This pattern will continue for every DNS resolution attempt, cycling through all of the A records configured and balancing the traffic across these IPs. That's the basics of how DNS round robin logic works. 
- Another resource record type that's becoming more and more popular is the Quad A record. A Quad A record is very similar to an A record except that it returns in IPv6 address instead of an IPv4 address.
- The CNAME record is also super common. A CNAME record is used to redirect traffic from one domain to another. Let's say that Microsoft runs their web servers at www.microsoft.com. They also want to make sure that anyone that enters just microsoft.com into their web browser will get properly redirected. By configuring a CNAME record for microsoft.com that resolves to www.microsoft.com, the resolving client would then know to perform another resolution attempt, this time for www.microsoft.com, and then use the IP returned by that second attempt.
- CNAMEs are really useful because they ensure you only have to change the canonical IP address of a server in one place. In fact, CNAME is just shorthand for canonical name.
- Another important resource record type is the MX record. MX stands for mail exchange and this resource record is used in order to deliver e-mail to the correct server. Many companies run their web and mail servers on different machines with different IPs, so the MX record makes it easy to ensure that email gets delivered to a company's mail server, while other traffic like web traffic would get delivered to their web server. 
- A record type very similar to the MX record is the SRV record. SRV stands for service record, and it's used to define the location of various specific services. It serves the exact same purpose as the MX resource record type except for one thing, while MX is only for mail services, an SRV record can be defined to return the specifics of many different service types. For example, SRV records are often used to return the records of services like CalDAV, which has a calendar and scheduling service. The text record type is an interesting one. 
- TXT stands for text and was originally intended to be used only for associating some descriptive text with a domain name for human consumption. The idea was that, you could leave notes or messages that humans could discover and read to learn more about arbitrary specifics of your network. But over the years as the Internet and services that run on it have become more and more complex, the text record has been increasingly used to convey additional data intended for other computers to process. Since the text record has a field that's entirely free form, clever engineers have figured out ways to use it to communicate data not originally intended to be communicated by a system like DNS. It's pretty clever, right? This text record is often used to communicate configuration preferences about network services that you've entrusted other organizations to handle for your domain. For example, it's common for the text record to be used to convey additional info to an email as a service provider, which is a company that handles your email delivery for you.

### Anatomy of a Domain Name
- Any given domain name has three primary parts, and they all serve specific purposes. Let's take the domain name www.google.com, the three part here should be pretty easy to spot since they're each set off from each other by a period. They're www, google, and com, the last part of a domain name is known as the TLD or Top Level Domain. In this case it's the .com portion of the domain name. There are only a certain restricted number of defined TLDs available, although that number has been growing a lot in recent years. The most common TLDs are ones you're probably already familiar with .com, .net, .edu and so on. You've probably also seen some country specific TLDs such as .de for Germany or .cn for China. Due to the growth of the Internet, many of the TLDs originally defined have become very crowded. So today, a number of vanity TLDs are available, everything from .museum to .pizza. Administration and definition of TLDs is handled by a non-profit organization known as ICANN, or the Internet Corporation for Assigned Names and Numbers and I can tell you what they do.
- ICANN is a sister organization to the IANA, and together they help define and control both the global IP spaces, along with the global DNS system.
- A domain is the name commonly used to refer to the second part of a domain name, which would be, google in our example. Domains are used to demarcate where control moves from a TLD name server, to an authoritative name server. This is typically under the control of an independent organization, or someone outside of ICANN. Domains can be registered and chosen by any individual or company, but they must all end in one of the predefined TLEs.
- That www portion of this is known as the subdomain, sometimes referred to as a host name if it's been assigned to only one host. When you combine all these parts together, you have what's known as a fully qualified domain name, or FQDN.
- While it costs money to officially register a domain with a registrar, subdomains can be freely chosen and assigned by anyone who controls such a registered domain. A registrar is just a company that has an agreement with ICANN to sell unregistered domain names.Technically you can have lots of subdomain names, for example host.sub.sub.subdomain.domain.com can be completely valid. Although you rarely see fully qualified domain names with that many levels. DNS can technically support up to 127 levels of domain in total for a single fully qualified domain name.
- There are some other restrictions in place for how your domain name can be specified. Each individual section can only be 63 characters long and a complete FQDN is limited to a total of 255 characters

### DNS Zones
- An authoritative name server is actually responsible for a specific DNS zone. DNS zones are a hierarchical concept. The root name servers we covered earlier are responsible for the root zone. Each TLD name server is responsible for the zone covering its specific TLD, and what we refer to as authoritative name servers are responsible for some even finer-grained zones underneath that. The root and TLD name servers are actually just authoritative name servers, too. It's just that the zones that they're authoritative for are special cases. I should call out that zones don't overlap. 
- For example, the administrative authority of the TLD name server for the.com TLD doesn't encompass the google.com domain. Instead, it ends at the authoritative server responsible for google.com. The purpose of DNS zones is to allow for easier control over multiple levels of a domain. As the number of resource records in a single domain increases, it becomes more of a headache to manage them all. Network administrators can ease this pain by splitting up their configurations into multiple zones. 
- Let's imagine a large company that owns the domain largecompany.com. This company has offices in Los Angeles, Paris, and Shanghai, very cosmopolitan. Let's say each office has around 200 people with their own uniquely named desktop computer. This would be 600 A records to keep track of if it was all configured as a single zone. What the company could do, instead, is split up each office into their own zone. So now, we could have la.largecompany.com, pa.largecompany.com, and sh.largecompany.com as subdomains, each with their own DNS zones. A total of four authoritative name servers would now be required for the setup, one for largecompany.com and one for each of the subdomains. 
- Zones are configured through what are known as zone files, simple configuration files that declare all resource records for a particular zone. So a zone file has to contain an SOA, or a Start of Authority resource record declaration. 
- This SOA record declares the zone and the name of the name server that is authoritative for it. Along with the SOA record, you'll usually find NS records which indicate other name servers that may also be responsible for this zone. For simplicity's sake, we've been referring to server in the singular when discussing what's responsible for its zone, whether at the root, TLD, or domain level, but there are often going to be multiple physical servers with their own FQDNs and IP addresses involved. Having multiple servers in place for something as important as DNS is pretty common. Why? Well, if one server were to have a problem or suffer a hardware failure, you could always rely on one of the other ones to serve DNS traffic. Besides SOA and NS records, you'll also find some or all of the other resource record types we've already covered, like A, quad A, and CNAME records along with configurations such as default TTL values for the records served by this zone. Just like how subdomains can go many, many layers deep, zones can be configured to do this too but, just like with subdomains, it's rare to see zones deeper than just a few levels. Sometimes, you'll also see what are known as reverse lookup zone files. These let DNS resolvers ask for an IP, and get the FQDN associated with it returned. These files are the same as zone files except, instead of A and quad A records, which resolve names to IPs, you'll find mostly pointer resource record declarations. As you might have guessed, a PTR, or Pointer Record, resolves an IP to a name.

## Dynamic Host Configuration Protocol
### Overview of DHCP
- Every single computer on a modern TCP/IP based network needs to have at least four things specifically configured. An IP address, the subnet mask for the local network, a primary gateway and a name server. On their own, these four things don't seem like much, but when you have to configure them on hundreds of machines it becomes super tedious. Out of these four things, three are likely the same on just about every node on the network. The subnet mask, the primary gateway, and DNS server. But the last item an IP address needs to be different on every single node on the network. That could require a lot of tricky configuration work, and this is where DHCP or Dynamic Host Configuration Protocol comes into play.

- DHCP is an application layer protocol that automates the configuration process of hosts on a network. With DHCP, a machine can query a DHCP server when the computer connects to the network and receive all the networking configuration in one go. Not only does DHCP reduce the administrative overhead of having to configure lots of network devices on a single network, it also helps address the problem of having to choose what IP to assign to what machine. Every computer on a network requires an IP for communications, but very few of them require an IP that would be commonly known. For servers or network equipment on your network, like your gateway router, a static and known IP address is pretty important. For example, the devices on a network need to know the IP of their gateway at all time. If the local DNS server was malfunctioning, network administrators would still need a way to connect to some of these devices through their IP. Without a static IP configured for a DNS server, it would be hard to connect to it to diagnose any problems if it was malfunctioning. But for a bunch of client devices like desktops or laptops or even mobile phones, it's really only important that they have an IP on the right network. It's much less important exactly which IP that is. Using DHCP you can configure a range of IP addresses that's set aside for these client devices. This ensures that any of these devices can obtain an IP address when they need one. But solves the problem of having to maintain a list of every node on the network and its corresponding IP.

- There are a few standard ways that DHCP can operate. DHCP dynamic allocation, is the most common, and it works how we described it just now. A range of IP addresses is set aside for client devices and one of these IPs is issued to these devices when they request one. Under a dynamic allocation the IP of a computer could be different almost every time it connects to the network. Automatic allocation is very similar to dynamic allocation, in that a range of IP addresses is set aside for assignment purposes. The main difference here is that, the DHCP server is asked to keep track of which IPs it's assigned to certain devices in the past. Using this information, the DHCP server will assign the same IP to the same machine each time if possible. Finally, there's what's known as fixed allocation. Fixed allocation requires a manually specified list of MAC address and their corresponding IPs. When a computer requests an IP, the DHCP server looks for its MAC address in a table and assigns the IP that corresponds to that MAC address. If the MAC address isn't found, the DHCP server might fall back to automatic or dynamic allocation, or it might refuse to assign an IP altogether. This can be used as a security measure to ensure that only devices that have had their MAC address specifically configured at the DHCP server will ever be able to obtain an IP and communicate on the network. It's worth calling out that DHCP discovery can be used to configure lots of things beyond what we've touched down here. Along with things like IP address, an primary gateway, you could also use DHCP to assign things like NTP servers. NTP stands for Network Time Protocol and is used to keep all computers on a network synchronized in time. We'll cover it in more detail in later courses, but for now it's just worth knowing that DHCP can be used for more than just IP, subnet mask, gateway and DNS server.

### DHCP in Action

- DHCP is an application layer protocol, which means it relies on the transport, network, data link and physical layers to operate. But you might have noticed that the entire point of DHCP is to help configure the network layer itself.
- The process by which a client configured to use DHCP attempts to get network configuration information is known as DHCP discovery. The DHCP discovery process has four steps. First, we have the server discovery step. The DHCP clients sends what's known as a DHCP discover message out onto the network. Since the machine doesn't have an IP and it doesn't know the IP of the DHCP server, a specially crafted broadcast message is formed instead. DHCP listens on UDP port 67 and DHCP discovery messages are always sent from UDP port 68. So the DHCPDISCOVER message is encapsulated in a UDP datagram with a destination port of 67 and a source port of 68. This is then encapsulated inside of an IP datagram with a destination IP of 255.255.255.255, and a source IP of 0.0.0.0. This broadcast message would get delivered to every node on the local area network. And if a DHCP server is present, it would receive this message. Next, the DHCP server would examine its own configuration and would make a decision on what, if any, IP address to offer to the client. This would depend on if it's configured to run with dynamic, automatic or fixed address allocation. The response would be sent as a DHCPOFFER message with a destination port of 68, a source port of 67, a destination broadcast IP of 255.255.255.255, and its actual IP as the source.

- Since the DHCP offer is also a broadcast, it would reach every machine on the network. The original client would recognize that this message was intended for itself. This is because the DHCPOFFER has the field that specifies the MAC address of the client that sent the DHCPDISCOVER message. The client machine would now process this DHCPOFFER to see what IP is being offered to it. Technically, a DHCP client could reject this offer. It's totally possible for multiple DHCP servers to be running on the same network, and for a DHCP client to be configured to only respond to an offer of an IP within a certain range. But this is rare.

- More often, the DHCP client would respond to the DHCPOFFER message with a DHCPREQUEST message. This message essentially says, yes, I would like to have an IP that you offer to me. Since the IP hasn't been assigned yet, this is again sent from an IP of 0.0.0.0, and to the broadcast IP of 255.255.255.255. Finally, the DHCP server receives the DHCPREQUEST message and responds with a DHCPACK or DHCP acknowledgement message. This message is again sent to a broadcast IP of 255.255.255.255, and with a source IP corresponding to the actual IP of the DHCP server. Again, the DHCP client would recognize that this message was intended for itself by inclusion of its MAC address in one of the message fields. The networking stack on the client computer can now use the configuration information presented to it by the DHCP server to set up its own network layer configuration.

- At this stage, the computer that's acting as the DHCP client should have all the information it needs to operate in a full fledged manner on the network it's connected to.

- All of this configuration is known as DHCP lease as it includes an expiration time. A DHCP lease might last for days or only for a short amount of time. Once a lease has expired, the DHCP client would need to negotiate a new lease by performing the entire DHCP discovery process all over again. A client can also release its lease to the DHCP server, which it would do when it disconnects from the network. This would allow the DHCP server to return the IP address that was assigned to its pool of available IPs.

## Network Address Translation or NAT
### Basics of NAT
- Unlike protocols like DNS and DHCP, network address translation or NAT, is a technique instead of a defined standard.
- Different operating systems and different network hardware vendors have implemented the details of NAT in different ways, but the concepts of what it accomplishes are pretty constant. 
- Network address translation does pretty much what it sounds like, it takes one IP address and translates it into another. There are lots of reasons why you would want to do this. They range from security safeguards to preserving the limited amounts of available IPv4 space.
- At its most basic level, NAT is a technology that allows a gateway, usually a router or firewall, to rewrite the source IP of an outgoing IP datagram while retaining the original IP in order to rewrite it into the response.
- Let's say we have two networks. Network A consists of the 10.1.1.0/24 address space and network B consists of the 192.168.1.0/24 address space. Sitting between these networks is a router that has an interface on network A with an IP of 10.1.1.1 and an interface on network B of 192.168.1.1. Now, let's put two computers on these networks. Computer 1 is on network A and has an IP of 10.1.1.100. And computer 2 is on network B and has an IP of 192.168.1.100. Computer 1 wants to communicate with a web server on computer 2. So it crafts the appropriate packet at all layers and sends this to its primary gateway, the router sitting between the two networks. So far, this is a lot like many of our earlier examples, but in this instance, the router is configured to perform NAT for any outbound packets. Normally, a router will inspect the contents of an IP datagram, decrement the TTL by 1, re-calculate the checksum, and forward the rest of the data at the network layer without touching it. But with NAT, the router will also rewrite the source IP address, which in this instance, becomes the router's IP on network B or 192.168.1.1. When the datagram gets to computer 2, it'll look like it originated from the router, not from computer 1.
Now, computer 2 crafts its response and sends it back to the router. The router, knowing that this traffic is actually intended for computer 1, rewrites the destination IP field before forwarding it along. What NAT is doing in this example, is hiding the IP of computer 1 from computer 2. This is known as IP masquerading. IP masquerading is an important security concept. The most basic concept at play here is that no one can establish a connection to your computer if they don't know what IP address it has. By using NAT in the way we've just described, we could actually have hundreds of computers on network A, all of their IPs being translated by the router to its own. To the outside world, the entire address space of network A is protected and invisible. This is known as one-to-many NAT, and you'll see it in use on lots of LANs today.

### NAT and the Transport Layer
- NAT at the network layer is pretty easy to follow. One IP address is translated to another by a device usually a router. But at the transport layer things get a little bit more complicated and several additional techniques come into play to make sure everything works properly. With one to many NAT, we've talked about how hundreds even thousands of computers can all have their outbound traffic translated via NAT to a single IP. This is pretty easy to understand when the traffic is outbound, but a little more complicated once return traffic is involved. We now have potentially hundreds of responses all directed at the same IP and the router at this IP needs to figure out which responses go to which computer. The simplest way to do this, is through port preservation. 
- Port preservation is a technique where the source port chosen by a client, is the same port used by the router. Remember that outbound connections choose a source port at random, from the ephemeral ports or the ports in the range 49,152 through 65, 535. In the simplest setup, a router setup to NAT outbound traffic, will just keep track of what this source port is, and use that to direct traffic back to the right computer. Let's imagine a device with an IP of 10.1.1.100. It wants to establish an outbound connection and the networking stack of the operating system chooses port 51,300 for this connection. Once this outbound connection gets to the router, it performs network address translation and places its own IP in the source address field of the IP datagram, but it leaves the source port in the TCP datagram the same and stores this data internally in a table. Now, when traffic returns to the router and port 51,300, it knows that this traffic needs to be forwarded back to the IP 10.1.1.100. Even with how large the set of ephemeral ports is, it's still possible for two different computers on a network to both choose the same source port around the same time. When this happens, the router normally selects an unused port at random to use instead. Another important concept about NAT and the transport layer, is port forwarding. 
- Port forwarding is a technique where a specific destination ports can be configured to always be delivered to specific nodes. This technique allows for complete IP masquerading, while still having services that can respond to incoming traffic. Let's use our network 10.1.1.0 \24 again to demonstrate this. Let's say there's a web server configured with an IP of 10.1.1.5. With port forwarding, no one would even have to know this IP. Prospective web clients would only have to know about the external IP of the router. Let's say it's 192.168.1.1. Any traffic directed at port 80 on 192.168.1.1, would get automatically forwarded to 10.1.1.5. Response traffic would have the source IP rewritten to look like the external IP of the router. This technique not only allows for IP masquerading, it also simplifies how external users might interact with lots of services all run by the same organization. Let's imagine a company with both a web server and mail server, both need to be accessible to the outside world but they run on different servers with different IPs. Again, let's say the web server has an IP of 10.1.1.5, and the mail server has an IP of 10.1.1.6. With port forwarding, traffic for either of these services could be aimed at the same external IP and therefore the same DNS name, but it would get delivered to entirely different internal servers due to their different destination ports.

### NAT, Non-Routable Address Space and the Limits of IPv4
- The IANA has been in charge of distributing IP addresses since 1988. Since that time, the internet has expanded at an incredible rate. The 4.2 billion possible IPv4 addresses have been predicted to run out for a long time and they almost have.

- For some time now, the IANA has primarily been responsible with assigning address blocks to the five regional internet registries or RIRs. The five RIRs are AFRINIC, which serves the continent of Africa, ARIN which serves the United States, Canada and parts of the Caribbean. APNIC, which is responsible for most of Asia, Australia and New Zealand and Pacific Island nations. LACNIC which covers Central and South America and any parts of the Caribbean not covered by ARIN. And finally RIPE, which serves Europe, Russia and the Middle East and portions of Central Asia. These five RIRs have been responsible for assigning IP address blocks to organizations within their geographic areas and most have already run out. The IANA assigned the last unallocated slash eight network blocks to various RIRs on February 3rd, 2011. Then in April 2011, APNIC ran out of addresses. RIPE was next, in September of 2012. LACNIC ran out of addresses to assign in June 2014. And ARIN did the same in September 2015. Only AFNIC has some IPs left, but those are predicted to be depleted by 2018.

- NAT and non-routable address space. Remember that non-routable address space was defined in RFC1918 and consists of several different IP ranges that anyone can use. And unlimited number of networks can use non-routable address space internally because internet routers won't forward traffic to it. This means there's never any global collision of IP addresses when people use those address spaces. Non-routable address space is largely usable today because of technologies like NAT. With NAT, you can have hundreds even thousands of machines using non-routable address space. Yet, with just a single public IP, all those computers can still send traffic to and receive traffic from the internet. All you need is one single IPv4 address and via NAT, a router with that IP can represent lots and lots of computers behind it. It's not a perfect solution, but until IPv6 becomes more globally available, non-routable address space and NAT will have to do.

## VPN'S and Proxies
### Virtual Private Networks
- Businesses have lots of reasons to want to keep their network secure, and they do this by using some of the technologies we've already discussed firewalls, Nat, use of non routable address space, things like that. Organizations often have proprietary information that needs to remain secure. Network services that are only intended for employees to access and other things. One of the easiest ways to keep network secure is to use various securing technologies, so only devices physically connected to their local area network can access these resources. But employees aren't always in the office. They might be working from home or on a business trip, and they might still need access to these resources in order to get their work done. That's where VPNs come in. Virtual private networks or VPNs are a technology that allows for the extension of a private or local network to host that might not work on that same local network. 
- VPNs come in many flavors and accomplish lots of different things. But the most common example of how VPNs are used is for employees to access their business's network when they're not in the office. VPNs are a tunneling protocol, which means they provision access to something not locally available. When establishing a VPN connection, you might also say that a VPN tunnel has been established. Let's go back to the example of an employee who needs to access company resources while not in the office. The employee could use a VPN client to establish a VPN tunnel to their company network. This would provision their computer with what's known as a virtual interface with an IP that matches the address space of the network they've established a VPN connection to. By sending data out of this virtual interface, the computer could access internal resources just like if it was physically connected to the private network. Most VPNs work by using the payload section of the transport layer to carry an encrypted payload that actually contains an entire second set of packets. The network, the transport and the application layers of a packet intended to traverse the remote network.

- Basically, this payload is carried to the VPNs end point where all the other layers are stripped away and discarded. Then the payload is unencrypted, leaving the VPN server with the top three layers of a new packet. This gets encapsulated with the proper data link layer information and sent out across the network. This process is completed in the inverse, in the opposite direction. VPNs usually requires strict authentication procedures in order to ensure that they can only be connected to by computers and users authorized to do so. In fact, VPNs were one of the first technologies where two-factor authentication became common. Two-factor authentication is a technique where more than just a username and password are required to authenticate. Usually a short lived numerical token is generated by the user through a specialized piece of hardware or software. VPNs can also be used to establish site to site connectivity. Conceptually, there isn't much difference between how this works compared to our remote employees situation. It's just that the router, or sometimes a specialized VPN device on one network establishes the VPN tunnel to the router or VPN device on another network. This way two physically separated offices might be able to act as one network and access network resources across the tunnel. It's important to call out that, just like Nat, VPNs are a general technology concept, not a strictly defined protocol. There are lots of unique implementations of VPNs, and the details of how they all work can differ a ton. The most important takeaway is that VPNs are a technology that use encrypted tunnels to allow for a remote computer or network to act as if it's connected to a network that it's not actually physically connected to.

### Proxy Services
- A proxy service is a server that acts on behalf of a client in order to access another service. Proxies sit between clients and other servers, providing some additional benefit, anonymity, security, content filtering, increased performance, a couple other things. If any part of this sounds familiar, that's good. - A gateway definitely meets the definition of what a proxy is and how it works. The concept of a proxy is just that, a concept or an abstraction. It doesn't refer to any specific implementation.Proxies exist at almost every layer of our networking model.

- Most often, you'll hear the term, proxy, used to refer to web proxies. As you might guess, these are proxies specifically built for web traffic. A web proxy can serve lots of purposes. Many years ago, when most Internet connections were much slower than they are today, lots of organizations used web proxies for increased performance. Using a web proxy, an organization would direct all web traffic through it, allowing the proxy server itself to actually retrieve the webpage data from the Internet. It would then cache this data. This way, if someone else requested the same webpage, it could just return the cached data instead of having to retrieve the fresh copy every time.

- This kind of proxy is pretty old and you wont often find them in use today, why? Well, for one thing, most organizations now have connections fast enough that caching individual webpages doesn't provide much benefit. Also, the Web has become much more dynamic. Going to www.twitter.com is going to look different to every person with their own Twitter account, so caching this data wouldn't do much good.

- A more common use of a web proxy today might be to prevent someone from accessing sites, like Twitter, entirely. A company might decide that accessing Twitter during work hours reduces productivity. By using a web proxy, they can direct all web traffic to it, allow the proxy to inspect what data is being requested, and then allow or deny this request, depending on what site is being accessed. Another example of a proxy is a reverse proxy. A reverse proxy is a service that might appear to be a single server to external clients, but actually represents many servers living behind it. A good example of this is how lots of popular websites are architected today. Very popular websites, like Twitter, receive so much traffic that there's no way a single web server could possibly handle all of it. A website that popular might need many, many web servers in order to keep up with processing all incoming requests.

- A reverse proxy, in this situation, could act as a single front-end for many web servers living behind it. From the clients' perspective, it looks like they're all connected to the same server. But behind the scenes, this reverse proxy server is actually distributing these incoming requests to lots of different physical servers. Much like the concept of DNS Round Robin, this is a form of load balancing.

- Another way that reverse proxies are commonly used by popular websites is to deal with decryption. More than half of all traffic on the Web is now encrypted, and encrypting and decrypting data is a process that can take a lot of processing power. You'll learn a lot more about encryption and how it works in another course in this program.

- Reverse proxies are now implemented in order to use hardware built specifically for cryptography, to perform the enryption and decryption work. So that the web servers are free to just serve content.

- Proxies come in many other flavors, way too many for us to cover them all here. But the most important takeaway is that proxies are any server that act as a intermediary between a client and another server. 


[Top](#Google-IT-Support)
</details>









