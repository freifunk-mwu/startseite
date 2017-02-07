---
permalink: /ffwi-calendar.ics
---
{::nomarkdown}
BEGIN:VCALENDAR
VERSION:2.0
PRODID:-//Freifunk Wiesbaden//EN
CALSCALE:GREGORIAN
METHOD:PUBLISH
X-WR-CALNAME:FFWI
X-WR-TIMEZONE:Europe/Berlin
X-WR-CALDESC:Termine Freifunk Wiesbaden
BEGIN:VTIMEZONE
TZID:Europe/Berlin
X-LIC-LOCATION:Europe/Berlin
BEGIN:DAYLIGHT
TZOFFSETFROM:+0100
TZOFFSETTO:+0200
TZNAME:CEST
DTSTART:19700329T020000
RRULE:FREQ=YEARLY;BYMONTH=3;BYDAY=-1SU
END:DAYLIGHT
BEGIN:STANDARD
TZOFFSETFROM:+0200
TZOFFSETTO:+0100
TZNAME:CET
DTSTART:19701025T030000
RRULE:FREQ=YEARLY;BYMONTH=10;BYDAY=-1SU
END:STANDARD
END:VTIMEZONE
BEGIN:VEVENT
ORGANIZER;CN=Freifunk Wiesbaden:MAILTO:info@freifunk-wiesbaden.de
DTSTART;TZID=Europe/Berlin:{{ site.data.upcomingEvents.first.start | date: "%Y%m%dT%k%M00" }}
DTEND;TZID=Europe/Berlin:{{ site.data.upcomingEvents.first.end | date: "%Y%m%dT%k%M00" }}
RRULE:FREQ=MONTHLY;BYSETPOS=-1;BYDAY=TH;INTERVAL=1
DTSTAMP:20150306T111045Z
UID:20150301T111015Z@freifunk-wiesbaden.de
CREATED:20150306T111015Z
CONTACT:info@freifunk-wiesbaden.de\; http://wiesbaden.freifunk.net
DESCRIPTION:Regelmaessiges Treffen der Wiesbadener Freifunk-Community
 in den Raeumlichkeiten des CCC ab 19:00 Uhr.\nCCCMZ e.V.\nSedanplatz 7\,
 65183 Wiesbaden
LAST-MODIFIED:{{ site.time | date: "%Y%m%dT%k%M00Z" }}
GEO:+50.08317;+8.22951
LOCATION:CCCMZ e.V. @ Sedanplatz 7\, 65183 Wiesbaden\, Deutschland
SEQUENCE:0
STATUS:CONFIRMED
SUMMARY:ffwi: Freifunk Treffen
URL:{{ site.url }}/treffen.html
TRANSP:OPAQUE
END:VEVENT
END:VCALENDAR
{:/}
