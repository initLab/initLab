# Миграция на lab-а от cassie към bob


## компоненти по cassie

### Хардуер

* реле за отваряне на вратата - DONE
	* мигрирано на neomontana-та
* мрежова карта с mac адрес, дето ни го знаят доставчиците


### routing

* ip4 тунели до marla през TBC
* ip6 тунели до tyler през TBC
* openvpn до marla за v4 и v6 през OD
* ip4 тунели до tyler през TBC
* ip6 тунели до tyler през TBC
* openvpn до tyler за v4 и v6 през OD
* openvpn до Мартин
* chaosVPN връзка


### софтуер

* asterisk
* fauna
* mrtg
* lamps
* dhcpd
* bind9
* mpd
* client175 (web контрол за mpd)
* chaosvpn
* radvd
* bgpd/quagga
* nginx
	* cassie.initlab.org cassie.ludost.net
	* fauna.initlab.org
	* vk.initlab.ludost.net
