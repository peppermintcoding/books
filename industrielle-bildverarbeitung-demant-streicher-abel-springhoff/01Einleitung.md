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