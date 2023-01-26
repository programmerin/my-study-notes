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

<br>

---

# Router typically has multiple MAC addresses

A router typically has multiple MAC addresses, one for each of its network interfaces. These interfaces can include LAN (Local Area Network) ports for connecting to devices on the internal network, and WAN (Wide Area Network) ports for connecting to the internet or other external networks.

Each interface on a router is assigned a unique MAC address by the manufacturer, and these addresses are used to identify the source and destination of network traffic. When a packet of data is sent from one device to another on the same network, the MAC address of the source device is used as the source address in the packet, and the MAC address of the destination device is used as the destination address.

When the data packet needs to be sent to a different network, the router uses its routing table to determine the best path for the packet and then uses the MAC address of the interface that connects to that network as the destination address.

A router's multiple MAC addresses work by allowing it to connect to multiple networks and route traffic between them. Each network interface on a router is assigned a unique MAC address, which is used to identify the source and destination of network traffic.

For example, consider a router that connects a LAN (Local Area Network) to a WAN (Wide Area Network) . The router has two interfaces:

1. LAN interface with MAC address 00:11:22:33:44:55

2. WAN interface with MAC address 66:77:88:99:AA:BB

When a device on the LAN (such as a computer) wants to communicate with a device on the WAN (such as a website), the router uses its routing table to determine the best path for the packet.

The router then uses the LAN interface's MAC address (00:11:22:33:44:55) as the source address in the packet and the WAN interface's MAC address (66:77:88:99:AA:BB) as the destination address.

This way, the device on the LAN knows that the packet is coming from the router, and the device on the WAN knows that the packet is intended for it. When the packet is received by the router, it uses the destination MAC address to determine which interface to forward the packet to, in this case the WAN interface.

Additionally, when a packet is received on a specific interface, the router checks the destination MAC address in the packet, if it matches with any of the interfaces MAC address that means the packet is intended for the router and it will process it accordingly.

In this way, the router can connect to multiple networks and route traffic between them using its multiple MAC addresses. The router keeps a table of MAC addresses and their corresponding interfaces, so that when a packet is received on a specific interface, the router knows where it should be forwarded.

<br>

---

# Broadcast IP address

A broadcast IP address is used to send a message to all devices on a network, rather than a specific device. In IP networking, a broadcast address is a network address at which all devices connected to a multiple-access communications network are enabled to receive datagrams.

An example of when a broadcast IP address might be used is in the process of DHCP (Dynamic Host Configuration Protocol) in which a device, such as a computer, requests an IP address from a DHCP server. The DHCP server sends a broadcast message to all devices on the network, offering an IP address to any device that requests one. The device that requested the IP address responds to the broadcast message, and the DHCP server assigns the requested IP address to that device.

Another example could be when a network administrator needs to send a message to all devices on a network, they can use the broadcast IP address to ensure that the message is received by all devices.

Note: Broadcast IP addresses are usually represented in dotted decimal notation, and it is identified by the fact that it has all host bits set to 1.

<br>

---

# Default Gateway

A default gateway is a routing device or host on a computer network that serves as an access point to other networks or the internet. It is used to forward network traffic from a device on a local network to other networks or the internet.

In most cases, a default gateway is a router. This router connects a local network to the internet or to another network. The default gateway is usually assigned an IP address, such as 192.168.1.1 or 10.0.0.1.

When a device on a local network wants to communicate with a device on another network or the internet, it sends the data to the default gateway. The default gateway then forwards the data to the next hop on the path to its destination.

For example, imagine a local network with several devices connected to a router. The router is connected to the internet. The router's IP address is 192.168.1.1, and it is configured as the default gateway for the devices on the local network. When one of the devices on the local network wants to access a website, it sends the request to the router at IP address 192.168.1.1. The router then forwards the request to the internet, where the website's server responds. The response is then sent back to the device via the router.

Another example, imagine a local network has multiple VLANs, and each VLAN has a different default gateway. Each VLAN is connected to different router, which is configured as the default gateway for the VLAN. When a device on one VLAN wants to communicate with a device on another VLAN, the device sends the data to its default gateway, the router which is configured for that VLAN, then the router forwards the data to the next hop on the path to its destination.

In short, a default gateway is an IP address that devices on a local network use to send data to other networks or the internet. It is typically a router that connects the local network to other networks or the internet.

