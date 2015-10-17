Asus switch/workroom
====================

* model Asys GigaX 1124+
* serial port 115200/no flow/8n1
* internal ip 192.168.192.8, in vlan 1

Ports
-----

DONE * 1 - pp1/online direct
DONE * 2 - tbc
DONE * 5 - airport
* 6 - pp 12/studio
DONE * 7 - pp 17/printer
DONE * 8 - pp 4/ruby room, chernobyl
DONE * 9 - pp 14/lecture hall, TMI
* 10 - pp 15/lecture hall/bench
* 11 - pp 6/lecture hall/door
* 12 - pp 11/studio
* 13 - pp 13/lecture hall
* 14 - pp 22/
* 15 - ripe atlas
DONE * 19 - coridor rack (trunk)
DONE * 20 - doorpi
* 21 - emergency mgmt
* 22 - cassie (trunk)

Vlans
-----

* 1 - mgmt
	* native/untagged 19
	* untagged 21, 22
* 2 - lan
	* ports 4-18 untagged
	* port 19, 22 tagged
* 5 - onlinedirect
	* port 1 untagged
	* port 19, 22 tagged
* 6 - tbc
	* port 2 untagged
	* port 19, 22 tagged
* 8 - doorpi
	* port 20 untagged
	* port 19, 22 tagged
