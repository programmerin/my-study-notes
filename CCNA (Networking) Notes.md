## What is Networking model ?

A networking model is a conceptual framework that describes how different elements of a network interact and communicate with each other.

Networking models categorize and provide a structure for networking **protocols** and **standards**.

#### What is networking protocols ?

A networking protocol is a set of rules and standards that define how devices on a network communicate with each other. Protocols are used to establish connections, transmit data, and ensure that data is transmitted reliably and in the correct order. They also establish how data is packaged, addressed, routed, and received.

---

## OSI Model

The OSI (Open Systems Interconnection) model is a framework used to understand and standardize how different communication protocols and technologies work together. It defines seven layers, each with a specific function, that work together to enable communication between devices on a network. The OSI model is a way to understand how the different protocols and technologies used in networking relate to each other and to the overall process of transmitting data over a network.

- Created by the "International Organization for Standardization" (ISO).

- Functions are divided into 7 Layers.

!["OSI (Open System Interconnection)"](/OSI-Model.png)

<span style="color:orange;font-weight:bold;font-size:21px;">7. Application Layer : </span> The Application Layer is the highest layer of the OSI (Open Systems Interconnection) model and <span style="color:#d19a66">**it is responsible for providing the interface between the application and the network.**</span> It defines the protocols and standards that are used to enable communication between applications and the network. The main goal of the Application Layer is to provide services that allow the application to access the network.

Here are a few examples of the functions and protocols that are typically associated with the Application Layer:

- <span style="color:#6699CC;font-weight:bold">Providing services to the application</span> : The Application Layer provides services such as file transfer, email, remote login, and database access to the application. For example, the File Transfer Protocol (FTP) is used to transfer files between computers, and the Simple Mail Transfer Protocol (SMTP) is used to send and receive email.

- <span style="color:#6699CC;font-weight:bold">Translating application data</span> : The Application Layer is responsible for converting application data into a format that can be transmitted across the network and then converting the received data back into a format that can be understood by the application. For example, the Hypertext Transfer Protocol (HTTP) is used to transmit web pages across the Internet, and the Simple Object Access Protocol (SOAP) is used to send and receive messages in web services.

- <span style="color:#6699CC;font-weight:bold">Authentication and security</span> : The Application Layer is responsible for ensuring that only authorized users can access the network and that the data being transmitted is secure. For example, the Secure Sockets Layer (SSL) and Transport Layer Security (TLS) are used to encrypt data that is transmitted over the Internet, and the Remote Authentication Dial-In User Service (RADIUS) is used to authenticate users who are trying to connect to a network.

Application layer protocols: `HTTP`, `HTTPS`, `FTP`, `SMTP`, `DNS`, `DHCP`, `SNMP`, `NFS` are some examples of application layer protocols.

It is important to note that the Application Layer does not interact directly with the network, but rather it communicates with the underlying layers, such as the Transport and Network Layers, which handle the actual transmission of data across the network. The Application Layer protocols are designed to be independent of the underlying network architecture, allowing the same application to work on different networks.

Functions of Layer 7 include:

- Identifying communication partners
- Synchronizing communication

#### Adjacent Layer Interaction

!["Adjacen Layer Interaction"](/adjacen-layer-interactions.png)

Both the **encapsulation** and **de-encapsulation** processes are examples of **Adjacen-layer-interaction** between the different layers of OSI model.

<br>

#### Same Layer Interaction

!["Same Layer Interaction"](/same-layer-interaction.png)

The communication between the **application layers** of the two different systems, is called **same-layer** interaction.

This **same-layer** ineraction between application layers is what allows the application layer to perform it's functions of **identifying** communication partners, **synchronizing communications**, etc.

<br>

<span style="color:orange;font-weight:bold;font-size:21px">6. Presentation Layer :</span> The Presentation Layer is the sixth layer of the OSI (Open Systems Interconnection) model and <span style="color:#d19a66">**it is responsible for converting data into a format that can be understood by the application. It also provides encryption and compression for the data.**</span> The main goal of the Presentation Layer is to provide a standard representation of the data that is being transmitted between devices on the network.

