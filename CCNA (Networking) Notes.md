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

# Ethernet frame
