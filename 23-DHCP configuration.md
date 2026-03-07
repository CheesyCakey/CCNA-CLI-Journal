1\)

R1:

conf t

int f0/0

ip address dhcp

***no shutdown***



3\) ***sh dhcp lease***



4\)

R1:

ip dhcp excluded-address 10.10.10.1 10.10.10.10

ip dhcp pool PC

dns-server 10.10.20.10

default-***router*** 10.10.10.1

***network 10.10.10.0 255.255.255.0***



8\) sh ip dhcp binding



9\) 

R1:

no ip dhcp pool PC

no ip dhcp excluded-address 10.10.10.1 10.10.10.10



13\)

R1:

int f0/1

ip helper-address 10.10.20.10



