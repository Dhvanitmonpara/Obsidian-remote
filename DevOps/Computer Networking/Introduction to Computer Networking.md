## What is a Network?

- A collection of interconnected devices that can communicate with each other.
- Devices can be computers, printers, servers, etc.
- Nodes: Individual devices on the network.

## Client-Server Architecture (In Short)

When a client pings a specific domain name, it sends a request to a DNS server (Domain Name System server) to translate the domain name into an IP address. The DNS server responds with the corresponding IP address. The client can then use this IP address to send a ping request directly to the target server. If the ping is successful, the target server sends a response message back to the client, indicating that it is reachable.

![[client-server-architecture.png]]

## Data Transmission

- Large messages are broken down into packets for efficient transfer.
- Packets contain data, header information (source & destination addresses), and error checking.

### The OSI Model

- A conceptual framework for network communication.
- Divides communication into 7 layers with specific functions.
    - Physical: Handles physical transmission of data bits (cables, wires).
    - Data Link: Ensures reliable data delivery at the link level (error detection/correction).
    - Network: Routes packets across the network (e.g., IP protocol).
    - Transport: Provides reliable data transfer between applications (e.g., TCP, UDP).
    - Session: Establishes, manages, and terminates sessions between applications.
    - Presentation: Deals with data format presentation and encryption/decryption.
    - Application: Provides network services to applications (e.g., HTTP, FTP). HTTP is used by W3 (World Wide Web).