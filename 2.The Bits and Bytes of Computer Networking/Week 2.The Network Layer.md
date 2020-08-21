# The Network Layer

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