<br>

---

# Network Topology

!["Network Topology"](/network-topology-types-diagram.png)

Network topology refers to the physical or logical layout of a computer network. It describes the arrangement of devices and the connections between them. The topology of a network can have a significant impact on its performance, security, and ease of management.

There are several common types of network topologies, including:

Bus topology: All devices are connected to a single cable or bus, which is the backbone of the network. Data is transmitted along the bus in both directions.

Star topology: All devices are connected to a central hub or switch. Data is transmitted from one device to the hub and then sent to the appropriate device.

Ring topology: All devices are connected in a closed loop. Data is transmitted around the loop in a single direction.

Mesh topology: Each device is connected to multiple other devices. Data can be transmitted along multiple paths to reach its destination.

Tree topology: A combination of bus and star topologies. A central bus or backbone connects to multiple branches, each containing multiple devices.

Hybrid topology: It is a combination of two or more different topologies. It is designed to overcome the limitations of a single topology.

The choice of network topology can depend on several factors, such as the size of the network, the type of devices and applications, the availability of resources and the desired level of fault tolerance.

In summary, Network topology refers to the physical or logical layout of a computer network, it describes the arrangement of devices and the connections between them. Different topologies have different advantages and disadvantages, and the choice of topology will depend on the needs of the network.

<br>

---

# 10/100/1000Base-T Ports (1 - 24) - Ports are Auto-MDIX

10/100/1000Base-T ports (1-24) refer to a range of Ethernet ports on a network device, such as a switch, that support 10Mbps, 100Mbps, and 1000Mbps speeds (also known as 10Base-T, 100Base-T, and 1000Base-T, respectively). These ports are typically labeled as "10/100/1000" or "Gigabit" Ethernet ports, and they are capable of automatically detecting and adjusting to the speed of the connected device.

<span style="color:#d19a66">**Auto MDIX (Auto Media-Dependent Interface Crossover) is a feature that allows the ports to automatically detect and configure the correct cable type (straight-through or crossover) and pinout (T568A or T568B) for the connection.**</span> This eliminates the need for manual configuration or the use of crossover cables.

For example, imagine you have a switch with 24 10/100/1000Base-T ports (1-24) and you want to connect it to a computer. Normally, you would need to check the pinout of the computer's Ethernet port and the switch port and use a crossover cable if they are different. But with Auto MDIX, you can simply use a straight-through cable and the switch will automatically detect and configure the correct pinout for the connection.

This feature allows for more flexibility when connecting devices, as it eliminates the need for different types of cables, and also reduces the chance of misconfiguration and connectivity issues.

It's also worth mentioning that not all networking equipment have this feature, so it's important to check the device's specifications before making a purchase.

<br>

---

# Different types of interfaces in Cisco devices

Cisco devices, such as routers and switches, have a variety of interface types that can be used for different purposes. Some of the most commonly used interface types include:

Ethernet interfaces - These are used to connect to LANs (Local Area Networks) and are typically used for data transfer between devices. An example of an Ethernet interface on a Cisco router would be Fast Ethernet interface 0/0.

Serial interfaces - These are used to connect to WANs (Wide Area Networks) and are typically used for data transfer between different locations. An example of a serial interface on a Cisco router would be Serial interface 0/0/0.

Console interface - This is a special type of interface that is used for local management of the device. It is typically used for initial configuration and troubleshooting. An example of a console interface on a Cisco router would be the default console interface.

AUX interface - This is also a special type of interface that is used for local management of the device. It is typically used for backup configuration and troubleshooting. An example of an AUX interface on a Cisco router would be the default AUX interface.

Virtual interfaces - These interfaces are logical interfaces that are used to create multiple virtual interfaces on a single physical interface. An example of a virtual interface on a Cisco router would be Virtual-Access interface 1.

Tunnel interfaces - These interfaces are logical interfaces that are used to create tunnels between two or more devices. An example of a Tunnel interface on a Cisco router would be Tunnel interface 1.

Loopback interfaces - These interfaces are logical interfaces that are used to create a virtual interface for testing and troubleshooting. An example of a loopback interface on a Cisco router would be Loopback interface 0.

In addition to these interface types, Cisco devices also have other specialized interfaces such as BVI (Bridge-Group Virtual Interface) for LAN switching, SVI (Switched Virtual Interface) for Layer 3 switching, and many others.
