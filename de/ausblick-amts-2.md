---
layout: nijida-topic
title: Ausblick auf AMTS 2
kicker: 2.0.0 Beta · Zusammenarbeit im Team
excerpt: AMTS 2 soll Teams koordinieren, Kerndaten schützen und Aufgaben sowie Feedback eindeutig einzelnen Mitgliedern zuordnen.
lang: de
nav_id: projects
local_nav_id: outlook
permalink: /de/ausblick-amts-2/
translations:
  de: /de/ausblick-amts-2/
  en: /en/amts-2-outlook/
  ja: /ja/amts-2-outlook/
---

AMTS 2.0.0 befindet sich in der frühen Beta-Konzeption. Die stabile
AMTS-1.x-Spezifikation bleibt davon unberührt, bis das neue Modell ausreichend
beschrieben und erprobt ist.

## Warum eingebaute Teamfähigkeit?

Wenn viele Menschen und Assistenzsysteme denselben Space laufend aktualisieren,
können sich Änderungen an zentralen Projekt- und Space-Daten überschneiden.
AMTS 2 soll deshalb zwischen geschützten, konsolidierten Kerndaten und
verteilten Beiträgen einzelner Mitglieder unterscheiden.

Space- und Projektverantwortliche pflegen die kanonischen Kerndaten. Mitglieder
schreiben Aufgabenstände, Ergebnisse und angeforderte Meinungen in ihren jeweils
zugeordneten Beitragsbereich. Verantwortliche können diese Beiträge lesen,
prüfen und anschließend bewusst in die Kerndaten übernehmen.

## Identität und Verantwortung

AMTS 2 soll Mitglieder lokal erkennen und sie im gemeinsamen Space über einen
stabilen öffentlichen Alias zuordnen. Dieser Alias kann ein ohnehin öffentlicher
GitHub-Benutzername oder ein frei gewählter Spitzname sein. Dabei werden
öffentliche und lokale Angaben streng getrennt:

- **Gemeinsam und synchronisiert:** öffentlicher Alias, Rollen sowie Space- und
  Projektzugehörigkeit.
- **Nur lokal:** offizieller oder privater Name, GitHub-Benutzername und andere
  Kontonamen, Benutzername des Rechners, lokale Repository-Pfade,
  gerätespezifische Identitäten und Verweise auf andere Spaces.

Eine lokale Alias-Tabelle ordnet alle bekannten lokalen Namen und Konten dem
öffentlichen Alias zu. Dadurch kann AMTS feststellen, ob eine Aufgabe für die
aktuelle Person bestimmt ist, ohne private Identitätsdaten zu synchronisieren.

Ein Space benennt seine Verantwortlichen. Jedes Projekt benennt ebenfalls
Verantwortliche und Mitglieder. Nur berechtigte Personen dürfen die geschützten
Kerndaten des jeweiligen Bereichs verändern.

## Vorgeschlagenes Beitragsmodell

Die genaue Dateistruktur ist Teil der Beta-Arbeit. Ein mögliches Modell ist:

```text
members/<member-id>/profile.md
governance.md
contributions/<member-id>/
projects/<Project>/governance.md
projects/<Project>/contributions/<member-id>/
```

Das öffentliche Verzeichnis eines Mitglieds enthält nur den öffentlichen Alias,
Rollen und zusammengefasste Beiträge. Aufgaben, Fortschritte, Ergebnisse und
Antworten auf Feedback-Anfragen werden dort so abgelegt, dass nicht mehrere
Personen dieselbe Arbeitsdatei überschreiben müssen.

`governance.md` ist ein derzeitiger Entwurf für die Beschreibung von
Verantwortlichen, Mitgliedschaften, geschützten Kerndaten und
Zusammenführungsregeln. Dateiname und genaues Format sind noch nicht normativ.

## Aufgaben und GitHub Issues

Eine Aufgabe gehört zu genau einem verantwortlichen Mitglied oder besitzt eine
ausdrücklich benannte federführende Person. Sie beschreibt ihren Scope und die
Kerndaten, in die ein Ergebnis später einfließen kann.

GitHub Issues sollen als erste externe Aufgabenquelle gelesen werden können.
Repository, Issue-Nummer und Assignee werden lokal über die Alias-Tabelle dem
öffentlichen AMTS-Alias zugeordnet. Das Issue bleibt die Quelle für seinen
laufenden Status; der Space bewahrt nur zusammengefasste AMTS-spezifische
Zuordnung, Ergebnisse und Zusammenführungsinformationen. Dadurch entsteht keine
zweite, schnell veraltende Kopie des vollständigen Issues.

## Meinungen und Feedback einholen

Ein Initiator kann gezielt Mitglieder oder Rollen um eine Einschätzung bitten.
Jede angefragte Person schreibt ihre Antwort im eigenen Beitragsbereich. Der
Initiator fasst die Ergebnisse zusammen und entscheidet, was in die eigene
Arbeit einfließt. Feedback ersetzt weder die Verantwortung des Initiators noch
die Freigabe geschützter Kerndaten.

Im gemeinsamen Aufgaben- und Feedbackbereich stehen nur Zusammenfassungen.
Vollständige Gespräche bleiben als private lokale Chats erhalten und werden nur
dann Teil des synchronisierten Space, wenn sie ausdrücklich geteilt werden.

Beim Einstieg in ein Projekt soll AMTS deshalb prüfen, ob für das lokal
erkannte Mitglied offene Aufgaben, erwartete Beiträge oder Feedback-Anfragen
vorliegen.

## Fragen bei der Initialisierung

Die Initialisierung oder Reinitialisierung soll schrittweise nach Folgendem
fragen:

1. gewünschte Anrede und öffentlicher Alias,
2. lokale Namen und Konten, einschließlich GitHub-Benutzername, die diesem
   Alias zugeordnet werden,
3. lokale Rechneridentität und Repository-Pfade je Gerät,
4. optionale lokale Querverweise auf weitere Spaces,
5. Verantwortliche und Mitglieder des Space,
6. Verantwortliche und Mitglieder bereits vorhandener oder neu eingerichteter
   Projekte.

Vor dem Schreiben identifiziert AMTS das aktuelle Mitglied, liest dessen
Aufgaben und Anfragen und prüft, ob die beabsichtigten Dateien zum eigenen
Beitragsbereich oder zu geschützten Kerndaten gehören.

## Regeln und technische Durchsetzung

AMTS kann Verantwortlichkeiten und Schreibregeln definieren, aber ein
Markdown-Space allein kann lokale Dateizugriffe nicht technisch verhindern.
Git-basierte Implementierungen können die Regeln zusätzlich mit geschützten
Branches, Review-Pflichten und `CODEOWNERS` absichern. Andere Speichersysteme
können eigene Zugriffsmechanismen verwenden.

Die 2.0.0-Beta muss noch klären, welche Dateien als Kerndaten geschützt werden,
wie Mitglieds-IDs Space-übergreifend stabil bleiben und wie konkurrierende oder
verwaiste Aufgaben übernommen werden.
