# Client-server Architecture

Client-server architecture is a fundamental network model that divides tasks and responsibilities between two types of programs: clients and servers. This division of labor streamlines network operations and makes it efficient to manage resources and serve multiple users.

**Key Players:**

- **Clients:** These are software applications that initiate requests for resources or services from a server. They typically run on user devices like personal computers, laptops, or mobile phones. Examples include web browsers, email clients, and online gaming applications.
- **Servers:** Powerful computers that store data and applications. They listen for requests from clients, process them, and send back the requested information or perform the desired action. Servers can host a variety of services, including web servers, file servers, email servers, and database servers.

![[client-server-architecture.png]]

**Communication Cycle:**

The client-server architecture follows a well-defined communication cycle:

1. **Client Request:** The client initiates the interaction by sending a request to the server. This request specifies the service or data needed. The request may include details like the desired web page, a specific file to download, or an email to be sent.
2. **Server Processing:** Upon receiving the request, the server interprets it and locates the requested resource. This might involve accessing a database, retrieving a web page, or performing a specific operation.
3. **Server Response:** Once the server processes the request, it sends a response back to the client. The response could be the requested data (e.g., a web page), a confirmation message (e.g., email sent successfully), or an error message if the request couldn't be fulfilled.
4. **Client Action:** The client receives the server's response and takes appropriate action based on it. This might involve displaying the requested information on the screen, saving a downloaded file, or informing the user of an error.

**Benefits of Client-Server Architecture:**

- **Centralized Management:** Data is stored and managed on a central server, simplifying data backup, security, and access control.
- **Scalability:** Servers can handle multiple client requests simultaneously, making the architecture suitable for large networks with many users.
- **Resource Sharing:** Clients can share resources like printers, databases, and applications hosted on the server, eliminating the need for each device to have its own copy.
- **Improved Performance:** Servers can be more powerful machines than client devices, offloading processing tasks and improving overall network efficiency.
- **Security:** Centralized data storage on the server allows for robust security measures to be implemented, protecting sensitive information.

**Applications of Client-Server Architecture:**

Client-server architecture is widely used in various applications like:

- **World Wide Web:** Web browsers (clients) request web pages from web servers (servers).
- **Email:** Email client software (clients) send and receive emails through email servers (servers).
- **Online Banking:** Banking apps (clients) interact with a bank's server for account access and transactions.
- **Database Management:** Database applications (clients) access and manage data stored on a database server (server).
- **Network File Sharing:** Client devices can access and share files stored on a central file server (server).

**Types of Client-Server Architecture:**

There are various types of client-server architecture, each catering to specific needs:

- **Two-Tier Architecture:** The simplest form with clients directly interacting with a server.
- **Three-Tier Architecture:** Introduces an application server layer between clients and the database server, handling business logic and database access.
- **N-Tier Architecture:** A more complex architecture with multiple layers of servers, each performing specialized tasks.

In conclusion, client-server architecture provides a structured and efficient way to manage resources and deliver services on a network. By dividing tasks between clients and servers, this architecture offers scalability, security, and efficient resource utilization, making it a cornerstone of modern network infrastructure.

# Peer to Peer Architecture (P2P)

Peer-to-peer (P2P) architecture is a decentralized network model where devices, or peers, communicate directly with each other to share resources and services. Unlike the client-server model with dedicated servers, all devices in a P2P network have equal capabilities and responsibilities.

**Conceptual Shift:**

Imagine a network without a central authority, where devices collaborate and share resources directly. This is the essence of P2P architecture. Each device acts as both a client, requesting resources, and a server, providing resources to others.

![[client-server-vs-p2p.png]]

**Benefits of P2P Architecture:**

- **Decentralization:** No single point of failure; the network continues to function even if some peers become unavailable.
- **Scalability:** The network can easily grow by adding more peers without requiring additional central server infrastructure.
- **Efficiency:** Utilizes the combined resources of all peers, potentially reducing reliance on expensive central servers.
- **Direct Communication:** Enables faster data transfer speeds as data travels directly between peers.

**Applications of P2P Architecture:**

- **File Sharing:** Popular for sharing large files like music, movies, and software. Examples include BitTorrent networks.
- **Collaboration:** Used for real-time communication and collaboration tools. Examples include video conferencing and online gaming applications.
- **Blockchain Technology:** The foundation of cryptocurrencies like Bitcoin, where all transactions are verified and recorded on a distributed ledger across all participating nodes.

