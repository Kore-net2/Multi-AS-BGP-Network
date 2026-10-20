# Multi-AS Enterprise Routing — GNS3 BGP, EIGRP, OSPF and ACLs

> **University network simulation coursework, not a production network.** The configuration files and GNS3 layouts were recovered from the original lab archives; router boot and end-to-end connectivity **have not been validated here**.

## What this repository contains

**Lab 6 — Inter-domain and intra-domain routing:**
- GNS3 topology with **52 nodes and 61 links**
- BGP peering across autonomous systems (configuration includes AS 100 and 200)
- EIGRP, OSPF/OSPFv3 and IPv4/IPv6 routing; selected route redistribution
- Dynamips router startup configurations and VPCS host scripts

**Lab 7 — Routing and traffic filtering:**
- Extended topology with **53 nodes and 62 links**
- BGP, EIGRP, OSPF/OSPFv3, IPv6 addressing and redistribution configurations
- IPv4 extended access control list (`FIREWALL-IPv4`) and other ACL rules

Both labs are snapshots intended for experimenting with routing convergence, reachability and policy controls. Protocol presence is confirmed in stored configuration text, **not by running routers**.

## Open in GNS3

1. Install GNS3 and configure Dynamips and VPCS.
2. Supply a **legally acquired** compatible Cisco IOS router image (not included in this repository). Some nodes reference Cisco 7200 templates; adjust templates where needed.
3. Open `lab6/project.gns3` or `lab7/project.gns3` from GNS3.
4. Check interfaces and router startup configurations before starting the nodes.
5. Use `show ip route`, `show ip bgp summary`, `show ipv6 route`, `show ip protocols`, `show access-lists`, and controlled ping/traceroute tests to validate operation in your environment.

## Project structure

```text
lab6/
  project.gns3
  project-files/dynamips/.../configs/*.cfg
  project-files/vpcs/.../startup.vpc
lab7/
  project.gns3
  project-files/dynamips/.../configs/*.cfg
  project-files/vpcs/.../startup.vpc
```

## Important notices

- This is **academic coursework**. Only claim work that you performed and check university publication rules.
- Original student reports, packet captures and simulator logs are **excluded**; they may contain private information and are not required to review the configs.
- No Cisco IOS image, virtual appliance binary or other proprietary router image is distributed.
- No standalone production credentials were detected in the included config files; use these as **isolated test-lab examples only**.
- Original topologies have been kept structurally intact; GNS3 compatibility, routing correctness and enforcement of ACLs still require simulator verification.
- No licence is provided for student/third-party coursework files.
