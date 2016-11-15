---
layout: post
title: "Verbindungsprobleme mit dem Internet behoben"
author: günni, kokel
teaser: "Verbindungsprobleme mit dem Internet behoben."
excerpt: "Verbindungsprobleme mit dem Internet behoben."
---

**TL;DR:**
Die Verbindungspobleme ins Internet über das Freifunk-Netz während der letzten Wochen wurden behoben. Das Freifunk-Netz kann
intern sowie ins Internet wieder in gewohnter Weise genutzt werden. Der Fehler war nicht ganz einfach zu finden. Am Ende hat
eine Teilfunktion des verwendeten Mesh-Protokolls B.A.T.M.A.N Advanced auf unseren Gateways nicht richtig funktioniert.

* * *

**Für alle die sich etwas tiefer für die Fehlerursache interessieren, haben wir eine ausführlichere Meldung verfasst:**  
Wir setzen im Freifunk-Netz Mainz, Wiesbaden und Umgebung das Layer-2 Mesh-Protokoll B.A.T.M.A.N Advanced [[1](https://www.open-mesh.org/projects/batman-adv/wiki/Wiki)] ein, in Folge Batman genannt.
Dieses Protokoll ist hinter den Kulissen dafür verantwortlich, dass jeder das Freifunk-Netz ganz simpel durch das Aufstellen weiterer
Freifunk-Knoten erweitern kann. Freifunk-Knoten in WLAN-Reichweite verbinden sich mittels der WLAN Technologie Ad-Hoc (IBSS) untereinander
und tauschen hierüber Batman Nachrichten aus, um die restliche Topologie des Netzes zu "lernen". Dazu gehört u.A. die Information, welche
anderen Freifunk-Knoten (Batman Originators) es im Netz gibt, und über welchen Nexthop man diese erreicht sowie welche Clients im Netz
über welchen Freifunk-Knoten zu erreichen sind.

Man kann sich das Freifunk-Netz wie einen großen, verteilten Layer-2 Switch vorstellen, bei dem Batman die Backplane bildet.
Im Batman Protokoll werkeln mehrere Mechanismen, um die Skalierungsgrenzen, die man technologiebedingt in Layer-2 Ethernet-Segmenten hat,
zu erhöhen. Eine dieser Mechanismen ist die Distributed ARP Table [[2](https://www.open-mesh.org/projects/batman-adv/wiki/DistributedArpTable)], DAT genannt. Mit dieser wird ein über das Netz verteilter ARP Cache
gepflegt, um zum einen schneller auf ARP-Anfragen zu reagieren und zum anderen den Broadcast Traffic zu reduzieren.

Nun zu unserem Problem: Dieser Mechanismus hat auf den Gateways leider nicht ordnungsgemäß funktioniert, sodass ARP-Einträge der Clients,
die über die Gateways mit dem Internet kommunizieren wollten, nicht aktualisiert wurden. Rückpakete aus dem Internet konnten nicht zugestellt werden,
weil die Info über die Zuordnung von MAC- zu IP-Adressen auf den Gateways fehlerhaft war.

Diese DAT Funktion des Batman Protokolls wurde zunächst deaktiviert, um die Funktion wiederherzustellen. Parallel versuchen wir mit den Entwicklern
des Batman Protokolls herauszufinden, warum die DAT Funktion nicht richtig funktioniert hat.

[1] https://www.open-mesh.org/projects/batman-adv/wiki/Wiki  
[2] https://www.open-mesh.org/projects/batman-adv/wiki/DistributedArpTable