Here are a few examples of the functions and protocols that are typically associated with the Presentation Layer:

- <span style="color:#6699CC;font-weight:bold">Data conversion</span> : The Presentation Layer is responsible for converting data between different formats.

  For example, it can convert text data into binary data, or vice versa. It can also convert data between different character encodings, such as ASCII and Unicode.

- <span style="color:#6699CC;font-weight:bold">Data compression</span> : The Presentation Layer can also compress data to reduce the amount of bandwidth needed to transmit it. This can improve the performance of the network by reducing the amount of data that needs to be transmitted.

  Some examples of data compression algorithms used in the Presentation Layer are: Huffman encoding, Lempel-Ziv-Welch (LZW) algorithm, and run-length encoding.

- <span style="color:#6699CC;font-weight:bold">Data encryption</span> : The Presentation Layer can also encrypt data to protect it from unauthorized access. Encryption algorithms such as RSA, AES, and DES are typically used to encrypt data at the Presentation Layer.

- <span style="color:#6699CC;font-weight:bold">Presentation layer protocols</span> : ASCII, EBCDIC, JPEG, TIFF, MPEG, MIDI, PICT, and QuickTime are some examples of presentation layer protocols.

It is important to note that the Presentation Layer does not define any specific protocols, but rather it provides a common interface for the application and the network, allowing them to communicate in a standardized format. The Presentation Layer protocols, such as ASCII and EBCDIC, are not widely used today as most of the data transfer happens in binary format.

<br>

<span style="color:orange;font-weight:bold;font-size:21px">5. Session Layer :</span> The Session Layer is the fifth layer of the OSI (Open Systems Interconnection) model, <span style="color:#d19a66">**it is responsible for establishing, maintaining, and terminating connections between applications on different devices.**</span> It also controls the flow of data between the devices. The main goal of the Session Layer is to provide a way for applications on different devices to communicate with each other in a coordinated and organized manner.

Here are a few examples of the functions and protocols that are typically associated with the Session Layer:

- <span style="color:#6699CC;font-weight:bold">Session establishment</span> : The Session Layer is responsible for establishing a session between two applications on different devices. This can include negotiation of the parameters of the session, such as the type of data that will be exchanged, and the protocols that will be used.

- <span style="color:#6699CC;font-weight:bold">Session management</span> : Once a session is established, the Session Layer is responsible for maintaining it. This includes keeping track of the state of the session, such as whether it is active or inactive, and handling any errors that may occur during the session.

- <span style="color:#6699CC;font-weight:bold">Session termination</span> : The Session Layer is also responsible for terminating a session when it is no longer needed. This can include releasing any resources that were allocated during the session, and notifying the applications that the session has been terminated.

- <span style="color:#6699CC;font-weight:bold">Session layer protocols</span> : Some examples of session layer protocols are: Remote Procedure Call (RPC), Named Pipes, NetBIOS, and X Window System.

It is important to note that the Session Layer is not commonly used today as many modern network protocols and applications do not require the explicit establishment and management of sessions. The functionality of session layer is often embedded in the application layer protocols.

> Note: Network engineers don't usually work with the top 3 layers. Application developers work with the top layers of the OSI model to connect their applications over networks.

<br>

<span style="color:orange;font-weight:bold;font-size:21px">4. Transport Layer</span> : The transport layer is the fourth layer of the OSI (Open Systems Interconnection) reference model, which is used to describe how data is transmitted over a network. <span style="color:#d19a66">**It is responsible for providing end-to-end communication services between applications running on different devices.**</span>

The main function of the transport layer is to ensure the reliable delivery of data between two devices. It does this by providing a variety of services, such as segmentation and reassembly of data, flow control, and error checking.

!["TCP vs UDP communication"](/udp-tcp.jpg)

One of the main protocols used at the transport layer is the Transmission Control Protocol (TCP). <span style="color:#d19a66">**TCP is a connection-oriented protocol that establishes a virtual circuit between two devices before any data is exchanged.**</span> This allows for reliable data transfer, as TCP can detect and recover from any errors that may occur during transmission.

