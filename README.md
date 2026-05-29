# GNS3 OSPF Lab

## Overview

This project is a multi-area OSPF network lab built in GNS3 using routers and VPCS hosts. The goal was to design, configure, and verify a routed network using OSPF instead of static routes.

The network uses the 10.1.0.0/20 address block, which was subnetted into point-to-point router links and LAN networks for end hosts. Area 0 is used as the OSPF backbone, with other OSPF areas connected through Area Border Routers.

## Skills Demonstrated

- GNS3 network simulation
- OSPF routing
- Multi-area OSPF design
- IP subnetting and CIDR planning
- Area Border Router configuration
- Route summarization
- Route redistribution
- Ping and traceroute testing
- OSPF neighbor verification
- Network troubleshooting
- Technical documentation

## Network Design

The lab includes 8 routers and multiple VPCS hosts. Routers R1, R2, R3, and R4 form the OSPF backbone area. Other routers connect through additional OSPF areas.

| OSPF Area | Routers |
|---|---|
| Area 0 | R1, R2, R3, R4 |
| Area 1 | R2, R5 |
| Area 2 | R4, R7, R8 |
| Area 3 | R1, R6 |

The project also includes route summarization and an external connected network redistributed into OSPF through R3.

## Verification

The network was tested using ping, traceroute, and OSPF verification commands. The results confirmed that hosts on different subnets could communicate across the routed network and that OSPF neighbor relationships formed correctly.

Example commands used:

```bash
show ip ospf neighbor
show ip ospf database
show ip route
ping <destination-ip>
trace <destination-ip>
