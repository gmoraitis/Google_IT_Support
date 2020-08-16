## The Network Layer

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
- Next is the identification field(16bits) and its used to to group messeges together.If the total amount of data is larger than what can fit in asingle datagram,the IP layer needs to split the data  into many individual packets.In this case the identification field understands that every packete with the same value is part of the same splitted transmission.
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




















[Back to main](/README.md)