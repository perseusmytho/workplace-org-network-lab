<h1>🌐 Workplace Organization Network Lab</h1>

<h2>📌 Overview</h2>
This project builds a **workplace organization network** in Cisco Packet Tracer, showcasing advanced network design. It includes **departmental VLANs**, a **Voice VLAN for IP phones**, a **DMZ for a web server**, a **wireless guest network**, **port security**, and inter-VLAN routing. The setup uses a multilayer switch, five access switches, a router, a wireless access point, and servers (DHCP, DNS, Web).

<h2>🛠 Tools & Technologies Used</h2>

- **Cisco Packet Tracer** – Network simulation and configuration  
- **Multilayer Switch (Cisco 3560)** – Inter-VLAN routing and VLAN management  
- **Access Switches (Cisco 2950)** – VLAN and Voice VLAN support, trunking  
- **Servers (DHCP, DNS, Web)** – IP assignment, name resolution, web hosting  
- **Router (Cisco 2911)** – External connectivity and NAT  
- **Wireless Access Point** – Guest network connectivity  
- **IP Phones (Cisco 7960)** – VoIP integration  

<h2>🔍 Network Configuration & Features</h2>

| Feature | Description | Implementation |
|---------|-------------|----------------|
| **VLAN Segmentation** | Organizes departments into isolated networks. | Configured VLANs: Staff (10), IT (20), HR (30), Guest (50), Management (99), Voice (110). |
| **Voice VLAN** | Separates IP phone traffic for VoIP support. | Set up VLAN 110 for all IP phones with dedicated access ports on switches. |
| **DHCP Configuration** | Automates IP address allocation for devices. | Configured DHCP pools on a server in VLAN 99, using `ip helper-address` for VLANs. |
| **DMZ** | Isolates a public-facing web server for security. | Created a DMZ (172.16.100.0/24) with Server_Web, accessible via NAT on Router0. |
| **Wireless Guest Network** | Enables secure wireless access for guests. | Set up VLAN 50 with AccessPoint0, secured with WPA2-PSK (passphrase: P@ssw0rd1234). |
| **Port Security** | Restricts access to authorized devices. | Applied `port-security` on access ports by administratively shutting down ports not in use. |
| **Inter-VLAN Routing** | Facilitates communication across VLANs. | Enabled routing on a multilayer switch with VLAN interfaces. |
| **Trunking** | Supports multiple VLANs across switch links. | Configured trunk ports on Switch0, Switch1, Switch2, Switch4, Switch5 with `switchport mode trunk`. |

<h2>📐 Network Topology</h2>

![Network Topology](https://github.com/user-attachments/assets/7db94b91-a760-45dd-8b55-b7b8344f42a4)   
*The topology includes a multilayer switch, five access switches (Switch0, Switch1, Switch2, Switch4, Switch5), a router, a wireless access point, servers (DHCP, DNS, Web), and IP phones in VLAN 110.*

<h2>✅ Networking Best Practices & Key Takeaways</h2>

🔹 **VLANs** provide **traffic isolation** for departments and voice devices.  
🔹 **Voice VLAN** supports **VoIP integration** by isolating IP phone traffic.  
🔹 **DHCP** ensures **efficient IP management** across multiple VLANs.  
🔹 **DMZ** enhances **security** for public-facing services like web servers.  
🔹 **Wireless Guest Network** with WPA2-PSK offers **secure guest access**.  
🔹 **Port Security** limits **unauthorized access** by shutting down ports not in use.  
🔹 **Inter-VLAN Routing** enables **seamless communication** between VLANs.  
🔹 **Trunking** ensures **VLAN traffic flow** across switches.  
