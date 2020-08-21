# The Transport and Application Layers

## Introduction to the Transport and Application Layers
- Transport layer allows traffic to be directed to specific network applications
- Application layer allows these applications to communicate in a way they understand.

## The Transport Layer
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









[Back to main](/README.md)