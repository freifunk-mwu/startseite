---
layout: post
title: "Ping – Wir leben noch.."
author: spky
---

Ein Blick [in unser Freifunk-API File](http://ffapi.freifunk-wiesbaden.de/ffapi_wi.json) verrät: Wir haben bereits am 13. November unseren ersten Geburtstag verpasst.

Ob das so wichtig ist, und ob man den Termin am ersten Treffen fest machen kann weiß ich nicht, wichtiger finde ich es an dieser Stelle einen kleinen Rückblick zu wagen:

Manch einer mag sich fragen, ob noch was zum Freifunk in Wiesbaden ist, das Blog wird spärlich gefüttert, der [Twitter-Account](http://twitter.com/freifunkwi) verkommt zur Status-Schleuder, und die [Mailing-Liste](http://lists.freifunk.net/mailman/listinfo/wiesbaden-freifunk.net) macht leider auch wenig her..

Doch in der Tat, wir leben, und erfreuen uns bester Laune:

Das letzte Jahr haben wir damit verbracht eine Gateway-Infrastruktur für Gluon auf die Beine zu stellen.

Nachdem das Admin-Team des [Freifunk Mainz](http://www.freifunk-mainz.de) den ersten Gluon Testserver mit dem &#8220;schönen&#8221; Namen &#8220;[Mettigel](http://de.wikipedia.org/wiki/Mettigel)&#8221; am laufen hatten (und das bis letzten Monat ohne größere Probleme, Hut ab!) verlangten Echtweltdinge mehr Aufmerksamkeit, und es wurde erstmal etwas ruhiger. In diese Zeit etwa fällt die Gründung des Freifunk Wiesbaden.

Irgendwie kam der Stein dann doch wieder ins Rollen, und es fanden sich Leute sowie Hardware zum experimentieren: &#8220;[Spinat](http://spinat.freifunk-mwu.de)&#8220;, &#8220;[Lotuswurzel](http://lotuswurzel.freifunk-mwu.de)&#8221; und &#8220;[Hinterschinken](http://hinterschinken.freifunk-mwu.de)&#8220;.

Nach den ersten Überlegungen kamen wir sehr schnell auf den Trichter:  
Mesh-Netzwerke sind von der Teilnehmeranzahl nach oben hin immer begrenzt. Lasst uns die Infrastruktur so bauen, dass wir pro Gateway mehrere Mesh-Netzwerke parallel bedienen können!

Und das haben wir jetzt &#8211; die drei Gateways versorgen momentan jeweils zwei Communities: Freifunk Mainz und uns.

Wie man das hinbekommt ist keine Rocket-Science, und haben wir sogar [aufgeschrieben](http://gluon-gateway-doku.readthedocs.org), allerdings sind wir wohl die Ersten die so etwas produktiv auch tun, und somit in diverse Probleme laufen.  

Dass Alfred nun auch wirklich parallel nebeneinander laufen kann &#8211; [daran sind wir schuld](http://www.open-mesh.org/projects/alfred/repository/revisions/6c6a6f735054a839bd809d5711c29287505ccdd5) :) An dieser Stelle nochmals vielen Dank an alle Beteiligten.

Momentan läuft die [Public-Beta-Phase](http://blog.freifunk-wiesbaden.de/2014/12/gluon-in-wiesbaden-geht-in-die-public-beta-phase/), bei der wir unter realen Bedingungen die Infrastruktur testen.

Die Tage habe ich alle git-Repositories der [Freifunk-MWU GitHub-Gruppe](https://github.com/freifunk-mwu) zusammengeschmissen, gut umgerührt, und dabei [sprang diese Visualisierung raus](https://vimeo.com/116180046):

<center><iframe src="//player.vimeo.com/video/116180046?byline=0&amp;portrait=0&amp;color=c9ff23" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen>
Dein Browser kann keine iframes.. Schade..
</iframe></center>

Diese deckt den Bereich von Beginn an (November 2013), bis zum 31. Dezember 2014 ab. <small>Dies ist nicht ganz korrekt, Freifunk Aktivitäten in der Region gab es schon länger, wir waren aber nicht immer auf GitHub und haben uns bei dem Wechsel dorthin einen großen Schwung alter Repos entledigt..</small>

Im letzten Jahr hat sich viel hinter den Kulissen getan, wir haben ein solides Freifunk-Netz vor der Tür stehen. Der Beta-Betrieb verläuft ohne größere Zwischenfälle, wobei ein paar Stellen noch Detailarbeit benötigen.. (Dies ist meine Einschätzung, kann nicht für alle im Admin-Team sprechen)

Schaut man auf die [Karte](http://map.freifunk-mwu.de), und zählt dort die Nodes/Clients zusammen wird eines ersichtlich:

Wir haben super wenig Nodes..

[![count_nodes_on_map](/images/blog/count_nodes_on_map.png)](/images/blog/count_nodes_on_map.png)

Es lässt sich leider schlecht mit den alten Zahlen des Twitter-Bots vergleichen, da wir das Mainzer Mesh-Netzwerk einfach mitbenutzt haben. Es geht hier nicht um den reinen Vergleich der Zahlen, man stellt aber grob fest:

Wir haben noch großen Nachholbedarf in der Community.

Was wir also brauchen:  
Menschen die das Konzept von Freifunk leben und erlebbar machen möchten, die die Idee mittragen und in und um Wiesbaden eine Community aufbauen möchten.

Genauso wie Menschen, die Freifunk auf der technischen, sozialen oder sonst einer Ebene fasziniert. Bevorzugt jene die Ihren Ideen auch Taten folgen lassen :-)

Wir müssen das hier Blog mit sinnvollen Inhalten füllen, per Twitter weitere, oben genannte Menschen zu erreichen, und die Mailingliste zu beleben.

Weiterhin sind wir dran, unsere Webseite umzubauen, um alles zu vereinheitlichen. Wir brauchen Leute, die z.B. darauf achten, dass die Anleitungen immer wieder aktuell gehalten werden. Leute die Probleme im Netz erkennen und diese mithilfe der Admins lösen (und bald selbst Admin werden :-). Menschen die Software für Freifunk schreiben oder (Netz-Interne-)Dienste betreiben möchten&#8230;

Auf der Echtweltseite ist unsere größte Werbefläche die SSID des WLANs &#8211; &#8216;wiesbaden.freifunk.net&#8217;  
Steckt alles drin, was man braucht &#8211; gibt man das im Browser ein landet man auf unserer Webseite, und sauberes, freies Netz gibts in dem WLAN auch! (Wobei wir darauf achten sollten, dass wir nicht zu einem Hotspot verkommen &#8211; Wir brauchen mehr interne Dienste!!1!)  
Somit brauchen wir auch schlicht Node-Betreiber.  
Auch sind Kontakte zu technisch interessanten oder strategisch günstigen Standorten (hohe Punkte, frequentierte Orte) die sich vom Konzept begeistern lassen von Vorteil.  
Flyer oder Plakate zu Freifunk wären schick, wer Grafik oder Texte kann, ist gerne gesehen.  
Genauso wie Menschen, die auf den Support-Treffen vor Ort sind, um anderen Freifunkern bei Problemen mit der Node zu helfen.

Und alles irgendwie dazwischen.

Da Neujahrsvorsätze eh nicht lang halten, und es dafür schon ein bisschen spät ist, machen wir das jetzt einfach so:  
Wir erwecken die Community Freifunk Wiesbaden zum Leben!

Wir treffen uns das nächste mal am Donnerstag, den 29. Januar 2015 in den Räumen des [Chaos Computer Club Mainz](http://www.cccmz.de) (wie [immer am letzten **Donnerstag** im Monat](http://blog.freifunk-wiesbaden.de/termine/?mc_id=20203)).

Sei live und in Farbe mit dabei, wie eine Community aufgebaut wird, jede helfende Hand und jeder kreativer Kopf wird gebraucht!
