---
layout: post
title: "Meshviewer - neue Freifunk-Karte"
author: kokel
---

{: .text-center}
[![Meshviewer](/images/blog/meshviewer.png 'Meshviewer')](/images/blog/meshviewer.png)

Für die Visualisierung des Freifunk-Netzes gibt es nun die neue Freifunk Karten-Software "Meshviewer", die ab heute die alte Freifunk-Karte ablösen wird. Ein Screenshot der Meshviewer-Startseite ist auf dem obigen Screenshot zu sehen.

 * [Externe Karte](http://map.wiesbaden.freifunk.net)
 * [Interne Karte](http://map.ffwi.org) (nur aus dem Freifunk-Netz erreichbar)

Die meisten Funktionen sind selbsterklärend, dennoch möchten wir Euch die wichtigsten Funktionen an dieser Stelle erläutern.

Der Meshviewer zeigt alle Freifunk-Knoten entweder in einer Karten- oder Graphen-Ansicht an. In der Geo-Karte (Standard-Ansicht) können nur Knoten mit hinterlegten Geo-Koordinaten angezeigt werden. Auf der linken Seite ist eine Infobox zu sehen, die Detail Informationen über das Netzwerk, die Knoten, Verbindungen und Statistiken anzeigt. Diese lässt sich jederzeit mit einem Klick auf das [![Meshviewer - Infobox ausblenden](/images/blog/meshviewer_icon_out.png 'Meshviewer - Infobox ausblenden'){:height="30px" width="30px"}](/images/blog/meshviewer_icon_out.png) und [![Meshviewer - Infobox einblenden](/images/blog/meshviewer_icon_in.png 'Meshviewer - Infobox einblenden'){:height="30px" width="30px"}](/images/blog/meshviewer_icon_in.png) Icon aus- und wieder einblenden.

Eine Klick auf die Knoten-, Verbindungs-Links, etc. blendet zusätzliche Informationen ein.

Knoten, die länger als 45 Tage offline sind werden automatisch entfernt.

<br />

<dl class="tabs four-up">
  <dd class="active"><a href="#simple1">Übersicht</a></dd>
  <dd><a href="#simple2">Knoten</a></dd>
  <dd><a href="#simple3">Verbindungen</a></dd>
  <dd><a href="#simple4">Statistiken</a></dd>
</dl>
<dl class="tabs three-up">
  <dd><a href="#simple5">Knoten Details</a></dd>
  <dd><a href="#simple6">Graph</a></dd>
  <dd><a href="#simple7">Map</a></dd>
</dl>
<ul class="tabs-content">
  <li class="active" id="simple1Tab">
    <p><a href="/images/blog/meshviewer_overview.png"><img src="/images/blog/meshviewer_overview.png" alt="Meshviewer - Übersicht" title="Meshviewer - Übersicht" class="right" width="500px" /></a></p>
    <p>Die erste Zeile gibt kurz und knackig Auskunft über die aktuellen Zahlen.</p>
    <p><strong>Neue Knoten</strong>:</p>
    <p>Knoten, die innerhalb der letzten 14 Tage neu hinzugekommen sind. Die Zeit-Angabe rechts neben den Knoten-Namen zeigt nicht die Uptime, sondern wann die Knoten Teil des Freifunk-Netzes geworden sind.</p>
    <p><strong>Verschwundene Knoten</strong>:</p>
    <p>Knoten, die keine Verbindung mehr zum Freifunk-Netz haben (offline). Sind Knoten länger als 14 Tage offline, werden diese auch hier nicht mehr angezeigt.</p>
  </li>
  <li id="simple2Tab">
    <p><a href="/images/blog/meshviewer_nodes.png"><img src="/images/blog/meshviewer_nodes.png" alt="Meshviewer - Knoten" title="Meshviewer - Knoten" class="right" width="500px" /></a></p>
    <p>Hier sind alle Knoten in alphabetischer Reihenfolge aufgelistet.</p>
    <p>Die Liste lässt sich durch einen Klick auf die Überschriften auch nach <strong>Uptime</strong> und nach <strong>Clients</strong> sortieren.</p>
  </li>
  <li id="simple3Tab">
    <p><a href="/images/blog/meshviewer_connections.png"><img src="/images/blog/meshviewer_connections.png" alt="Meshviewer - Verbindungen" title="Meshviewer - Verbindungen" class="right" width="500px" /></a></p>
    <p>Diese Liste zeigt alle Mesh-Verbindungen im Freifunk-Netz an, die zunächst nach Entfernungen sortiert sind (absteigend).</p>
    <p>Jede Zeile zeigt eine Verbindung zwischen 2 Knoten mit der aktuellen Verbindungsqualität (TQ in %) und bei Mesh-Verbindungen die Entfernung in Metern an.</p>
    <p>Die VPN-Verbindungen der Knoten zu unseren Gateways werden mit (VPN) gekennzeichnet.</p>
    <p>
      <a href="/images/blog/meshviewer_link_details.png"><img src="/images/blog/meshviewer_link_details.png" alt="Meshviewer - Link-Details" title="Meshviewer - Link-Details" class="left" width="400px" /></a>
    </p>
    <p>Ein Klick auf eine Verbindung zoomt die Verbindung auf der Karte heran, stellt diese gestrichelt dar und blendet eine zusätzliche Infobox mit weiteren Informationen ein.</p>
  </li>
  <li id="simple4Tab">
    <p><a href="/images/blog/meshviewer_statistics.png"><img src="/images/blog/meshviewer_statistics.png" alt="Meshviewer - Statistiken" title="Meshviewer - Statistiken" class="right" width="500px" /></a></p>
    <p>Hier werden Statistiken über Firmwareversionen, Hardwaremodelle, Autoupdater und dem gewählten Gateway (B.A.T.M.A.N. Advanced - Mesh Protokoll) angezeigt.</p>
  </li>
  <li id="simple5Tab">
    <p><a href="/images/blog/meshviewer_node_details.png"><img src="/images/blog/meshviewer_node_details.png" alt="Meshviewer - Knoten Details" title="Meshviewer - Knoten Details" class="right" width="500px" /></a></p>
    <p>Klickt man auf einen Knoten (Namen in der Infobox oder Knoten-Symbol auf der Karte/im Graphen) werden weitere Informationen über diesen Knoten angezeigt.</p>
    <p><strong>Tipp</strong>: Mit einem Klick auf die als Link angezeigte IP-Adresse(n) wird die Status-Page der Freifunk-Knoten geöffnet (nur innerhalb des Freifunk-Netzes möglich).</p>
  </li>
  <li id="simple6Tab">
    <p><a href="/images/blog/meshviewer_graph.png"><img src="/images/blog/meshviewer_graph.png" alt="Meshviewer - Knoten Graph" title="Meshviewer - Knoten Graph" class="right" width="500px" /></a></p>
    <p><img src="/images/blog/meshviewer_icon_graph.png" alt="Meshviewer - Graph Icon" title="Meshviewer - Graph Icon" heigth="30px" width="30px" /> Zur Graphen-Ansicht wechseln</p>
    <p><img src="/images/blog/meshviewer_icon_map.png" alt="Meshviewer - Map Icon" title="Meshviewer - Map Icon" heigth="36px" width="36px" /> Zur Karten-Ansicht wechseln.</p>
    <p>Graue, dünne Linien stellen die VPN-Verbindungen zu unseren Gateways dar. Mesh-Verbindungen werden durch eine dickere Linie dargestellt. Je nach Verbindungsqualität wird diese mit einer anderen Farbe, von Rot = schlecht über Orange und Gelb zu Grün = sehr gut, angezeigt.</p>
    <p>Die Namen der Knoten werden erst bei näherem Zoom eingeblendet.</p>
  </li>
  <li id="simple7Tab">
    <p><a href="/images/blog/meshviewer_map.png"><img src="/images/blog/meshviewer_map.png" alt="Meshviewer - Map" title="Meshviewer - Map" class="right" width="500px" /></a></p>
    <p>Die Karte zeigt alle Freifunk-Knoten mit hinterlegten Geo-Koordinaten an. Mit Doppelklick und Shift+Doppelklick kann man in der Karte auch zoomen.</p>
    <p><img src="/images/blog/meshviewer_icon_locate.png" alt="Meshviewer - Locate Icon" title="Meshviewer - Locate Icon" heigth="30px" width="30px" /> <strong>ermittelt deinen aktuellen GPS-Standort</strong></p>
    <p><img src="/images/blog/meshviewer_icon_addprovider.png" alt="Meshviewer - Provider Icon" title="Meshviewer - Provider Icon" heigth="30px" width="30px" /> <strong>anderen Karten-Provider hinzufügen</strong></p>
    <p>Per Klick auf letzteres Symbol lassen sich sogenannte <a target="_blank" href="http://leaflet-extras.github.io/leaflet-providers/preview/">Leaflet-Provider</a> hinzufügen (Den Namen der am rechten Bildschirmrand angezeigten Karten in das Pop-Up Fenster kopieren).</p>
    <p>Mit dem <img src="/images/blog/meshviewer_icon_layer.png" alt="Meshviewer - Layer Icon" title="Meshviewer - Layer Icon" heigth="30px" width="30px" /> Icon können die hinzugefügten Karten-Provider ausgewählt und somit das Kartenmaterial ganz einfach ausgetauscht werden.</p>
    <p>Dein Browser merkt sich alle hinzugefügten Karten für deinen nächsten Besuch.</p>
  </li>
</ul>

<br clear="all" />

#### Legende ####

{: .left }
[![Meshviewer - Infobox ausblenden](/images/blog/meshviewer_icon_out.png 'Meshviewer - Infobox ausblenden'){:height="30px" width="30px"}](/images/blog/meshviewer_icon_out.png)
[![Meshviewer - Infobox einblenden](/images/blog/meshviewer_icon_in.png 'Meshviewer - Infobox einblenden'){:height="30px" width="30px"}](/images/blog/meshviewer_icon_in.png)
Infobox ein- und ausblenden
<br />
[![Meshviewer - Graph Iconn](/images/blog/meshviewer_icon_graph.png 'Meshviewer - Graph Icon'){:height="30px" width="30px"}](/images/blog/meshviewer_icon_graph.png)
[![Meshviewer - Map Icon](/images/blog/meshviewer_icon_map.png 'Meshviewer - Map Icon'){:height="30px" width="30px"}](/images/blog/meshviewer_icon_map.png)
Zwischen Graphen/Karte wechseln
<br />
[![Meshviewer - Locate Icon](/images/blog/meshviewer_icon_locate.png 'Meshviewer - Locate Icon'){:height="30px" width="30px"}](/images/blog/meshviewer_icon_locate.png)
ermittelt deinen aktuellen GPS-Standort
<br />
[![Meshviewer - Provider Icon](/images/blog/meshviewer_icon_addprovider.png 'Meshviewer - Provider Icon'){:height="30px" width="30px"}](/images/blog/meshviewer_icon_addprovider.png)
anderen Karten-Provider hinzufügen
<br />
[![Meshviewer - Layer Icon](/images/blog/meshviewer_icon_layer.png 'Meshviewer - Layer Icon'){:height="30px" width="30px"}](/images/blog/meshviewer_icon_layer.png)
Karten-Provider auswählen

{: .right }
<p>
  <svg height="22px" width="300px">
    <circle cx="7" cy="7" r="6" stroke-linejoin="round" stroke-linecap="round" stroke="#1566A9" stroke-opacity="0.5" stroke-width="2" fill="#93E929" fill-opacity="1" />
    <text x="20" y="12">Neuer Knoten (jünger als 14 Tage)</text>
  </svg>
  <br />
  <svg height="22px" width="300px">
    <circle cx="7" cy="7" r="6" stroke-linejoin="round" stroke-linecap="round" stroke="#1566A9" stroke-opacity="0.5" stroke-width="2" fill="#1566A9" fill-opacity="0.5" />
    <text x="20" y="12">Online Knoten (älter als 14 Tage)</text>
  </svg>
  <br />
  <svg height="23px" width="300px">
    <circle class="node-alert" cx="7" cy="7" r="6" stroke-linejoin="round" stroke-linecap="round" stroke="#D43E2A" stroke-opacity="0.8" stroke-width="2" fill="#D43E2A" fill-opacity="0.8" />
    <text x="20" y="12">Knoten Offline (nicht länger als 3 Tage)</text>
  </svg>
  <br />
  <svg height="22px" width="300px">
    <circle cx="7" cy="7" r="6" stroke-linejoin="round" stroke-linecap="round" fill-rule="evenodd" stroke="#D43E2A" stroke-opacity="0.8" stroke-width="1" fill="#D43E2A" fill-opacity="0.8" />
    <text x="20" y="12">Knoten Offline (länger als 3 Tage)</text>
  </svg>
  <br />
  <svg height="15px" width="300px">
    <circle cx="5" cy="5" r="3" stroke-linejoin="round" stroke-linecap="round" fill-rule="evenodd" stroke="#D43E2A" stroke-opacity="0.5" stroke-width="2" fill="#D43E2A" fill-opacity="0.5" />
    <text x="15" y="11">Knoten Offline (länger als 14 Tage)</text>
  </svg>
</p>

<br clear="all" />

Wir bedanken uns außerordentlich bei dem Entwickler des Meshviewers für dieses wunderbare Stück Software, dessen [Source Code](https://github.com/tcatm/meshviewer) öffentlich zugänglich ist (Open Source).
