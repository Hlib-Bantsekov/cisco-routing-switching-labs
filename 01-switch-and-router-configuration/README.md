# 01. Basic Switch & Router Configuration

Initial CLI configuration, device hardening, and IPv4 interface setup for Cisco Catalyst switches and ISR routers in **Cisco Packet Tracer**.

## Project Files
- [router config.pkt](./cisco%20files/router%20config.pkt) — Cisco router baseline configuration and IPv4 interface addressing.
- [switch config.pkt](./cisco%20files/switch%20config.pkt) — Cisco Catalyst switch security hardening, console/VTY protection, and baseline setup.

## Key Objectives & Technologies
- **Device Hardening:** Configured hostnames, disabled DNS lookup (`no ip domain-lookup`), encrypted plaintext passwords (`service password-encryption`), and configured MOTD security banners.
- **Line Security:** Secured console and VTY lines with password authentication.
- **Interface Configuration:** Assigned IPv4 addresses and subnet masks on router interfaces and verified link states (`no shutdown`).

## Topology & Verification

### Router Configuration
![Router Topology](./screenshots/router%20topology.png)
![Router Interface Brief](./screenshots/router%20interface%20brief.png)

### Switch Configuration & Hardening
![Switch Topology](./screenshots/switch%20topology.png)
![Switch Running Configuration](./screenshots/switch%20running%20conf.png)
![Switch Interface Brief](./screenshots/swicth%20ip%20interface%20brief.png)
