# 04. Centralized DHCPv4 Server & DHCP Relay Agent

Automated IPv4 address allocation across multiple subnets using a centralized router-based DHCPv4 server and `ip helper-address` relay configuration.

## Project Files
- [dhcp and relay.pkt](./cisco%20files/dhcp%20and%20relay.pkt) — Full topology featuring Router-on-a-Stick, static routing, multi-pool DHCPv4 server, and remote DHCP relay.

## Key Objectives & Technologies
- **Inter-VLAN & Static Routing:** Configured Router-on-a-Stick sub-interfaces (`G0/0/1.100`, `G0/0/1.200`) on R1 and default static routes between R1 and R2.
- **Switch Security:** Isolated unused switch ports into `VLAN 999` and configured `VLAN 1000` as the Native VLAN on trunk port `Fa0/5`.
- **Multi-Pool DHCPv4 Server (R1):** Excluded static gateway addresses (`ip dhcp excluded-address`) and configured separate DHCP pools for local and remote subnets.
- **DHCP Relay Agent (R2):** Configured `ip helper-address 10.0.0.1` on R2's LAN interface to forward broadcast DHCP requests as unicast packets to R1.

## Topology & Verification
![DHCPv4 and Relay Topology](./screenshots/dhcp%20topology.png)
![DHCPv4 Active Bindings](./screenshots/dhcp%20binding.png)
