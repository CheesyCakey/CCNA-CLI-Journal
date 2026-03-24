1\) sh spanning-tree summary



2\) spanning-tree mode rapid-pvst



3\) 

***spanning-tree vlan 10 root primary***

***spanning-tree vlan 10 root secondary***



4\) 

int f0/1

spanning-tree portfast 

spanning-tree ***bpduguard enable***



***Portfast and BPDU Guard to be enabled on ports connected to PCs and routers***



5\)

int f0/21

***spanning-tree guard root***

