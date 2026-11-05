<h1 align="center">Enterprise Network Design and Management</h1>

<p align="center">
  A design report for a scalable, secure organisational network, covering logical and
  physical design, FCAPS management, a phased implementation plan and a costed budget.
</p>

---

**Network Management, Year 3. BTech Networking Technologies (TU716), TU Dublin, December 2024.**
Cathal Flood

---

## What it covers

The report designs a network for an organisation such as a hospital, university or retail
chain, where downtime is expensive and the network has to grow with the business. It works
from the requirements (business goals, technical goals and the applications the network must
carry) through to a design, an implementation plan and a budget.

### Logical design
- **Topology:** a three-layer hierarchy (core, distribution and access) in a hybrid star and
  mesh layout, with redundant links in the core to remove single points of failure.
- **Addressing:** hierarchical IPv4 subnetting per department, with dual-stack IPv6 for growth,
  and DNS naming that follows the organisation's structure.
- **Routing and switching:**
  - OSPF inside the organisation, for fast convergence and VLSM support.
  - BGP for ISP connections.
  - VLANs to segment traffic, with Spanning Tree to prevent loops.
- **Security:** perimeter and internal firewall policies, ACLs on routers and switches, TLS
  between endpoints and IPsec for VPN traffic.
- **Quality of service:** traffic classification, guaranteed bandwidth for voice and video,
  and Weighted Fair Queueing.
- **Management:** SNMP monitoring, a SIEM for security events, and configuration automation.

### Physical design
- **Equipment:** core, distribution and access-layer hardware, with PoE at the access layer
  for phones and access points.
- **Cabling:** Cat 6/6a copper for short runs and fibre between layers, following TIA-568
  structured cabling.
- **Resilience:** dual links, dual power supplies with UPS, and hardware load balancing.

### Management problems and solutions (FCAPS)
For each of fault, configuration, accounting, performance and security management, the report
names the typical problem and a matching control. Examples are real-time monitoring and
redundancy for faults, automation and version-controlled configs for configuration,
NetFlow-style visibility for accounting, and layered IDS/IPS and SIEM for security.

### Implementation and budget
- **Rollout:** a phased plan running from assessment and procurement, through core-first
  installation, configuration and end-to-end testing, to staff training, failover testing and
  ongoing maintenance.
- **Budget:** €93,000 in total. That is €50,000 of hardware, €18,000 of software and
  licensing, €15,000 of labour, and a €10,000 contingency.

## Files

```
docs/report.pdf         The full design report
network-design.pkt      Cisco Packet Tracer file submitted with the report
```

Open the `.pkt` file with Cisco Packet Tracer (free with a Cisco Networking Academy account).
