Design and Implement a Small Office Network
Project Overview
This project demonstrates the design and implementation of a small office network using Cisco devices. The network supports four departments: Admin, HR, Accounts, and IT, each in its own VLAN with wireless access. Devices are assigned IP addresses via DHCP, and inter-department communication is enabled.

Requirements
Router: Cisco 2811 IOS15
Switch: Cisco 2950T-24
Wireless Access Points (APs): AP-PT
Devices:
Admin: 3 users (PCs), Network Printers
HR: 3 users (Laptops)
Accounts: 4 users (Tablets)
IT: 3 users (Smartphones)
Network Design
IP Addressing Scheme
Base Network: 192.168.1.0/24

VLAN 10 (Admin Team):

Network: 192.168.1.0/26
Usable IP Range: 192.168.1.1 - 192.168.1.62
VLAN 20 (HR Team):

Network: 192.168.1.64/26
Usable IP Range: 192.168.1.65 - 192.168.1.126
VLAN 30 (Accounts Team):

Network: 192.168.1.128/26
Usable IP Range: 192.168.1.129 - 192.168.1.190
VLAN 40 (IT Team):

Network: 192.168.1.192/26
Usable IP Range: 192.168.1.193 - 192.168.1.254
Wi-Fi SSID Configuration
Admin WiFi: admin@123
HR WiFi: hrteam@123
Accounts WiFi: account@123
IT WiFi: itteam@123
Inter-VLAN Routing
Inter-VLAN routing is configured using a router-on-a-stick setup, enabling communication between VLANs via a router sub-interface for each VLAN.

DHCP Configuration
Each VLAN has a dedicated DHCP pool on the router, ensuring devices automatically receive IP addresses.

Troubleshooting and Testing
Ping Test
Verifies IP connectivity between VLANs.
Example: From Admin PC (192.168.1.2) to HR PC (192.168.1.67) - Success
Traceroute Test
Verifies routing paths between devices.
Example: From Admin PC to Accounts PC (192.168.1.131).
Common Issues and Solutions
Issue: Devices in different VLANs cannot communicate.

Solution: Verified inter-VLAN routing was enabled and trunk ports were correctly configured.
Issue: Devices not receiving IP addresses via DHCP.

Solution: Ensured DHCP pools were configured correctly and router interfaces were active.
Conclusion
This project implements a fully functional small office network, providing isolated and secure communication between departments, while ensuring devices are dynamically assigned IPs and have wireless access. All configurations were tested successfully using ping and traceroute commands.

This README summarizes the project while adhering to GitHub’s format for easy understanding. You can adjust it as needed to fit specific formatting preferences or additional details you want to include.






