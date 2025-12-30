# 🖧 EIGRP-Based Network Configuration (Cisco Packet Tracer)

## 📌 Project Overview
This project demonstrates the configuration of **EIGRP (Enhanced Interior Gateway Routing Protocol)** on a multi-router network using **Cisco Packet Tracer**.  
The topology consists of three routers (**Colombo, Kandy, Badulla**) connected via serial links, each serving a separate LAN.

---

## 🗺️ Network Topology
- **Colombo Router** → Admin LAN (192.168.1.0/24)
- **Kandy Router** → User LAN (192.168.2.0/24)
- **Badulla Router** → User LAN (192.168.3.0/24)
- Serial point-to-point links use **/30 subnetting**

---

## 🌐 IP Addressing Scheme

### Router Interfaces

| Router  | Interface | IP Address        | Subnet Mask        |
|--------|----------|------------------|-------------------|
| Colombo | Fa0/0 | 192.168.1.1 | 255.255.255.0 |
| Colombo | Se0/0/0 | 10.10.10.1 | 255.255.255.252 |
| Kandy | Fa0/0 | 192.168.2.1 | 255.255.255.0 |
| Kandy | Se0/0/0 | 10.10.10.2 | 255.255.255.252 |
| Kandy | Se0/1/0 | 20.20.20.1 | 255.255.255.252 |
| Badulla | Fa0/0 | 192.168.3.1 | 255.255.255.0 |
| Badulla | Se0/0/0 | 20.20.20.2 | 255.255.255.252 |

---

## ⚙️ Routing Protocol
- **Protocol:** EIGRP
- **AS Number:** 1
- **Auto-summary:** Disabled

---

## 🚀 Configuration Summary

### Enable EIGRP (Example – Colombo)
```bash
router eigrp 1
network 192.168.1.0 0.0.0.255

```
---
## 🔍 Verification Commands
show ip eigrp neighbors
show ip route eigrp
show ip eigrp interfaces
show ip interface brief

---
network 10.10.10.0 0.0.0.3
no auto-summary
