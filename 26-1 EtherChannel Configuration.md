1\) 100 Mbps



2\) \& 4)

***int range f0/23-24***

***channel-group 1 mode active/desirable/on*** 

***int port-channel 1***

***description LINK TO CD1***

***switchport mode trunk***

***switchport trunk native vlan 199***



9\)

int range 

channel-group 1 mode active

int port-channel 1

ip address 192.168.0.1 255.255.255.252

no shutdown



12\) sh etherchannel summary



13\) 

router ospf 1

network 192.168.0.0 0.0.0.255 area 0



14\) 

sh ip route

sh ip ospf neighbor

