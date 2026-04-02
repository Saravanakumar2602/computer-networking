# Network Layer: Routing and Addressing

## Introduction

The **Network Layer** (Layer 3 in OSI, Layer 2 in TCP/IP) is responsible for routing packets across networks, addressing, and managing traffic between devices that are not directly connected.

---

## Key Functions

- **Logical Addressing:** Assigns unique IP addresses to devices
- **Routing:** Determines the best path for data to travel
- **Packet Forwarding:** Moves packets from source to destination
- **Fragmentation:** Splits large packets to fit network constraints

---

## Routers and Routing

**Routers** are devices that connect different networks and forward packets based on IP addresses.

**Routing Table:**
- List of routes to different network destinations
- Used by routers to decide where to send packets

**Control Plane vs Data Plane:**
- Control plane: Makes routing decisions (OSPF, BGP)
- Data plane: Forwards packets based on those decisions

---

## Routing Types

- **Static Routing:** Manually configured routes; simple but not scalable
- **Dynamic Routing:** Uses protocols to update routes automatically (OSPF, RIP, BGP)

**Example:**
Home router uses static routes; ISPs use dynamic routing

---

## IPv4 and IPv6

### IPv4
- 32-bit address (e.g., 192.168.1.1)
- 4.3 billion addresses
- Classes A-E, private/reserved ranges

### IPv6
- 128-bit address (e.g., 2001:db8::1)
- 3.4×10^38 addresses
- No NAT required, built-in security

---

## Subnetting and CIDR

**Subnetting:** Divides a network into smaller segments for efficiency and security

**Subnet Mask Example:** 255.255.255.0 (Class C)
**CIDR Notation:** 192.168.1.0/24

**Private IP Ranges:**
- 10.0.0.0/8
- 172.16.0.0/12
- 192.168.0.0/16

---

## Packets and TTL

- **Packet:** Unit of data at the network layer
- **TTL (Time to Live):** Prevents infinite loops; decremented at each hop

---

## Middleboxes and Firewalls

- **Middleboxes:** Devices that inspect, modify, or filter traffic (firewalls, NAT, proxies)
- **Firewalls:**
	- **Stateless:** Inspects packets individually
	- **Stateful:** Tracks connection state

---

## NAT (Network Address Translation)

**NAT** maps private IP addresses to public IPs for internet access.

**Types:**
- Static NAT: One-to-one mapping
- Dynamic NAT: Pool of public IPs
- PAT (Port Address Translation): Many-to-one (most common)

---

## DHCP (Dynamic Host Configuration Protocol)

**DHCP** automatically assigns IP addresses, subnet masks, gateways, and DNS servers.

**Process:**
1. Discover
2. Offer
3. Request
4. Acknowledge

---

## ICMP (Internet Control Message Protocol)

Used for diagnostics (ping, traceroute), error reporting, and network management.

---

## ARP (Address Resolution Protocol)

Maps IP addresses to MAC addresses for local delivery.

---

## Summary Table

| Concept   | Purpose                  | Example/Protocol |
|-----------|--------------------------|------------------|
| Routing   | Path selection           | OSPF, BGP, RIP   |
| Addressing| Unique device IDs        | IPv4, IPv6       |
| NAT       | Private/public mapping   | PAT, Static NAT  |
| DHCP      | Auto IP assignment       | DHCP             |
| ICMP      | Diagnostics              | ping, traceroute |
| ARP       | IP to MAC mapping        | ARP              |

---

## Further Reading

- [Network Layer (Cloudflare)](https://www.cloudflare.com/learning/network-layer/what-is-the-network-layer/)
