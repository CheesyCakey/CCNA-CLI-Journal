1\)

~~SW1(config)# vlan 99~~

~~SW1(config-vlan)# UNUSED~~

SW1(config)# int range f0/3-24

SW1(config-if)# shutdown

~~SW1(config-if)# switchport mode access~~

~~SW1(config-if)# switchport access vlan 99~~



SW1(config)# int range g0/1-2

SW1(config-if)# shutdown



2\)

SW1(config)# int f0/1

**SW1(config-if)# switchport mode access**

SW1(config-if)# switchport port-security

SW1(config-if)# switchport port-security maximum 2

SW1(config-if)# switchport port-security mac-address 0000.1111.1111



3\) 

SW1(config)# int f0/2

SW1(config-if)# switchport mode access

SW1(config-if)# switchport port-security



4)ping 



5\) sh port-security **address**



6\) sh port-security int f0/1, sh port-security int f0/2



