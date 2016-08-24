---
layout: post
title: "Aktivierung von öffentlichem IPv6 am 15.09.2016"
author: kokel (in Zusammenarbeit mit der Community/ basiert auf Blog-Eintrag von Freifunk Mainz)
teaser: "Ab dem 15.09.2016 aktivieren wir öffentliches IPv6 im Freifunk-Netz."
excerpt: "Ab dem 15.09.2016 aktivieren wir öffentliches IPv6 im Freifunk-Netz. Was das bedeutet und wieso wir das machen."
---

Schon seit Längerem planen wir die Aktivierung von öffentlichem [IPv6](https://de.wikipedia.org/wiki/IPv6) im Wiesbadener Freifunk-Netz.
 Genauer gesagt betrifft es die Freifunk-Netze in Mainz, Wiesbaden und Umgebung gleichermaßen, da die technische Infrastruktur im Hintergrund
 gemeinsam betrieben wird. Dieser Schritt wurde nun über viele Monate hinweg bei den [Treffen](/treffen.html) und auf der 
 [Mailing-Liste](https://lists.freifunk.net/mailman/listinfo/wiesbaden-freifunk.net) ausreichend diskutiert, sodass der nächste
 Schritt angegangen werden kann.

An dieser Stelle wollen wir nochmal die Knackpunkte hervorheben, die innerhalb der Community den meisten Diskussionsbedarf hatten:

**Erstens** die nach Umstellung weltweite Sichtbarkeit von Kontaktdaten in den Freifunk-Knoten. Schließlich ist jeder Knoten dann ja weltweit
 erreichbar und bietet auf seiner IPv6-Adresse auch seine Status-Seite an. Hier gab es bei den Treffen wie auch auf der Mailing-Liste kritische
 Stimmen, die sagten, dass sie nicht gerne hätten, dass ihre Kontaktdaten dann in noch größerem Stil abrufbar seien. Hierfür brauchen wir also
 auf jeden Fall eine Lösung. Diese kann Opt-Out (wer will, löscht seine Daten) oder Opt-In (wir löschen alle Daten mit dem nächsten Update und
 wer will, trägt sie wieder ein) sein. Wir haben uns für Opt-Out entschieden, mehr dazu siehe unten.

**Das zweite Thema** war die Angreifbarkeit der einzelnen Endgeräte: Mit öffentlichem IPv6 sind auch die Endgeräte dann zukünftig weltweit erreichbar,
 also auch angreifbar. Hier haben wir hin und her überlegt und uns Gedanken über die Verantwortung gemacht, die wir auch für unsere Netz-Nutzer
 mit tragen.

**Klar ist:** Wir wollen gemäß [Pico-Peering-Agreement](http://www.picopeer.net/PPA-de.shtml) keine Eingriffe in den Datenverkehr, also auch keine
 Inhalte-Filterung sowie Firewalls im Freifunk. Wir wollen Netzneutralität und einen “Free Flow of Information”. D.h. wir müssen uns bewusst sein:
 Durch IPv6 steigt der Angriffsvektor auf die Endgeräte und wir werden keine Schutzmechanismen wie Firewalls im Freifunk-Netz etablieren, d.h. jede/r
 Nutzer/In muss zukünftig noch mehr dafür sorgen, dass sein Endgerät möglichst sicher ist. Allerdings: Das müssen die NutzerInnen heute schon!
 Die NutzerInnen dürfen sich auch heute nicht drauf verlassen, dass ein öffentliches WLAN sie vor irgendetwas schützt.

Auch heute schon werden alle WLANs in der Regel einfach so genutzt, ohne dass NutzerInnen wissen, ob ein NAT und/oder eine Firewall verwendet wird
 oder nicht. Die Endgeräte müssen damit also generell klar kommen und mit immer mehr offenen Netzen auch darauf ausgelegt und vorbereitet werden.

Und auf der anderen Seite ist es so, dass es für uns heute schon eine schwierige Situation ist, kein IPv6 anzubieten. Kein IPv6 anzubieten,
 bedeutet schließlich auch, Kommunikation netzseitig zu verhindern.

Insgesamt sind wir nach Abwägung aller Argumente zu dem Schluss gekommen, dass wir IPv6 via Freifunk Rheinland-Backbone auf den Gateways
 aktivieren wollen, d.h. das Admin-Team darum bitten werden, dies zu tun.

**Wir haben uns folgende Vorgehensweise überlegt:**

**1.** Damit niemandes Kontaktdaten gegen dessen Willen im Netz abrufbar sind, weisen wir Alle auf die Umstellung hin und erklären, wie die 
  Kontaktdaten gelöscht/geändert werden können, wenn sie das wollen:

  * [Per Konfigurationsmodus](https://wiki.freifunk-mwu.de/w/Howto/Gluon_Konfig_Aendern#Variante_1:_den_Router_nochmal_im_Konfig-Modus_starten)
  * [Per Kommandozeile](https://wiki.freifunk-mwu.de/w/Howto/Gluon_Konfig_Aendern#Kontaktdaten_.C3.A4ndern)

  Wir schreiben dazu einen Blogbeitrag (this) und senden eine Mail an alle, die eine Adresse hinterlegt haben. Wer keine Mail-Adresse
  hinterlegt hat, aber eine Telefonnummer, den rufen wir an (das sind hoffentlich nur ganz wenige).

**2.** Zum 15. September aktivieren wir dann öffentliches IPv6 im Wiesbadener Freifunk-Netz. Außerdem erklären wir in einem weiteren Blogbeitrag
  und ggfs. per Pressemitteilung, dass und wie man sich in öffentlichen WLANs schützen sollte.

Bis zur Umstellung haben wir jetzt also noch weniger als einen Monat Zeit um alle zu informieren. Wer will, kann seine Kontaktdaten bis dahin
 manuell rauslöschen.

Bei Fragen oder Anmerkungen meldet euch bitte auf unserer [Mailing-Liste](https://lists.freifunk.net/mailman/listinfo/wiesbaden-freifunk.net)

<script src="https://stat.ripe.net/widgets/widget_api.js"></script>
<div class="statwdgtauto"><script>ripestat.init("registry-browser",{"use_live_lookups":0,"include_backward_refs":0,"resource":"2a03:2260:11b::/48"},null,{"size":"small","show_controls":"no","disable":["feedback","maximize","info","footer-buttons","info"]})</script></div>
