# Claudes Chat-Suche und Speicher

> Referenzdokument, abgelegt zur internen Nutzung. Quelle: Anthropic Support-Artikel
> „Nutzen Sie Claudes Chat-Suche und Speicher, um auf vorherigen Kontext aufzubauen".

Dieses Dokument fasst zusammen, wie Claudes Chat-Suche und Speicherfunktion funktionieren:
was Claude sich merkt bzw. nicht merkt, wie man den Speicher einsieht und bearbeitet, und
wie sich die Funktionen aktivieren oder deaktivieren lassen.

**Hinweis zur Migration:** Nach Einführung des verbesserten Speichererlebnisses können
Nutzer bis zum 9. September 2026 unter **Einstellungen > Speicher** ihren älteren Speicher
exportieren, falls bei der Migration etwas vergessen wurde.

## Frühere Chats durchsuchen

Verfügbar für bezahlte Pläne (Pro, Max, Team, Enterprise) im Web, in der Desktop- und in
den Mobile-Apps.

Claude kann auf Zuruf vorherige Gespräche durchsuchen (Retrieval-Augmented Generation),
um relevante Informationen über Sitzungen hinweg zu finden, z. B.:

- „Was haben wir über [Thema] besprochen?"
- „Kannst du unser Gespräch über [Thema] finden?"
- „Lass uns dort weitermachen, wo wir mit [Projekt] aufgehört haben."

**Suchbereich:** alle Chats außerhalb von Projekten, sowie einzelne Projektgespräche
(auf das jeweilige Projekt beschränkt).

**Deaktivieren:** Einstellungen > Speicher > Schalter „Chats durchsuchen und
referenzieren" ausschalten.

**Einzelne Chats ausschließen:** über Incognito-Chats (Geistersymbol oben rechts bei
neuem Chat außerhalb eines Projekts) — werden nicht im Verlauf gespeichert und nicht
durchsucht.

## Claudes Speicher

Speicher macht aus Claude einen Assistenten, der über die Zeit Verständnis aufbaut,
statt bei jedem Chat bei null anzufangen.

- Standardmäßig aktiviert für Free-, Pro- und Max-Pläne (Web, Desktop, Mobile).
- Bei Team-/Enterprise-Plänen standardmäßig deaktiviert, aktivierbar durch einen Owner.
- Speicher wird zwischen Chat und Claude Cowork geteilt — **nur wenn Cowork in der
  Cloud läuft**, nicht bei lokal ausgeführten Cowork-Sitzungen.

### Wie Speicher gespeichert wird

Claude speichert laufend einzelne Themen während des Chats (statt Gespräche erst am
Ende zusammenzufassen). Man kann Claude auch explizit bitten, sich etwas zu merken.

### Projektspeicher

Jedes Projekt hat einen eigenen, getrennten Speicherbereich inkl. eigener
Projektzusammenfassung.

### Sensible Themen

Standardmäßig speichert Claude keine sensiblen Themen (Gesundheit, Ethnizität,
Religion, Politik, Geschlechtsidentität u. ä.). Aktivierbar über **Einstellungen >
Speicher > Sensible Themen im Speicher einbeziehen**. Danach erscheint bei jeder
Speicherung eines solchen Themas eine Benachrichtigung.

Nie gespeichert werden, unabhängig von der Einstellung: Ausweisdaten, Strafregister,
Nummern von Finanzkonten, Einwanderungsstatus.

### Was Claude sich merkt

- Rolle, Projekte, beruflicher Kontext
- Personen und Orte im Arbeits- und Lebensumfeld
- Kommunikationspräferenzen und Arbeitsstil
- Technische Vorlieben und Codierungsstil
- Projektdetails und laufende Arbeiten

### Was Claude nicht merkt

- **Incognito-Chats**: temporäre Gespräche, weder im Chatverlauf noch im Speicher.

## Speicher verwalten

- Übersicht/Bearbeitung unter **Einstellungen > Speicher > Themen** (lesen, bearbeiten,
  löschen).
- Direkt im Chat: Claude mitteilen, was gemerkt, geändert oder vergessen werden soll —
  wirkt ab dem nächsten Gespräch.
- Zitate aus früheren Chats verlinken auf das Ursprungsgespräch und bieten die Option,
  es zu löschen.
- Chat-Suche und Speicher lassen sich unter **Einstellungen > Speicher** unabhängig
  voneinander ein-/ausschalten.

### Speicher aktivieren/deaktivieren

Unter **Einstellungen > Speicher**, Schalter „Speicher aus Chats generieren":

- **Speicher pausieren:** bestehender Speicher bleibt erhalten, es werden aber keine
  neuen Einträge erzeugt; Gespräche während der Pause werden bei Reaktivierung nicht
  nachträglich übernommen.
- **Speicher zurücksetzen:** löscht unwiderruflich allen Speicher inkl. Projektspeicher.

## Datenspeicherung und Datenschutz

- Speicher spiegelt Änderungen an Gesprächen in Echtzeit wider.
- Löschen/Ablaufen eines Gesprächs entfernt nicht automatisch zugehörige
  Speichereinträge — einzelne Erinnerungen können aber jederzeit gelöscht werden.
- Speicherdaten sind Teil regulärer Datenexporte.
- Für Enterprise gelten die jeweiligen Aufbewahrungsrichtlinien für Chat-Suche und
  Incognito-Chats.

## Steuerung für Team-/Enterprise-Owner

- Speicher und „sensible Themen" sind zwei getrennte, standardmäßig deaktivierte
  Schalter auf Organisationsebene (**Organisationseinstellungen > Funktionen**).
- Nach Aktivierung verwalten einzelne Nutzer ihre eigenen Speichereinstellungen.
- Deaktiviert ein Owner den Speicher organisationsweit, werden **alle** bestehenden
  Speichereinträge aller Nutzer sofort gelöscht.
- Speicher ist nicht verfügbar für Organisationen mit HIPAA-, Public- oder
  benutzerdefinierten Datenaufbewahrungsvereinbarungen.
- Audit-Log erfasst Aktivierung/Deaktivierung auf Organisationsebene (nicht einzelne
  Nutzerbearbeitungen).

## Legacy-Speicher (ältere Team-/Enterprise-Organisationen)

Ein kleiner Teil der Team-/Enterprise-Organisationen nutzt noch das ältere
Gedächtnis-Erlebnis (**Einstellungen > Funktionen**, nicht „Speicher"). Unterschiede:

- Automatische, alle 24 Stunden aktualisierte Gesamt-Zusammenfassung des
  Chatverlaufs (ohne Projekt-Chats) statt fortlaufender Einzelthemen.
- Eigene Projektzusammenfassung pro Projekt.
- Aktivieren/Deaktivieren, Pausieren und Zurücksetzen funktionieren analog zum neuen
  Speicher, wirken sich aber zusätzlich auf die **monatliche Zusammenfassung** aus, da
  diese aus demselben Chatverlauf erzeugt wird.
- Aktuell nicht für Cowork verfügbar (nur Web, Desktop, Mobile).
