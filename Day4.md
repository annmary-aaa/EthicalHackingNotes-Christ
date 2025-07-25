# TCP vs UDP

| Feature             | TCP (Transmission Control Protocol)         | UDP (User Datagram Protocol)        |
|---------------------|----------------------------------------------|-------------------------------------|
| Connection Type     | Connection-oriented                          | Connectionless                      |
| Reliability         | Reliable (guarantees delivery, order)        | Unreliable (no delivery guarantees) |
| Error Checking      | Yes (with ACK and retransmission)            | Yes (no retransmission)             |
| Ordering of Data    | Guarantees order                             | No ordering                         |
| Speed               | Slower due to overhead                       | Faster, minimal overhead            |
| Header Size         | 20 bytes                                     | 8 bytes                             |
| Congestion Control  | Yes                                          | No                                  |
| Flow Control        | Yes                                          | No                                  |
| Use Cases           | Web, FTP, Email                              | Video streaming, Gaming, VoIP       |
| Acknowledgments     | Yes                                          | No                                  |
| Connection Setup    | 3-way handshake required                     | No setup needed                     |
| Data Integrity      | High                                         | Lower                               |

# Networking Basics

## 1. IP Address

**IP Address (Internet Protocol Address)** is a unique identifier assigned to each device connected to a network. It allows devices to locate and communicate with each other over the internet or a local network.

- Acts like a postal address for your computer.
- Can be **static** (permanently assigned) or **dynamic** (changes over time).

### Types of IP Addresses:
- **Private IP Address**: Used within a local network (e.g., 192.168.1.1)
- **Public IP Address**: Assigned by the ISP to access the internet
- **Static IP Address**: Manually configured, does not change
- **Dynamic IP Address**: Assigned automatically, changes periodically

---

## 2. MAC Address

**MAC (Media Access Control) Address** is a hardware identifier that is unique to each network interface card (NIC).

- Example format: `00:1A:2B:3C:4D:5E`
- Assigned by the device manufacturer and hardcoded into the hardware.
- Used at the **Data Link Layer** (Layer 2) of the OSI model.
- Cannot be changed easily (though it can be spoofed in software).

---

## 3. Dynamic IP Address

A **Dynamic IP Address** is automatically assigned by a **DHCP (Dynamic Host Configuration Protocol)** server.

- Changes each time a device connects to the network.
- Commonly used in homes and small networks.
- Reduces IP address management complexity.
- Good for general browsing, but not suitable for servers that need a consistent address.

---

## 4. IPv4

**IPv4 (Internet Protocol version 4)** is the 4th version of IP and the most widely used.

- 32-bit address (e.g., `192.168.0.1`)
- Provides approximately **4.3 billion** unique addresses
- Exhaustion led to the development of IPv6
- Example:
  - Class A: `0.0.0.0 – 127.255.255.255`
  - Class B: `128.0.0.0 – 191.255.255.255`
  - Class C: `192.0.0.0 – 223.255.255.255`

---

## 5. IPv6

**IPv6 (Internet Protocol version 6)** is the successor to IPv4.

