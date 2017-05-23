---
layout: post
title: "Umstellung von IBSS auf 802.11s"
author: kokel
teaser: "Wir stellen den WLAN-Modus, der für die automatische WLAN-Verbindung zwischen Knoten, die in WLAN-Reichweite zueinander stehen, auf eine neue Technologie um."
excerpt: "Wir stellen den WLAN-Modus, der für die automatische WLAN-Verbindung zwischen Knoten, die in WLAN-Reichweite zueinander stehen, auf eine neue Technologie um."
---

### TL;DR
Wir stellen den WLAN-Modus, der für die automatische WLAN-Verbindung
zwischen Knoten, die in WLAN-Reichweite zueinander stehen, auf eine neue
Technologie um.
Alle Knotenbereiber werden gebeten ihre Freifunk-Knoten während des
Update-Zeitraums in Betrieb zu nehmen, damit diese mit der aktuellen
Firmware versorgt werden können. Andernfalls ist manuelle Arbeit im
Nachhinein erforderlich.

**Update-Zeitraum:** 06.06.2017 - 11.06.2017

#### WLAN-Mesh
Habt ihr euch schon einmal gefragt was dieses "Meshing" eigentlich
bedeutet und wofür das gebraucht wird?
Das "Meshing" ist eine besondere Funktion in Freifunk Netzwerken und
dafür verantwortlich, dass sich eure Freifunk-Knoten automatisch über
WLAN untereinander verbinden.
In WLAN-Meshes, die aus mehreren Freifunk-Knoten bestehen existieren
immer mehrere, mögliche Verbindungen zum Ziel, um die Daten von
Endgeräten weiter zu transportieren. Von diesen wird immer die mit der
besten Qualität für das Weiterleiten von Daten verwendet. Fällt ein
Knoten aus, wird automatisch eine andere Verbindung über einen anderen
Knoten verwendet. Dadurch wird ein dezentrales, selbstverwaltetes
WLAN-Netzwerk erst möglich. Es können Knoten ausfallen und dazugekommen,
ohne weitere Konfiguration.

Genau genommen sind beim "Meshing" zwei Technologien im Einsatz.
Freifunk-Knoten verwenden neben dem Client-WLAN (AP-Modus) ein zweites
WLAN im sogenannten [IBSS](https://de.wikipedia.org/wiki/Ad-hoc-Netz)-Modus (auch als Ad-hoc-Modus bekannt). Dieses
wird auch auf Endgeräten mit so einem komischen Namen wie z.B.
"64:32:16:08:04:02" ([SSID](https://de.wikipedia.org/wiki/Service_Set#Service_Set_Identifier)) angezeigt.
Wenn zwei WLAN Geräte, in unserem Fall die Freifunk-Knoten, im
IBSS-Modus dieselbe SSID verwenden, wird automatisch eine WLAN
Punkt-zu-Punkt Verbindung aufgebaut. In WLAN-Meshes mit mehreren Knoten
findet hierdurch eine Vollvermaschung statt.
Ohne Weiteres bringen uns diese Punkt-zu-Punkt Verbindungen aber nicht
viel. Jede dieser Punkt-zu-Punk Verbindungen kann man sich wie ein
LAN-Kabel zwischen zwei PCs vorstellen, die man ohne weitere
Konfiguration (IP-Adressen) nur bedingt nutzen kann.
Hier kommt das Mesh-Protokoll [B.A.T.M.A.N Advanced](https://www.open-mesh.org/projects/batman-adv/wiki) zum Einsatz, dass
unsere Freifunk-Knoten über die WLAN IBSS-Verbindung für die oben
angesprochenen Funktionen der automatischen Wegewahl sowie dynamisches
Umrouting verwenden.

#### Umstellung auf 802.11s
Die IBSS-Technologie hat leider verschiedene Nachteile, weswegen die
IEEE einen neuen Standard für WLAN Mesh Verbindungen geschaffen hat.
Dieser ist sowohl effizienter, als auch stabiler als der häufig nur
schlecht implementierte IBSS-Modus. Dieser Standard heißt [IEEE 802.11s](https://de.wikipedia.org/wiki/IEEE_802.11s)
und ist bereits seit einiger Zeit in Gluon verfügbar.
Da auch wir von diesen Vorteilen und der neueren Technik profitieren
möchten, wechseln wir in einem zweistufigen Verfahren mit den Firmware
Updates 2016.2.5+mwu2 und 2016.2.5+mwu3 von IBSS auf 802.11s.

Bei der Umstellung gehen wir wie folgt vor: In Version 2016.2.5+mwu2
aktivieren wir zusätzlich zum bestehenden IBSS-Modus 802.11s. Das führt
dazu, dass die Knoten dann beide Modi parallel benutzen. In Version
2016.2.5+mwu3 deaktivieren wir dann den IBSS-Modus. Dieser zweistufige
Prozess ist notwendig, um auch alle Mesh-Only Knoten mit zu nehmen, die
wir sonst bei einer harten Umstellung eventuell vom Netz abtrennen
würden. Mesh-Only Knoten können Firmware-Updates nur über die
Mesh-Verbindung erhalten.

##### Zeitplan
**Phase 1:** Verteilung der Firmware 2016.2.5+mwu2 (IBSS+802.11s) per
Autoupdater im Zeitraum 06.06.2017 - 09.06.2017  
**Phase 2:** Verteilung der Firmware 2016.2.5+mwu3 (802.11s) per Autoupdater
ab 09.06.2017

**Sehr wichtig:** Bitte sorgt dafür, dass eure Freifunk-Knoten (vor allem
Mesh-Only Knoten) während des Update-Zeitraum angeschlossen und mit dem
Freifunk-Netz verbunden sind!
Sobald die Phase 2 abgeschlossen ist, können Knoten, die mit einer
Firmware-Version 2016.2.5+mwu1 oder älter laufen, nicht mehr mi
aktuellen Knoten meshen. Mesh-Only Knoten, die während des
Update-Zeitraums offline waren, müssen manuell mit der neuen Firmware
versorgt werden.

*Wir bitten daher alle Knotenbetreiber darum, ihren Knoten online zu
nehmen, damit diese das Firmware-Update erhalten können und später keine
manuelle Arbeit notwendig wird.
Für Knoten die während oder nach dem Update in Probleme laufen, stehen
wir natürlich via Maschinenraum-Liste mit Rat und Tat zur Seite.*

<div class="panel callout radius">
ACHTUNG:  
Bei Geräten mit ath10k Treiber ist diese Art der Migration leider nicht sicher
und das Gelingen hängt von der Reihenfolge ab, in der sich die Knoten aktualisieren.
Aufgrund einer Limitierung in der Firmware können IBSS und 802.11s nicht gleichzeitig aktiviert werden.
Wenn ihr TP-Link Archer C5 oder C7 betreibt bitten wir euch, diese Geräte und
ihre Nachbarknoten manuell auf 2016.2.5+mwu3 zu aktualiseren.
</div>
