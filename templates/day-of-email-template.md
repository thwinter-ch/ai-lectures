# Kursmail-Vorlage — Tag der Vorlesung

Erinnerungsmail am Kurstag mit Link zu den Materialien. Variablen in `{{...}}` ersetzen.

## Variablen

| Variable | Beschreibung | Beispiel |
|----------|-------------|---------|
| `{{kurs_titel}}` | Name des Kurses | KI-Produktivitäts-Hacks |
| `{{datum_zeit}}` | Datum und Uhrzeit | heute Nachmittag (13:00–16:45) |
| `{{repo_url}}` | GitHub-Repository-Link | https://github.com/thwinter-ch/ai-lectures/tree/master/2026_02_07_AIF |
| `{{dozent}}` | Dozent | Thomas Winter |

---

## Vorlage (Deutsch, du-Form)

**Betreff:** {{datum_zeit}}: Materialien & Vorbereitung | {{kurs_titel}}

---

Hallo zusammen,

ich freue mich auf {{datum_zeit}}.

Alle Materialien — Slides, Übungsanleitungen und fertige Prompts zum Kopieren — findest du hier:

**{{repo_url}}**

Die Slides sind in der Ablauf-Tabelle verlinkt. Die Übungen (03, 05, 07) enthalten Schritt-für-Schritt-Anleitungen.

**Bitte vor dem Kurs erledigen, falls noch nicht geschehen:**

- **Notion-Account** erstellen (kostenlos): https://notion.so
- **Claude Pro** abonnieren ($20/Monat): https://claude.ai

Wir bauen heute ein System, bei dem Claude direkt in deine Notion-Datenbank schreibt. Ohne Claude Pro funktioniert das leider nicht. Alternativ geht auch **Perplexity Pro** ($20/Monat). Falls du die Investition nicht tätigen möchtest — kein Problem, du kannst die Übung trotzdem mitverfolgen. Das Abo ist monatlich kündbar.

Bis gleich,
{{dozent}}
