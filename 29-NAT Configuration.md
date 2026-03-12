1\) 

ip nat inside source static 10.0.1.10 203.0.113.3



int f0/1

ip nat inside



int f0/0

ip nat outside



4\) sh ip nat translation



5\)

int f1/0

ip nat inside



int f0/0

ip nat outside



ip nat pool Flackbox 203.0.113.4 203.0.113.12 ***netmask*** 255.255.255.240



access-list 1 permit 10.0.2.0 0.0.0.255



ip nat inside source list 1 pool Flackbox 



6\) debug ip nat



7\) ***sh ip nat translation*** 



9\) 

***clear ip nat translation \****

***ip nat inside source list 1 pool Flackbox overload***



11\) \& 12) 

int f0/0

shutdown

no ip address ***203.0.113.2 255.255.255.240***

ip address dhcp 

no shutdown



13\)

int f1/0

ip nat inside



int f0/0

ip nat outside



***ip nat pool int f0/0 (no need)***

access-list 1 permit 10.0.2.0 0.0.0.255

ip nat inside source list 1 int f0/0 overload



14\) debug ip nat



17\) sh ip nat translation



18\) sh ip nat statistics





