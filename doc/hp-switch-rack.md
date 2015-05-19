HP 2424/rack/corridor
=====================

* Model HP procurve 2626
* serial port 9600
* ssh user admin
* internal ip 192.168.192.3, in vlan 1

Ports
-----

* 1 - ripe atlas
* 2 - relay control
* 3 - door pi
* 24 - emergency mgmt
* 25 - bob (trunk)
* 26 - workroom (trunk)

VLANs
-----

* 1 - mgmt
	* untagged 24
	* native/untagged 25, 26
* 2 - lan
	* untagged 1
	* tagged 25, 26
* 5 - online direct
	* tagged 25, 26
* 6 - tbc
	* tagged 25, 26
* 8 - doorpi
	* untagged 2,3
	* tagged 25, 26
