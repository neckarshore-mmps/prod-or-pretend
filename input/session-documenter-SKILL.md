---
name: session-documenter
description: Automatically document an ongoing brainstorming, planning, or discovery conversation into structured Markdown checkpoints as the session progresses. Use this skill whenever the user starts a session with phrases like "lass uns diskutieren und dokumentieren", "begleite unser Gespräch", "halte das fest", "checkpoint", "sichere das", "schreib das auf", or when a session is clearly iterative and produces decisions, insights, or open questions that should be preserved. Also trigger when the user asks for a mid-session summary or says "bevor wir weitermachen, sicher mal". Always use this skill instead of improvising a documentation structure — it ensures nothing gets lost in long sessions.
---

# Session Documenter Skill

Begleitet eine laufende Unterhaltung und erstellt strukturierte Markdown-Checkpoints bevor der Kontext zu groß wird oder wichtige Entscheidungen verloren gehen.

## Kernprinzip

Der Documenter hat zwei Modi:

1. Reaktiv – Der Nutzer fragt explizit nach einem Checkpoint oder einer Sicherung
2. Proaktiv – Der Documenter erkennt selbst, wann genug neues Material für einen Checkpoint vorhanden ist und kündigt das kurz an

## Wann proaktiv dokumentieren?

Erstelle automatisch einen Checkpoint wenn:
- 5–7 substanzielle neue Antworten seit dem letzten Checkpoint vorliegen
- Ein klarer Themenblock abgeschlossen wurde
- Eine wichtige Entscheidung gefallen ist (Name, Strategie, Architektur, Zielgruppe)
- Der Nutzer eine neue Richtung einschlägt oder den Scope erweitert

Ankündigung: "Ich dokumentiere jetzt kurz – wir haben genug Neues beisammen." Dann Checkpoint erstellen, dann weiter.

## Output Format

Jeder Checkpoint ist eine eigene Markdown-Datei mit Obsidian-Properties.

```
title:: [Session-Titel] – [Thema oder Phase] Teil [N]
version:: 0.1
created:: [YYYY-MM-DD]
modified:: [YYYY-MM-DD]
tags:: [domain-tags], brainstorming, session-doc
```

### Pflichtbestandteile jedes Checkpoints

1. Session-Zusammenfassung (Key Decisions auf einen Blick)
   - Nummerierte Liste der wichtigsten Entscheidungen dieser Session
   - Maximal 7 Punkte, je ein Satz

2. Inhaltliche Sections
   - Eine Section pro abgeschlossenem Themenblock
   - Entscheidungen klar als solche markieren
   - Offene Punkte explizit benennen

3. Offene Fragen & nächste Schritte
   - Was ist noch ungeklärt?
   - Was wurde bewusst zurückgestellt?
   - Was kommt als nächstes?

## Dateinamens-Konvention

```
[projekt-name]-session-[NN].md
```

Beispiel: `prod-or-pretend-session-01.md`, `prod-or-pretend-session-02.md`

Nummerierung läuft über die gesamte Projekt-Lebensdauer durch – nicht pro Gespräch neu starten.

## Qualitätskriterien

Vor dem Speichern prüfen:
- [ ] Keine wichtige Entscheidung fehlt
- [ ] Offene Punkte sind explizit als offen markiert
- [ ] Der Checkpoint ist ohne Kenntnis der gesamten Session verständlich
- [ ] Sprache und Formulierungen des Nutzers wurden beibehalten wo möglich
- [ ] Nichts wurde erfunden – nur was tatsächlich besprochen wurde

## Qualitätsbewertung

Nach jedem Checkpoint intern bewerten: Würde eine Person, die dieses Gespräch nicht geführt hat, aus diesem Dokument 90% des relevanten Kontexts verstehen? 

- Ja → Checkpoint ist fertig
- Nein → Section vertiefen bevor speichern

## Session-Abschluss

Am Ende einer Session:
1. Finalen Checkpoint erstellen
2. Alle Dokumente der Session auflisten mit kurzem Titel
3. Vorschlagen: "Soll ich daraus jetzt ein PRD oder ein konsolidiertes Dokument erstellen?"

## Zusammenspiel mit brainstorming-to-prd

Session Documenter und brainstorming-to-prd ergänzen sich:
- Session Documenter = laufende Sicherung während des Gesprächs
- brainstorming-to-prd = strukturierter Abschluss wenn genug Material da ist

Der Documenter produziert das Rohmaterial, der PRD-Skill formt es zum finalen Dokument.
