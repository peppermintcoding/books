# Einleitung

## Warum noch ein Buch über Bildverarbeitung?

Es gibt bereits drei verschiedene Arten von Büchern über digitale Bildverarbeitung.

1. Werke mit Fokus auf die grunlegenden Verfahren und Algorithmen dabei sehr mathematisch und isoliert voneinander.
2. Konkrete Entwicklung und Implementation von Software.
3. Vorstellung von Anwendungen aus der Industrie, jedoch mit wenig Tiefgang.

Durch die Verbreitung von PCs ist die Nutzund von Bildverarbeitung leichter denn je und somit ist es wichtig das Wissen und Know-How weiterzugeben. Hierbei sollen vorallem funktionierende Lösungen aus der Praxis vorgestellt werden um zu zeigen wie Algorithmen gezielt eingesetzt und genutzt werden können. Jedoch ist die Bedienung und Aufbau von Bildverarbeitungssystemen kein einfaches Gebiet und wird es auch in Zukunft nicht sein.
Deswegen soll vorallem nicht erklärt werden wie die Algorithmen im Detail funktionieren, sondern wie sie sich zu einem Großen Ganzen zusammen setzten lassen um Probleme zu lösen.


## Möglichkeiten und Grenzen

Das Hauptproblem bei der Bilderkennung für Maschinen ist ihre triviale Natur für das menschliche Auge. Ein Detail, welches für uns als Menschen klar und deutlich zu sehen ist, ist nicht immer so leicht zu erkennen für eine Maschine. Deswegen muss man sich vorerst verdeutlichen wie eine Maschine überhaupt *sieht*.
Auch werden diese Systeme oft mit Menschen mit höchster Konzentration verglichen, welche über einen ganzen Arbeitstag stark schwankt und absinkt. Daher kann ein System mit 80% Trefferquote einen Menschen auf lange Sicht übertrumpfen. Hierbei sind einige Grundregeln zu beachten:

* die Aufgabe wurde präzise, detailliert und auf die Maschine abgestimmt beschrieben
* alle zulässigen Antwortmöglichkeiten wurden erfasst
* die Umgebungsbedingungen werden so geschaffen, dass die Fehler maschinell erfassbar sein können
* die Umgebungsbedingungen bleiben stabil


## Typen von Sichtprüfaufgaben

Man kann Aufgaben nach dem verfolgten Ziel oder nach der Struktur der Vorgehensweise unterteilen. Bei der Einteilung nach Prüfziel kann man folgende Klassen nennen:

* Lageerkennung
* Kennzeichnungsidentifikation
* Form- und Maßprüfung bzw. Vermessung
* Vollständigkeitsprüfung
* Farbverarbeitung
* Bild- und Objektvergleich
* Oberflächeninspektion
* 3D-Bildverarbeitung

## Aufbau von Bildverarbeitungssystemen

Jedes Bildverarbeitungssystem besteht grob aus drei Blöcken: *Sensoren*, *Rechnern* und *Mommunikationseinheiten*.

Als Sensoren können unter anderem Kameras, andere bildgebende Sensoren wie etwa Laserabtast- oder Ultraschallsensoren. Scanner ähnliche Sensoren sind aufgrund ihrer langsamen Geschwindigkeit meist unbrauchbar in der Praxis. Zur Übertragung der Daten werden meist Bluetooth, Ethernet, USB oder neuerdings auch vermehrt WLAN benutzt. 

Bei datenintensiven Auswertungen, wie etwa der Produktion von Stahl, Papier oder Textilien werden meist speizalisierte Parallelrechner verwendet. Durch die Verbreitung von multicore PCs können viele dieser Aufgaben aber auch vermehrt auf handelsüblichen PCs bewältigt werden. Auch die steigende Durchsatzrate des Datenflusses hatte eine positive Auswirkung auf den Einsatz von Bildverarbeitung im allgemeinen.

Das System muss im Gleichtakt mit dem Produktionsprozess arbeiten und sich von außen steuern lassen, es muss seine Ergebnisse nach außen melden und automatisch Ergebnisse verarbeiten können. Mittelfristig wird diese Steuerung wohl auch über das Internet funktionieren und somit die Steuerung von überall ermöglichen. Jedoch sind hier die Sicherheitsrisiken zu bedenken und abzuwägen.

Der Signalfluss eines Bildverarbeitungssystems ist denkbar einfach: das System nimmt ein Bild auf, analysiert es und übersetzt es in eine Aussage. Dabei ist die Aussage sehr individuell. Es kann Aussage über Qualität mittels eines Zahlenwertes, einer Gut/Schlecht-Aussage oder ein physisches Signal getroffen werden. Das aufgenommene Bild wird meist als eine Matrix aus Zahlen oder mehrerer Matrizen dargestellt. Hierbei unterscheidet man zwei Faktoren: *Rasterung* und *Quantisierung*.
Die Rasterung beschreibt die Anzahl der Pixel, die ein Bild am Ende besitzt. Der eintretende Informationsverlust richtet sich nach dem *Shannonschen Abtasttheorem*. Der Abstand zwischen zwei Bildpunkten darf höchstens halb so groß sein wie das kleinste relevante Detail des realen Objekts.
Als Quantisierung wird die Spanne an möglichen Helligkeitswerten bezeichnet. Diese ist aufgrund von Speicher und Verarbeitungszeit meist sehr viel kleiner als durch die Sensoren möglich wäre. Hierbei werden oft 8 Bit pro Farbkanal oder Helligkeitsstufe genutzt, da sie dem internen Speichersystem eines jeden modernen Computers folgen. Es ist anzumerken, dass das menschliche Auge nur etwa 30 verschiedene Graustufen unterscheiden kann, ein Byte an Speicher aber 256 zulässt. Es kommt somit eher auf die Art der Ausleuchtung und auf den Kontrast im Bild an.

Der Signalfluss innerhalb des Verarbeitungssystems wird dann in drei Ebenen unterteilt:
* die *ikonische* Ebene beschreibt das ankommende gerasterte und quantisierte Bild
* im Inneren wird dieses Bild dann in der *Objekt-Ebene* in eine Art von Datenstruktur umgewandelt, welche etwa eine Beschreibung der Größe oder Form des Objekts besitzt. Dies wird als *Segmentierung* bezeichnet.
* in der *symbolischen* Ebene werden dann eines oder mehrerer dieser Objekte zu einer Aussage zusammengeführt. Hierbei wird aus vielen Daten durch eine Reduktion Wissen gewonnen.




