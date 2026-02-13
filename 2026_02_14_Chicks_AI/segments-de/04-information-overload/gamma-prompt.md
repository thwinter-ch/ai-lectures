# GAMMA-Prompt: Informationsflut & RAG

**Segment:** Talk — Informationsflut & RAG (15 Minuten)
**Folien:** 3
**Gamma Theme ID:** `zewcfhidto4owzx`
**Sprache:** Deutsch (Schweizerdeutsch-freundlich, "ss" statt "ß")
**Stil:** Locker, visuell, wenig Text. Zielgruppe: Leute ohne technischen Hintergrund.

---

## Globale Design-Anweisungen

- **Wenig Text pro Folie** — maximal 15-20 Wörter. Bilder und Grafiken dominieren.
- **Ton:** Freundlich, ermutigend, null Fachjargon
- **Farbpalette:** Hell, einladend, nicht corporate-dunkel
- **Typografie:** Gross, lesbar, serifenlos
- **Bildstil:** Illustrativ, Cartoon-artig wo passend, keine Stockfotos

---

### Folie 1: Warum mehr nicht besser ist

**Titel:** Dein Gehirn hat ein Limit

**Visuell:** Zweigeteilt:
- **Links:** Grosse, illustrative "7±2" — sieben bunte Kreise/Kugeln, die im Kopf Platz finden. Darüber: "Das passt rein."
- **Rechts:** Eine Infografik-Kurve durch den Tag: Morgens hoch (65%), Nachmittags fast null (~0%). Darunter: "Israelische Richter — gleiche Fälle, andere Tageszeit."

**Schlüsseltext:** "7 Dinge gleichzeitig. Mehr geht nicht. Biologie, nicht Disziplin."

**Sprechernotiz:** "Euer Gehirn hält ungefähr 7 Dinge gleichzeitig. Das ist nicht Faulheit — das ist Biologie. Und es wird schlimmer: Israelische Richter haben 1'100 Entscheide gefällt. Morgens: 65% Bewährung. Kurz vor Mittag: fast 0%. Nicht weil die Fälle schlechter waren — weil das Gehirn müde war. Jede Nachmittagsentscheidung ist potenziell beeinträchtigt — durch Blutzuckerspiegel."

---

### Folie 2: Von Push zu Pull

**Titel:** Früher lesen. Heute fragen.

**Visuell:** Einfacher Zwei-Zeilen-Vergleich als Flussdiagramm:
- **Oben (durchgestrichen/ausgegraut):** "Info → Du → Filtern → Vielleicht nutzen" (überladen, chaotisch)
- **Unten (hervorgehoben, leuchtend):** "Frage → KI → Antwort → Handeln" (sauber, klar)

**Schlüsseltext:** "Nicht mehr lesen. Gezielt fragen."

**Sprechernotiz:** "Früher musste man alles lesen, um informiert zu bleiben. Das hat funktioniert, als Information knapp war. Heute ertrinken wir. Die Lösung: Nicht mehr alles lesen. Stattdessen: Der KI die richtige Frage stellen. Das nennt man 'Pull statt Push'. Und genau das machen wir jetzt gleich mit YouTube-Videos und Dokumenten."

---

### Folie 3: Was ist RAG?

**Titel:** Die KI liest DEIN Dokument

**Visuell:**
- Illustration: Eine Person sitzt in einer Prüfung mit einem offenen Buch. Das Buch hat ein Label: "Dein PDF / Dein Video / Dein Dokument"
- Oder: Links ein geschlossenes Buch ("Ohne RAG: KI weiss nur, was sie gelernt hat"), rechts ein offenes Buch ("Mit RAG: KI liest DEIN Material")

**Schlüsseltext:** "Open-Book-Prüfung für die KI"

**Unterstützend (klein):**
- "Die KI liest nicht das Internet"
- "Die KI liest DEIN Dokument"
- "Deshalb funktioniert NotebookLM so gut"

**Sprechernotiz:** "Stellt euch vor, ihr habt eine Prüfung. Ohne Unterlagen — ihr müsst alles aus dem Kopf wissen. Das ist KI normalerweise. Aber RAG — das ist wie eine Open-Book-Prüfung. Ihr gebt der KI EUER Dokument, EUER Video, EUER PDF. Und sie liest es und beantwortet eure Fragen dazu. Die KI googelt nichts — sie liest, was IHR ihr gebt. Deshalb funktioniert NotebookLM so gut: Ihr ladet ein Dokument hoch, und die KI macht einen Podcast daraus. Das ist RAG in Aktion."

---

## GAMMA-Generierungshinweise

**Seitenverhältnis:** 16:9
**Animation:** Minimale Übergänge
**Bildstil:** Illustrativ, Cartoon-artig, fröhlich. Keine Stockfotos.
**Datenvisualisierung:** 7±2 und Richter-Kurve klar und lesbar

**Vermeiden:**
- Stockfotos
- Generische KI-Bilder (Gehirne, Schaltkreise)
- Textlastige Folien
- Englische Begriffe (ausser Fachbegriffe wie "RAG")
- Corporate-dunkle Farben

**Betonen:**
- Cartoon-Illustrationen
- Klare visuelle Hierarchie
- Maximal eine Kernbotschaft pro Folie
- Die Open-Book-Prüfung-Analogie auf Folie 3

---

## Prompt für GAMMA (Kopieren-Einfügen-fertig)

```
Erstelle eine 3-Folien-Präsentation über Informationsflut und RAG für einen lockeren KI-Workshop mit 5 Teilnehmern ohne technischen Hintergrund. Sprache: Deutsch (Schweiz). Stil: Hell, einladend, Cartoon-artig, wenig Text.

Folien:

1. "Dein Gehirn hat ein Limit" — Links: Grosse illustrative "7±2" mit sieben bunten Kreisen die ins Gehirn passen. Rechts: Infografik-Kurve durch den Tag (morgens 65%, nachmittags ~0%) mit Text "Israelische Richter — gleiche Fälle, andere Tageszeit." Schlüsselsatz: "7 Dinge gleichzeitig. Mehr geht nicht. Biologie, nicht Disziplin."

2. "Früher lesen. Heute fragen." — Zwei-Zeilen-Flussdiagramm: Oben durchgestrichen/ausgegraut "Info → Du → Filtern → Vielleicht nutzen" (chaotisch). Unten leuchtend "Frage → KI → Antwort → Handeln" (sauber). Schlüsselsatz: "Nicht mehr lesen. Gezielt fragen."

3. "Die KI liest DEIN Dokument" — Illustration: Person in Prüfung mit offenem Buch, Buch beschriftet "Dein PDF / Dein Video". Vergleich: Geschlossenes Buch = "KI weiss nur was sie gelernt hat" vs. Offenes Buch = "KI liest DEIN Material". Schlüsselsatz: "Open-Book-Prüfung für die KI". Drei Punkte: Die KI liest nicht das Internet. Die KI liest DEIN Dokument. Deshalb funktioniert NotebookLM so gut.

Stil: Helle Farben, Cartoon-Illustrationen, serifenlose Schrift, maximal 15-20 Wörter pro Folie. Keine Stockfotos, keine generischen KI-Gehirn-Bilder, keine dunklen Hintergründe. Fröhlich, einladend, ermutigend.
```
