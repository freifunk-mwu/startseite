---
layout: post
title: "Neue stabile Firmware 2016.2.2+mwu1"
author: kokel
teaser: "Unser Firmware-Team hat die neue stabile Version 2016.2.2+mwu1 der Freifunk-Firmware veröffentlicht."
excerpt: "Wir wünschen euch allen einen exzellenten Start in das neue Jahr 2017! Wir vom Firmware-Team beginnen das neue Jahr erstmal mit einer neuen _stabilen_ Firmware!"
---

Wir wünschen euch allen einen exzellenten Start in das neue Jahr 2017! Wir vom Firmware-Team beginnen das neue Jahr erstmal mit einer neuen _stabilen_ Firmware!
Seit 3-4 Monaten testen wir nun die neue Gluon Version 2016.2.x in einer nun schon recht langen Testphase - während dieser wurden seitens Gluon schon 2 Bugfix Releases veröffentlicht und auch wir haben ein paar Änderungen an der Konfiguration vorgenommen. Nun ist die Zeit gekommen, die Testphase abzuschließen und unsere Testing-Firmware als stabil zu deklarieren.

Die neue Firmware könnt ihr [hier](/firmware.html) herunterladen. Bestehende Knoten updaten sich automatisch innerhalb der nächsten 5 Tage, sofern ihr die Autoupdater-Funktion eingeschaltet habt. Bitte habt in dieser Zeit ein Auge auf eure Knoten.

