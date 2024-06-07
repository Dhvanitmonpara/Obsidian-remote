### Remember that
| Layer     | Data format                | Protocol                          |
| --------- | -------------------------- | --------------------------------- |
| Transport | Data transfers in Segments | HTTP, DHCP, POP etc.              |
| Network   | Data transfers in Packets  | TCP/UDP                           |
| Data Link | Data transfers in Frames   | IP which contains Network address |

# Routing


![[unicast_routing.jpg]]

So many routes are connected in between is called network. Every route has its own network address, which allows them to send data packets. This works like path finding algorithm.

When you send a packet to the receiver router will  check it with the destination address through forwarding table ([DNS forwarding table is like data structure](https://www.geeksforgeeks.org/routing-tables-in-computer-network/)), If it isn't found same then forward it to next router, This is called[ Hop-by-Hop routing](https://www.researchgate.net/figure/Source-Routing-vs-Hop-by-Hop-routing-In-source-routing-shown-left-source-node-u-on_fig1_325638695#:~:text=In%20hop%2Dby%2Dhop%20routing,sinks%20are%20the%20designated%20servers.&text=We%20study%20a%20problem%20of,over%20an%20arbitrary%20network%20topology.).

Every device has its own MAC address.

![[cn_purple_fig4.jpg]]

Network address lives in IP address. Refer to [GeeksForGeeks](https://www.geeksforgeeks.org/what-is-a-network-address/), [Tutorial Point](https://www.tutorialspoint.com/structure-and-types-of-ip-address) or [MS docs](https://learn.microsoft.com/en-us/troubleshoot/windows-client/networking/tcpip-addressing-and-subnetting)

**Note:** Network address and subnet mask (Subnet ID) are same.

Control plane creates this routing tables which is superset of forwarding tables.

### Types of Routing

- **Static routing:** This is done by adding address manually which is time consuming.
- **Dynamic routing:** This is path finding algorithm.

Visit [Tutorial point](https://www.tutorialspoint.com/data_communication_computer_network/network_layer_routing.htm) for more information.

# IP (Internet Protocol)

It lies in network layer, Router works on [subnet mask](https://www.geeksforgeeks.org/role-of-subnet-mask/), There were group of IPs which is routing from Hop-to-Hop (Like a path finding algorithm), Not individual router does it. This routes are IPs called subnet.

![[internet-architecture.svg]]

### Classes of IP address

| Class | Range                       |
| ----- | --------------------------- |
| A     | 0.0.0.0 - 127.255.255.255   |
| B     | 128.0.0.0 - 191.255.255.255 |
| C     | 192.0.0.0 - 223.255.255.255 |
| D     | 224.0.0.0 - 239.255.255.255 |
| E     | 240.0.0.0 - 255.255.255.255 |

### IPv4

IPv4: 36 bit architecture, 4 words

![[0_o26gkcQ5xnr4gI0L.png]]

- 1 byte == 8 bits
- It includes IP version, Identification, Flags, Protocols, Checksums, Address, TTL etc.
- Size: 2^23  == 4294967296

### IPv6

IPv6: 128 bit architecture

![[it04-01-ipv-6-structure-and-format.PNG]]



Refer [Ms Docs](https://learn.microsoft.com/en-us/azure/architecture/networking/guide/ipv6-architecture) for more information.