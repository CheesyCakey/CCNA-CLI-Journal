1\) sh vlan brief

2\) sh int g0/0 switchport 

3\) 

**SW1:**

conf t

int g0/1

switchport mode trunk



**SW3:**

conf t

int g0/2

switchport mode trunk



**SW2:**

conf t 

int g0/1

switchport trunk encap dot1q

switchport mode trunk



int g0/2 

switchport trunk encap dot1q

switchport mode trunk



4\)

**SW1:**

conf t

vtp domain Flackbox

vtp mode server



5\)

**SW2:**

conf t

vtp mode transparent



6\)

**SW3:**

conf t

vtp mode client

*vtp domain Flackbox*



7 \& 10)

**vlan configuration on SW1:**

conf t

vlan 10

name ENG

vlan 20 

name SALES

vlan 199

name Native



int range f0/1-2

switchport mode access

switchport access vlan 10



int f0/3

switchport mode access

switchport access vlan 20



**vlan configuration on SW2:**

conf t

vlan 10

name ENG

vlan 20

name SALES

vlan 199

name Native



**vlan configuration on SW3:**

conf t

vlan 10

name ENG

vlan 20

name SALES

vlan 199

name Native



int range f0/1-2

switchport mode access

switchport access vlan 20



int f0/3

switchport mode access

switchport access vlan 10



8\) sh vlan brief



9\) 

**SW1:**

int g0/1

switchport trunk native vlan 199



**SW2:**

int g0/1

switchport trunk native vlan 199

int g0/2

switchport trunk native vlan 199



**SW3:**

int g0/2

switchport trunk native vlan 199



13\)

**R1:**

int f0/0

no shutdown

ip address 10.10.10.1 255.255.255.0



14\)

**R1:**

int f0/1

no shutdown

ip address 10.10.20.1 255.255.255.0



15\)

**SW2:**

int f0/1

switchport mode access

switchport access vlan 10

int f0/2

switchport mode access

switchport access vlan 20



19\)

**R1:**

int f0/0

no ip address 10.10.10.1 255.255.255.0



int f0/0.10

ip address 10.10.10.1 255.255.255.0

encap dot1q *10*



int f0/0.20

ip address 10.10.20.1 255.255.255.0

encap dot1q *20*



20\)

**SW2:**

int f0/1

switchport mode trunk

switchport trunk encap dot1q



24\)

**SW2:**

conf t

ip routing



25\)

**SW2:**

int vlan 10

ip address 10.10.10.1 255.255.255.0



int vlan 20

ip address 10.10.20.1 255.255.255.0























