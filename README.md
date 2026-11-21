# Cisco Routing & Switching Labs

![Cisco](https://img.shields.io/badge/Cisco-IOS_CLI-1BA0D7?style=flat-square&logo=cisco&logoColor=white)
![Packet Tracer](https://img.shields.io/badge/Simulator-Packet_Tracer-00BCEB?style=flat-square)
![Focus](https://img.shields.io/badge/Focus-CCNA_Routing_%26_Switching-2EA44F?style=flat-square)

A collection of hands-on network topologies built and verified in **Cisco Packet Tracer**. Each lab focuses on practical Layer 2 and Layer 3 configuration, basic device hardening, and CLI-based troubleshooting. This repository is organized by progressively more advanced topics, covering everything from initial device setup to redundancy, dynamic addressing, and routing protocols.

> **Work in Progress:** This repository is maintained alongside ongoing networking coursework. Additional completed labs covering subsequent routing and switching topics are being documented and uploaded incrementally as time permits.

## Lab Modules

| # | Module | Configured Features & Protocols |
| :--- | :--- | :--- |
| 01 | [Switch and Router Configuration](./01-switch-and-router-configuration) | Cisco IOS CLI basics, hostname & MOTD banner setup, console/VTY line security, password encryption, IPv4 interface addressing |
| 02 | [VLAN and Trunking](./02-vlan-and-trunking) | Multi-switch VLAN segmentation, access ports, static IEEE 802.1Q trunking, Native VLAN modification, Router-on-a-Stick inter-VLAN routing |
| 03 | [EtherChannel (LACP)](./03-etherchannel-lacp) | Link aggregation via IEEE 802.3ad (LACP), logical `Port-Channel` trunking, Layer 2 redundancy without STP port blocking |
| 04 | [DHCPv4 and DHCP Relay](./04-dhcpv4-and-relay) | VLSM subnetting (`192.168.1.0/24`), unused port isolation (`VLAN 999`), multi-pool DHCPv4 server, `ip helper-address` relay across routed networks |

## Repository Layout

Every lab directory follows a uniform structure for quick review:

```text
├── 0X-lab-name/
│   ├── cisco files/      # Ready-to-run Cisco Packet Tracer (.pkt) topologies
│   ├── screenshots/      # Logical topology diagrams and CLI verification outputs
│   └── README.md         # Lab objectives, configuration breakdown, and test results
```

## Verification & Troubleshooting Approach

All topologies were validated end-to-end using standard Cisco IOS diagnostic commands rather than relying solely on simulation mode:
- **Layer 1 / Layer 2 State:** `show ip interface brief`, `show vlan brief`, `show interfaces trunk`
- **Link Aggregation:** `show etherchannel summary` (verifying `SU` / `P` flags across member links)
- **Dynamic Addressing & Routing:** `show ip dhcp binding`, `show ip route`, and host-level `ipconfig` / `ping` reachability tests

## How to Run

1. Install **Cisco Packet Tracer** (version 8.2 or newer recommended).
2. Navigate to any module folder and download the `.pkt` file from the `cisco files/` directory.
3. Open the file in Packet Tracer — all device configurations are saved to `startup-config` (`copy running-config startup-config`) and ready for inspection.