Another common protocol used at the transport layer is the User Datagram Protocol (UDP). <span style="color:#d19a66">**Unlike TCP, UDP is a connectionless protocol that does not establish a virtual circuit before data is exchanged.**</span> This makes it a faster and more efficient option for applications that don't require the reliability of TCP.

An example of a transport layer protocol in action is when you load a webpage in your browser. The browser sends a request to the server for the webpage using HTTP (Hypertext Transfer Protocol), which runs on top of TCP. The server then sends the requested webpage back to the browser over the same TCP connection.

Another example is video conferencing application like Zoom. <span style="color:#d19a66">**The video and audio data are sent as packets over the internet**</span>, and the transport layer protocols like UDP are used to ensure that the packets are delivered quickly and efficiently to the correct destination.

In summary, the transport layer plays a crucial role in ensuring the reliable and efficient delivery of data across a network. It provides a variety of services such as segmentation, flow control, and error checking, and uses protocols like TCP and UDP to accomplish this.

<br>

<span style="color:orange;font-weight:bold;font-size:21px">3. Network Layer :</span> The network layer is the third layer of the OSI (Open Systems Interconnection) reference model, which is used to describe how data is transmitted over a network. <span style="color:#d19a66">**It is responsible for routing and forwarding data packets between devices on a network.**</span> The main function of the network layer is to ensure that data packets are delivered to the correct destination by routing them through the appropriate paths in a network.

One of the main protocols used at the network layer is the Internet Protocol (IP). IP is the primary protocol used to route and forward data packets on the internet. <span style="color:#d19a66">**It is responsible for addressing and identifying devices on a network, and for determining the best path for data packets to travel to reach their destination.**</span>

Another common protocol used at the network layer is the Internet Control Message Protocol (ICMP). ICMP is used to send error messages and operational information about network conditions, such as when a destination host or network is unreachable.

An example of the network layer in action is when you use a web browser to load a webpage. When you enter the webpage's URL, your computer sends a request to a DNS (Domain Name System) server to resolve the URL to an IP address. This is the first step in the process of routing the request to the correct server. Once the IP address is obtained, the request is sent to the server over the internet via IP packets. These packets are then routed through various routers and switches on the network, until they reach the server, where the requested webpage is sent back to the client.

Another example is when you send an email. The network layer protocol (IP) is responsible for addressing the email message and routing it through the internet to the recipient's mail server.

In summary, the network layer plays a crucial role in ensuring that data packets are delivered to the correct destination by routing them through the appropriate paths in a network. It uses protocols like IP and ICMP to accomplish this, and it is used in everyday applications such as web browsing, email and file transfer.

<br>

<span style="color:orange;font-weight:bold;font-size:21px">2. Data Link Layer :</span> The Data Link Layer is the second layer of the OSI (Open Systems Interconnection) reference model, which is used to describe how data is transmitted over a network. <span style="color:#d19a66">**It is responsible for creating a link between devices on the same network segment.**</span> It deals with the physical addressing of devices and the organization of data into frames, which are the units of data that are transmitted at the data link layer.

The main function of the data link layer is to provide reliable data transfer between devices on a local network. It does this by providing error detection and correction, as well as flow control and media access control.

There are two sublayers of the data link layer: the Logical Link Control (LLC) and the Media Access Control (MAC). The LLC sublayer provides flow control and error detection, while the MAC sublayer provides media access control and physical addressing.

One of the main protocols used at the data link layer is the Ethernet. Ethernet is a standard for wired LAN (Local Area Network) that uses CSMA/CD (Carrier Sense Multiple Access with Collision Detection) for media access control. It specifies the physical and data link layers of the OSI model.

Another example of Data Link Layer is when you use a wireless network, the data link layer protocol is Wireless LAN (WLAN) protocol like IEEE 802.11 which provides the mechanism for wireless device to communicate with each other, providing features such as access control, error detection and correction, and flow control.

