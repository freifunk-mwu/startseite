---
layout: post
title: "Neue stabile Firmware 2016.2.6+mwu1"
author: MAGIC
teaser: "Unser Firmware-Team hat die neue stabile Version 2016.2.6+mwu1 der Freifunk-Firmware veröffentlicht."
excerpt: "Nachdem keine Fehlermeldungen mit der testing-version 2016.2.6+mwu1 eingegangen sind, ist diese Version nun wie angekündigt stable."
---

Hallo Freifunkas in Mainz, Wiesbaden und Umgebung,

Nach dem erfolgreichen Wechsel auf das [802.11s Mesh-Protokoll](https://de.wikipedia.org/wiki/IEEE_802.11s) steht eine weitere große Änderung bei Gluon ins Haus. Seit Samstag gibt es das neues Major Release v2017.1. 
Dieses basiert nicht mehr auf [OpenWrt](http://openwrt.org/) sondern auf [LEDE](https://lede-project.org/) (Linux Embedded Development Environment). LEDE ist ein Fork des OpenWrt Projektes, der vor etwas mehr als einem Jahr ins Leben gerufen wurde und seither viele Neuerungen erfahren hat. So wurde z.B. der Linux Kernel von 3.18 auf 4.4 aktualisiert. 
Bevor wir diesen allerdings verteilen können müssen wir noch die Version v2016.2.6 veröffentlichen, da es eine Änderung am Updateprozess gab auf den die Knoten mit diesem Release vorbereitet werden. Ansonsten bringt das Update lediglich neue Images für den TL-WR841N v12 mit, der bisher nur von unserer experimental Firmware unterstützt wurde.
Darüber hinaus haben wir das Paket *tecff-ath9k-broken-wifi-workaround* gegen *ffho-ath9k-blackout-workaround* ausgetauscht.

**Bitte achtet darauf, dass sich eure Knoten aktualisieren und aktualisiert auch eure Knoten, auf denen ihr Autoupdates deaktiviert habt, weil diese Version ein wichtiger Migrationsschritt zur nächsten Major-Version 2017.1 ist.**

Wenn ihr Probleme mit dieser neuen Firmware feststellt schreibt bitte einen Fehlerbericht an unsere [Maschinenraum-Liste](https://lists.freifunk-mwu.de/mailman/listinfo/maschinenraum).

Happy Flashing wünscht,
das Firmware-Team

#### Infos zur neuen stabilen Firmware

* **MWU Firmware Version**: 2016.2.6+mwu1
* **Gluon Firmware Version**: v2016.2.6
* **Gluon Source Code**: [https://github.com/freifunk-gluon/gluon/releases/tag/v2016.2.6](https://github.com/freifunk-gluon/gluon/releases/tag/v2016.2.6)
* **Gluon Release-Notes**: [http://gluon.readthedocs.io/en/stable/releases/v2016.2.6.html](http://gluon.readthedocs.io/en/stable/releases/v2016.2.6.html)
* **MWU Gluon-Konfiguration**: [https://github.com/freifunk-mwu/sites-ffmwu/releases/tag/2016.2.6+mwu1](https://github.com/freifunk-mwu/sites-ffmwu/releases/tag/2016.2.6+mwu1)
* **Link zur Firmware Mainz**: [https://firmware.freifunk-mainz.de/stable](https://firmware.freifunk-mainz.de/stable)
* **Link zur Firmware Rheingau**: [https://firmware.freifunk-rtk.de/rheingau/](https://firmware.freifunk-rtk.de/rheingau/)
* **Link zur Firmware Taunus**: [https://firmware.freifunk-rtk.de/taunus/](https://firmware.freifunk-rtk.de/taunus/)
* **Link zur Firmware Wiesbaden**: [https://firmware.wiesbaden.freifunk.net/stable](https://firmware.wiesbaden.freifunk.net/stable)
