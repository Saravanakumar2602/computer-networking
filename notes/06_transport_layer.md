# Transport Layer: Reliable Delivery and Speed

## Introduction

The **Transport Layer** (Layer 4 in OSI, Layer 3 in TCP/IP) is responsible for end-to-end communication between applications on different devices. It ensures data is delivered reliably, in order, and without duplication—or, for some applications, as quickly as possible.

---

## Key Functions

- **Segmentation and Reassembly:** Splits large data into smaller segments for transmission; reassembles them at the destination.
- **Multiplexing/Demultiplexing:** Uses port numbers to direct data to the correct application.
- **Error Detection and Recovery:** Ensures data integrity and retransmits lost segments (TCP).
- **Flow and Congestion Control:** Prevents overwhelming the receiver or the network.

---

## TCP (Transmission Control Protocol)

**TCP** is a connection-oriented protocol that provides reliable, ordered, and error-checked delivery of data.

**Key Features:**
- Connection establishment (3-way handshake)
- Sequence numbers and acknowledgments
- Retransmission of lost packets
- Flow control (windowing)
- Congestion control (slow start, congestion avoidance)

**3-Way Handshake:**
```
Client                Server
	|------SYN--------->|
	|<-----SYN-ACK------|
	|------ACK--------->|
	|   Connection Established
```

**Example:**
Downloading a file from a website—TCP ensures every byte arrives in order.

---

## UDP (User Datagram Protocol)

**UDP** is a connectionless protocol that provides fast, but unreliable, delivery of data.

**Key Features:**
- No connection setup
- No guarantee of delivery, order, or duplication protection
- Lower overhead than TCP

**Header Fields:**
- Source port (2 bytes)
- Destination port (2 bytes)
- Length (2 bytes)
- Checksum (2 bytes)

**Max Data Size:** 65527 bytes (65535 - 8)

**Example:**
Video streaming, online gaming, DNS queries

---

## Multiplexing and Demultiplexing

- **Multiplexing:** Combining data from multiple applications for transmission
- **Demultiplexing:** Delivering incoming data to the correct application using port numbers

**Diagram:**
```
App1  App2  App3
	|     |     |
 [Transport Layer]
	|     |     |
 [Network Layer]
```

---

## Error Detection: Checksum

Both TCP and UDP use checksums to detect errors in transmitted data. If the checksum does not match, the packet is discarded.

---

## Flow and Congestion Control

- **Flow Control:** Prevents sender from overwhelming receiver (TCP window size)
- **Congestion Control:** Adjusts sending rate based on network conditions (TCP slow start, congestion avoidance)

---

## Summary Table

| Protocol | Connection | Reliable | Ordered | Use Case           |
|----------|------------|----------|---------|--------------------|
| TCP      | Yes        | Yes      | Yes     | Web, email, file   |
| UDP      | No         | No       | No      | Video, gaming, DNS |

---

## Further Reading

- [TCP vs UDP (Cloudflare)](https://www.cloudflare.com/learning/ddos/glossary/user-datagram-protocol-udp/)
