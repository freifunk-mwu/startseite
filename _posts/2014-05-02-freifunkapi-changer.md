---
layout: post
title: "FreifunkAPI changer"
author: spky
---

Die [FreifunkAPI](https://github.com/freifunk/api.freifunk.net) &#8211; eine grandiose Idee nach dem Vorbild der (Hacker-) [SpaceAPI](http://spaceapi.net/), jede community sollte sich ein [api-File generieren](http://freifunk.net/api-generator/) und die Adresse [hinterlegen](https://github.com/freifunk/directory.api.freifunk.net).

Dennoch, so finde ich, ist dies nur ein Teil von dem was die FreifunkAPI erfüllen kann.

Am Beispiel mancher Apps, die Daten aus der SpaceAPI beziehen, kann man sehen, dass die SpaceAPI mehr davon lebt, dass die Inhalte der api-Files automatisch mit neuen Daten der Hackerspaces befüllt werden:

Hier zum Beispiel [die Auswertungen der offen/geschlossen Zeiten](http://spacestatus.bastinat0r.de/) eines zufälligen Hackerspaces aus der Region:

[![spacestatus_commonground](/images/blog/spacestatus_commonground-1024x1006.png)](/images/blog/spacestatus_commonground.png)

Das ist sehr schick. Dennoch: Solange alle Jubeljahre manuell die API-Files jeder Community wieder auf den neuesten Stand gebracht werden, sind solche Anwendungen undenkbar.

Deshalb habe ich mich die Tage mal hingesetzt und ein Modul geschrieben, dass Freifunk-API-Files einlesen und (bestehende) Werte ändern kann:

[changeffapi.git auf github](https://github.com/Freifunk-Mainz/changeffapi)

Zum installieren:

Klonen (nach ~/software/changeffapi),

	git clone https://github.com/Freifunk-Mainz/changeffapi ~/software/changeffapi
	cd ~/software/changeffapi/

sein eigentliches API-File nach **ffapi_file.json** symlinken:

	ln -s /var/www/path/to/ffapi/file.json ~/software/changeffapi/ffapi_file.json

Die Integration ist relativ simpel, hier ein Beispiel wie man die Anzahl der Nodes setzt:

![changeffapi-sample](/images/blog/changeffapi-sample.png)

Bei uns (und in Mainz) wird die Anzahl der Nodes anhand der [Kartendaten](map.freifunk-mainz.de/nodes.json) aus der [Karte](http://map.freifunk-mainz.de/) (auf Basis von [ffmap-d3](https://github.com/ffnord/ffmap-d3)) ermittelt, und dann ins API-File geschrieben: **[mapnodes.py](https://github.com/Freifunk-Mainz/changeffapi/blob/master/mapnodes.py)**

Als Bonus wird das ganze noch gettwittert, als submodul kommt dazu [notify.git](https://github.com/spookey/notify) zum Einsatz.

[![freifunkwi_statustweet](/images/blog/freifunkwi_statustweet-300x123.png)](/images/blog/freifunkwi_statustweet.png)

[freifunkwi](https://twitter.com/freifunkwi/status/462205630997360641), [freifunkmainz](https://twitter.com/freifunkmainz/status/462203912297390080)

Nicht über die exorbitant hohen Zahlen seitens Wiesbaden wundern, die Netze von Mainz und Wiesbaden sind ein und das selbe, beziehen also auch ihre Daten aus der selben Quelle.

**Update**

Ein kleiner Bug hat das Script daran gehindert das API-File zu finden, wenn es durch die Crontab gestartet wurde. [Gefixt](https://github.com/Freifunk-Mainz/changeffapi/commit/80a7d304a1209101a1ab5385dc997220a2862388), funktioniert jetzt.

Einmal [täglich](https://twitter.com/freifunkwi/status/468049136693293056) [die Anzahl](https://twitter.com/freifunkwi/status/468441725082820608) [der Teilnehmer](https://twitter.com/freifunkwi/status/468804111325216768) [twittern](https://twitter.com/freifunkwi/status/469166495147499520) [kann man verkraften](https://twitter.com/freifunkwi/status/469528881935183872), oder? Was denkt Ihr dazu?