In summary, the Data Link Layer plays a crucial role in ensuring reliable data transfer between devices on a local network. It provides error detection and correction, flow control and media access control, and uses protocols like Ethernet and IEEE 802.11 to accomplish this. It deals with physical addressing of devices and the organization of data into frames. It is used in everyday applications such as wired and wireless LANs.

<br>

<span style="color:orange;font-weight:bold;font-size:21px">1. Physical Layer :</span> The Physical Layer is the first layer of the OSI (Open Systems Interconnection) reference model, which is used to describe how data is transmitted over a network. <span style="color:#d19a66">**It is responsible for the physical connection between devices on a network, and for transmitting raw bits of data over a communication channel.**</span> It deals with the physical characteristics of the network such as signaling method, cable type, and connector type.

The main function of the physical layer is to establish, maintain and terminate the physical link between devices. <span style="color:#d19a66">**It also provides the means for transmitting and receiving raw bits of data over the communication channel.**</span> The physical layer is responsible for the electrical, mechanical, functional and procedural characteristics of the interface between the communication equipment and the transmission medium.

Examples of the Physical Layer are the various types of cables and connectors used to connect devices to a network. For example, Ethernet cables (RJ45) and connectors, fiber-optic cables and connectors, and coaxial cables are all examples of physical layer technologies.

Another example is when you use a wireless network, the physical layer protocol is the radio frequency (RF) technology that transmits and receives signals over the air. The physical layer protocols define the characteristics of the RF signals such as the frequency band, modulation, and transmit power levels that are used to connect the devices.

In summary, the Physical Layer plays a crucial role in the establishment, maintenance, and termination of the physical link between devices, and for transmitting and receiving raw bits of data over the communication channel. It deals with the physical characteristics of the network such as signaling method, cable type, and connector type. It is used in everyday applications such as wired and wireless LANs, and it uses technologies like cables, connectors and RF to accomplish this.

---

# Network Layer's Header and Trailer

!["Protocol Data Units"](</Protocole%20Data%20Units%20(PDU).png>)

A Protocol Data Unit (PDU) refers to the specific format and structure of data that is exchanged between network devices using a specific protocol. The PDU contains both control information and user data. The structure of a PDU can vary depending on the protocol being used.

Layer 1 (Physical Layer) PDU is called `"bit"`.

As data is transmitted through the network, each layer adds a header or trailer to the data packet, which contains information specific to that layer.

- <span style="color:#6699CC;font-weight:bold">The Physical Layer :</span> This layer deals with the physical connection between devices on a network. It adds no headers or trailers to the data packet.

- <span style="color:#6699CC;font-weight:bold">The Data Link Layer :</span> This layer is responsible for creating a link between devices on the same network segment. It adds a header and trailer to the data packet, known as a Frame. The header contains information such as the source and destination MAC addresses, and the trailer contains error checking information.

- <span style="color:#6699CC;font-weight:bold">The Network Layer :</span> This layer is responsible for routing data packets between devices on a network. It adds a header to the data packet, known as an IP packet. The header contains information such as the source and destination IP addresses, and the packet's routing information.

- <span style="color:#6699CC;font-weight:bold">The Transport Layer :</span> This layer is responsible for providing end-to-end communication services between applications running on different devices. It adds a header to the data packet, known as a segment. The header contains information such as the source and destination ports, and the protocol being used (TCP or UDP).

- <span style="color:#6699CC;font-weight:bold">The Session Layer :</span> This layer is responsible for establishing and maintaining communication sessions between devices. It adds a header to the data packet, known as a session header. The header contains information such as the session ID and status of the connection.

- <span style="color:#6699CC;font-weight:bold">The Presentation Layer :</span> This layer is responsible for converting data into a format that can be understood by the application layer. It adds a header or trailer to the data packet, known as a presentation header or trailer. The header or trailer contains information such as the data's encoding format.

- <span style="color:#6699CC;font-weight:bold">The Application Layer :</span> This layer is responsible for providing the interface between the user and the network. It adds no headers or trailers to the data packet.

