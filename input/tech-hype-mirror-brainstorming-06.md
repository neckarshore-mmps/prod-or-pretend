title:: Tech Hype Mirror – Brainstorming Session Teil 6
version:: 0.1
created:: 2026-03-26
modified:: 2026-03-26
tags:: neckarshore-ai, prod-or-pretend, monetarisierung, crm, open-source, github, kpis, brainstorming

## Session-Zusammenfassung: Key Decisions auf einen Blick

1. Monetarisierung läuft über LinkedIn als Akquise-Kanal – nicht über das Tool selbst
2. KPIs und Funnel-Messung sind Pflicht – kein Schreien in leere Turnhallen
3. CRM: aktuell LinkedIn + Calendly + Outlook, HubSpot Free oder Pipedrive wenn nötig
4. GitHub Organisation neckarshore-ai wird aufgemacht – Trennung privat/beruflich
5. prod-or-pretend wird schnell öffentlich – Glaubwürdigkeit durch Transparenz
6. OMIXSIS-Repos bleiben vorerst privat, ziehen später zu neckarshore-ai um

---

## Monetarisierung: Akquise-Kanal, kein Produkt mit Paywall

Das Geld kommt nicht aus dem Tool selbst, sondern aus dem was das Tool auslöst. Prod or Pretend ist ein Akquise-Kanal für Consulting-Mandate und Dienstleistungen unter neckarshore.ai. Das ist die primäre Monetarisierungsstrategie.

Sekundäre Optionen die offen bleiben:
1. Bezahlter Content-Kanal – möglich wenn Reichweite da ist
2. Security-Scan als bezahlter Self-Service – längerfristig denkbar
3. Inbound Leads über Sichtbarkeit – das ist der Hauptpfad

## KPIs und Funnel-Messung

Ohne Messung weiß man nicht ob man in eine leere Turnhalle schreit. Prod or Pretend soll berufliche Ziele verfolgen und direkt oder indirekt Geld generieren – kein Selbstbefriedigungsmechanismus.

### Funnel
LinkedIn Reichweite → Artikel-Views → Profil-Besuche → Kontaktanfragen → Gespräche → Mandat

### Nicht-monetäre KPIs (Awareness)
1. Follower-Wachstum auf LinkedIn und X
2. Post-Reichweite und Impressions
3. Engagement-Rate (Kommentare, Shares, nicht nur Likes)
4. Artikel-Views pro Veröffentlichung

### Monetäre KPIs (Conversion)
1. Profil-Besuche nach Post-Veröffentlichung
2. Kontaktanfragen pro Monat
3. Calendly-Buchungen – wer geht durch den Sales Funnel?
4. Gesprächsanfragen – wer vereinbart ein Erstgespräch?
5. Conversion Rate Gespräch → Mandat

### Was noch fehlt
Die Verbindung zwischen LinkedIn-Aktivität und tatsächlichem Verkauf passiert meist außerhalb von LinkedIn – per E-Mail, Telefon, persönlichem Gespräch. Das muss nachgetragen und manuell verknüpft werden bis ein CRM das übernimmt.

## CRM-Strategie

### Aktueller Stand
LinkedIn als primäres CRM, Calendly für Terminbuchung, Outlook für E-Mail. Das reicht für den MVP vollkommen.

Grundsatz: Ein CRM das nicht genutzt wird ist schlechter als kein CRM.

### Auswahlliste für später
Kriterien: Cloud-basiert, niedrige Einstiegskosten, fair bepreist, skalierbar, LinkedIn-Integration.

1. HubSpot Free – kostenlos bis gewissem Volumen, LinkedIn-Integration, Calendly-Verbindung, E-Mail-Tracking. Risiko: wird schnell teuer in bezahlten Tiers
2. Pipedrive – im DACH-Raum beliebt für Consultants, fokussiert auf Sales-Funnel, faire Preise, kein Overengineering
3. Notion als CRM – ausgeschlossen, da Obsidian-Nutzer

### Entscheidung
Erst CRM einführen wenn Kontakte durch die Lappen gehen oder der Überblick verloren geht. Nicht vorher.

## GitHub: Trennung privat/beruflich

### Entscheidung
GitHub Organisation `neckarshore-ai` wird aufgemacht. Trennung von persönlichem Account (GmanFooFoo) und beruflichem Kontext ist überfällig.

### Repository-Strategie
1. `prod-or-pretend` – erstes öffentliches Repo, geht schnell live
2. OMIXSIS-Repos (omixsis-testmanagement, omixsis-document-ingestor, etc.) – aktuell privat auf GmanFooFoo, ziehen später zu neckarshore-ai um
3. OMIXSIS-Repos bleiben privat bis Security-Updates gemacht sind

### Warum prod-or-pretend schnell öffentlich wird
Wer andere Repos analysiert und Schwachstellen aufzeigt, muss das eigene Haus in Ordnung haben. Glaubwürdigkeit durch Transparenz – das ist kein Nice-to-have, das ist die Grundvoraussetzung für die Positionierung. Außerdem: Community-Feedback ist unbezahlter Qualitätsdienst. Wer den Repo findet und kritisiert, schickt praktisch seine Beteiligung rüber.

## Offene Punkte

1. Lizenz für prod-or-pretend – MIT, Apache 2.0, oder BSL? (offen, gehört auf die Entscheidungsliste)
2. Zeitplan für Migration der OMIXSIS-Repos zu neckarshore-ai
3. HubSpot Free vs. Pipedrive – Entscheidung wenn CRM-Bedarf entsteht
4. OMIXSIS-Integration in Prod or Pretend – kommt mit Doku (zurückgestellt)
