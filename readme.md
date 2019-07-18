# Projekt Inventarisierung

* Klasse EID11D der Staatlichen Berufsschule 1 Ingolstadt
* Dauer: 28.03.2019 - 25.07.2019

## Projektziel

Ziel des Projektes ist es, einen Prototyp einer Inventarverwaltung für die Berufsschule zu entwickeln. Diese Inventarverwaltung soll es ermöglichen Objekte unabhängig von deren Typ zu hinterlegen und Probleme mit diesem zu melden.

Hier wurde eine Unterteilung in drei Bereiche vorgenommen: Eine **Handy App** um Probleme zu melden, eine **Weboberflächte** um Probleme einzusehen, diese zu bearbeiten und neue Objekte zur Inventarierung hinzuzufügen sowie ein **Backend Server** um die Daten zu speichern und die Kommunikation zwischen allen Komponenten zu ermöglichen.

## Projektorganisation

Bei der Bildung der Teams wurde darauf geachtet, dass jedem Team eine Person mit bereits gutem Vorwissen sowie eine Person mit möglichst wenig bis keinem Vorwissen in dem jeweiligen Bereich zugeteilt wird. Dies hatte den Planungshintergrund, dass ein ständiger Informationsfluss zustande kommt und jeder etwas dazulernt.

Das Projekt selbst wurde nach dem **Agilen Prinzip des Scrums** organisiert. Dieses Prinzip zeichnet sich dadurch aus, dass nach kurzen Sprints(in der Realität mehrere Wochen bis maximal ein paar Monate, in unserem Projekt jeweils eine Doppelstunde) immer wieder Besprechungen abgehalten werden, in denen die Fortschritte des Projekts mit anderen besprochen werden, Feedback der Share- und Stakeholder eingeholt wird und die nächsten Schritte geplant werden. Durch diese **kurzen Intervalle und hohe Kundeneinbindung** ist eine möglichst hohe Agilität gewährleistet.

Die Resultate der jeweiligen Scrums sind auf dieser Webseite festgehalten: https://bs1in.github.io/scrum/

Jedem Team stand es frei, sich innerhalb des Teams frei zu organisieren.

Der Code der einzelnen Teams wurde mit dem **Versionsmanagement Tool Git** auf der Plattform GitHub festgehalten. Git ist ein Revisionsbasiertes Versionskontrollsystem in dem **lediglich die vorgenommenen Änderungen** auf einen zentralen Speicherpunkt(Repository) auf einem Server übertragen und dort zusammengeführt werden. So werden Konflikte bestmöglich vermieden. Durch die in Git integrierten Kolloborationsfeatures wird es ebenfalls ermöglicht, dass mehrere Personen in jedem Team zugleich am Code arbeiten, ohne die Fortschritte eines anderen Mitglieds dabei zu überschreiben.

Die Code Repositories sind unter folgenden Adressen erreichbar:

* App: https://github.com/bs1in/app
* Backend: https://github.com/bs1in/backend
* Web: https://github.com/bs1in/web

## Teams

Um einen reibungslosen Entwicklungsablauf zu gewährleiten wurden möglichst früh im Projekt alle API Datenformate/Adressen festgelegt. Dies hat zum Ziel, dass sich nicht nach jedem Entwicklugsschritt neu abgesprochen werden muss und jeder von Anfang jeder seine Klassen, etc. darauf basieren kann. Eine Übersicht über diese ist unter dieser URL zu finden: https://bs1in.github.io/scrum/daten

(Doku der Teams von jedem Team individuell)

## Gelernte Lektionen

Besonders bemerkenswert war ein Wechsel der Technologien des Backend Teams von PHP & NoSQL zu Java & SQL nach Verstreichen von ~75% der Zeit. Hintergrund des Wechsels war eine erhoffte verbesserte Produktivität im neuen Ecosystem, da da einige Teammitglieder mit Java Entwicklung bereits Erfahrung hatte, während PHP neu für alle war. Unabhäning davon ob dieser Technologiewechsel erforderlich war oder nicht, ist die hier gelernte Lektion dass vor Projektbeginn die Technologien nicht nur nach deren rein **sachlichen Stärken** und Einsatzgebieten sondern auch nach den **subjektiven Erfahrungen** von Präferenz der Entwickler ausgewählt werden muss. Wertungslos gesprochen: Auch die beste Programmiersprache ist von wenig nutzen wenn sie nicht korrekt eingesetzt werden kann.

Ebenfalls hat die **häufige Abwesenheit** einiger Mitglieder in einigen Teams zu Engpässen geführt. Diese wurden dadurch überbrückt, dass entweder die Projektleitung oder Mitglieder anderer Teams helfend eingesprungen sind. Hier ist für die Zukunft jedoch auch eine höhere Redudanz der Teammitglieder zu planen um zu vermeiden dass ein längerfristiger Ausfall eines Teammitgliedes dieses zum erliegen bringt.

Zuletzt haben die Datenformate häufiger zu Problemen geführt, was dazu gesorgt hat, dass die meisten Teams gegen Ende ihre **eigene Version der Datenstrukturen** hatten welche untereinander nicht kompatibel waren. Dies hat gegen Ende das Projektes etwas Zeit gekostet, diese soweit aufeinander abzustimmen dass eine reibungslose Kommunikation gewährleitet war. Hier wäre beispielsweise ein Workshop sinnvoll gewesen, in welchem man sich über das Format dieser Daten unterhält und eventuelle Unklarheiten abklärt.

## Fazit

Das Projekt wurde nicht vollständig fertiggestellt. Dies war in Angesicht der vorhandenen Zeit jedoch auch nicht das Ziel. Stattdessen sollte ein funktionsfäiger, gut dokumentierter Prototyp aufgestellt werden(**MVP - Minimum Viable Product**), welcher problemlos erweitert und potentiell fertiggestellt werden kann.

Auch haben die meisten Personen auf Rückfrage gemeldet, dass die Aufteilung der Gruppen nach Wissen dazu geführt hat, dass unabhängig vom vorherigen Wissenstand **etwas dazugelernt wurde**: Entweder dadurch, dass man selbst Fragen stellen konnte oder das eigene Wissen durch das Erklären an andere festigen konnte.
