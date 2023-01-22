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
