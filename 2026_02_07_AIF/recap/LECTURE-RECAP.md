# KI-Produktivitäts-Hacks für Führungskräfte — Vorlesungs-Recap

**CAS AI in Finance** | HWZ Zürich | 7. Februar 2026, 13:00–16:45
**Dozent:** Thomas Winter | **Studiengangsleiter:** Patrick Comboeuf

---

## Überblick

In einer 3,5-stündigen Praxis-Session bauten 21 Finanzfachleute drei funktionierende KI-Systeme von Grund auf: ein persönliches Schreibstil-Profil, einen strukturierten Unternehmensrecherche-Workflow und ein Claude-to-Notion «Second Brain». Die Vorlesung selbst wurde mit denselben Tools erstellt, die gelehrt wurden — eine bewusste Meta-Demonstration von KI-gestützter Inhaltsproduktion.

**Was die Teilnehmenden mitgenommen haben:**

1. **Schreibstil-Profil** — Ein persönliches Stimmdokument, das der KI beibringt, wie man selbst schreibt — statt generischem KI-Einheitsbrei
2. **Unternehmensrecherche-Workflow** — Eine zweistufige Prompt-Kette (Deep Research → Strategy Synthesis) für vorstandstaugliche Briefings
3. **Second Brain** — Eine Notion-Datenbank mit Claude-Anbindung für automatische Wissenserfassung

**Kernthese:** KI-Erfolg ist keine technische Fähigkeit — es ist eine Führungskompetenz. Dieselben Qualitäten, die jemanden zu einem guten Manager machen (klare Delegation, Qualitätsurteil, iteratives Feedback), bestimmen auch, wer mit KI erfolgreich ist.

---

## Segment für Segment

