---
layout: post
title: "Neue testing Firmware 2017.1.4+mwu4"
author: MAGIC
teaser: "Unser Firmware-Team hat die neue testing Firmware 2017.1.4+mwu4 der Freifunk-Firmware veröffentlicht."
excerpt: "Da der radv-filterd Patch in 2017.1.4+mwu2 immer noch Probleme gemacht und beim (Neu)starten eines Knotens nicht immer zuverlässig gestartet ist haben wir versucht das Problem mit einem Patch, der in 2017.1.4+mwu3 eingeflossen ist, zu beheben."
---

Hallo Freifunkas in Mainz, Wiesbaden und Umgebung,

da der radv-filterd Patch in 2017.1.4+mwu2 immer noch Probleme gemacht und beim (Neu)starten eines Knotens nicht immer zuverlässig gestartet ist haben wir versucht das Problem mit einem Patch, der in 2017.1.4+mwu3 eingeflossen ist, zu beheben. Dieser Patch hat auch seinen Zweck erfüllt hätte aber aufgrund der unsauberen Implementierung zu Probleme führen können weshalb wir uns gegen das Ausrollen der Version entschieden haben. Glücklicherweise hat kurz darauf einer der Gluon Entwickler den gesamten radv-filterd einem Code Review unterzogen und mehrere Fehler gefunden und behoben. Diese Version haben wir für v2017.1.4 zurückportiert und darauf basierend den Release 2017.1.4+mwu4 gebaut.

Zusätzlich zu oben genannter Änderung haben wir uns dazu entschieden einen [Patch](https://github.com/freifunk-gluon/gluon/commit/f799518194307857510c0ce3ee9df582081353ee) aus der aktuellen Entwicklungsversion von Gluon zu übernehmen der die Bridge Loop Avoidance (BLA) funktionsfähig macht. In der Vergangenheit kam es immer wieder vor, dass Knotenbetreiber versehentlich (das hoffen wir jedenfalls) die LAN-Ports von zwei oder mehr Knoten verbunden haben ohne diese für Mesh-on-LAN zu konfigurieren. Dadurch wird eine Netzwerkschleife erzeugt, die den gleichen Traffic immer und immer wieder durch das Freifunk-Netz schickt bis dieses unbenutzbar wird. Mit dem Patch können zwei Knoten, die auf diese Weise verbunden sind, das Problem erkennen und die Schleife unterbrechen.


Wenn ihr Probleme mit dieser neuen Firmware feststellt schreibt bitte einen Fehlerbericht an unsere [Maschinenraum-Liste](https://lists.freifunk-mwu.de/mailman/listinfo/maschinenraum).

Happy Flashing wünscht,
das Firmware-Team

#### Infos zur neuen testing Firmware

* **MWU Firmware Version**: 2017.1.7+mwu4
* **Gluon Firmware Version**: v2017.1.7
* **Gluon Source Code**: [https://github.com/freifunk-gluon/gluon/releases/tag/v2017.1.4](https://github.com/freifunk-gluon/gluon/releases/tag/v2017.1.4)
* **Gluon Release-Notes**: [http://gluon.readthedocs.io/en/stable/releases/v2017.1.4.html](http://gluon.readthedocs.io/en/stable/releases/v2017.1.4.html)
* **MWU Gluon-Konfiguration**: [https://github.com/freifunk-mwu/sites-ffmwu/releases/tag/2017.1.4+mwu1](https://github.com/freifunk-mwu/sites-ffmwu/releases/tag/2017.1.4+mwu1)
* **Link zur Firmware Mainz**: [https://firmware.freifunk-mainz.de/stable](https://firmware.freifunk-mainz.de/testing)
* **Link zur Firmware Rheingau**: [https://firmware.freifunk-rtk.de/rheingau/](https://firmware.freifunk-rtk.de/rheingau/)
* **Link zur Firmware Taunus**: [https://firmware.freifunk-rtk.de/taunus/](https://firmware.freifunk-rtk.de/taunus/)
* **Link zur Firmware Wiesbaden**: [https://firmware.wiesbaden.freifunk.net/stable](https://firmware.wiesbaden.freifunk.net/testing)