An example of the OSI model in action is when you use a web browser to load a webpage. The browser sends a request to the server for the webpage using HTTP (Hypertext Transfer Protocol), which runs on top of TCP at the application layer. The transport layer adds a header containing the source and destination ports, and the protocol being used (TCP) to the data packet. The network layer adds a header containing the source and destination IP addresses, and the packet's routing information to the data packet. The data link layer adds a header and trailer containing the source and destination MAC addresses and error checking information to the data packet. And finally, the physical layer transmit the packet over the network.

In summary, as data is transmitted through the network, each layer of the OSI model adds a header or trailer to the data packet, which contains information specific to that layer. This allows for the efficient and accurate transmission of data across a network.

---

# TCP/IP Suite

!["TCP/IP Stack"](/IP_stack_connections.svg)

---

# IPv4 Addressing

!["Routing"](/Routing.png)

The notation "192.168.1.0/24" and "192.168.2.0/24" are examples of CIDR (Classless Inter-Domain Routing) notation, which is used to specify the IP address range and the subnet mask of a network.

The IP address "192.168.1.0" is the first address in the range of IP addresses that make up the network, and the number "24" following the "/" symbol is the subnet mask. The subnet mask is used to determine the number of bits that make up the network portion of the IP address, and the remaining bits make up the host portion of the IP address.

In the case of "192.168.1.0/24", the first 24 bits of the IP address are used to define the network portion of the address, and the remaining 8 bits are used to define the host portion of the address. This means that the network can contain up to 256 possible IP addresses (2^8 = 256), with the range of IP addresses being "192.168.1.0" to "192.168.1.255".

Similarly, "192.168.2.0/24" is another example of CIDR notation which covers the IP address range from "192.168.2.0" to "192.168.2.255".

An example of how these networks can be used:

- The network "192.168.1.0/24" could be used for the devices in an office building, while the network "192.168.2.0/24" could be used for devices in a factory.

- Another example would be if you have two different physical locations and you want to separate their networks, you can use the "192.168.1.0/24" for location 1 and "192.168.2.0/24" for location 2.

It's worth mentioning that these IP address ranges are from the private IP address space, which means they are not publicly routed on the internet and only can be used for internal networks.

### Router typically needs multiple IP addresses

A router typically needs multiple IP addresses because it connects multiple networks together and acts as a gateway between them. Each network interface on a router corresponds to a unique IP address, as each network interface represents a connection to a different network.

!["Router IP addresses"](/router-public-private-ip.png)

For example, consider a router that connects a local area network (LAN) to the internet. The router would have at least two network interfaces: one for the LAN and one for the internet connection. The LAN interface would have a private IP address, such as "192.168.1.1", while the internet interface would have a <span style="color:#d19a66">**public IP address assigned by the internet service provider (ISP).**</span>

<span style="color:#d19a66">**The private IP address on the LAN interface is used to communicate with devices on the local network, while the public IP address on the internet interface is used to communicate with devices on the global internet.**</span>

Another example would be in a situation where a router connects multiple LANs together, it can use different IP addresses on different interfaces to separate the traffic between the LANs and maintain security.

In addition, routers use different IP addresses on different interfaces to route traffic between networks. <span style="color:#d19a66">**The router uses the IP address and subnet mask of each interface to determine which interface to forward the incoming packet to.**</span> This allows the router to efficiently route traffic between networks, even if the networks have overlapping IP address ranges.

In summary, routers use multiple IP addresses to connect and route traffic between multiple networks. Each IP address corresponds to a unique network interface, which represents a connection to a different network. This enables the router to act as a gateway between networks and facilitates communication between devices on different networks.

### IPv4 Addresses

!["IPv4 Addresses"](/IPv4%20Addresses.png)

IPv4 addresses are 32-bit binary numbers that are typically represented in decimal format using the dot-decimal notation. Each decimal number in an IPv4 address, also known as an octet, is between 0 and 255. The four octets of an IPv4 address are separated by dots and represent the network and host portions of the address.

### IPv4 address Classes

IPv4 addresses are divided into five classes: A, B, C, D, and E. Each class has a specific range of addresses, and the classes are defined based on the value of the first octet (the first number) of the IP address.

