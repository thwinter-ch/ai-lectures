# Templates

Operative Vorlagen fuer die Vorlesungslogistik. Dozenten-seitig, nicht fuer Teilnehmende.

Fuer Uebungen und Prompts siehe [practices/](../practices/).

## Verfuegbare Vorlagen

| Vorlage | Zweck | Versand via |
|---------|-------|-------------|
| [prereqs-email-template.md](prereqs-email-template.md) | Vorbereitungs-E-Mail mit Voraussetzungen (DE/EN) | n8n oder manuell |
| [day-of-email-template.md](day-of-email-template.md) | Erinnerung am Kurstag mit Materialien-Link | n8n oder manuell |

## Variablen-Konvention

Alle Vorlagen verwenden `{{variable}}` Platzhalter:
- `{{name}}` -- Teilnehmer-Vorname
- `{{session_title}}` -- Kurstitel
- `{{session_date}}` -- Datum
- `{{session_time}}` -- Uhrzeit
- `{{repo_url}}` -- GitHub-Link zu den Materialien
- `{{instructor_names}}` -- Dozentennamen