Wenn ihr Probleme mit dieser neuen Firmware feststellt schreibt bitte einen Fehlerbericht an unsere [Maschinenraum-Liste](https://lists.freifunk-mwu.de/mailman/listinfo/maschinenraum).

Das Announcement zur ersten **2016.2+mwu1** Testing-Firmware (per Mail, es gab keinen Blog-Eintrag) ist nun schon etwas her, sodass wir hier nochmal alle Änderungen seit der letzten stabilen Version **0.3.3-stable** aufführen.

### Neues Versionsschema:
Beginnend mit diesem Release werden wir unser bisheriges Versionsschema einmotten und an das von Gluon angleichen. Außerdem haben wir bisher nach einer erfolgreichen Beta-Phase die Firmware immer komplett neu kompiliert was zur Folge hatte, dass Knoten mit Beta-Version sich ein weiteres mal aktualisiert haben wenn sie wieder auf Stable umgestellt wurden. Deshalb haben wir stable/beta aus dem Releasenamen entfernt und der Status einer Version wird jetzt dadurch festgelegt in welchem Ordner sie liegt. Zusätzlich wird der Beta-Branch in Testing umbenannt da dies den Status aus unserer Sicht besser widerspiegelt.
Eine detaillierte Beschreibung des Versionsschemas findet ihr auf [GitHub](https://github.com/freifunk-mwu/sites-ffmwu/blob/experimental/README.md#version-schema).

### Infos zur neuen stabilen Firmware

* **MWU Firmware Version**: 2016.2.2+mwu1
* **Gluon Firmware Version**: v2016.2.2
* **Gluon Source Code**: [https://github.com/freifunk-gluon/gluon/releases/tag/v2016.2.2](https://github.com/freifunk-gluon/gluon/releases/tag/v2016.2.2)
* **Gluon Release-Notes**: [http://gluon.readthedocs.io/en/stable/releases/v2016.2.2.html](http://gluon.readthedocs.io/en/stable/releases/v2016.2.2.html)
* **MWU Gluon-Konfiguration**: [https://github.com/freifunk-mwu/sites-ffmwu/releases/tag/2016.2.2+mwu1](https://github.com/freifunk-mwu/sites-ffmwu/releases/tag/2016.2.2+mwu1)
* **Link zur Firmware Mainz**: [https://firmware.freifunk-mainz.de/stable/](https://firmware.freifunk-mainz.de/stable/)
* **Link zur Firmware Rheingau**: [https://firmware.freifunk-rtk.de/rheingau/](https://firmware.freifunk-rtk.de/rheingau/)
* **Link zur Firmware Taunus**: [https://firmware.freifunk-rtk.de/taunus/](https://firmware.freifunk-rtk.de/taunus/)
* **Link zur Firmware Wiesbaden**: [https://firmware.wiesbaden.freifunk.net/stable/](https://firmware.wiesbaden.freifunk.net/stable/)


### Neu unterstützte Hardware-Modelle

|Hersteller|Modell|Gluon Target|
|----------|------|------------|
|ALFA Network|Tube2H N2|ar71xx-generic|
|ALFA Network|Tube2H N5|ar71xx-generic|
|Buffalo|WZR-HP-G300NH2|ar71xx-generic|
|GL Innovations|GL-AR150|ar71xx-generic|
|OpenMesh|MR1750 v1, v2|ar71xx-generic|
|OpenMesh|OM2P-HS v3|ar71xx-generic|
|OpenMesh|OM5P-AC v1, v2|ar71xx-generic|
|TP-Link|Archer C5 v1|ar71xx-generic|
|TP-Link|Archer C7 v2|ar71xx-generic|
|TP-Link|CPE210/510 EU/US Versionen|ar71xx-generic|
|TP-Link|TL-WR710N v2.1|ar71xx-generic|
|TP-Link|TL-WA801N/ND v3|ar71xx-generic|
|TP-Link|TL-WR841ND v11 EU/US Versionen|ar71xx-generic|
|TP-Link|TL-WR842N/ND v3|ar71xx-generic|
|TP-Link|TL-WA901ND v4|ar71xx-generic|
|Ubiquiti|UniFi AP AC Lite|ar71xx-generic|
|Ubiquiti|UniFi AP AC Pro|ar71xx-generic|
|Raspberry|Pi 1|brcm2708-bcm2708|
|Raspberry|Pi 2|brcm2708-bcm2709|

### Konfigurationsänderungen (site) seit Version "0.3.3-stable":
* neue Pakete zur Unterstützung diverser USB und PCI Netzwerkkarten zu den x86/x86-64 Images hinzugefügt
* GLUON_ATH10K_MESH und GLUON_REGION gesetzt um Geräte mit ath10k-Chip zu unterstützen
* [WLAN Frequenzen für 802.11b deaktiviert](http://blogs.cisco.com/wireless/wi-fi-taxes-digging-into-the-802-11b-penalty)
* Einheitliches Repository für eigene Gluon-Pakete
* Paket [gluon-ebtables-segment-mld](http://gluon.readthedocs.io/en/stable/package/gluon-ebtables-segment-mld.html) hinzugefügt
* Paket [tecff-ath9k-broken-wifi-workaround](https://github.com/freifunk-mwu/packages-ffmwu/tree/master/tecff-ath9k-broken-wifi-workaround) hinzugefügt
* Paket [ffmwu-beta-to-testing](https://github.com/freifunk-mwu/packages-ffmwu/tree/master/ffmwu-beta-to-testing) hinzugefügt:
  * Dieses Paket benennt den alten Firmware Branch "beta" in "testing" um
* Paket [gluon-radv-filterd](https://github.com/freifunk-mwu/packages-ffmwu/tree/master/gluon-radv-filterd) hinzugefügt:
  * Dieses Paket filtert alle [Router Advertisements](https://de.wikipedia.org/wiki/Neighbor_Discovery_Protocol#Router_Advertisement_.E2.80.93_Type_134) außer denen die vom aktuell gewählten B.A.T.M.A.N Advanced Gateway kommen
* Vier zusätzliche Gateways (spare) für zukünftige Nutzung hinzugefügt


### Wichtige Änderungen/Neuerungen in Gluon:

Hier sind nicht alle Änderungen aufgeführt, sondern nur ein Auszug.

* Viele Ubiquiti airMAX XM Modelnamen werden jetzt richtig erkannt (z.B. wird eine "Nanostation Loco M" nicht mehr als "Bullet M" angezeigt); [Pull Request](https://github.com/freifunk-gluon/gluon/pull/632)
* batman-adv: mesh_no_rebroadcast ist jetzt per default auf allen Mesh-on-WAN/LAN Verbindung aktiv; [Issue](https://github.com/freifunk-gluon/gluon/issues/652)
* Die neue UCI-Option gluon-core.@wireless[0].preserve_channels kann jetzt dazu genutzt werden um das Zurücksetzen geänderter WLAN-Kanäle bei einem Firmwareupdate zu verhindern; [Pull Request](https://github.com/freifunk-gluon/gluon/pull/640)
* PoE-Passthrough kann jetzt über die "Erweiterten Einstellungen" für TP-Link CPE 210/510 und Ubiquiti NanoStations aktiviert werden; [Issue](https://github.com/freifunk-gluon/gluon/issues/328)
* In Knotennamen können jetzt beliebige UTF-8 Zeichen benutzt werden; [Issue](https://github.com/freifunk-gluon/gluon/issues/414)
* Dropbear (SSH) wurde auf eine aktuellere Version aktualisiert, um neue Kryptographie Methoden zu erlauben und alte unsichere zu deaktivieren; [Issue](https://github.com/freifunk-gluon/gluon/issues/223)
* Die Stabilität des ath9k WLAN Treibers wurde signifikant verbessert; [Issue](https://github.com/freifunk-gluon/gluon/issues/605)
* Treiber und Dienste wie mac80211 und hostapd wurden aus LEDE 42f559e zurückportiert
* Der “Experten Modus/Expert Mode” wurde in “Erweiterte Einstellungen/Advanced Settings” umbenannt
* Die Statusseite kann mit deaktivierten Cookies/Local Storage aufgerufen werden
* Kernel auf 3.18.44 aktualisiert (CVE-2016-5195 + CVE-2016-7117)
* PATA und MMC Support für x86 und x86-64 Images (z.B. werden die Futros dadurch nun nativ unterstützt)

### Bugfixes

* Booten einiger QCA955x-basierten Geräte (z.B. OpenMesh OM5P AC v2); [Pull Request](https://github.com/freifunk-gluon/gluon/pull/965)
* Diverse Probleme bzgl. des Compiliervorganges
* Fehlerhafte Interfacezuordnung von WAN/LAN auf der CPE210; [Commit](https://github.com/freifunk-gluon/gluon/commit/59deb2064d54a37e27139b76a3b6064f5f10f364)
* Hohe CPU Auslastung aufgrund zu hoher LED-Frequenz der Signastärken Signalisierung; [Issue](https://github.com/freifunk-gluon/gluon/issues/897)
* Probleme mit dem Ethernet Port des Ubiquiti UAP AC Lite; [Issue](https://github.com/freifunk-gluon/gluon/issues/911)
* Fehlerhafter RX Filter auf dem Ubiquiti UAP Outdoor+; [Commit](https://github.com/freifunk-gluon/gluon/commit/d43147a8e03dd17bc27e4ab203736f2151f9db3d)

### Bekannte Probleme

* TX Power auf vielen Ubiquiti Geräten ist zu hoch; [Issue](https://github.com/freifunk-gluon/gluon/issues/94)
  * Manuelles Herabsetzen der TX Power via Expert Mode wird empfohlen
* MAC-Adresse des WAN Interfaces wird verändert, auch wenn Mesh-On-Wan deaktiviert ist; [Issue](https://github.com/freifunk-gluon/gluon/issues/496)
  * Führt zu Problemen wenn eine feste MAC-Adresse erwartet wird, z.B. bei VMware mit deaktiviertem Promiscious Mode
* Inkonsistente respondd/announced API; [Issue](https://github.com/freifunk-gluon/gluon/issues/522)
  - die aktuelle API ist inkonsistent und wird in einem zukünftigen Release ersetzt. Die alte API wird noch eine Weile unterstützt.