!["IPv4 Address Classes"](/IPv4%20Address%20Classes.png)

!["IPv4 Address Classes"](/IPv4%20Addresses%20Classes.png)

!["IPv4 Address Classes"](/class-a-b-c.png)

!["IPv4 Address Classes Chart"](/IPv4-classes-chart.png)

!["Netmask"](/Netmask.png)

- Class A addresses have a first octet in the range of 1 to 126. The first octet is the network address, and the remaining three octets are used for identifying individual hosts. An example of a Class A address is 10.0.0.1, where 10 is the network address and 0.0.1 is the host address.

- Class B addresses have a first octet in the range of 128 to 191. The first two octets are used for the network address, and the remaining two octets are used for identifying individual hosts. An example of a Class B address is 172.16.0.1, where 172.16 is the network address and 0.1 is the host address.

- Class C addresses have a first octet in the range of 192 to 223. The first three octets are used for the network address, and the remaining octet is used for identifying individual hosts. An example of a Class C address is 192.168.1.1, where 192.168.1 is the network address and 1 is the host address.

- Class D addresses are used for multicast addresses, which are used to send a single packet to multiple hosts. Class D addresses have a first octet in the range of 224 to 239.

- Class E addresses are reserved for experimental use and have a first octet in the range of 240 to 255.

It's worth noting that, IPv4 address classes are not widely used anymore, due to the scarcity of IPv4 address, instead CIDR (Classless Inter-Domain Routing) notation is used to represent IP addresses.

!["Network Address"](/Network%20Address.png)

!["Broadcast Address"](/Braoadcast%20Address.png)

### Loopback Addresses

!["Loopback Address"](/loopback-address.jpg)

A loopback address is a special IP address, usually assigned to the loopback interface, <span style="color:#d19a66">**that is used to test the network configuration and connectivity of a device.**</span> The most commonly used loopback address is 127.0.0.1, which is assigned to the IPv4 loopback interface. Additionally, the IPv6 loopback address is ::1.

When a device sends a packet to the loopback address, the packet is looped back to the device itself, rather than being sent out onto the network. This allows the device to test its own network interface, without the need for another device to be connected to the network.

For example, a computer can use the loopback address to test its own network interface card (NIC) by pinging the loopback address. If the computer can successfully ping the loopback address, it means that the NIC is working properly and that the TCP/IP stack is configured correctly.

Additionally, Loopback address is used in some applications and protocols to bind on to the localhost or loopback interface, this allows the application to listen to network connections only from the local host, and not from remote hosts, this enhance the security of these applications and protocols.

In summary, loopback addresses are a useful tool for testing the basic functionality of a device's network interface and TCP/IP stack, and also used in some applications and protocols to bind to the localhost or loopback interface for security reason.

> Note: The first address in each network is the <span style="color:#d19a66; font-weight:medium">"Network address"</span>, it can't be assigned to hosts. Also the last address of the network is the <span style="color:#d19a66; font-weight:medium">"Broadcast address"</span>, the Layer 3 address used when you want to send traffic to all hosts. It also can't be assigned to hosts.

---

# CISCO Device Configuration Using CLI

!["CISCO IOS device modes"](/Router-Mods-and-Prompt.png)

!["IOS Mode Hierarchical"](/IOS%20mode%20hierarichal.png)

### 1. User exec mode

User exec mode, also known as user mode, is one of the three main modes of operation in Cisco IOS. It is the default mode when you first log into a Cisco device. <span style="color:#d19a66">**In this mode, you can view basic system information and perform a limited set of commands.**</span>

Examples of commands that can be used in user exec mode include:

- `show version`: Displays information about the version of IOS running on the device, as well as the device's hostname, uptime, and memory usage.

- `show interfaces`: Displays information about the status of the device's interfaces, such as their speed, duplex, and whether they are up or down.

- `ping`: Sends ICMP echo requests to a specified IP address to test connectivity.

Commands that allow you to make changes to the device's configuration, such as `configure terminal` or `interface`, will not be available in user exec mode, as those require privilege level 15 or higher.

