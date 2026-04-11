1\) ping



2\)



R1(config)# access-list 1 deny 10.0.2.0 0.0.0.255

**R1(config)# access-list 1 permit 10.0.1.0 0.0.0.255**

R1(config)# int f0/0

R1(config-if)# ip access-group 1 out



3\) ping



4\)

R1(config)# access-list 100 permit tcp host 10.0.1.10 host 10.0.0.2 eq 23

~~R1(config)# access-list 100 deny ip any any~~

**R1(config)# access-list 100 deny tcp 10.0.1.0 0.0.0.255 host 10.0.0.2 eq 23**

**R1(config)# access-list 100 permit ip any any**



**R1(config)# int f1/0**

**R1(config-if)# ip access-group 100 in**



6\) sh access-list 

**sh access-lists 100**



7\)

R1(config)# ip access-list extended RULE

R1(config-ext-nacl)# permit tcp host 10.0.1.10 host 10.0.0.2 eq telnet

R1(config-ext-nacl)# deny tcp 10.0.1.0 0.0.0.255 host 10.0.0.2 eq telnet

R1(config-ext-nacl)# permit **icmp** host 10.0.1.11 host 10.0.0.2 ~~eq~~ echo ~~request~~ 

R1(config-ext-nacl)# deny ~~ip~~ **icmp** 10.0.1.0 0.0.0.255 host 10.0.0.2 ~~eq~~ echo ~~request~~

R1(config-ext-nacl)# permit ip any any



**R1(config)# int f1/0**

**R1(config-if)# ip access-group RULE in**

