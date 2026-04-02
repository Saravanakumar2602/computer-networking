# Protocols in Computer Networks

## Introduction

Protocols are formal rules and conventions that define how data is transmitted and received across networks. They ensure that devices from different manufacturers and platforms can communicate reliably and efficiently. Protocols are defined and standardized by organizations such as the Internet Society (ISOC), IETF, and IEEE.

---

## Why Are Protocols Important?

- **Interoperability:** Allow devices and software from different vendors to communicate.
- **Reliability:** Ensure data is delivered accurately and in the correct order.
- **Efficiency:** Optimize network resource usage and prevent congestion.
- **Security:** Provide mechanisms for authentication, encryption, and integrity.

---

## Types of Protocols

### 1. Transmission Control Protocol (TCP)

**TCP** is a connection-oriented protocol that provides reliable, ordered, and error-checked delivery of data between applications. It is widely used for applications where data integrity is critical, such as web browsing, email, and file transfers.

**Key Features:**
- Connection establishment (3-way handshake)
- Reliable delivery (acknowledgments, retransmissions)
- Ordered data transfer (sequence numbers)
- Flow and congestion control

**Example:**
When you load a website (HTTP), TCP ensures all parts of the webpage arrive correctly and in order.

**Diagram:**

```
Client                Server
	|------SYN--------->|
	|<-----SYN-ACK------|
	|------ACK--------->|
	|   Connection Established
```

---

### 2. User Datagram Protocol (UDP)

**UDP** is a connectionless protocol that provides fast, but unreliable, delivery of data. It is used for applications where speed is more important than reliability, such as video streaming, online gaming, and VoIP.

**Key Features:**
- No connection setup
- No guarantee of delivery, order, or duplication protection
- Lower overhead than TCP

**Example:**
In a video call, if a few packets are lost, the call continues without waiting for retransmission.

---

### 3. Hypertext Transfer Protocol (HTTP)

**HTTP** is the foundation of data communication on the World Wide Web. It defines how messages are formatted and transmitted, and how web servers and browsers should respond to various commands.

**Key Features:**
- Stateless protocol
- Uses TCP (port 80)
- Supports methods like GET, POST, PUT, DELETE

**Example:**
When you visit a website, your browser sends an HTTP GET request to the server, which responds with the webpage content.

---

### 4. File Transfer Protocol (FTP)

**FTP** is used to transfer files between computers on a network. It uses separate control (port 21) and data (port 20) connections.

**Key Features:**
- Supports authentication
- Can transfer large files
- Not secure by default (use SFTP/FTPS for security)

---

### 5. Simple Mail Transfer Protocol (SMTP)

**SMTP** is used to send emails from clients to servers or between servers. It operates over TCP port 25.

**Key Features:**
- Push protocol (sends emails)
- Works with POP3/IMAP for receiving

---

### 6. Post Office Protocol 3 (POP3) & Internet Message Access Protocol (IMAP)

**POP3** downloads emails from the server to the client and usually deletes them from the server. **IMAP** keeps emails on the server, allowing access from multiple devices.

**Key Features:**
- POP3: Simple, offline access
- IMAP: Synchronization across devices

---

### 7. Dynamic Host Configuration Protocol (DHCP)

**DHCP** automatically assigns IP addresses and other network configuration to devices on a network.

**Key Features:**
- Reduces manual configuration
- Supports dynamic, static, and reserved IP assignments

---

### 8. Domain Name System (DNS)

**DNS** translates human-readable domain names (like www.example.com) into IP addresses.

**Key Features:**
- Hierarchical, distributed database
- Critical for internet usability

---

### 9. Secure Shell (SSH)

**SSH** provides secure remote login and command execution over an unsecured network.

**Key Features:**
- Encrypts all traffic
- Uses public-key authentication

---

### 10. Telnet

**Telnet** allows remote command-line access to another computer. It is insecure and largely replaced by SSH.

**Key Features:**
- Plaintext communication
- Uses TCP port 23

---

### 11. Other Protocols

- **VNC:** Remote desktop sharing
- **SNMP:** Network management
- **HTTPS:** Secure HTTP (uses SSL/TLS)
- **NTP:** Network time synchronization

---

## Sockets

A **socket** is a software endpoint that establishes bidirectional communication between devices over a network. It is defined by an IP address and a port number.

**Example:**
When your browser connects to a web server, it opens a socket to the server's IP address on port 80 (HTTP).

---

## Ports

Ports are logical endpoints for network communication. They allow multiple services to run on a single device.

**Port Ranges:**
- **Well-known ports:** 0–1023 (HTTP: 80, HTTPS: 443, FTP: 21)
- **Registered ports:** 1024–49151 (MongoDB: 27017)
- **Dynamic/private ports:** 49152–65535 (used for temporary connections)

**Total number of ports:** 2^16 = 65,536

---

## Ephemeral Ports

Ephemeral ports are temporary ports assigned by the operating system for client-side communications. They are used for the duration of a connection and released afterward.

**Example:**
When you visit a website, your browser uses an ephemeral port to connect to the server's port 80.

---

## Protocol Stack Example

When you send an email:
1. **Application Layer:** SMTP formats the message.
2. **Transport Layer:** TCP ensures reliable delivery.
3. **Internet Layer:** IP routes the packet.
4. **Link Layer:** Ethernet transmits the data.

---

## Summary Table

| Protocol | Layer | Purpose | Port |
|----------|-------|---------|------|
| HTTP     | Application | Web browsing | 80 |
| HTTPS    | Application | Secure web | 443 |
| FTP      | Application | File transfer | 21 |
| SMTP     | Application | Email sending | 25 |
| POP3     | Application | Email receiving | 110 |
| IMAP     | Application | Email sync | 143 |
| DNS      | Application | Name resolution | 53 |
| DHCP     | Application | IP assignment | 67/68 |
| SSH      | Application | Secure remote login | 22 |
| Telnet   | Application | Remote login | 23 |
| TCP      | Transport | Reliable delivery | - |
| UDP      | Transport | Fast, unreliable | - |

---

## Further Reading

- [IETF RFCs](https://www.ietf.org/standards/rfcs/)
- [Wikipedia: List of network protocols](https://en.wikipedia.org/wiki/List_of_network_protocols_(OSI_model))