### Segment 01: How I Built This
**Typ:** Vortrag | **Dauer:** 15 Min. | [Slides](https://gamma.app/docs/01-Wie-ich-diese-Vorlesung-erstellt-habe-atjj9amvea35m4a)

Das Eröffnungssegment diente als Glaubwürdigkeitsbeweis: Die gesamte Vorlesung wurde mit den KI-Tools erstellt, die in der Session gelehrt werden. Thomas führte durch die Produktionskette — von einem Sprach-Brainstorm beim Spazieren (Wispr Flow) über Research (Perplexity), parallele Agenten-Ausführung (Claude Code), Slide-Generierung (Gamma) bis zur Wissenserfassung (Notion).

**Highlights aus der Live-Session:**
- «This isn't theory. This is me eating my own cooking.»
- Der Zeitrahmen vom Voice-Note zur fertigen Vorlesung: unter zwei Wochen, als Nebenprojekt
- Ehrliches Eingeständnis: «AI gives you draft 7 instead of draft 1. You still need to get to draft 10.»

**Kernkonzepte:**
- **Dogfooding-Prinzip** — Wer KI-Workflows unterrichtet, sollte damit auch die Vorlesung gebaut haben
- **Produktion leiten statt Inhalte erstellen** — Die Rolle verschiebt sich vom Tun zum Orchestrieren
- **Infrastruktur, nicht Tools** — «Ihr lernt keine Tools. Ihr baut Infrastruktur. Der Payoff ist nicht heute — sondern jeden Tag danach.»

---

### Segment 02: Die Technologie-Revolution
**Typ:** Vortrag | **Dauer:** 15 Min. | [Slides](https://gamma.app/docs/02-Die-Technologie-Revolution-myy1vq3y7d4x16s)

2026 ist das Jahr, in dem alle technischen Barrieren gefallen sind. Der neue Engpass ist nicht, was KI kann — sondern ob Menschen klar genug formulieren können, um zu delegieren.

**Kernkonzepte:**
- **Der 2026er Durchbruch-Stack:** Consumer-taugliche Hardware, anhaltende Aufmerksamkeit (Agenten arbeiten stundenlang fokussiert), persistenter Speicher über Sessions hinweg, MCP + Skills als Tool-Standard, autonome Browser-/Datei-Interaktion
- **Sie sind die Übersetzungsschicht** — «Der Engpass hat sich verschoben. Früher: Kann die KI das? Heute: Können SIE klar genug definieren, was gemacht werden soll?»
- **Das Mini-Me-Rennen** — Wer baut Ihren KI-Zwilling zuerst? Sie, Ihr Konkurrent oder niemand? Compound Returns bedeuten: Frühstarter vergrössern den Abstand monatlich
- **Zwei-Schichten-Architektur** — Übersetzungsschicht (wo Menschen interagieren, Ambiguität klären) + Task-Execution-Schicht (wo Agenten glänzen, zuverlässig ausführen)

**Diskussionshighlights:**
- Thomas demonstrierte live, wie Claude Code einen fehlerhaften Link im Repository in Echtzeit reparierte — «Lecture as Code» in Aktion
- Mehrere Teilnehmende fragten nach Tool-Auswahl; Thomas betonte: «Die Frage ist nicht welches Tool — 201-Skills sind werkzeugunabhängig»

---

### Segment 03: Writing Profile Übung
**Typ:** Übung | **Dauer:** 25 Min. | [Übungsanleitung](https://github.com/thwinter-ch/ai-lectures/blob/master/2026_02_07_AIF/segments-de/03-writing-profile-exercise/README.md)

Die Teilnehmenden bauten persönliche Stimm-Profile mit der Ruben-Hassid-Methode — ein strukturiertes Selbstinterview, das die eigene «Schreib-DNA» extrahiert: Überzeugungen, Einschränkungen, Abneigungen und Muster.

**Was es macht:**
- 10-Fragen «Lite Interview» über 7 Kategorien von Kommunikationspräferenzen
- Produziert ein Markdown-Stimmprofil mit verbotenen Wörtern, Signatur-Phrasen, Tonalitäts-Markern
- Das Profil kann an jede KI-Konversation angehängt werden, damit Outputs wie man selbst klingen

**Live-Beobachtungen:**
- Thomas: «Das wird teilweise zu einer Psychologie-Session — es sagt einem auch etwas über sich aus, wo bin ich präzis, wo bin ich nicht präzis»
- Teilnehmende fanden es überraschend aufschlussreich: Der Rahmen drängt über vage Antworten wie «ich halte es gerne einfach» hinaus zu konkreten Präferenzen
- Die Übung baut direkt die erste «201-Skill» auf — Kontextqualität

---

### Segment 04: KI als Führungskompetenz
**Typ:** Vortrag | **Dauer:** 15 Min. | [Slides](https://gamma.app/docs/v5gsyrz3bf5anxo)

Das datenreichste Segment. Thomas präsentierte Forschung darüber, warum 80% der Menschen nach 3 Wochen aufgeben — und was die erfolgreichen 20% anders machen.

**Kerndaten:**
- **Microsoft Copilot-Studie:** 300'000 Mitarbeitende getrackt. 80% gaben KI-Tools nach drei Wochen auf. Nicht 80% der Underperformer — 80% von allen.
- **BCG-Harvard-Studie (758 Consultants):** Innerhalb der KI-Fähigkeitszone: +12% mehr Tasks, 25% schneller, 40% höhere Qualität. Ausserhalb: 19 Prozentpunkte *schlechter* als ohne KI.
- **The Jagged Frontier:** KI-Fähigkeiten sind keine saubere Linie. Sie sind zerklüftet, uneben und oft unsichtbar. «Wenn Sie nicht wissen, wo die Grenze ist, hilft KI nicht nur nicht — sie verschlechtert Ihre Leistung aktiv.»

**Kernkonzepte:**
- **Zentaur-Arbeit** — Klare Arbeitsteilung. Mensch macht Strategie, KI macht den Entwurf. Saubere Übergaben. Funktioniert am besten für definierte Aufgaben.
- **Cyborg-Arbeit** — Kontinuierliche Integration. KI beginnt einen Satz, Sie beenden ihn. Hin und her, fliessend. Funktioniert für kreative, explorative Arbeit.
- **Die sechs 201-Skills:** Kontextqualität, Qualitätsurteil, Aufgabenzerlegung, iterative Verfeinerung, Workflow-Integration, Grenz-Awareness — «Das sind dieselben Fähigkeiten, die jemanden gut im Führen von Menschen machen.»
- **Die Erlaubnislücke** — Ihre gewissenhaftesten Mitarbeitenden steigen zuerst aus, wenn Sie keine explizite Erlaubnis geben zu lernen, vorübergehend schlechtere Ergebnisse zu liefern und zu experimentieren.

**Live-Diskussion — Change Management (ausgedehnte Q&A):**

Dieses Segment löste die längste Diskussion der Session aus. Kernpunkte:

- **Reverse Mentoring:** «Die Enthusiasten sollen die anderen an die Hand nehmen — aber sagen Sie ihnen, dass es Empathie braucht. Nicht jeder checkt es beim dritten Mal. Denken Sie daran wie Kindern das Laufen beibringen.»
- **Organisationsrealität:** «Wenn man KI ohne Change Management einführt, ist das Ergebnis Wildwuchs, nicht Kollaboration. 20% werden Experten, 20% schleppen sich nach, und die Mehrheit sagt: Blödsinn.»
- **Der Lern-Dip:** «Ihr bester Finanzauditor ist plötzlich für drei Monate nicht mehr der beste. Wenn Sie ihm keine Erlaubnis geben für diesen Dip, kündigt er entweder die KI oder den Job.»
- **Grenzen des Arbeitgebers:** «Man hat nicht die unendliche Verantwortung, jeden mitzuschleppen. Irgendwann, wenn jemand über keinen Weg Resultate liefern kann, ist das auch eine Realität.»

---

### Segment 05: Unternehmensrecherche Übung
**Typ:** Übung | **Dauer:** 30 Min. | [Übungsanleitung](https://github.com/thwinter-ch/ai-lectures/blob/master/2026_02_07_AIF/segments-de/05-company-research-exercise/README.md)

Ein zweistufiger KI-Research-Workflow für vorstandstaugliche Unternehmens-Briefings.

**Stufe 1 — Deep Research (Perplexity Pro):**
- Strukturierter Research-Prompt mit 30'000+ Wörtern Analyse
- Executive Summary, Produkt-Tabelle, Wettbewerbs-Matrix, Risiko-Flags mit Quellenangaben
- Teilnehmende recherchierten ihre eigenen Firmen, Kunden oder Wettbewerber

**Stufe 2 — Strategy Synthesis (Claude):**
- Stufe-1-Output wird in Framework-Synthese eingespeist
- Produziert: Golden Circle (Why/How/What), Business Model Canvas (9 Blöcke), Value Proposition Canvas (Jobs/Pains/Gains)
- Output: 10'000-Wörter Strategiedokument mit visuellen Hilfen

**Live-Beobachtungen:**
- Thomas: «Wenn Sie in ein Erstgespräch kommen mit einem kompletten Research plus Golden Circle plus BMC plus VPC, sind Sie sofort der Hero — weil der Kunde das Gefühl hat, Sie interessieren sich wirklich für sein Business.»
- Ein Teilnehmer produzierte einen Research mit 7'800 Quellen — eine Demonstration sowohl der Leistung als auch der «Wie finde ich das Signal im Lärm?»-Herausforderung
- Diskussion über Living Documents: monatlich durchführen, als Markdown speichern, KI quartalsweise Trendveränderungen identifizieren lassen

---

### *Pause (15 Minuten)*

---

### Segment 06: Informationsflut + Kognitive Grenzen
**Typ:** Vortrag | **Dauer:** 15 Min. | [Slides](https://gamma.app/docs/e3131dy593gw4ai)

Dieses Segment kombinierte das Informationsüberflutungs-Material mit kognitiver Forschung und schuf die theoretische Grundlage für die Second Brain Übung.

**Kerndaten:**
- Führungskräfte erhalten 120+ E-Mails/Tag, verbringen 28% ihrer Arbeitswoche allein mit E-Mail
- Manager verbringen durchschnittlich 23 Stunden/Woche in Meetings
- 23 Minuten zum Refokussieren nach einer Unterbrechung (UC Irvine Studie)

**Kernkonzepte:**
- **Millers 7±2 Gesetz** — Das Arbeitsgedächtnis hält ungefähr 7 Elemente fest. «Jede Führungskraft in diesem Raum operiert im selben 7±2-Gefängnis. Auch Mark Zuckerberg und Einstein.»
- **Die israelische Richter-Studie** — Bewährungsquote sank von 65% nach dem Frühstück auf fast 0% vor dem Mittagessen. «Jede Nachmittagsentscheidung ist potenziell beeinträchtigt. Nicht durch Informationsasymmetrie — durch den Blutzuckerspiegel.»
- **Information Escape Velocity** — «Der Führungsvorteil war früher der Zugang zu Information. Heute ist es die Fluchtgeschwindigkeit aus der Information.»
- **Pull statt Push** — Das alte Modell (alles abonnieren, breit lesen) brach zusammen, als Information unendlich wurde. Das neue Modell: Die Frage definieren, die KI die Schwerstarbeit machen lassen.
- **KI als kognitive Erweiterung** — Nicht Ersatz. Dieselbe Progression wie Schrift das Gedächtnis erweiterte, Taschenrechner die Arithmetik, Suchmaschinen das Abrufen von Wissen.

**Live-Insights:**
- Thomas zeichnete die Datenexplosion nach: von Kilobytes (vor 1500) über Petabytes (1980er), Exabytes (2000er) zu Zettabytes (heute)
- Verbindung zur vorherigen Übung: «Ihr habt gerade 80'000 Wörter Research produziert. Wer liest das? Das ist genau das Informationsmanagement-Problem.»
- Ehrliches Eingeständnis: «Ich habe bei einem VR-Seminar im Dezember gesagt, dass persönliches Informationsmanagement das eine Problem ist, das ich nicht gelöst habe. Ich habe Evernote probiert, OneNote, Capacities — same shit, different logo.»

---

### Segment 07: Second Brain Übung
**Typ:** Übung | **Dauer:** 25 Min. | [Übungsanleitung](https://github.com/thwinter-ch/ai-lectures/blob/master/2026_02_07_AIF/segments-de/07-second-brain-exercise/README.md)

Die Teilnehmenden verbanden Claude mit Notion und bauten ein Wissenserfassungs-System.

**Was gebaut wurde:**
1. Claude-to-Notion-Verbindung (Ein-Klick MCP-Integration)
2. Eine Notion-Datenbank mit strukturierten Feldern (Thema, Tags, Quelle, Action Items)
3. Auto-Push-Anweisungen: Am Ende jeder Claude-Konversation «speichere das» sagen, und es fasst zusammen + schreibt in die Datenbank

**Warum das wichtig ist:**
- «Die meisten Wissensmanagement-Systeme sterben an Reibung. Das hier entfernt die Reibung.»
- «Wenn man es regelmässig füttert, entstehen Muster. Die KI kann sagen, mit welchen Themen man sich beschäftigt hat — es wird zum Spiegel des eigenen Geistes.»

**Live-Herausforderungen und Workarounds:**
- Einige Teilnehmende hatten kein Mikrofon-Zugriff in Claude im Browser — die Mobile App funktionierte als Fallback
- ChatGPT-Nutzer stellten fest, dass es aus Notion nur lesen, aber nicht schreiben kann (Produktentscheidung von OpenAI, keine technische Limitation)
- Thomas half mehreren Teilnehmenden beim Connector-Setup — «Diese Konnektoren können manchmal etwas bockig sein»
- Diskussion über Wispr Flow als Alternative für Spracheingabe

**Die Telegram-Demo:**
Thomas demonstrierte sein eigenes erweitertes Setup: Ein Telegram-Kanal, in dem Sprachnachrichten, Fotos und Text automatisch von einer Serverless Function klassifiziert und in eine getaggte Notion-Datenbank geschrieben werden. «Das ist ein kleiner Schritt über das hinaus, was ihr gerade gebaut habt. Ich habe einfach das Interface schmäler gemacht und automatische Klassifizierung hinzugefügt.»

---

### Segment 08: Ausblick & Realitätscheck
**Typ:** Vortrag + Demo | **Dauer:** 20 Min. | [Slides](https://gamma.app/docs/twkfm2mwi1334ud)

Das Schlusssegment kombinierte Live-Demos fortgeschrittener KI-Fähigkeiten mit wichtigen Warnungen zu Sicherheit und Souveränität.

**Teil A — Live-Demos:**

1. **Lecture as Code** — Zeigte, wie ein Fehlerbericht eines Teilnehmers in Echtzeit mit Claude Code behoben wurde: «Der Teilnehmer sagte, ein Link sei kaputt. Ich habe Claude gesagt, er soll investigieren. Innerhalb von 2 Minuten war das öffentliche Repository aktualisiert.»

2. **Hugo (OpenClaw Agent)** — Demonstration eines autonomen KI-Agenten, der:
   - Seinen eigenen LinkedIn-Kanal verwaltet
   - In Echtzeit einen Social-Media-Post über die Vorlesung generierte
   - Über die Gemini API ein Bild erstellte
   - Via Typefully automatisiert posten kann
   - Seit 2 Tagen Krypto im Paper-Trading-Account handelt (Alpaca API)

3. **Personalisierte Meeting-Zusammenfassungen** — Zeigte einen n8n-Workflow, der:
   - Meeting-Transkripte + Teilnehmerprofile + Interessengebiete verarbeitet
   - Individuelle Zusammenfassungen für jeden Teilnehmer produziert
   - «Jeder bekommt seine eigene Infografik und personalisierte Takeaways»

**Teil B — Realitätscheck:**

4. **Datensouveränität & Cloud Act:**
   - «Der Cloud Act ist nicht der Grund, nicht in die Cloud zu gehen. Das ist ‹Clarifying Lawful Overseas Use of Data› — 95% der Anfragen werden von den Cloud-Providern abgelehnt.»
   - Bei kriminellen Bedrohungen: Grosse Cloud-Anbieter bieten bessere Sicherheit als die meisten mittelgrossen Firmen selbst aufbauen können
   - Bei staatlichen Bedrohungen: Andere Kalkulation. FISA 702, National Security Letters operieren ohne öffentliche Bekanntgabe
   - «Für 90% der Anwendungen sind die grossen Player tiptop. Für regulierte Branchen mit kompetitivem IP, das in Konflikt stehen könnte mit einer mächtigen US-Firma — dort braucht es Full Sovereignty.»
   - Schweizer Kontext: Die FINMA hat die meisten Cloud-Nutzungen im Bankwesen genehmigt. Data-Residency-Anforderungen existieren, sind aber handhabbar. Privatbanken sind typischerweise strenger aus Wahl, nicht wegen Regulierung.

5. **KI-Chat-Privatsphäre:** «Behandeln Sie KI-Chats wie E-Mails an Jeffrey Epstein. Planen Sie keine Verbrechen mit ChatGPT — Chat-Protokolle können per Durchsuchungsbefehl angefordert werden.»

6. **Passwort-Hygiene:**
   - Einzigartiges Passwort pro Anwendung (automatisch generiert)
   - Passwort-Manager (1Password, NordPass oder Dashlane — nicht der Browser-basierte)
   - Zwei-Faktor-Authentifizierung überall
   - API-Keys: separat pro Anwendung, rotieren bei Leak
   - Realer Fall: Der Colonial-Pipeline-Hack begann mit einem einzigen Standard-Passwort (test123)

---

## Q&A und Diskussionshighlights

Die Session war durchgehend hochinteraktiv. Zentrale Diskussionsstränge:

### Change Management und KI-Adoption
- **Die Enthusiasmus-Lücke:** Intrinsisch motivierte Leute finden KI spielerisch und sehen die Vorteile. Wer es als aufgezwungen empfindet, sucht nach Fehlern und Gründen dagegen.
- **Reverse Mentoring Rezept:** Enthusiasten mit Skeptikern zusammenbringen, aber Empathie von den Jungen einfordern — «Die müssen das behandeln wie Kindern das Laufen beibringen, nicht wie Code debuggen»
- **Die 80%-Realität:** Wie bei jeder Technologie-Einführung — Teams, Zoom, alle hatten dieselbe Adoption-Kurve. «Kein Change-Management-Budget» ist das Erste, das gestrichen wird, und dann wundert man sich, warum Adoption stagniert.

### Tool-Auswahl und Plattform-Entscheidungen
- Claude Pro für Notion-Schreibzugriff (ChatGPT kann nur lesen)
- Perplexity Pro für Web-Research mit Quellenangaben
- Gemini für Bildgenerierung und YouTube-Video-Interpretation
- Claude Code für alles, was lokalen Maschinenzugriff erfordert
- «Ich versuche plattformagnostisch zu sein, wo immer möglich. Jedes Tool hat seinen Sweet Spot.»

### Die «Next Level»-Diskussion
- Mehrere Teilnehmende fragten nach autonomen Agenten (OpenClaw)
- Thomas' ehrliche Einschätzung: «Das User Experience ist noch nicht für ein Business-Publikum tauglich. Aber es kommt.»
- Eigene VPS und Docker Container hat er erst zwei Wochen vor der Vorlesung aufgebaut — «Ich bin Ingenieur, aber ich habe 20 Jahre nicht programmiert. Claude Code hat es mir beigebracht.»

---

## Übungs-Schnellreferenz

| Übung | Was sie macht | Zeit | Link |
|-------|-------------|------|------|
| **Writing Profile** | Erstellt ein persönliches Stimm-Dokument, das KI Ihren Stil beibringt | 20 Min. | [Anleitung](https://github.com/thwinter-ch/ai-lectures/blob/master/2026_02_07_AIF/segments-de/03-writing-profile-exercise/README.md) |
| **Company Research** | Zweistufiger KI-Research für vorstandstaugliche Firmen-Briefings | 45 Min. | [Anleitung](https://github.com/thwinter-ch/ai-lectures/blob/master/2026_02_07_AIF/segments-de/05-company-research-exercise/README.md) |
| **Second Brain** | Verbindet Claude mit Notion für automatische Wissenserfassung | 25 Min. | [Anleitung](https://github.com/thwinter-ch/ai-lectures/blob/master/2026_02_07_AIF/segments-de/07-second-brain-exercise/README.md) |

**Slide Decks (Gamma):**

| Segment | Deck |
|---------|------|
| 01 — How I Built This | [Öffnen](https://gamma.app/docs/01-Wie-ich-diese-Vorlesung-erstellt-habe-atjj9amvea35m4a) |
| 02 — Die Technologie-Revolution | [Öffnen](https://gamma.app/docs/02-Die-Technologie-Revolution-myy1vq3y7d4x16s) |
| 04 — KI als Führungskompetenz | [Öffnen](https://gamma.app/docs/v5gsyrz3bf5anxo) |
| 06 — Informationsflut | [Öffnen](https://gamma.app/docs/e3131dy593gw4ai) |
| 08 — Ausblick & Realitätscheck | [Öffnen](https://gamma.app/docs/twkfm2mwi1334ud) |

---

## Tools & Ressourcen

### Der verwendete Tech Stack

| Tool | Rolle in der Session | Link |
|------|---------------------|------|
| **Claude Pro** | Primärer KI-Assistent + Notion-Connector | [claude.ai](https://claude.ai) |
| **Perplexity Pro** | Web-Research mit Quellenangaben | [perplexity.ai](https://perplexity.ai) |
| **Notion** | Second Brain Datenbank | [notion.so](https://notion.so) |
| **Claude Code** | Vorlesung damit gebaut, Live-Debugging | [claude.ai/claude-code](https://claude.ai/claude-code) |
| **Gamma** | Slide-Generierung aus Text-Prompts | [gamma.app](https://gamma.app) |
| **Wispr Flow** | Voice-to-Text Erfassung | [wispr.ai](https://wispr.ai) |
| **Optiverse** | Schweizer Meeting-Transkription (Schweizerdeutsch-fähig) | [optiverse.ch](https://optiverse.ch) |
| **n8n** | Workflow-Automatisierung | [n8n.io](https://n8n.io) |
| **OpenClaw** | Autonome KI-Agenten (Hugo) | [openclaw.com](https://openclaw.com) |
| **Typefully** | Social Media Scheduling | [typefully.com](https://typefully.com) |
| **1Password** | Passwort-Management | [1password.com](https://1password.com) |

### Empfohlene nächste Schritte

1. **Diese Woche:** Schreibstil-Profil in 3 verschiedenen KI-Konversationen verwenden. Merken, wo es dünn ist, und ergänzen.
2. **Diesen Monat:** Die Unternehmensrecherche-Übung auf einen echten Kunden oder Wettbewerber anwenden — vor dem nächsten wichtigen Meeting.
3. **Laufend:** Second Brain täglich füttern. Nach einer Woche Claude fragen: «Mit welchen Themen habe ich mich diese Woche befasst?»
4. **Für Ambitionierte:** Claude Code (Terminal-basiert) erkunden für Aufgaben, die lokalen Maschinenzugriff brauchen.
5. **Für Teams:** Den «Reverse Mentoring»-Ansatz in Betracht ziehen — KI-Enthusiasten mit Skeptikern zusammenbringen, beiden Erlaubnis zum Lernen geben.

---

## Was ich gerne vorher gewusst hätte

Praktische Tipps aus der Live-Durchführung:

1. **Der Notion-Connector ist fragil** — Extra Zeit für Setup einplanen. Einige Teilnehmende brauchten 10+ Minuten allein für den MCP-Autorisierungsflow.
2. **ChatGPT kann nicht in Notion schreiben** — Nur Claude und Perplexity haben native Schreib-Connector. Das hat mehrere ChatGPT-Plus-Abonnenten überrascht.
3. **Prompt-Output-Länge ist relevant** — 30'000-Wörter-Research-Outputs können manche Tools überfordern. Mit 5'000-Wörter-Summaries starten für schnelle Resultate; nur bei Bedarf in die Tiefe gehen.
4. **Spracheingabe variiert nach Plattform** — Claude im Browser hat manchmal keinen Mikrofon-Zugriff. Die Mobile App funktioniert. Wispr Flow ist ein Workaround für Desktop-Spracheingabe.
5. **Gamma Slides brauchen Fullscreen** — Thomas hat einen Teil der Vorlesung damit verbracht, herauszufinden, wie Gamma Fullscreen präsentiert. Als PDF herunterladen oder den nativen Präsentationsmodus verwenden.
6. **Der wahre Wert liegt in der zweiten Stufe** — Deep Research ist beeindruckend, aber überwältigend. Die Strategy Synthesis (Golden Circle + BMC + VPC) macht es handlungsfähig.
7. **Monatlich durchführen, quartalsweise tracken** — Research-Outputs als Markdown speichern. Monatlich durchführen. KI quartalsweise Trendveränderungen identifizieren lassen. Der Zinseszins-Effekt ist enorm.

---

## Schlüsselzitate aus der Session

> «AI gives you draft 7 instead of draft 1. You still need to get to draft 10.»

> «Der Engpass hat sich verschoben. Früher: Kann die KI das? Heute: Können Sie klar genug formulieren, um zu delegieren?»

> «Die 80%, die aufgeben, erwarteten eine bessere Suchmaschine. Die 20%, die blieben, verstanden, dass sie einen fähigen, aber unzuverlässigen Mitarbeiter führen.»

> «Der Führungsvorteil war früher der Zugang zu Information. Heute ist es die Fluchtgeschwindigkeit aus der Information.»

> «Behandeln Sie KI-Chats wie E-Mails an Jeffrey Epstein.»

> «Der Cloud Act ist nicht Ihr Feind. 95% der Anfragen werden abgelehnt.»

> «Erkläre mir das wie einem Vollidioten — weil ich komme nicht raus, was du mir sagst.» *(Sein liebster Claude Code Prompt)*

---

*Dieses Recap wurde aus dem Gemini-Live-Transkript, der Optiverse-Zusammenfassung, den vorbereiteten Vorlesungsskripten und Übungsmaterialien erstellt. Die Vorlesungsaufzeichnung steht eingeschriebenen Studierenden zur Verfügung.*

*Repository: [github.com/thwinter-ch/ai-lectures](https://github.com/thwinter-ch/ai-lectures)*
