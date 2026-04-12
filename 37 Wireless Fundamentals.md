1\)

S1(config)# vlan 10

S1(config-vlan)# name Management



2\) 

S1(config)# int **vlan 10**

S1(config-if)#ip address 192.168.10.1 255.255.255.0



5\) 

S1(config)# vlan 22

S1(config-vlan)# name Corporate



6\)

S1(config)# int **vlan 22**

S1(config-if)#ip address 192.168.22.1 255.255.255.0



7\) 

S1(config)# vlan 23

S1(config-vlan)# name Guest



8\)

S1(config)# int **vlan 23**

S1(config-if)#ip address 192.168.23.1 255.255.255.0



10\)

S1(config)# int g1/0/5

***S1(config-if)# switchport trunk encap dot1q***

S1(config-if)# switchport mode trunk

S1(config-if)# switchport trunk allowed vlan **10**,22,23

***S1(config-if)# spanning-tree portfast trunk***



11\)

S1(config)# int range g1/0/3-4

**<i>~~S1(config-int-range)# switchport trunk encap dot1q~~</i>**

S1(config-int-range)# switchport mode ~~trunk~~ access

S1(config-int-range)# switchport access vlan 10

~~S1(config-int-range)# switchport trunk allowed vlan **10**,22,23~~

***S1(config-int-range)# spanning-tree portfast ~~trunk~~***







