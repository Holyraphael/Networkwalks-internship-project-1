Task 1: Lab Setup — VirtualBox and Kali Linux

📌 Overview

This project documents the setup and configuration of a Kali Linux virtual machine using Oracle VirtualBox as part of the Week 1 cybersecurity practical training.

The task involved creating the Kali Linux virtualized environment, configuring a custom NAT Network, connecting the virtual machine to the network, assigning a static IP address, and testing network connectivity.

The project also documents a network connectivity issue encountered during the initial setup and the troubleshooting steps used to identify and resolve the problem.

---

🎯 Objectives

The main objectives of this task were to:

- Set up Kali Linux in Oracle VirtualBox.
- Configure a custom NAT Network.
- Configure the Kali Linux virtual machine's network adapter.
- Assign a static IPv4 address to Kali Linux.
- Configure the subnet mask, gateway, and DNS servers.
- Test network connectivity.
- Identify and troubleshoot network connectivity problems encountered during setup.

---

🖥️ Lab Environment

Component| Configuration
Host Operating System| Windows 11 Pro
Hypervisor| Oracle VirtualBox Manager
Guest Operating System| Kali Linux
Virtual Machine| "kali-linux-2026.2-virtualbox-amd64"
Base Memory| 2048 MB
Processors| 2
Storage| 80.09 GB VDI

---

🌐 NAT Network Configuration

A custom NAT Network named "NatNetwork" was created in Oracle VirtualBox to provide the networking environment for the Kali Linux virtual machine.

Configuration

- Network Name: "NatNetwork"
- IPv4 Prefix: "10.0.0.0/24"
- DHCP Server: Enabled
- IPv6: Disabled

Evidence

"NAT Network Configuration" (screenshots/02_NATNetwork.jpeg)

---

⚙️ Virtual Machine Network Adapter Configuration

The Kali Linux virtual machine was configured to use the custom "NatNetwork".

Adapter Configuration

- Adapter: Adapter 1
- Status: Enabled
- Attached to: NAT Network
- Network: "NatNetwork"
- Adapter Type: Intel PRO/1000 MT Desktop (82540EM)
- Promiscuous Mode: Allow All
- Cable Connected: Enabled

Evidence

"Network Adapter Configuration" (screenshots/03_Selecting_NATNetwork.jpeg)

---

🔐 Static IP Configuration

After booting Kali Linux, the network settings for Wired connection 1 were configured manually.

Network Configuration

Setting| Value
Connection| Wired connection 1
Method| Manual
IP Address| "10.0.0.2"
Netmask| "24"
Gateway| "10.0.0.1"
DNS Servers| "8.8.8.8", "10.0.0.1"

Evidence

"Kali Linux Static IP Configuration" (screenshots/04_Setting_Address.jpeg)

---

⚠️ Problem Encountered During Setup

During the initial configuration of the NAT Network, I encountered a network connectivity problem.

The problem occurred because I initially forgot to enable the DHCP Server when configuring the "NatNetwork".

As a result, Kali Linux did not have proper network connectivity. When I attempted to test the connection by pinging "8.8.8.8" and accessing the Internet through the browser, the connection was unsuccessful.

---

🔍 Troubleshooting

I investigated the network configuration to determine the cause of the connectivity problem.

After reviewing the NAT Network settings in VirtualBox, I discovered that the DHCP Server was not enabled.

I returned to the "NatNetwork" configuration and enabled the DHCP Server option. After applying the change, I returned to Kali Linux and reapplied the network configuration.

I then went back to confirm the address i setup.

Evidence

"DHCP CONFIRMINATION" (screenshots/05_Confirming_Address.jpeg)

---

✅ Resolution

After enabling the DHCP Server on the "NatNetwork", the network connectivity problem was resolved.

I was then able to continue with the lab setup and successfully test the network connection.

This troubleshooting experience helped me understand the importance of correctly configuring DHCP when establishing network connectivity within a virtualized environment.

---

🌐 Connectivity Testing

Network connectivity was tested by attempting to ping Google's public DNS server:

ping 8.8.8.8

Internet connectivity was also tested by opening a web browser in Kali Linux and accessing the Internet.

The initial tests were unsuccessful because the DHCP Server had not been enabled on the NAT Network. After enabling DHCP and reapplying the network configuration, connectivity was restored.

Evidence

"Connectivity Test" (screenshots/06_Network_Connectivity.jpeg)

---

📊 Result

The Kali Linux virtual machine was successfully configured in Oracle VirtualBox and connected to the custom "NatNetwork".

The required static IPv4 configuration was applied:

IP Address: 10.0.0.2/24
Gateway:    10.0.0.1
DNS:        8.8.8.8, 10.0.0.1

The initial connectivity problem was identified as being related to the DHCP Server configuration. After enabling DHCP on the NAT Network and reapplying the network configuration, the connectivity issue was resolved.

---

📝 Conclusion

This task provided practical experience in setting up a Kali Linux virtual machine using Oracle VirtualBox and configuring its network environment.

I configured a custom NAT Network, connected the Kali Linux virtual machine to the network, assigned a static IP address, and tested network connectivity.

The troubleshooting process also provided practical experience in identifying a network configuration problem, determining that DHCP was disabled, and resolving the connectivity issue.

This successfully established the initial virtualized cybersecurity environment required for subsequent practical exercises.

---

📸 Evidence Summary

The following screenshots provide evidence of the major stages completed during this task:

1. NAT Network configuration
2. Virtual machine network adapter configuration
3. Kali Linux static IP configuration
4. Corrected NAT Network configuration with DHCP enabled
5. Network connectivity test

---

🛠️ Tools Used

- Oracle VirtualBox
- Kali Linux
- Linux Terminal
- Ping
- Web Browser
