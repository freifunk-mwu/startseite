---
layout: post
title: "Aktuelle Probleme mit der Internetverbindung"
author: günni, mattsches
teaser: "Ab dem 15.09.2016 aktivieren wir öffentliches IPv6 im Freifunk-Netz."
excerpt: "Ab dem 15.09.2016 aktivieren wir öffentliches IPv6 im Freifunk-Netz. Was das bedeutet und wieso wir das machen."
---

In den letzten Tagen kam es immer wieder zu Problemen beim Surfen über Freifunk Wiesbaden. Wir sind diesen Problemen auf den Grund gegangen.

Die Störung hat leider gleich mehrere Ursachen. Eine Ursache liegt am dezentralen Ansatz von Freifunk, der dazu führt, dass wir gleich vier Gateways, also Server im Internet, betreiben. Die Gateways kommunizieren untereinander. Seit der [Umstellung auf öffentliche IPv6-Adressen](/2016/08/24/Public-IPv6-Aktivierung.html) ist der Datenverkehr zwischen den Gateways angestiegen. Wir werden daher die Kommunikation in Bahnen lenken, indem wir zwischen den Gateways virtuelle Tunnel einrichten. So wird die Intergate-Kommunikation reduziert.

Eine zweite Ursache war ein Konfigurationsfehler auf einem der Gateways, der mittlerweile behoben worden wurde. Die dritte Ursache ist etwas schwieriger zu beheben, da sie zum wesentlichen Teil auf unserer aktuell angewandten Technik beruht. Wir setzen das Programm [fastd](https://wiki.freifunk.net/Fastd) für die gesicherte Verbindung zwischen Knoten und Gateways ein. Dieses Programm stellt in unserem Fall einen Flaschenhals dar, da es nicht parallel mehrere CPU-Kerne auslasten kann.

Wir hoffen jedoch, dass schon durch die ersten von uns vorgenommenen Änderungen das Surfen bereits wieder reibungslos funktioniert, und bitten um etwas Geduld.