<br>

### 2. Privileged exec mode

Privileged exec mode, also known as privileged mode or enable mode, is one of the three main modes of operation in Cisco IOS. It is the mode you enter after logging into a Cisco device in user exec mode and issuing the command enable. In this mode, you have access to a much wider range of commands, including those that allow you to make changes to the device's configuration.

In privileged exec mode, you have access to all commands that are available in user exec mode, as well as additional commands such as:

- `configure terminal`: Enters global configuration mode, where you can make changes to the device's overall configuration.

- `interface`: Enters interface configuration mode, where you can make changes to specific interfaces on the device.

- `copy`: Allows you to copy files to and from the device's file system, such as copying a configuration file from a TFTP server to the device.

- `debug`: Allows you to enable debugging on the device, which can be useful for troubleshooting.

- `show running-config`: Displays the current, active configuration of the device.

You can also enter other configuration modes such as line configuration mode, route-map configuration mode, policy-map configuration mode, etc.

To enter privileged exec mode, you must first log into the device in user exec mode and then issue the command `enable`. By default, the enable password is the same as the user exec mode password, but it can be configured differently.

Example:

```sh
Router> enable
Password:
Router#
```

You are now in privileged exec mode, indicated by the "#" prompt.

```sh
Router# configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)# interface gigabitEthernet 0/0
Router(config-if)# ip address 10.10.10.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit
Router(config)# exit
Router#
```

In this example, the user first enters privileged exec mode by using the `enable` command and the correct password. They then <span style="color:#d19a66">**enter global configuration mode by using the `configure terminal` command.**</span> Next, they enter interface configuration mode to configure an IP address and bring up the interface. Finally, they exit configuration mode by using the `exit` command.

It is important to note that in privileged exec mode you have the ability to change the device's configuration, so it is important to be cautious and use the right commands, otherwise, it can cause problems in the network.

<br>

### 3. Global configuration mode

Global configuration mode, also known as global config mode, is a sub-mode of privileged exec mode in Cisco IOS. It allows you to make changes to the overall configuration of a Cisco device, such as setting the device's hostname, configuring its interfaces, and defining routing protocols.

To enter global configuration mode, you must first log into the device in privileged exec mode and then issue the command configure terminal. This command allows you to make changes to the device's configuration that will be applied globally, rather than to a specific interface or other sub-section of the device.

Once in global configuration mode, you can use a variety of commands to configure the device. Some examples include:

- `hostname`: Sets the hostname of the device.

- `interface`: Enters interface configuration mode, where you can make changes to specific interfaces on the device, such as configuring IP addresses, enabling or disabling interfaces, etc.

- `ip routing`: Enables IP routing on the device, which allows it to forward packets between different networks.

- `line vty`: Enters line vty configuration mode, where you can configure settings for virtual terminal lines, such as setting the login and password requirements for remote access.

- `no shutdown`: brings up or activates an interface or other feature that was previously shut down.

- `router eigrp`: Enters EIGRP routing protocol configuration mode, where you can configure settings for the EIGRP routing protocol, such as setting the autonomous system number.

Example:

```sh
Router# configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)# hostname RouterA
RouterA(config)# interface gigabitEthernet 0/0
RouterA(config-if)# ip address 10.10.10.1 255.255.255.0
RouterA(config-if)# no shutdown
RouterA(config-if)# exit
RouterA(config)# ip routing
RouterA(config)# router eigrp 100
RouterA(config-router)# network 10.0.0.0
RouterA(config-router)# exit
RouterA(config)# exit
RouterA#
```

In this example, the user first enters global configuration mode by using the `configure terminal` command. They then set the hostname of the device to "RouterA" using the `hostname `command. Next, they enter interface configuration mode to configure IP address and bring up the interface. After that, they enable IP routing on the device using the `ip routing` command. Then, they enter EIGRP routing protocol configuration mode using the `router eigrp` command and set the network to 10.0.0.0. Finally, they exit configuration mode by using the `exit` command.

