# Network Types & Topologies

## Introduction

Computer networks can be classified by their size, coverage, and design. Understanding network types and topologies is essential for designing, troubleshooting, and scaling networks.

---

## Types of Networks

### 1. Local Area Network (LAN)
- Covers a small area (home, office, school)
- High speed, low latency
- Technologies: Ethernet, Wi-Fi

**Example:**
Your home Wi-Fi network connecting your phone, laptop, and smart TV.

### 2. Metropolitan Area Network (MAN)
- Spans a city or large campus
- Connects multiple LANs
- Technologies: Fiber optics, leased lines

**Example:**
City-wide Wi-Fi or a university campus network.

### 3. Wide Area Network (WAN)
- Covers large geographic areas (cities, countries, continents)
- Connects multiple LANs and MANs
- Technologies: Optical fiber, satellite, MPLS

**Example:**
The internet, or a bank's network connecting branches across the country.

---

## Network Topologies

Network topology refers to the physical or logical arrangement of devices and cables.

### 1. Bus Topology
- All devices share a single communication line (the bus)
- Simple, cheap, but prone to collisions and single point of failure

**Diagram:**
```
[PC1]---[ ]---[ ]---[ ]---[PC2]
				 |    |    |
			(bus backbone)
```

### 2. Ring Topology
- Devices connected in a closed loop
- Data travels in one direction
- Failure of one device can disrupt the network

**Diagram:**
```
[PC1]---[PC2]
	|       |
[PC4]---[PC3]
```

### 3. Star Topology
- All devices connect to a central hub or switch
- Easy to manage, isolate faults
- Hub/switch failure brings down the network

**Diagram:**
```
			[PC2]
				|
 [PC1]--[Hub]--[PC3]
				|
			[PC4]
```

### 4. Tree Topology
- Hierarchical, combines star and bus
- Used in large organizations
- Failure at higher levels affects all connected branches

**Diagram:**
```
				[Root]
				 /   \
		 [Hub1] [Hub2]
		 /   \     \
 [PC1] [PC2] [PC3]
```

### 5. Mesh Topology
- Every device connects to every other device
- High reliability, expensive, complex
- Used in backbone networks, critical systems

**Diagram:**
```
 [A]---[B]
	| \ / |
 [C]---[D]
```

---

## Physical & Wireless Media

- **Physical:** Twisted pair cables, coaxial cables, optical fiber
- **Wireless:** Wi-Fi, Bluetooth, 3G/4G/5G, satellite

**Example:**
Wi-Fi uses radio waves; fiber optics use light pulses.

---

## Choosing a Topology

- **Bus:** Small, simple networks
- **Star:** Most common for modern LANs
- **Ring:** Legacy, rarely used
- **Mesh:** High-availability, backbone networks

---

## Further Reading

- [Network Topology (Cisco)](https://www.cisco.com/c/en/us/solutions/enterprise-networks/what-is-network-topology.html)
