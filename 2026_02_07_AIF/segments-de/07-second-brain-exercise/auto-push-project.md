# Claude Projekt + Notion Auto-Push

**Einrichtungszeit: ca. 10 Minuten**

Mach jede Claude-Konversation zu einem dauerhaften Wissens-Asset. Du konfigurierst ein Claude-Projekt, das auf Zuruf Erkenntnisse zusammenfasst und in dein Notion Second Brain schreibt.

---

## Voraussetzungen

- Claude Pro Abonnement (für die Projekte-Funktion)
- Notion mit Claude verbunden (siehe [claude-notion-setup.md](./claude-notion-setup.md))

---

## Schritt 1: Notion-Datenbank erstellen lassen

Starte eine Claude-Konversation und sag:

> «Erstelle mir eine Second-Brain-Datenbank in Notion mit Feldern für Titel, Datum, Kernerkenntnisse, Quelle, Tags, Aktionspunkte und Konfidenz. Gib mir die Datenbank-ID.»

Claude erstellt die Datenbank und gibt dir die ID. **Kopiere diese ID.**

---

## Schritt 2: Claude-Projekt einrichten

1. Gehe zu [claude.ai](https://claude.ai) → **Projekte** (linke Sidebar)
2. Klicke auf **Neues Projekt**
3. Gib einen Namen ein (z.B. "Second Brain")
4. Öffne die **Projektanweisungen** und füge den Text unten ein
5. Ersetze `[HIER DEINE ID EINFÜGEN]` mit deiner Datenbank-ID aus Schritt 1

### Projektanweisungen (kopieren & einfügen)

```
# Wissenserfassungsprotokoll

Du hast Zugriff auf Notion via MCP. Am Ende substantieller Gespräche überträgst du Erkenntnisse in mein Second Brain.

## Notion-Datenbank
- Datenbank-ID: [HIER DEINE ID EINFÜGEN]

## Wann übertragen
Übertragung zu Notion bei:
- Ich sage «speichere das», «erfasse das», «push zu Notion» oder «Sitzung beenden»
- Gespräch enthält umsetzbare Erkenntnisse, Entscheidungen oder neuartige Frameworks
- Recherche liefert wiederverwendbare Ergebnisse

NICHT übertragen bei:
- Schnellen Frage-Antwort-Sequenzen ohne dauerhaften Wert
- Fehlerbehebungssitzungen (es sei denn, sie offenbaren wiederverwendbare Muster)
- Beiläufigen Gesprächen

## Erfassungsformat
Bei Übertragung zu Notion so strukturieren:

**Titel**: [Prägnantes Thema — max. 60 Zeichen]

**Kernerkenntnisse** (3-5 Punkte):
- Mit dem Nicht-Offensichtlichen beginnen
- Fokus auf «was mein Denken verändert hat» oder «was ich nutzen kann»
- Überspringe Kontext, der googlebar ist

**Tags**: [Relevante Domänen-Tags]
**Quelle**: Claude Chat
**Konfidenz**: Hoch / Mittel / Spekulativ
**Aktionspunkte**: [Nur wenn echte nächste Schritte vorhanden]

## Verhalten
- Vor Übertragung nachfragen, wenn der Wert unklar ist
- Zusammenfassen, was erfasst werden soll, bevor die Übertragung erfolgt
- Erfolgreiche Übertragung mit dem Eintragstitel bestätigen
```

---

## Schritt 3: Testen

1. Öffne eine neue Konversation **innerhalb deines Projekts** (nicht eine normale Konversation)
2. Führe ein kurzes Gespräch — z.B. frag nach einer Zusammenfassung eines Themas
3. Sag am Ende: **«Speichere das in Notion»**
4. Prüfe in Notion, ob der Eintrag erscheint

### Beispiel

```
Du: «Erkläre mir die wichtigsten Prinzipien von Value Investing.»

Claude: [erklärt Value Investing]

Du: «Speichere das in Notion.»

Claude: «Übertragung in dein Second Brain:

Titel: Value Investing — Kernprinzipien
Kernerkenntnisse:
- Intrinsischer Wert > Marktpreis = Sicherheitsmarge
- Langfristiger Horizont schlägt kurzfristige Volatilität
- Qualitätsunternehmen zu fairem Preis > günstige Unternehmen
Tags: #investing #frameworks
Konfidenz: Hoch

Bestätigt: Eintrag erfolgreich erstellt.»
```

---

## So benutzt du es im Alltag

| Du sagst... | Claude macht... |
|-------------|-----------------|
| «Speichere das in Notion» | Sofortige Übertragung |
| «Sitzung beenden» | Zusammenfassen + übertragen + bestätigen |
| «Was ist erfassenswert?» | Claude schlägt vor, du genehmigst |
| «Übertrage [spezifische Erkenntnis]» | Gezielte Erfassung |

---

## Fehlerbehebung

| Problem | Lösung |
|---------|--------|
| «Kann nicht auf Notion zugreifen» | In Claude unter Einstellungen → Integrationen prüfen, ob Notion verbunden ist |
| Übertragung schlägt fehl | Datenbank-ID in den Projektanweisungen prüfen |
| Falsche Datenbank | Bestätigen, dass die Datenbank-ID verwendet wird, nicht die Seiten-ID |
| Fehlende Eigenschaften | Sicherstellen, dass die Notion-Datenbank alle Spalten hat |
| Übertragung nicht ausgelöst | Sicherstellen, dass du innerhalb des Projekts arbeitest, nicht in einer normalen Konversation |

---

## Optionale Erweiterungen (nach dem Kurs)

Du kannst die Projektanweisungen um Modi erweitern. Öffne dein bestehendes Projekt, gehe zu **Projektanweisungen**, und füge den gewünschten Block am Ende ein.

### Recherche-Modus

Füge diesen Text in deine Projektanweisungen ein:

```
## Recherche-Modus
Wenn ich «Recherche-Modus» sage:
- Erfasse jede substantielle Erkenntnis einzeln mit Quellen-URL
- Markiere Konfidenz pro Erkenntnis (Hoch/Mittel/Spekulativ)
- Bei «Recherche abschliessen»: Erstelle einen konsolidierten Eintrag mit allen Erkenntnissen, gruppiert nach Thema
```

### Meeting-Modus

```
## Meeting-Modus
Wenn ich «Meeting-Modus: [Name]» sage:
- Erfasse nur: Entscheidungen, Aktionspunkte (mit Verantwortlichen), offene Fragen
- Ignoriere Smalltalk und Hintergrundinfos
- Titel-Format: «Meeting — [Name] — [Datum]»
- Bei «Meeting Ende»: Übertrage sofort mit Aktionspunkten als Checkliste
```

### Brainstorming-Modus

```
## Brainstorming-Modus
Wenn ich «Brainstorming-Modus» sage:
- Erfasse auch spekulative und unfertige Ideen
- Konfidenz immer «Spekulativ» setzen
- Für jede Idee ein Kill-Kriterium notieren (was müsste stimmen, damit die Idee funktioniert?)
- Bei «Brainstorming Ende»: Übertrage alle Ideen als einzelnen Eintrag, sortiert nach Potenzial
```
