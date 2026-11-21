# 02. VLAN Segmentation, 802.1Q Trunking & Router-on-a-Stick

Logical network segmentation using Virtual LANs, static 802.1Q trunking across switches, and inter-VLAN routing via router sub-interfaces.

## Project Files
- [conf vlans.pkt](./cisco%20files/conf%20vlans.pkt) — Multi-switch VLAN creation, access port assignment, and 802.1Q trunk configuration.
- [conf router on a stick.pkt](./cisco%20files/conf%20router%20on%20a%20stick.pkt) — Inter-VLAN routing using 802.1Q sub-interfaces (`encapsulation dot1Q`).

## Key Objectives & Technologies
- **VLAN Architecture:** Created isolated broadcast domains and assigned access ports (`switchport mode access`).
- **802.1Q Trunking:** Configured static trunk links between switches and toward the router, modifying the Native VLAN for Layer 2 security.
- **Inter-VLAN Routing:** Configured Router-on-a-Stick sub-interfaces with 802.1Q tagging to route traffic between VLAN subnets.

## Topology & Verification

### Part 1: Multi-Switch VLANs & Trunking
![VLANs Topology](./screenshots/vlans%20topology.png)
![S1 VLAN Verification](./screenshots/s1%20brief%20in%20conf%20vlans.png)
![S2 VLAN Verification](./screenshots/s2%20brief%20in%20conf%20vlans.png)

### Part 2: Router-on-a-Stick Inter-VLAN Routing
![Router-on-a-Stick Topology](./screenshots/router%20on%20a%20stick%20topology.png)
![Router Sub-interfaces](./screenshots/router%20interface%20brief.png)
![S1 Trunk & VLAN Verification](./screenshots/s1%20bief%20in%20router%20on%20a%20stick.png)
![S2 Trunk & VLAN Verification](./screenshots/s2%20brief%20in%20router%20on%20a%20stick.png)
