# DHCP Server Configuration

Server address: `192.168.1.5/24`  
Server gateway: `192.168.1.1`

| Pool | Gateway | DNS | Start | Mask | Maximum clients | WLC address |
|---|---|---|---|---|---:|---|
| IT-Pool | `192.168.10.1` | `8.8.8.8` | `192.168.10.11` | `255.255.255.0` | 200 | `192.168.50.5` |
| HR-Pool | `192.168.20.1` | `8.8.8.8` | `192.168.20.11` | `255.255.255.0` | 200 | `192.168.50.5` |
| FIN-Pool | `192.168.30.1` | `8.8.8.8` | `192.168.30.11` | `255.255.255.0` | 200 | `192.168.50.5` |
| MGMT-Pool | `192.168.50.1` | `8.8.8.8` | `192.168.50.11` | `255.255.255.0` | 200 | `192.168.50.5` |

R1 relays client DHCP broadcasts to this server with `ip helper-address 192.168.1.5` on each wireless VLAN subinterface.
