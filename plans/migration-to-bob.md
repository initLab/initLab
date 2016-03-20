# Миграция на lab-а от cassie към bob


## компоненти по cassie

### Хардуер

* DONE реле за отваряне на вратата
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
	* не се ползва
* chaosVPN връзка


### софтуер

* asterisk
* arpwatch
	* има някакви мои patch-ове за да не реве
* fauna
	* има копие на bob
* mrtg
* lamps
* dhcpd
* bind9
* mpd
	* няма нужда от него
* client175 (web контрол за mpd)
	* няма нужда от него
* samba
	* отдавна никой не го ползва
	* стои там музиката на лаба
* chaosvpn
* radvd
* bgpd/quagga
	* ще се смени с bird, има вече подкаран на bob
* nginx
	* cassie.initlab.org cassie.ludost.net
	* fauna.initlab.org
	* vk.initlab.ludost.net
* метеорологичната станция
* doorpi monitoring
* switch monitoring


## План

### Предварително

* DONE native vlan 1 на порта на bob и другите нужни vlan-и
* DONE bgp daemon на bob
* setup на arpwatch на bob
* setup на asterisk-а на bob
	* слагане на звуците
	* копиране на скриптовете
	* връзване на външната регистрация да звъни и на bob
	* връзване на разните устройства към asterisk-а на bob
* DONE renumber на fauna на отделно ip
* install на bind9 и конфигуриране
* местене на lamps скрипта
	* копиране на нещото, дето смята залеза
* копиране на музиката
* копиране на mrtg
* местене на метеорологичната станция
* Вдигане на тунели до marla и tyler
* местене на doorpi и switch monitoring-а до bob

### местене

* start downtime
* местене на v4 и v6 gw адресите до bob
* спиране на dhcpd на cassie
* копиране на dhcpd конфигурацията и пускане
* спиране на radvd-то на cassie
* копиране и пускане на radvd на bob
* гасене на fauna
* dump на базата на fauna, преливане на bob
* местене на ip-то на fauna на bob
* палене на fauna на bob
* звънене на OD да сменим mac адреса
* вдигане на OD адреса на bob
* вдигане на openvpn-а до marla и tyler през OD


### Тестване

* Звънене на телефона
* fauna - отваряне, отключване, заклюване
* dhcp/свързаност за локалната мрежа
