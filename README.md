# Cisco Routing & Switching Labs

Enterprise network topologies, VLAN segmentation, Layer 2 link aggregation, and automated IP addressing configurations built and verified in **Cisco Packet Tracer**.

## Repository Structure

| # | Lab Module | Key Technologies & Protocols |
| :--- | :--- | :--- |
| 01 | [Switch and Router Configuration](./01-switch-and-router-configuration) | Cisco IOS CLI, SSH/VTY hardening, password encryption, SVI management, basic IPv4 addressing |
| 02 | [VLAN and Trunking](./02-vlan-and-trunking) | IEEE 802.1Q trunking, access ports, Native VLAN security, unused port isolation (`Parking_Lot` VLAN) |
| 03 | [EtherChannel (LACP)](./03-etherchannel-lacp) | Link Aggregation Control Protocol (802.3ad), `Port-Channel` load balancing, Layer 2 redundancy |
| 04 | [DHCPv4 and DHCP Relay](./04-dhcpv4-and-relay) | Router-on-a-Stick inter-VLAN routing, static routing, multi-pool DHCPv4 server, `ip helper-address` relay |

## Core Engineering Practices Applied

- **Device Hardening:** Disabled DNS lookup (`no ip domain-lookup`), configured encrypted privileged EXEC and line passwords (`service password-encryption`), and set MOTD security banners.
- **Layer 2 Security:** Isolated unused switch ports into a dedicated parking VLAN and administratively shut them down; moved Native VLAN away from default VLAN 1.
- **Verification & Troubleshooting:** Validated end-to-end reachability and protocol states using `show ip interface brief`, `show vlan brief`, `show interfaces trunk`, `show etherchannel summary`, and `show ip dhcp binding`.
