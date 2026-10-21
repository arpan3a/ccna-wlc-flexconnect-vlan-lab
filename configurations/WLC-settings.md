# WLC Settings

## Controller

| Setting | Value |
|---|---|
| System name | XO-WLC |
| Model | Cisco 3504 |
| Management IP | `192.168.50.5` |
| Mask | `255.255.255.0` |
| Gateway | `192.168.50.1` |
| Management VLAN | 50 |
| Virtual IP | `192.0.2.1` |

## Dynamic interfaces

| Name | VLAN | Address | Mask | Gateway | DHCP server |
|---|---:|---|---|---|---|
| VLAN10 | 10 | `192.168.10.7` | `/24` | `192.168.10.1` | `192.168.1.5` |
| VLAN20 | 20 | `192.168.20.7` | `/24` | `192.168.20.1` | `192.168.1.5` |
| VLAN30 | 30 | `192.168.30.7` | `/24` | `192.168.30.1` | `192.168.1.5` |

## WLANs

| WLAN ID | Profile | SSID | Mapping | Security |
|---:|---|---|---|---|
| 1 | IT-WIFI | IT | VLAN10 | WPA2-PSK/AES |
| 2 | HR-WIFI | HR | VLAN20 | WPA2-PSK/AES |
| 3 | Finance-WIFI | FIN | VLAN30 | WPA2-PSK/AES |
| 4 | Management-WIFI | MGMT | Management/VLAN50 | WPA2-PSK/AES |

All WLANs are enabled. FlexConnect local switching and local authentication were enabled in this Packet Tracer lab. Pre-shared keys are intentionally excluded from the repository.