It is important to note that any changes made in global configuration mode will take effect immediately, and it is recommended to test the changes in a lab environment before applying them to a production network.

### 'Running-config' and the 'Startup-config'

There are two main configuration files that are kept on a Cisco device: the running-config and the startup-config.

1. `Running-config`: The running-config is the current, active configuration of the device. It is stored in the device's memory and is used to control the device's behavior. Any changes made to the running-config take effect immediately. The running-config can be viewed using the command show running-config.
   Example:

```sh
Router# show running-config
Building configuration...

Current configuration : 983 bytes
!
version 15.4
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
!
hostname RouterA
!
interface GigabitEthernet0/0
 ip address 10.10.10.1 255.255.255.0
 no shutdown
!
ip routing
!
router eigrp 100
 network 10.0.0.0
!
end
```

In this example, the user can see the current configuration of the RouterA including the hostname, interface configurations, IP routing, and EIGRP routing protocol.

2. `Startup-config`: The startup-config is a copy of the running-config that is stored in non-volatile memory on the device, such as flash memory. This means that the startup-config will persist even if the device is rebooted or powered off. <span style="color:#d19a66">**The `startup-config` is loaded into the `running-config` when the device is first booted or when the command `reload` is issued.**</span> The startup-config can be viewed using the command show startup-config.

Example:

```sh
Router# show startup-config
Building configuration...

Current configuration : 983 bytes
!
version 15.4
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
!
hostname RouterA
!
interface GigabitEthernet0/0
 ip address 10.10.10.1 255.255.255.0
 no shutdown
!
ip routing
!
router eigrp 100
 network 10.0.0.0
!
end
```

In this example, the user can see that the startup-config is exactly the same as the running-config.

It is important to regularly save the running-config to the startup-config using the command `copy running-config startup-config` or `write memory` in order to ensure that the device's configuration is not lost in the event of a power failure or reboot. This is a best practice to have a backup of the configuration and restore it if needed.

<br>

### Service Password Encryption

The "service password-encryption" command is used on Cisco routers and switches to encrypt all plaintext passwords that are stored in the device's configuration file. This includes passwords for local user accounts, as well as passwords for remote access protocols such as Telnet and SSH.

When a password is encrypted, it is transformed into a scrambled version of the original, making it more difficult for unauthorized users to read it if they gain access to the configuration file.

Here's an example of how to use the "service password-encryption" command:

```sh
Router#configure terminal
Router(config)#service password-encryption
Router(config)#end
```

This will enable password encryption on the device. Once enabled, any new passwords that are set will be encrypted automatically.

It's important to note that while this command can help to secure passwords, it is not a foolproof method of protection. Encrypted passwords can still be decrypted using specialized tools and techniques, so it's important to use strong, complex passwords and to use other security measures in conjunction with password encryption.

<br>

### Enable Secret

The "enable secret" command in Cisco is used to set a password for the privileged EXEC mode (also known as enable mode) on a Cisco device. This password is used to restrict access to the device's privileged commands and features.

When you set an enable secret password, it is encrypted using a one-way hashing algorithm and stored in the device's configuration file. Unlike the "enable password" command, the enable secret password is not displayed in the configuration file and is much more secure.

Here's an example of how to use the "enable secret" command:

```sh
Router#configure terminal
Router(config)#enable secret cisco
Router(config)#end
```

This will set the enable secret password to "cisco".

It's important to note that the "enable secret" password takes precedence over the "enable password" command. If both are set, the "enable secret" password is used for authentication.

Additionally, "enable secret" command also support the use of type 5 and type 8 encryption. Type 5 is considered as the most secured encryption which is the SHA-256 algorithm, Type 8 uses the PBKDF2 algorithm.

For example:

```sh
Router#configure terminal
Router(config)#enable secret 5 $1$jGq7$Mg.8nhFVu/fBz/7bRc/
Router(config)#end
```

This will set the enable secret password with type 5 encryption using the hashed value provided.

It's important to mention that the enable secret command is not reversible, meaning the original password cannot be retrieved once it is set. Therefore, it is important to keep a record of the password in a secure location.
