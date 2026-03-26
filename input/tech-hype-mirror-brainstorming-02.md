title:: Tech Hype Mirror – Brainstorming Session Teil 2
version:: 0.3
created:: 2026-03-26
modified:: 2026-03-26
tags:: neckarshore-ai, ideation, product, linkedin, automation, hype-detection, brainstorming, zielgruppe, output-format

## Automatisierung als Grundprinzip

Alles was automatisierbar ist, wird automatisiert. Manuelle Arbeit ist zu vermeiden wo immer möglich – das ist kein Nice-to-have, sondern ein Designprinzip für das gesamte Produkt. Die eigene Lebenszeit ist zu wertvoll für repetitive Aufgaben.

## LinkedIn: Zugang und Datenstrategie

Direktes Scraping über LinkedIn-API ist eingeschränkt. Der pragmatische Weg läuft über Drittanbieter-Tools wie Taplio, Eilla AI, Shield Analytics oder Apify, die LinkedIn-Content legal aggregieren und zugänglich machen. Das ist kein ToS-Verstoß und ein etablierter Ansatz im LinkedIn-Automatisierungsumfeld.

## Interaktionsstrategie: Dosiert, gezielt, respektvoll

Das ist kein Spray-and-Pray-Bot, sondern eine kuratierte, dosierte Intervention. Die Leitplanken:

1. Es wird eine Watch-Liste von Personen/Profilen geführt – manuell oder automatisiert angelegt
2. Pro Person maximal eine Interaktion pro Woche, auch wenn die Person täglich postet
3. Pro Person maximal 2–3 Interaktionen insgesamt – danach wird die Person in Ruhe gelassen
4. Kommentiert wird nur, wenn man der erste oder zweite Kommentator sein kann – sonst kein Wert
5. Bei Influencern mit hoher Reichweite: Abstand zwischen Interaktionen vergrößern, Anzahl reduzieren (ggf. nur 1), um unbemerkt zu bleiben
6. Das Ziel ist, dass der Original-Poster gar nicht merkt, was dahinter steckt – kein Konflikt, kein Krieg, kein "Bär aufwecken"

## Human-in-the-Loop: Phasenmodell für Automatisierung

Seriöse Softwareentwicklung bedeutet: erst Vertrauen aufbauen, dann automatisieren.

### Phase 1 – Kalibrierung
- Der Hype-Detektor läuft, aber der Mensch entscheidet
- Das System dokumentiert Treffer: "Das wäre ein valides Ziel gewesen – das hätte ich kommentiert – das hätte ich analysiert"
- Kein automatisches Posten, nur Beobachtung und Protokollierung
- Ziel: Den Detektor so weit trainieren, dass False Positives gegen Null gehen

### Phase 2 – Automatisierung
- Erst wenn die Trefferquote bei ~99% liegt, wird der Prozess vollständig automatisiert
- Das ist kein willkürlicher Schwellenwert – es geht darum, das eigene Branding nicht durch False Positives zu beschädigen
- Das Produkt selbst ist das Schaufenster: Wir predigen Qualität und praktizieren sie

## Hype-Detektor: Kriterien noch offen

Was einen Post zum validen Ziel macht, ist eines der wesentlichsten Elemente der späteren Umsetzung. Konkrete Signalkriterien (Phrasen, Engagement-Schwellen, Reichweite des Posters, etc.) werden in Phase 1 datenbasiert kalibriert. Bewusst offen gelassen – es braucht echte Beobachtungsdaten.

## Output-Format: Kontextabhängig und skaliert

Es gibt keinen fixen Output-Kanal – die Entscheidung hängt vom Ziel ab:

1. Kein direktes Kommentieren unter dem Original-Post als Default – zu riskant, zu aufdringlich
2. Ausnahme: Influencer mit sehr hoher Reichweite, wo der Kontext-Effekt es rechtfertigt – aber dann mit noch größerer Vorsicht und weniger Frequenz
3. Primärer Kanal: Eigene LinkedIn-Timeline – eigene Posts, ggf. als Repost mit Kommentar
4. LinkedIn als Leitmedium: Hochwertige, professionelle Artikel und Analysen – kein Quick-Content
5. Perspektivisch: Eigener X/Twitter-Account als weiterer Kanal, wenn das Format einschlägt
6. Langfristig denkbar: Instagram oder YouTube, wenn das Format skaliert

