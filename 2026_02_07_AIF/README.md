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

### Erforderliche Accounts

| Tool | Kosten | Wozu | Anmeldung |
|------|--------|------|-----------|
| **GitHub** | Kostenlos | Wissens-Repository | [github.com/signup](https://github.com/signup) |
| **Notion** | Kostenlos | Second Brain Interface | [notion.so](https://notion.so) |
| **Claude Pro** | $20/Monat | KI mit Notion-Schreibzugriff | [claude.ai](https://claude.ai) |

### Warum Claude Pro?

Wir haben alle grossen KI-Plattformen fuer die Notion-Integration validiert:

| Plattform | Notion lesen | In Notion schreiben | Setup |
|-----------|--------------|---------------------|-------|
| **Claude Pro** | Ja | Ja (nativ) | Einfach |
| **Perplexity Pro** | Ja | Ja (nativ) | Einfach |
| ChatGPT Plus | Ja | Nein (braucht Custom GPT + API) | Komplex |

**Claude Pro und Perplexity Pro** bieten beide native Notion-Schreibfaehigkeit. Fuer diese Session empfehlen wir Claude Pro wegen der Projektfunktion (persistenter Kontext).

### Optional (empfohlen)

- **Wispr Flow** — Sprache-zu-Text fuer schnelle Erfassung ([wispr.ai](https://wispr.ai))
- **5-10 Schreibproben** — E-Mails, Berichte, LinkedIn-Posts (fuer Ihr Stilprofil)

### Hardware

- Laptop mit modernem Browser (Chrome, Firefox, Safari, Edge)
- Kopfhoerer (fuer Sprachuebungen)

---

## Vorbereitung (15 Minuten)

Vor der Session erledigen:

- [ ] GitHub-Account erstellen und E-Mail verifizieren
- [ ] Notion-Account erstellen
- [ ] Claude Pro abonnieren
- [ ] Wispr Flow installieren (optional)
- [ ] 5-10 Schreibproben in einem Ordner sammeln
- [ ] Dieses Repository in Ihren GitHub-Account forken

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

## Das System, das Sie aufbauen

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

**Kernprinzip:** Ihr Wissen liegt in portablem Markdown (nicht in proprietaeren Tools eingesperrt). KI verbindet und klassifiziert. Notion macht es durchsuchbar.

---

## Fragen?

Kontaktieren Sie den Dozenten oder erstellen Sie Issues in diesem Repository.

---

*Zuletzt aktualisiert: 1. Februar 2026*
