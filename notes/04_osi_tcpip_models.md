# OSI & TCP/IP Models: The Blueprint of Networking

## Introduction

Network models provide a framework for understanding how data moves from one device to another. The two most important models are the **OSI Model** and the **TCP/IP Model**.

---

## OSI Model (Open Systems Interconnection)

The OSI model is a conceptual framework with **seven layers**, each with specific functions. It helps standardize networking protocols and troubleshooting.

### The 7 Layers of OSI

1. **Physical Layer**
	- Transmits raw bits (0s and 1s) over physical media (cables, radio waves)
	- Defines voltage, connectors, pin layout
	- **Example:** Ethernet cables, Wi-Fi signals

2. **Data Link Layer**
	- Responsible for node-to-node data transfer
	- Uses MAC addresses for local delivery
	- Error detection/correction (frames)
	- **Example:** Switches, Ethernet, Wi-Fi

3. **Network Layer**
	- Handles routing of packets across networks
	- Uses IP addresses
	- **Example:** Routers, IPv4, IPv6

4. **Transport Layer**
	- Ensures reliable or fast delivery (TCP/UDP)
	- Segmentation, flow control, error recovery
	- **Example:** TCP, UDP, port numbers

5. **Session Layer**
	- Manages sessions (connections) between applications
	- Controls dialog, synchronization
	- **Example:** Remote procedure calls, NetBIOS

6. **Presentation Layer**
	- Translates, encrypts, compresses data
	- Ensures data is readable by the receiving system
	- **Example:** SSL/TLS, JPEG, ASCII

7. **Application Layer**
	- Closest to the user
	- Provides network services to applications
	- **Example:** HTTP, FTP, SMTP, DNS

**Diagram:**
```
| 7. Application   |
| 6. Presentation  |
| 5. Session       |
| 4. Transport     |
| 3. Network       |
| 2. Data Link     |
| 1. Physical      |
```

---

## TCP/IP Model

The TCP/IP model is the foundation of the modern internet. It has **four layers** and is more practical than the OSI model.

### The 4 Layers of TCP/IP

1. **Network Interface (Link) Layer**
	- Handles physical transmission (Ethernet, Wi-Fi)
2. **Internet Layer**
	- Handles logical addressing and routing (IP)
3. **Transport Layer**
	- Provides end-to-end communication (TCP, UDP)
4. **Application Layer**
	- Provides network services to applications (HTTP, FTP, DNS)

**Diagram:**
```
| 4. Application   |
| 3. Transport     |
| 2. Internet      |
| 1. Network Intf. |
```

---

## OSI vs TCP/IP: Comparison Table

| OSI Layer         | TCP/IP Layer      | Example Protocols      |
|-------------------|------------------|------------------------|
| Application       | Application      | HTTP, FTP, SMTP, DNS   |
| Presentation      | Application      | SSL, JPEG, ASCII       |
| Session           | Application      | NetBIOS, RPC           |
| Transport         | Transport        | TCP, UDP               |
| Network           | Internet         | IP, ICMP, ARP          |
| Data Link         | Network Interface| Ethernet, Wi-Fi        |
| Physical          | Network Interface| Cables, radio waves    |

---

## Real-World Example: Sending an Email

1. **Application Layer:** SMTP formats the message
2. **Transport Layer:** TCP ensures reliable delivery
3. **Internet Layer:** IP routes the packet
4. **Network Interface:** Ethernet transmits the data

---

## Client-Server vs Peer-to-Peer Models

### Client-Server
- Central server provides resources/services to multiple clients
- Easy to manage, secure, but single point of failure

**Example:**
Web browsing, email

### Peer-to-Peer (P2P)
- Devices (peers) share resources directly
- No central server, more resilient, but harder to manage

**Example:**
File sharing (BitTorrent), blockchain

---

## Further Reading

- [OSI Model Explained (Cloudflare)](https://www.cloudflare.com/learning/network-layer/what-is-the-osi-model/)
- [TCP/IP Model (Wikipedia)](https://en.wikipedia.org/wiki/Internet_protocol_suite)
