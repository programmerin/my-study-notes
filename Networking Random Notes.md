# CIDR

CIDR (Classless Inter-Domain Routing) is a method used to assign IP addresses and define network masks (subnets) in IP routing. It allows for more efficient use of IP addresses by allowing for variable-length subnet masks (VLSMs), which means that the number of bits used to identify the network portion of an IP address can be different depending on the size of the network.

The CIDR notation is used to specify the IP address range and the subnet mask of a network, and it is represented in the format of IP address/subnet mask length. For example, "192.168.1.0/24" is a CIDR notation that defines a network with the IP address range of "192.168.1.0" to "192.168.1.255" and the subnet mask of 255.255.255.0.

Here are some examples of CIDR notation:

- "192.168.1.0/24" - This notation defines a network with 256 IP addresses (from "192.168.1.0" to "192.168.1.255") and a subnet mask of 255.255.255.0

- "172.16.0.0/16" - This notation defines a network with 65,536 IP addresses (from "172.16.0.0" to "172.16.255.255") and a subnet mask of 255.255.0.0

- "10.0.0.0/8" - This notation defines a network with 16,777,216 IP addresses (from "10.0.0.0" to "10.255.255.255") and a subnet mask of 255.0.0.0

CIDR notation is a more efficient way to assign IP addresses and subnet masks, as it allows for smaller and more specific networks, which results in better use of IP address space. This is important in today's world as the internet is growing and IP addresses are becoming scarce.

It is worth mentioning that CIDR notation is not only used for IPv4 addresses but also for IPv6 addresses, it's the same concept of variable-length subnetting but with IPv6 the subnet mask is represented in a different format (prefix length) instead of the traditional dot-decimal notation.

---

# IP Routing

IP routing is the process of forwarding data packets from one network to another based on their IP addresses. It is a fundamental aspect of internetworking and is used to determine the best path for data to travel from its source to its destination.

When a device, such as a computer or a router, receives a data packet, it checks the destination IP address and compares it to the entries in its routing table. The routing table is a collection of information that defines the networks that the device is aware of and the best path to reach each network.

For example, if a data packet is sent from a computer with IP address 192.168.1.100 to a computer with IP address 192.168.2.200, the router will look at the routing table and find the best path to reach the destination network. The router will then forward the data packet to the next hop, which is the next device on the path to the destination network. This process continues until the data packet reaches its destination.

There are different types of routing protocols that can be used to determine the best path for data to travel. Some examples include:

- Routing Information Protocol (RIP) and Open Shortest Path First (OSPF) are examples of distance-vector routing protocols. These protocols determine the best path by measuring the distance (or "cost") to a destination network.

- Border Gateway Protocol (BGP) is an example of a path-vector routing protocol. BGP is used to route data packets between different autonomous systems (AS) on the Internet.

- Link-State Routing Protocols (LSRP) like IS-IS, OSPF are the routing protocols that use the link state information to determine the shortest path to a destination.

Each of these routing protocols have their own advantages and disadvantages, and the choice of which one to use will depend on the specific requirements of a network.

For example, a small network with only a few devices might use the Routing Information Protocol (RIP) while a large enterprise network would use Open Shortest Path First (OSPF) due to its scalability and support for VLSM.

In summary, IP routing is the process of forwarding data packets based on their IP addresses, using a routing table and routing protocols. It is a fundamental aspect of internetworking and enables communication between different networks.

---

# Network Interface Card (NIC)

A Network Interface Card (NIC) is a hardware component that connects a computer to a network. It is responsible for transmitting and receiving data between the computer and the network. In terms of the OSI (Open Systems Interconnection) model, the NIC operates at the Data Link Layer (layer 2).

The NIC has a unique Media Access Control (MAC) address that is assigned to it at the time of manufacture. This MAC address is used to identify the NIC on the network and is used by the Data Link Layer protocols to send and receive data.

When a computer wants to send data to another device on the network, it <span style="color:#d19a66">**first sends the data to the NIC. The NIC then encapsulates the data in a Data Link Layer frame, which includes the MAC address of the destination device.**</span> The NIC then sends the frame over the network to the destination device, where it is received by the NIC on that device.

The NIC on the receiving device then checks the MAC address in the frame to ensure that the data is intended for it. If the MAC address matches, the NIC sends the data up to the next layer of the OSI model, the Network Layer (layer 3).

In summary, a NIC is a hardware component that connects a computer to a network, operates at the Data Link Layer and is responsible for transmitting and receiving data between the computer and the network, it uses MAC address to identify and communicate with other devices on the network.

### Router's Network Interface Card (NIC)

Yes, a router typically has a Network Interface Card (NIC) or multiple NICs, which allow it to connect to different networks and receive and transmit data.

<span style="color:#d19a66">**When a router receives a frame at the Data Link Layer (layer 2) from one of its NICs, it first checks the MAC address in the frame to determine the destination of the data. If the frame is intended for a device on the same network as the router, the router will forward the frame to the appropriate NIC to send it to the destination device.**</span>

If the frame is intended for a device on a different network, the router will use its routing table to determine the best path for the data to reach its destination. It then encapsulates the frame in a new Data Link Layer frame, with the appropriate MAC address, and sends it out of the appropriate NIC to the next hop in the path towards the destination.

Routers are important devices in networks that allow communication between different networks and devices, they use routing tables and protocols such as IP (Internet Protocol) to determine the best path for data to travel, and then forward the data using their NICs.

---

# Wireless Network Adapter

A mobile phone does not have a traditional Network Interface Card (NIC) like a computer does, but it does have a wireless network adapter that allows it to connect to a wireless network.

The wireless network adapter in a mobile phone is built into the phone's hardware, and is responsible for transmitting and receiving data over the wireless network. It may be referred to as a wireless module, wireless chip, or similar.

It's important to note that, in mobile phones, the wireless network adapter typically operates at the Physical and Data Link Layer (layer 1 and 2) of the OSI model, allowing the phone to communicate with the network and establish a connection. The phone's operating system and software stack are responsible for handling higher layers of the OSI model, to enable communication and data transfer between the phone and other devices.

In summary, while a mobile phone does not have a traditional NIC card, it has a built-in wireless network adapter that allows it to connect to wireless networks and communicate with other devices.

---

# Ethernet

Ethernet is a technology for connecting devices on a Local Area Network (LAN). It is a set of standards for physical and data link layers of the OSI (Open Systems Interconnection) model, that defines how data is transmitted over a wired network.

Ethernet uses a bus or star topology, where devices are connected to a central hub or switch using twisted-pair or coaxial cables. Data is transmitted over the network in the form of frames, which contain the data as well as the source and destination MAC (Media Access Control) addresses.

Ethernet supports several different data rates, known as Ethernet speeds, the most common being:
10 Mbps, 100 Mbps, 1 Gbps, 10 Gbps, and 40 Gbps and 100 Gbps, and even higher.

Ethernet also supports a variety of different media types, such as twisted-pair cables, coaxial cables, and fiber-optic cables, which can be used to connect devices over different distances.

Ethernet is a widely used technology and is the foundation for many networks, including LANs in homes and businesses, as well as the backbone of many enterprise and service provider networks.

In summary, Ethernet is a technology for connecting devices on a LAN, it defines a set of standards for physical and data link layers, it uses a bus or star topology, twisted-pair or coaxial cables and supports different data rates and media types, it
