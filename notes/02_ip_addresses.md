# IP Addresses: The Foundation of Networking

## What is an IP Address?

An **IP address** (Internet Protocol address) is a unique identifier assigned to every device connected to a network. It allows devices to locate and communicate with each other, much like a postal address for computers.

**Example:**
- 192.168.1.10 (IPv4)
- 2001:0db8:85a3:0000:0000:8a2e:0370:7334 (IPv6)

---

## Types of IP Addresses

### 1. Local (Private) IP Address

- Used within a local network (home, office, business)
- Not routable over the public internet
- Enables communication between devices on the same local network

**Common Private IP Ranges:**
- 10.0.0.0 – 10.255.255.255
- 172.16.0.0 – 172.31.255.255
- 192.168.0.0 – 192.168.255.255

**Example:**
- Your laptop: 192.168.1.5
- Your phone: 192.168.1.6

### 2. Global (Public) IP Address

- Assigned by your Internet Service Provider (ISP)
- Routable over the public internet
- Used for communication with external networks (websites, cloud services)

**Example:**
- Your home router: 49.205.67.123

---

## How IP Addresses Work

When you connect to the internet, your device is assigned a local IP by your router. The router itself has a public IP assigned by your ISP. The router uses **NAT** (Network Address Translation) to map local devices to the public IP.

**Diagram:**

```
Internet <----> [Public IP: 49.205.67.123] Router [Local IP: 192.168.1.1] <----> Devices (192.168.1.5, 192.168.1.6)
```

---

## Network Address Translation (NAT)

NAT allows multiple devices on a local network to share a single public IP address. It keeps track of which device made each request using port numbers.

**Why NAT?**
- Conserves public IP addresses
- Adds a layer of security (devices are not directly exposed)

**Types of NAT:**
- Static NAT: One-to-one mapping
- Dynamic NAT: Many-to-many mapping
- PAT (Port Address Translation): Many-to-one mapping (most common)

---

## Internet Service Provider (ISP)

An **ISP** is a company that provides internet access to individuals and organizations. Examples: Airtel, Tata, Jio, Comcast.

**Role of ISP:**
- Assigns public IP addresses
- Connects your home or business to the global internet

---

## IP Address Classes (IPv4)

IPv4 addresses are divided into classes (A, B, C, D, E) based on their leading bits and intended use.

| Class | Range | Example Use |
|-------|----------------------|-------------------|
| A     | 1.0.0.0 – 126.255.255.255 | Large networks |
| B     | 128.0.0.0 – 191.255.255.255 | Medium networks |
| C     | 192.0.0.0 – 223.255.255.255 | Small networks |
| D     | 224.0.0.0 – 239.255.255.255 | Multicast |
| E     | 240.0.0.0 – 255.255.255.255 | Reserved |

---

## IPv6 Addresses

IPv6 was introduced to solve the exhaustion of IPv4 addresses. It uses 128 bits, allowing for 3.4×10^38 unique addresses.

**Format:**
- 2001:0db8:85a3:0000:0000:8a2e:0370:7334

**Advantages:**
- Vast address space
- Built-in security (IPsec)
- No need for NAT

---

## Subnetting and Subnet Masks

Subnetting divides a network into smaller segments, improving efficiency and security.

**Subnet Mask Example:**
- 255.255.255.0 (Class C)
- CIDR notation: 192.168.1.0/24

**Usable Hosts Formula:**
- Usable hosts = 2^(32 - subnet bits) - 2

---

## Data Transfer Rates

- **Mbps:** Megabits per second (1,000,000 bits/s)
- **Gbps:** Gigabits per second (1,000,000,000 bits/s)
- **Kbps:** Kilobits per second (1,000 bits/s)

**Note:** 1 byte = 8 bits. Mbps is not megabytes per second!

---

## Reserved and Special IP Addresses

- 127.0.0.1: Loopback (localhost)
- 0.0.0.0: Default route
- 255.255.255.255: Broadcast

---

## Further Reading

- [What is an IP Address? (Cloudflare)](https://www.cloudflare.com/learning/network-layer/what-is-an-ip-address/)
- [IPv6 Explained (Wikipedia)](https://en.wikipedia.org/wiki/IPv6)