**Challenges of P2P Architecture:**

- **Security:** Without a central authority, ensuring data security and access control can be more complex.
- **Scalability (Double-Edged Sword):** While the network can grow easily, managing large-scale content discovery and efficient resource allocation can be challenging.
- **Content Legality:** Copyright infringement can be an issue in file-sharing P2P networks.

**Types of P2P Architecture:**

- **Pure P2P:** All peers have equal roles and responsibilities for searching, sharing, and routing data.
- **Centralized P2P:** A central server helps with tasks like indexing content and facilitating peer discovery, but doesn't store the actual data.
- **Hybrid P2P:** Combines elements of both pure P2P and centralized P2P, offering a balance between decentralization and efficiency.

**In Conclusion:**

P2P architecture offers a powerful and flexible way to share resources and build collaborative networks. However, it's important to consider its advantages and disadvantages to determine its suitability for specific applications. As technology evolves, P2P architecture will likely continue to play a significant role in distributed computing and resource sharing.


# Networking Devices

These devices play a vital role in connecting devices and managing data flow on a network. Here's a breakdown of each device and its function:

### Repeaters:

- **Function:** Signal boosters. They amplify weak network signals to extend their reach over longer distances. Often used in coaxial cable networks.
- **Drawbacks:** Can amplify noise along with the signal, potentially degrading signal quality.
- **Use Case:** Extending the range of a network segment where the signal has become weak.

### Hubs (Legacy Devices):

- **Function:** Simple data distribution points. They act as a central connection point for devices on a network, broadcasting any received data to all connected devices.
- **Drawbacks:** Inefficient for larger networks as broadcasts create congestion, especially with heavy traffic.
- **Use Case:** Rarely used in modern networks due to limitations. They might be found in older, very small networks.

### Bridges:

- **Function:** Connect separate network segments that use the same protocol (like Ethernet). They filter and forward data packets based on their MAC address, improving network efficiency compared to hubs.
- **Drawbacks:** Limited functionality compared to switches. They cannot segment networks based on IP addresses (Layer 3) and can create bottlenecks with heavy traffic.
- **Use Case:** Connecting two similar LAN segments that need to be separated but still allow some communication.

### Switches:

- **Function:** Intelligent data forwarding devices. They operate at the data link layer (using MAC addresses) and learn the MAC addresses of devices connected to their ports. When a device sends data, the switch forwards it only to the specific port of the intended recipient, reducing congestion and improving network performance.
- **Benefits:** More efficient than hubs and bridges, offering better performance and reduced network congestion.
- **Use Case:** Found in most modern networks to connect devices within a network segment and forward data efficiently.

### Routers:

- **Function:** The traffic directors of your network. Routers connect different networks (like your home network to the internet) and forward packets based on their destination IP addresses. They maintain routing tables that map IP addresses to network paths, ensuring data reaches its intended destination across different networks.
- **Benefits:** Essential for connecting networks and enabling communication between devices on different networks (e.g., your home network and the internet).
- **Use Case:** A core component for connecting networks and enabling internet access.

### Gateways:

- **Function:** Act as a general term for devices that provide access to another network. Routers can be considered a type of gateway, but gateways can have a broader meaning. For example, an email gateway might translate emails between different email systems.
- **Benefits:** Provide a connection point or protocol conversion between different networks.
- **Use Case:** Routers are a common example, but gateways can encompass various devices that enable communication between dissimilar networks.

### Brouters (Rare):

- **Function:** A combination of a bridge and a router. They can operate at the data link layer (like a bridge) and the network layer (like a router). This allows them to connect networks using different protocols and forward data packets based on MAC addresses or IP addresses.
- **Drawbacks:** Rarely used in modern networks as router functionality is often sufficient.
- **Use Case:** In specific scenarios where connecting networks with different protocols and needing both bridge and router functionalities.

# Protocols

### TCP/IP:
- [[HTTP-HTTPS]]
- [[DHCP]]
- [[FTP]]
- [[SMTP]]
- [[POP-IMAP]]
- [[SSH]]
- [[VNC]]

[[TELNET]] (Outside of TCP/IP)
# UDP
Stateless Protocol