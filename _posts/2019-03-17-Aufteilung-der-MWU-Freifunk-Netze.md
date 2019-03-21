---
layout: post
title: "Aufteilung der MWU Freifunk-Netze"
author: Admin-Team
excerpt: "Das Wachstum der letzten Jahre ist technisch nicht spurlos am Freifunk-Netz vorbeigegangen. Um weiter wachsen zu können und Ressourcen besser auszunutzen wird das Netz in den kommenden Wochen in Domains aufgeteilt."
---

Hallo Freifunkas in Mainz, Wiesbaden und Umgebung,

das Wachstum der letzten Jahre ist technisch nicht spurlos am Freifunk-Netz vorbeigegangen. Um weiter wachsen zu können und Ressourcen besser auszunutzen wird das Netz in den kommenden Wochen in Domains aufgeteilt.
{: .text-justify}

### Technischer Hintergrund

Das Freifunk-Netz ist technisch gesehen ein großes Layer 2 (Ethernet) Netzwerk. Man kann sich das Freifunk-Netz also wie einen übergroßen Switch vorstellen, an dem alle Teilnehmer (Nutzer wie Knoten) angeschlossen sind. Damit alle Knoten das Wissen besitzen um Daten in die richtige Richtung zu senden müssen in regelmäßigen Abständen alle Knoten eine Nachricht aussenden, die bestätigt, dass sie noch Teil des Netzes sind. Dieser und noch weitere Management-Datenverkehre (ARP, NDP) sind im Falle unseres Netzes nun bei etwa 170 kbit/s, die an jedem Knoten anfallen, in der täglichen Spitze angekommen.
{: .text-justify}

Ein Aufteilen des Netzes in mehrere Domains führt zu einer drastischen Reduzierung dieses Datenverkehrs, da Routinginformationen an viel weniger Knoten verteilt werden müssen.
{: .text-justify}

### Domainauswahl & Meshfähigkeit

Freifunker, welche einen neuen Knoten flashen, werden bereits seit Firmware *2018.1.1+mwu1* zur Auswahl einer solchen Domain aufgefordert. Die aktuelle Aufteilung orientiert sich an den verschiedenen Communities im MWU Gebiet. Mainz, Wiesbaden, Bingen, Rheingau, Taunus, Weilrod und seit neustem Limburg.
{: .text-justify}

