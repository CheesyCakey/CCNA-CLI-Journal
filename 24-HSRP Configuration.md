1\)

|R1|R2|
|-|-|
|conf t<br />int g0/1<br />ip address 10.10.10.2 255.255.255.0<br />no shutdown<br />standby 1 ***ip*** 10.10.10.1|conf t<br />int g0/1<br />ip address 10.10.10.3 255.255.255.0<br />no shutdown<br />standby 1 ***ip*** 10.10.10.1|



2) ***sh standby*** (check HSRP state)



8\)

R1:

conf t

int g0/1

***standby 1 priority 110***



10\)

R1:

conf t

int g0/1

standby 1 preempt



{Highest priority router → preempt}





