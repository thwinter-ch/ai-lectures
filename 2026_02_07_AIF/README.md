# KI-Produktivitaets-Hacks fuer Fuehrungskraefte

**Start hier** | CAS AI in Finance | HWZ Zuerich

[English Version](README.en.md)

---

| | |
|---|---|
| **Datum** | Samstag, 7. Februar 2026 |
| **Zeit** | 13:00 - 16:45 |
| **Dozent** | Thomas Winter |
| **Modul** | Applied AI |

---

## Was Sie aufbauen werden

Am Ende dieser Session haben Sie ein funktionierendes persoenliches Produktivitaetssystem:

1. **GitHub Repository** — Ihre versionskontrollierte Wissensbasis
2. **Notion Datenbank** — Ihr durchsuchbares "Second Brain"
3. **Schreibstil-Profil** — KI, die wie Sie schreibt
4. **Unternehmensanalyse** — Strukturierte Business-Analyse
5. **Funktionierende KI-Integrationen** — GitHub + Notion + Claude

Das ist keine Theorie. Sie verlassen den Kurs mit einem funktionierenden System, das Sie am Montag nutzen koennen.

---

## Voraussetzungen (vor dem 7. Februar erledigen)

### Erforderlich

| Tool | Kosten | Wozu | Anmeldung |
|------|--------|------|-----------|
| **Laptop** | — | Mit aktuellem Browser (Chrome, Firefox, Safari, Edge) | — |
| **Notion** | Kostenlos | Second Brain Interface | [notion.so](https://notion.so) |
| **Claude Pro** | $20/Monat | KI mit Notion-Schreibzugriff | [claude.ai](https://claude.ai) |

Alternativ zu Claude Pro: **Perplexity Pro**

### Warum die Bezahlversion?

Fuer die Second Brain Uebung bauen wir ein System, bei dem die KI automatisch in eure Notion-Datenbank schreibt:

| Plattform | Notion lesen | In Notion schreiben |
|-----------|--------------|---------------------|
| **Claude Pro** | Ja | Ja (nativ) |
| **Perplexity Pro** | Ja | Ja (nativ) |
| Claude (kostenlos) | Nein | Nein |
| Perplexity (kostenlos) | Nein | Nein |
| ChatGPT Plus | Ja | Nein |

Falls ihr die CHF 20 nicht investieren moechtet: Kein Problem — ihr koennt die Uebung theoretisch mitverfolgen. Das Abo kann nach dem ersten Monat gekuendigt werden.

---

## Vorbereitung

- [ ] Notion-Account erstellen
- [ ] Claude Pro oder Perplexity Pro abonnieren

---

## Ablauf

| # | Segment | Typ | Inhalt |
|---|---------|-----|--------|
| 01 | [How I Built This](segments/01-how-i-built-this-lecture/) | Vortrag | System in Aktion, Komponenten verstehen |
| 02 | [Technology Revolution](segments/02-technology-revolution-lecture/) | Vortrag | 2026 als Durchbruchsjahr fuer KI-Agenten |
| 03 | [Writing Profile](segments/03-writing-profile-exercise/) | Uebung | Ihr persoenliches Schreibstil-Profil erstellen |
| 04 | [AI as Managerial Skill](segments/04-ai-managerial-skill-lecture/) | Vortrag | Warum 80% die KI-Nutzung abbrechen |
| 05 | [Company Research](segments/05-company-research-exercise/) | Uebung | Strukturierte Unternehmensanalyse mit KI |
| | *Pause* | | |
| 06 | [Information Overload](segments/06-information-overload-lecture/) | Vortrag | Das Problem, das wir loesen |
| 07 | [Second Brain](segments/07-second-brain-exercise/) | Uebung | Claude + Notion einrichten |
| 08 | [Cognitive Limits](segments/08-cognitive-limits-lecture/) | Vortrag | Warum Mensch-KI-Systeme funktionieren |
| 09 | [Demo: Personalized Summary](segments/09-demo-personalized-summary-lecture/) | Demo | n8n-Workflow in Aktion |

---

## Ressourcen

Alle Materialien befinden sich im [segments/](segments/) Ordner:
- Jeder Segment-Ordner enthaelt `script.md` (Vortragsnotizen) und `gamma-prompt.md` (Folien-Generator)
- Uebungen enthalten Schritt-fuer-Schritt-Anleitungen

---

## Das System, das ich nutze (Demo)

```
Spracheingabe (Wispr Flow)
        |
        v
   Roher Content
        |
        v
  GitHub (Markdown)  <---->  Claude Pro  <---->  Notion (Datenbanken)
        |                        |
        v                        v
Versionskontrollierte       Klassifiziert,
Wissensbasis                durchsuchbares
                           Second Brain
```

**Kernprinzip:** Wissen liegt in portablem Markdown (nicht in proprietaeren Tools eingesperrt). KI verbindet und klassifiziert. Notion macht es durchsuchbar.

*Wispr Flow ([wisprflow.ai](https://wisprflow.ai)) ist Teil meines Workflows, den ich in der Session zeige — keine Voraussetzung fuer die Uebungen.*

---

## Fragen?

Kontaktieren Sie den Dozenten oder erstellen Sie Issues in diesem Repository.

---

*Zuletzt aktualisiert: 1. Februar 2026*
