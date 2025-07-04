
# OSPF Multi-Area Routing Lab (8-Router Topology)

A Cisco Packet Tracer project featuring 8 routers configured with OSPF in multiple areas. Built for practicing advanced routing concepts, troubleshooting skills, and developing patience you didn’t know you needed.

---

## 📂 Project Details

- **Filename:** `IP Routing and Configuration (Multi-Area for 8 Routers).pkt`
- **Software:** Cisco Packet Tracer (v8.2+ recommended)
- **Focus:** OSPF Multi-Area Routing, Inter-Area Communication, and CLI Troubleshooting

---

## 🗺️ Topology Overview

- 8 routers (Cisco 2901)
- Subnet ranges: `192.168.10.0/24` to `192.168.20.0/24`
- Divided into multiple OSPF areas:
  - Area 0 (Backbone)
  - Area 1 (and potentially Area 2, if expanded)

---

## 🧪 Lab Goals

- ✅ Configure Multi-Area OSPF on all routers  
- ✅ Verify OSPF adjacencies and LSAs  
- ✅ Ensure inter-area communication  
- 🔁 Troubleshoot ICMP failures  
- 😵‍💫 Panic and start over when things go wrong

---

## 🔍 Observed Troubleshooting Case

> “All was well until Router 3 in Area 1 couldn’t ping Router 5 in Area 0...”

- 🔎 **Symptoms**:
  - Ping from `192.168.20.1` to `192.168.16.2` fails
  - OSPF neighbor relationships seem stable
- 🧯 **Possible Causes**:
  - Misconfigured OSPF area borders
  - Incorrect/missing `network` statements
  - Passive interfaces enabled on transit links
  - Router IDs clashing or missing
- **Lesson Learned**:  
  Asking ChatGPT helped... until it didn't. 😂

---

## 🛠️ Commands to Remember

```bash
show ip ospf neighbor
show ip route
show ip ospf interface
ping [ip address]
traceroute [ip address]
```

---

## 🚀 To-Do / Future Enhancements

- [ ] Add loopback interfaces and use them for router IDs
- [ ] Apply summarization at ABRs
- [ ] Add client PCs to simulate end-to-end traffic
- [ ] Simulate Internet connectivity via NAT cloud
- [ ] Introduce authentication on OSPF links

---

## 💡 Tips

- Double-check OSPF area assignments
- Use `show` commands generously
- Save configs often (trust me 😭)
- Sometimes... starting over is the real fix

---

## 🧾 License

This lab is free to use for educational purposes. If it makes you cry, please blame the `debug` output, not the README author.

