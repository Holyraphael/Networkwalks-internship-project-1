# 🔎 Network Scanning with Zenmap

![Zenmap](https://img.shields.io/badge/Tool-Zenmap-blue)
![Nmap](https://img.shields.io/badge/Technology-Nmap-green)
![Cybersecurity](https://img.shields.io/badge/Field-Cybersecurity-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview

This project demonstrates a **network discovery exercise using Zenmap**, the graphical interface for Nmap.

The goal was to discover active hosts on a local network, examine basic host information, and visualize the discovered network using Zenmap's topology feature.

**Target Network:** `10.0.0.0/24`

---

## 🎯 Objective

* Discover live hosts on the local subnet.
* Identify their IP addresses and available MAC address information.
* Perform host discovery using Nmap.
* Visualize the discovered network topology.
* Document the reconnaissance results.

---

## 🛠️ Tools Used

* **Zenmap**
* **Nmap**
* **Windows Command Prompt**
* **`ipconfig` / `ipconfig /all`**

---

## 🔍 Network Scanning

The local network configuration was identified using:

```text
ipconfig
```

Observed network:

```text
Local IP: 10.0.0.1
Subnet:   10.0.0.0/24
```

A **Ping Scan** was then performed in Zenmap using:

```bash
nmap -sn 10.0.0.0/24
```

The scan discovered **2 live hosts**:

| IP Address | Status | MAC Address         |
| ---------- | ------ | ------------------- |
| `10.0.0.1` | Live   | `52:54:00:12:35:00` |
| `10.0.0.2` | Live   | Not displayed       |

The `10.0.0.1` address was identified with a **QEMU virtual NIC**.

---

## 🗺️ Network Topology

Zenmap's **Topology** feature was used to visualize the discovered hosts and network relationships.

The resulting topology was exported as:

**`Zenmap-Topology.pdf`**

---

## 🧠 Skills Demonstrated

* Network reconnaissance
* Host discovery
* Nmap / Zenmap
* IP addressing and CIDR
* Network analysis
* MAC address identification
* Network topology visualization
* Technical documentation

---

## 💡 Key Takeaways

This exercise provided practical experience with **network reconnaissance and host discovery**.

I learned how to:

* Identify active hosts within a subnet.
* Use Nmap's `-sn` option for host discovery.
* Interpret basic Nmap results.
* Use Zenmap to visualize network topology.
* Document reconnaissance findings professionally.

---

## 📚 References

* [Nmap Official Documentation](https://nmap.org/book/man.html)
* [NetworkWalks — Zenmap Network Scanning Practice Lab](https://networkwalks.com/zenmap-network-scanning-practice-lab/)

---

## ⚠️ Ethical Use

This exercise was performed in a controlled learning environment for cybersecurity education.

Network scanning should only be performed against systems and networks that you own or have explicit authorization to test.
