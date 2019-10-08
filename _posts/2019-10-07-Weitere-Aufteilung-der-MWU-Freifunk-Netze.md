---
layout: post
title: "Weitere Aufteilung der MWU Freifunk-Netze"
author: Admin-Team
excerpt: "Umzug der Mainzer und Wiesbadener Knoten auf ihre neuen Netze"
teaser: "Umzug der Mainzer und Wiesbadener Knoten auf ihre neuen Netze"
---

Hallo Freifunker in Mainz, Wiesbaden und Umgebung,

Nachdem wir Anfang Mai bereits erfolgreich die Knoten aus Bingen, Rheingau, Taunus und Weilrod auf eigene Netze migriert haben, steht nun der Umzug der Mainzer und Wiesbadener Knoten auf ihre neuen Netze an. Der automatische Wechsel findet am Mittwoch den 30.10.2019 um 20 Uhr statt. Knoten die per Richtfunk angebunden sind, werden nicht umgestellt.
{: .text-justify}

Die technischen Hintergründe und Details zur Migration könnt ihr unserer letzten [Ankündigung](https://www.wiesbaden.freifunk.net/2019/03/17/Aufteilung-der-MWU-Freifunk-Netze.html) entnehmen. Bei weiteren Fragen könnt ihr euch auch gerne an die Admin-Liste wenden.
{: .text-justify}

<admin@lists.freifunk-mwu.de>

Solltet ihr Firewall-Regeln für eure(n) Knoten definiert haben, müsst ihr diese anpassen. Bisher wurden die Ports 10037/UDP (Mainz) und 10056/UDP (Wiesbaden) verwendet. Nach der Umstellung wird, je nach Domain, ein Port aus dem Bereich 10000-10007/UDP verwendet. Da es in Zukunft aber zu weiteren Änderungen an den Domains kommen kann empfehlen wir euch den Bereich 10000-10099/UDP freizugeben.
{: .text-justify .panel .callout .radius}

