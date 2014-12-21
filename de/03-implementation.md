---
title: Implementierung
heading: Praktische Implementierung
categories: de
---
Nach dem Start von Cjdns auf einem Knoten (Heim PC, Smartphone, Router, Server)
wird von diesem eine eindeutige Adresse generiert, mit der er im Netzwerk
erreichbar ist. Dies geschieht durch die Generierung des Hashes seines Public
Keys. Die entstehende Adresse ist eine normale IPv6 Adresse an die sich jeder
auf dem Knoten laufende Service binden kann. Nun verbindet er sich der Knoten zu
allen ihm bekannten Knoten. Diese Verbindung können über jedes erdenkliche
Medium wie z.B. Kupfer- oder Glasfaserkabel, Wifi, Laser, Satelliten oder das
bestehende Internet hergestellt werden.

Nachdem mindestens eine Verbindung hergestellt wurde erstellt Cjdns seine
Routingtabelle. In dieser werden nur nahe Nachbarn gespeichert. Entferntere
Knoten werden mit Hilfe einer Verteilten Hashtabelle gefunden. Durch diese
Herangehensweise werden teure high-end Router mit gigantisch großen
Routingtabellen überflüssig. Weitere Information und Vorteile des Routings kann
man auch [hier](https://github.com/cjdelisle/cjdns/blob/master/doc/Whitepaper.md#what-is-the-routing-table-and-why-does-it-keep-getting-bigger)
finden.

Zu diesem Zeitpunkt ist es möglich jeden anderen Knoten im Netzwerk zu
erreichen. Das einzige was hierzu benötigt wird ist IPv6 Adresse des Ziels. Die
Verbindung kann über jedes gewünschte Programm oder Protokoll hergestellt werden
ohne das eine weitere Konfiguration notwendig ist. Cjdns nimmt keinen Einfluss
im OSI Model oberhalb von Layer drei.