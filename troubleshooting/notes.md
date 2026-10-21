# Design and Troubleshooting Notes

## Management port cleanup

The management PC was initially connected to a switch port configured as a trunk. Because an ordinary endpoint does not need to carry multiple tagged VLANs, Fa0/3 was converted to a static access port in VLAN 50:

```cisco
interface FastEthernet0/3
 description Management-PC
 switchport mode access
 switchport access vlan 50
 spanning-tree portfast
```

Unused trunk commands were removed. Verification confirmed static access operation and VLAN 50 assignment.

## Trunk hardening

Trunks initially allowed VLANs `1-1005`. They were restricted to the VLANs required by the lab:

```cisco
switchport trunk allowed vlan 10,20,30,50
```

## Initial ping loss

One inter-VLAN test lost its first ICMP echo while subsequent replies succeeded. In Packet Tracer, this commonly occurs while ARP entries are being resolved. Repeating the ping after ARP resolution should normally produce 0% loss.
