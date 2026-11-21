# 03. Link Aggregation with EtherChannel (LACP)

Layer 2 bandwidth aggregation and physical link redundancy between switches using IEEE 802.3ad Link Aggregation Control Protocol (LACP).

## Project Files
- [etherchannel.pkt](./cisco%20files/etherchannel.pkt) — Multi-link LACP Port-Channel configuration and Spanning Tree loop prevention verification.

## Key Objectives & Technologies
- **LACP Negotiation:** Bundled multiple physical switch links into a single logical `Port-Channel` interface using active/passive LACP modes.
- **Layer 2 Redundancy & STP:** Prevented Spanning Tree Protocol (STP) port blocking across parallel uplinks while providing automatic failover.
- **Trunking over Port-Channel:** Configured 802.1Q trunking directly on the logical `Port-Channel` interface.

## Topology & Verification
![EtherChannel Topology](./screenshots/etherchannel%20topology.png)
![EtherChannel Summary](./screenshots/etherchannel%20brief.png)
