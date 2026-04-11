2)EIGRP



3\) sh ip route



5\) 

R1(config)# int f0/1

R1(config-if)# ipv6 address ***2001:DB8::1/64***

**R1(config-if)# no shutdown**



R1(config)# int f0/0

R1(config-if)# ipv6 address 2001:DB8:0:1::1/64

**R1(config-if)# no shutdown**



R2(config)# int f0/0

R2(config-if)# ipv6 address 2001:DB8:0:1::2/64

**R2(config-if)# no shutdown**



R2(config)# int f0/1

R2(config-if)# ipv6 address 2001:DB8:0:2::2/64

**R2(config-if)# no shutdown**



R3(config)# int f0/0

R3(config-if)# ipv6 address 2001:DB8:0:2::1/64

**R3(config-if)# no shutdown**



R3(config)# int f0/1

R3(config-if)# ipv6 address 2001:DB8:0:3::1/64

**R3(config-if)# no shutdown**



***6)***

***PC1(config)# int f0/0***

***PC1(config-if)# ipv6 address 2001:db8::/64 eui-64***

***PC1(config-if)# no shut***



***PC2(config)# int f0/0***

***PC2(config-if)# ipv6 address 2001:db8:0:3::/64 eui-64***

***PC2(config-if)# no shut***



7\) sh ipv6 int brief



8\) 

PC1:2001:DB8::200:CFF:FE47:14C0

PC2:2001:DB8:0:3:201:C7FF:FE50:8E8A



9\)

***R1(config)# int f0/1***

***R1(config-if)# ipv6 address FE80::1 link-local***



***R1(config)# int f0/0***

***R1(config-if)# ipv6 address FE80::1 link-local***



***R2(config)# int f0/0***

***R2(config-if)# ipv6 address FE80::2 link-local***



***R2(config)# int f0/1***

***R2(config-if)# ipv6 address FE80::2 link-local***



***R3(config)# int f0/0***

***R3(config-if)# ipv6 address FE80::3 link-local***



***R3(config)# int f0/1***

***R3(config-if)# ipv6 address FE80::3 link-local***



10\) sh ipv6 int brief



11\) sh ipv6 neighbor



13\) sh ipv6 protocols



***17) ipv6 route ::/0 2001:DB8:0::1***



18\) ipv6 route ::/0 2001:DB8:0:3::1



20\) 

R2(config)# ipv6 route 2001:db8::/64 2001:db8:0:1::1



***22) ipv6 unicast routing***



25\)

R1(config)# ipv6 route 2001:db8:0:2::/64 2001:db8:0:1::2

R1(config)# ipv6 route 2001:db8:0:3::/64 2001:db8:0:1::2



R2(config)# ipv6 route 2001:db8:0:3::/64 2001:db8:0:2::1

R2(config)# ipv6 route 2001:db8::/64 2001:db8:0:1::1



R3(config)# ipv6 route 2001:db8:0:1::/64 2001:db8:0:2::2

R3(config)# ipv6 route 2001:db8::/64 2001:db8:0:2::2















