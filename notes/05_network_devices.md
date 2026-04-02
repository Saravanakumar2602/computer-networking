# Network Devices: Building Blocks of Communication

## Introduction

Network devices are hardware components that connect computers, manage traffic, and ensure data reaches its destination. Each device operates at specific layers of the OSI model and serves unique functions.

---

## 1. Repeater

- **Function:** Amplifies and retransmits weak signals to extend network range.
- **Layer:** Physical (Layer 1)
- **Use Case:** Extending Ethernet or Wi-Fi coverage in large buildings.

**Diagram:**
```
[PC1]---[Repeater]---[PC2]
```

---

## 2. Hub

- **Function:** Connects multiple devices in a LAN, broadcasts data to all ports.
- **Layer:** Physical (Layer 1)
- **Types:**
	- Passive: No amplification
	- Active: Amplifies signals
	- Multi-port: More than 4 ports
- **Disadvantage:** Causes network congestion (broadcast storms), outdated by switches.

**Diagram:**
```
[PC1]   [PC2]
	 \     /
		[Hub]
		 |
	 [PC3]
```

---

## 3. Bridge

- **Function:** Connects and filters traffic between two LAN segments using MAC addresses.
- **Layer:** Data Link (Layer 2)
- **Types:**
	- Transparent: Learns MAC addresses automatically
	- Source Route: Used in Token Ring networks
- **Use Case:** Reducing network congestion, segmenting networks.

**Diagram:**
```
[LAN1]---[Bridge]---[LAN2]
```

---

## 4. Switch

- **Function:** Connects devices, forwards data only to the intended recipient using MAC addresses.
- **Layer:** Data Link (Layer 2)
- **Advantage:** Reduces collisions, increases efficiency, supports VLANs.

**Diagram:**
```
[PC1]   [PC2]
	 \     /
	 [Switch]
		 |
	 [PC3]
```

---

## 5. Router

- **Function:** Routes packets between different networks using IP addresses.
- **Layer:** Network (Layer 3)
- **Use Case:** Connecting LANs to the internet, inter-network communication.

**Diagram:**
```
[LAN1]---[Router]---[LAN2]
```

---

## 6. Gateway

- **Function:** Translates data between networks using different protocols or architectures.
- **Layer:** All layers (mainly Application)
- **Use Case:** Connecting a company network to the internet, protocol conversion.

---

## 7. Brouter

- **Function:** Combines bridge and router functions (filters by MAC and routes by IP).
- **Layer:** Data Link (2) & Network (3)
- **Use Case:** Legacy networks, specialized scenarios.

---

## 8. Modem

- **Function:** Converts digital data to analog for transmission over phone lines (modulation/demodulation).
- **Layer:** Physical (Layer 1)
- **Use Case:** DSL, dial-up internet.

---

## 9. Access Point (AP)

- **Function:** Provides wireless connectivity to a wired network.
- **Layer:** Data Link (Layer 2)
- **Use Case:** Wi-Fi in homes, offices, public spaces.

---

## 10. Firewall

- **Function:** Monitors and controls incoming/outgoing network traffic based on security rules.
- **Layer:** Network (Layer 3) and above
- **Use Case:** Protecting networks from unauthorized access.

---

## Summary Table

| Device     | OSI Layer(s) | Main Function                |
|------------|--------------|------------------------------|
| Repeater   | 1            | Signal amplification         |
| Hub        | 1            | Broadcasts to all devices    |
| Bridge     | 2            | Segments LANs by MAC         |
| Switch     | 2            | Directs data by MAC          |
| Router     | 3            | Routes by IP                 |
| Gateway    | All          | Protocol translation         |
| Brouter    | 2,3          | Bridge + Router              |
| Modem      | 1            | Digital/analog conversion    |
| Access Pt. | 2            | Wireless access              |
| Firewall   | 3+           | Security filtering           |

---

## Further Reading

- [Network Devices (Cisco)](https://www.cisco.com/c/en/us/products/switches/what-is-a-network-switch.html)
