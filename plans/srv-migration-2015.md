Миграция на сървърите на initlab към rack-а в коридора
======================================================

* Планирана дата: няма
* Време: един ден
* Downtime: под 2 часа


Цел
---

* Да се махне cassie
* Всички неща от cassie да идат на bob
	* fauna
	* asterisk
	* отваряне на вратата
	* router/nat/firewall
		* gwping
		* quagga/bgpd
	* weather station
	* cassie.initlab.org сайт
	* музика
	* freeradius
	* mrtg
* Да се премести bob в rack-а в коридора
* Да се премане rack-а от работната стая, там да останат само:
	* patch панела
	* оптичния конвертор на TBC
	* един по-тих switch
	* малкия ups
* Да си освободим един порт в аквариума, който да може да се ползва
* Да пуснем по възможност мрежата на лаба на гигабит


Защо
----

* Cassie почнаха да и горят разни неща
* Rack-а заема много място в работната стая и имаме вече къде да сложим друг

Действия преди Dday
-------------------

* Пускане на нов кабел от работната стая до rack-а в коридора
* Подготвяне на rack-а в коридора
	* измиване
	* преместване на техниката, която няма да се ползва най-отдолу
	* поставяне на тави
	* поставяне на switch
		* XXX още не е ясно дали ще сложим switch или директно ще забием кабела в bob
	* Пускане на захранване от стената до rack-а
* Тестване на двупортовата серийна платка
* Update на bob
	* update до jessie
	* инсталация на нужните пакети
	* partiton-и
	* инсталация на fauna и средата и
		* ruby
		* postgresql
	* инсталация на asterisk, копиране на конфигурацията
	* инсталация на freeradius

D-Day
-----

* гасене на bob
	* Инсталиране на двупортовата серийна платка
	* Модификации така че да може да се включва лесно релето в него
	* Местене в rack-а в коридора
* Начало на downtime
	* обаждане в tbc да ни свалят от monitoring
	* гасене на целия rack в работната стая
* местене на техника от rack-а в работната стая до коридора
	* UPS
* разглобяване на rack-а в работната стая
	* Вадене на patch-панела така, че да не му се прекъсват връзките
* До-окабеляване на rack-а в коридора
	* Прехвърляне на кабела до бутона за отваряне на вратата в rack-a
	* Свързване на кабела до работната стая до switch-а в rack-а (или до bob)
	* Прехвърляне и свързване на UPS-а и разклонителите му
* Включване на RIPE atlas-а


Проверка
--------

* Тест на отключването на вратата
* Тест на отварянето на вратата
* Тест на двете internet връзки
* Тест на ipv6 свързаността
* Тест на wifi мрежата

Post-D-Day
----------

* Подкарване на метеорологичната станция на bob