- 128-bit address (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`)
- Supports **340 undecillion (3.4×10³⁸)** addresses
- Solves address exhaustion
- Enhanced features:
  - No need for NAT (Network Address Translation)
  - Built-in security (IPSec)
  - Auto-configuration (like DHCPv6)

---

## 6. Types of Network Adapters

A **Network Adapter** is a hardware component that enables a device to connect to a network.

### Types:

| Adapter Type                | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| **Ethernet Adapter**        | Wired connection; commonly uses RJ-45 cables for LAN                        |
| **Wi-Fi Adapter**           | Wireless connection; connects to routers via radio signals                  |
| **USB Network Adapter**     | External device connected via USB port for wired/wireless connectivity      |
| **PCI Network Adapter**     | Internal card mounted on motherboard slot (usually for desktops)            |
| **Bluetooth Adapter**       | Used to connect to Bluetooth-enabled devices (short range)                  |
| **Cellular (4G/5G) Adapter**| Used in mobile broadband modems and mobile hotspots                         |
| **Virtual Network Adapter** | Created by virtual machines (e.g., VMware, VirtualBox) for virtual networking |

---

## Summary Table

| Concept        | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| IP Address     | Logical identifier of a device on a network                                 |
| MAC Address    | Physical address assigned to the network interface                          |
| Dynamic IP     | Temporary IP assigned by DHCP                                               |
| IPv4           | 32-bit address format, older standard                                       |
| IPv6           | 128-bit address format, modern standard                                     |
| Network Adapter| Device that enables network connectivity                                    |
# 🛡️ Cyber Attack Timeline

This document outlines the typical **timeline of a cyber attack**, including the sequential phases used by attackers or penetration testers. Understanding the attack timeline is crucial for identifying, preventing, and responding to security breaches.

---

## ⏱️ Attack Timeline Phases

### 1. 🔍 Reconnaissance
**Objective:** Gather information about the target.

- Identify domain names, IP addresses, subdomains
- Use OSINT (Open Source Intelligence) tools like:
  - `whois`, `nslookup`, `theHarvester`
- Passive & Active scanning

### 2. 📡 Scanning
**Objective:** Identify vulnerabilities in the target systems.

- Port scanning (`nmap`)
- Service enumeration
- Vulnerability scanning (`nikto`, `OpenVAS`, `Nessus`)

### 3. 🎯 Gaining Access
**Objective:** Exploit vulnerabilities to enter the system.

- Use tools like `Metasploit`, `SQLmap`, `Hydra`
- Exploitation methods:
  - Credential brute force
  - Code injection (e.g., SQLi, XSS)
  - Software bugs

### 4. 🐚 Privilege Escalation
**Objective:** Gain higher access rights in the system.

- Exploit kernel or local vulnerabilities
- Leverage misconfigurations or weak permissions
- Tools: `linux-exploit-suggester`, `winPEAS`, `linPEAS`

### 5. 📂 Maintaining Access
**Objective:** Establish persistent access.

- Create backdoors or cron jobs
- Modify registry or scheduled tasks (Windows)
- Install rootkits or RATs (Remote Access Tools)

### 6. 📤 Data Exfiltration / Execution
**Objective:** Achieve the attack’s purpose.

- Steal sensitive data
- Execute ransomware or destructive payloads
- Screenshot, keylogging, database dump

### 7. 🧹 Covering Tracks
**Objective:** Remove evidence of the attack.

- Clear logs (`bash_history`, Event Viewer)
- Delete tools and temporary files
- Use anti-forensics techniques

### 8. 🔁 Post-Exploitation / Pivoting
**Objective:** Move laterally to other systems.

- Enumerate internal network
- Crack hashes (e.g., `JohnTheRipper`, `hashcat`)
- Use compromised machine as a foothold

---

## 🕒 Sample Timeline Table

| Time (HH:MM) | Phase               | Activity                          |
|--------------|---------------------|-----------------------------------|
| 09:00        | Reconnaissance       | Gathered domain & IP info         |
| 09:20        | Scanning             | Ran `nmap` to find open ports     |
| 09:45        | Gaining Access       | Exploited vulnerable login page   |
| 10:10        | Privilege Escalation | Exploited kernel vulnerability    |
| 10:30        | Maintaining Access   | Installed reverse shell           |
| 10:45        | Data Exfiltration    | Downloaded confidential files     |
| 11:00        | Covering Tracks      | Deleted logs and shell history    |
| 11:15        | Post-Exploitation    | Accessed internal file server     |

---

## 🔐 Disclaimer

This timeline is for **educational and ethical use only**. Unauthorized access to computer systems is illegal and unethical. Always have **written permission** before conducting penetration testing.

---

## 📚 Related Tools

- `nmap` – Port scanning
- `Metasploit` – Exploitation framework
- `JohnTheRipper` – Password cracking
- `netcat` – Reverse shell and port communication
- `Burp Suite` – Web app analysis