![graphische Darstellung der Domains auf einer Karte](https://i.ibb.co/D16ZYfQ/domains.png)

Jeder eingezeichnete Bereich entspricht einer solchen Domain. Nur Knoten innerhalb der gleichen Domain können miteinander meshen. An diesen Grenzen wird es in Zukunft immer wieder Änderungen geben um die Netze den aktuellen Gegebenheiten anzupassen.
{: .text-justify}

### Automatische Migration
In den nächsten Wochen werden wir Knoten, die eine aktuelle Stable-Firmware (*2018.2+mwu2* und neuer) einsetzen, automatisch eine passende Zieldomain zuweisen, da wir nicht erwarten, dass wir in der gebotenen Kürze der Migration jeden Betreiber erreichen und zur manuellen Rekonfiguration bewegen können. Die automatische Migration erfolgt dann zu einem programmierten Zeitpunkt, damit vorhandene Mesh-Netze gleichzeitig rekonfiguriert werden, so dass nur eine kurzzeitige Unterbrechung entsteht.
{: .text-justify}

Für die automatische Domainmigration beziehen wir automatisch die [BSSID](https://de.wikipedia.org/wiki/Service_Set#SSID,_ESSID_und_BSSID) und Empfangsstärke benachbarter WLAN-Netze von den Knoten, die wir ausschließlich für die temporäre Geolokalisierung der Knoten verwenden und nicht dauerhaft speichern. Dies ist notwendig, da wir für eine große Menge von Knoten keinerlei Positioninformationen kennen, diese aber grob bekannt sein müssen um die passende Zieldomain auszuwählen. Sollten keine WLAN-Netze in der Nähe sein, so wird die Position des Knotens auf der Karte herangezogen. Die Funktion der automatischen Domainmigration kann im Config-Mode unter **Erweiterte Einstellungen -> Multidomain** oder über die Kommandozeile deaktiviert werden. Wir empfehlen aber diese Option aktivert zulassen, so dass euer Knoten immer in die für ihn am passendste Domain wechseln kann.
{: .text-justify}

~~~
uci set ffda.director.enabled='0'
uci commit ffda
~~~

<p>
<div class="alert-box secondary">
Ja, <b>ffda</b> ist an dieser Stelle richtig! Die Erweiterung stammt vom Freifunk Darmstadt und um Namenskonflikte mit anderen Gluon Paketen zu vermeiden wird hier der Präfix <i>ffda</i> verwendet.
</div>
</p>

Es werden im ersten Schritt nur Knoten migriert die sich aktuell in den Domains **ffbin**, **ffrhg** und **ffta** befinden. Knoten aus den Domains **ffwi** und **ffmz** werden noch nicht berücksichtigt.
{: .text-justify}

Den genauen Zeitpunkt für den Wechsel geben wir bekannt sobald alle Knoten auf *2018.2+mwu2* oder neuer aktualisiert wurden.
{: .text-justify}

### Manuelle Migration

Falls du schon früher in deine Zieldomain wechseln möchtest, kannst du dies, ab Firmware *2018.2+mwu2*, einfach über den Konfigurationsmodus tun. Dort ist dann ein Drop-Down-Menü mit den neuen Domains zu finden.
{: .text-justify}

### Häufige Fragen

##### Was passiert, sollte mein Freifunk-Knoten am Stichtag ausgeschaltet sein?

In diesem Fall muss unterschieden werden, ob dein Knoten eine VPN-Verbindung zu unseren Gateways aufbaut oder ob dieser ein reiner Mesh-Knoten ist.
{: .text-justify}

Sollte dein Knoten eine Verbindung zu unseren Gateways haben, wird dieser innerhalb von 24 Stunden seine Zieldomain erfragen und in diese wechseln.
{: .text-justify}

Ist dein Knoten ein reiner Mesh-Knoten, so kommt es darauf an, ob dieser bereits vor dem Stichtag die Firmware *2018.2+mwu2* bezogen hat und anschließend im Freifunk-Netz aktiv war oder nicht. War der Knoten mit dieser Firmware vor dem Stichtag bereits im Netz und hat seine Zieldomain bezogen, so wechselt er innerhalb von 7 Stunden automatisch in seine Zieldomain. Während dieses Zeitraums ist der Knoten allerdings offline!
{: .text-justify}

Sollte dein Knoten noch mit einer älteren Firmware laufen, so ist eine Aktualisierung sowie manuelle Einstellung der Domain nötig. Aktualisiere hierfür über den Config-Mode zuerst die Firmware. Anschließend kannst du, ebenda, deine zugehörige Domain auswählen.
{: .text-justify}

#### Was ist mit bestehenden Mesh-Netzen?

Wir beachten aktuell bestehende Mesh-Verbindungen und behalten diese auch während der Migration bei. Besteht eine Mesh-Verbindung zwischen zwei Knoten mit unterschiedlichen Zieldomains, werden beide Knoten der gleichen Zieldomain zugeordnet. Die erste in einem Mesh ermittelte Domain gilt für alle Knoten in dieser Meshwolke.
{: .text-justify}

#### Was ist nach der Umstellung zu beachten?

Für Clients passiert die Umstellung weitgehend unbemerkt. Allerdings werden nun IPv6-Adressen mit einem anderen Präfix vergeben. Damit ändert sich auch die IP-Adresse deines Knotens. Die neue IPv6-Adresse deines Knotens kannst du auf unserer Karte in Erfahrung bringen.
{: .text-justify}