Das alles läuft unter neckarshore.ai als Dachmarke – nicht unter German Rauhut direkt, aber nicht davon getrennt.

## Tonalität: Lösungsorientiert, nicht problemfokussiert

Der Kern der Positionierung kommt aus einer persönlichen Führungserfahrung: "Hör auf zu meckern. Sag mir nicht was schief läuft – sag mir was du ändern möchtest und wie ich dir konkret helfen kann."

Das überträgt sich direkt auf das Produkt:
- Nicht: "Hier sind 5 Probleme mit deinem Code"
- Sondern: "Hier ist was möglich wäre – und so könnte es konkret aussehen"

Das Produkt soll positiv und konstruktiv sein. Der Original-Poster soll sich nicht angegriffen fühlen. Neckarshore.ai als Dachmarke darf durch keine Interaktion beschädigt werden. Dass manche falsch reagieren lässt sich nicht vermeiden – deswegen sind Interaktionen zeitlich und mengenmäßig begrenzt.

## Zielgruppe: Nicht Entwickler, sondern Geldgeber

Das ist ein entscheidender strategischer Punkt. Die Inhalte richten sich nicht an Entwickler, sondern an:

1. Entscheider, die Entwicklung budgetieren – CTOs, Geschäftsführer, Produktverantwortliche
2. Teamleiter von Entwicklungsteams, die ihre eigene Truppe besser einschätzen wollen
3. Mittelständler, die Software entwickeln lassen und sich fragen: "Wofür gebe ich hier eigentlich Geld aus?"

Das sind die Menschen, die eine Dienstleistung kaufen würden. Entwickler sind das Thema, nicht die Audience.

## Das Kernproblem, das gelöst wird

Vertrauensverlust durch Intransparenz – konkret:

1. Der Geldgeber kann nicht einschätzen, ob das was sein Team oder ein externer Dienstleister baut wirklich produktionsreif ist – oder nur gut aussieht
2. Er hat keine Sprache und kein Werkzeug, um Qualität zu hinterfragen, ohne als "der der nichts versteht" dazustehen
3. Er wurde möglicherweise schon mal mit einem teuren Projekt im Stich gelassen, das live gegangen ist und dann gecrasht, gehackt oder nicht skaliert hat
4. Er sieht Hype überall – KI, neue Tools, "wir brauchen das jetzt" – und weiß nicht, was davon Substanz hat

neckarshore.ai bietet einen unabhängigen, faktenbasierten Spiegel – ohne Entwickler-Arroganz, ohne Beraterkauderwelsch.

## Open Source als Produktstrategie

Der gesamte Tech-Hype-Mirror-Ansatz wird Open Source. Das ist kein Widerspruch zur Monetarisierung:

1. Es demonstriert, dass Qualität gepredigt und praktiziert wird
2. Der Code ist das Schaufenster, nicht das Produkt selbst
3. Der echte Wert liegt im Betrieb, der Kuratierung, dem Branding und den daraus entstehenden Services
4. Andere können es nachbauen – das erhöht die Sichtbarkeit von neckarshore.ai, nicht das Risiko

## Offene Fragen (Stand 2026-03-26)

1. Verlinkung auf Original-Post im eigenen Post – ja oder nein, und wenn ja unter welchen Bedingungen?
2. Wann wird der Ton zu ironisch/sarkastisch – wo ist die konkrete Grenze?
3. Open Source: Wann, unter welcher Lizenz, auf welchem GitHub-Account?
4. Schutzwall: Marke neckarshore.ai, persönlicher Ruf German Rauhut, oder beides kombiniert?
5. Wie sieht der MVP konkret aus – was ist das kleinste sinnvolle erste Experiment für Phase 1?
