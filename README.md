<h1>🌐 Workplace Organization Network Lab</h1>

<h2>📌 Overview</h2>
This project simulates a **workplace organization network** in Cisco Packet Tracer. It focuses on **VLAN configuration, Voice VLAN for IP phones, DHCP setup, DMZ for a web server, wireless guest access, port security, and inter-VLAN routing** to segment departments, secure the network, and enable communication across VLANs using a multilayer switch. The network includes five access switches, a router, a wireless access point, and servers (DHCP, DNS, Web).

<h2>🛠 Tools & Technologies Used</h2>

- **Cisco Packet Tracer** – Network simulation and configuration  
- **Multilayer Switch (Cisco 3560)** – Inter-VLAN routing and VLAN management  
- **Access Switches (Cisco 2950)** – VLAN segmentation, Voice VLAN, and trunking  
- **Servers (DHCP, DNS, Web)** – Dynamic IP assignment, domain resolution, and web hosting  
- **Router (Cisco 2911)** – External connectivity and NAT  
- **Wireless Access Point** – Guest network connectivity  
- **IP Phones (Cisco 7960)** – VoIP integration  

<h2>🔍 Network Configuration & Features</h2>

| Feature | Description | Implementation |
|---------|-------------|----------------|
| **VLAN Segmentation** | Separates departments for security and organization. | Configured VLANs: Staff (10), IT (20), HR (30), Guest (50), Management (99), Voice (110). |
| **Voice VLAN** | Isolates IP phone traffic for VoIP integration. | Set up VLAN 110 for all IP phones with dedicated access ports on switches. |
| **DHCP Configuration** | Assigns IP addresses dynamically to devices. | Configured DHCP pools on a server in VLAN 99 with `ip helper-address` on VLAN interfaces. |
| **DMZ** | Hosts a public-facing web server with isolation. | Created a DMZ (172.16.100.0/24) with Server_Web, accessible via NAT on Router0. |
| **Wireless Guest Network** | Provides secure wireless access for guests. | Set up VLAN 50 with AccessPoint0, using WPA2-PSK security (passphrase: P@ssw0rd1234). |
| **Port Security** | Enhances security by limiting device access. | Applied `port-security` on access ports by administratively shutting down extra ports. |
| **Inter-VLAN Routing** | Enables communication between VLANs. | Configured a multilayer switch with VLAN interfaces and routing enabled. |
| **Trunking** | Carries multiple VLAN traffic between switches. | Set up trunk ports on Switch0, Switch1, Switch2, Switch4, and Switch5 with `switchport mode trunk`. |

<h2>📐 Network Topology</h2>

![Network Topology](https://github.com/user-attachments/assets/dfbe1fca-38f0-4f8a-989b-9a507d5d42ee)   
*The topology includes a multilayer switch connected to five access switches (Switch0, Switch1, Switch2, Switch4, Switch5), a router, a wireless access point, servers (DHCP, DNS, Web), IP phones in VLAN 110, and devices in VLANs 10, 20, 30, 50, and 99.*

<h2>✅ Networking Best Practices & Key Takeaways</h2>

🔹 **VLANs** enhance **network security** by isolating department and voice traffic.  
🔹 **Voice VLAN** ensures efficient **VoIP integration** for IP phones.  
🔹 **DHCP** simplifies IP management with **dynamic addressing** across VLANs.  
🔹 **DMZ** provides **secure isolation** for public-facing services like web servers.  
🔹 **Wireless Guest Network** with WPA2-PSK ensures **secure guest access**.  
🔹 **Port Security** prevents **unauthorized access** by limiting MAC addresses.  
🔹 **Inter-VLAN Routing** ensures efficient communication across departments.  
🔹 **Trunking** is critical for **multi-VLAN traffic** between switches.  
