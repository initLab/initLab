Switch in the corridor rack
===========================

* WS-C3750G-24PS
* serial port 9600
* telnet user root
* internal ip 192.168.192.6, in vlan 1

Ports
-----

|Port|Name|
|----|----|
|Gi1/0/1   |spitfire|
|Gi1/0/2   |spitfire/ilo|
|Gi1/0/3   |PP24/AP-paiak|
|Gi1/0/4   |ups|
|Gi1/0/5   |mp104 (phones)|
|Gi1/0/6   |ripe atlas|
|Gi1/0/7   |leica (user)|
|Gi1/0/8   |WR7/PP14/lecture-sw|
|Gi1/0/9   |PP3/WR3/ap-work|
|Gi1/0/10  |tmp:WR8/PP4/ruby|
|Gi1/0/11  |tmp:vin/onboard (openfest server)|
|Gi1/0/12  |tmp:vin/10gbe (openfest server)|
|Gi1/0/13  |beta (backup login)|
|Gi1/0/14  |netcontrol|
|Gi1/0/15  |WR9/wr-switch|
|Gi1/0/16  |tmp:WR5/PP12/studio|
|Gi1/0/22  |WR1/PP16/casshe|
|Gi1/0/23  |PP23/doorpi|
|Gi1/0/28  |ipacct (external fiber)|


VLANs
-----

* 1 - mgmt
* 2 - lan
* 8 - devices
* 9 - colocation
* 10-25 - openfest test vlans
* 38 - lab streaming
* 1024 - internal
* 4001 - ipacct-to-3dc/marla

