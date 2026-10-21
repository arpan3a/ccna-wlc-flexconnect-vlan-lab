# Verification Checklist

## Layer 2

- [x] VLANs 10, 20, 30, and 50 exist on SW1.
- [x] VLAN 50 is the native VLAN on genuine trunk links.
- [x] Trunks allow only VLANs 10, 20, 30, and 50.
- [x] Fa0/3 is a static access port in VLAN 50.
- [x] Fa0/3 does not appear in `show interfaces trunk`.

## Routing and DHCP

- [x] R1 has gateway subinterfaces for all four VLANs.
- [x] R1 relays DHCP requests to `192.168.1.5`.
- [x] Each wireless client receives an address from the correct scope.
- [x] Clients receive the correct default gateway.

## WLC and WLANs

- [x] WLC management is reachable at `192.168.50.5`.
- [x] Dynamic interfaces exist for VLANs 10, 20, and 30.
- [x] Four WLANs are enabled.
- [x] WLANs map to their intended interfaces/VLANs.
- [x] WPA2-PSK with AES is enabled.
- [x] FlexConnect local switching is enabled.

## Connectivity

- [x] Management PC reaches `192.168.50.1`.
- [x] Management PC reaches `192.168.50.5`.
- [x] VLAN 50 wireless client reaches a VLAN 10 wireless client.

## Additional recommended captures

- [ ] WLC Monitor > Access Points showing all APs joined.
- [ ] WLC Monitor > Clients showing associated tablets.
- [ ] A second inter-VLAN ping after ARP resolution showing 0% loss.

Recommended IOS commands:

```cisco
show vlan brief
show interfaces trunk
show interfaces FastEthernet0/3 switchport
show ip interface brief
show ip route
```
