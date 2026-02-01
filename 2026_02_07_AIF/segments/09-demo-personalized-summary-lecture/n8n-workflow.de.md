# n8n Workflow: Personalisierter Zusammenfassungs-Agent

## Workflow-Diagramm

```mermaid
flowchart TD
    subgraph TRIGGER["1. TRIGGER"]
        A[Manueller Trigger] --> B{Input-Quelle}
        A2[Geplanter Trigger] --> B
    end

    subgraph INPUT["2. INPUT"]
        B --> C[Meeting-Transkript]
        B --> C2[Dokument-Upload]
        C --> D[Text-Extraktion]
        C2 --> D
    end

    subgraph CONTEXT["3. KONTEXT ABRUFEN"]
        D --> E[Notion: Benutzerprofil abrufen]
        E --> F[Benutzer-Präferenzen]
        F --> F1[Zusammenfassungsstil]
        F --> F2[Fokusgebiete]
        F --> F3[Sprache/Ton]
    end

    subgraph MERGE["4. MERGE"]
        D --> G[Kontext kombinieren]
        F1 --> G
        F2 --> G
        F3 --> G
        G --> H[Prompt-Template erstellen]
    end

    subgraph AI["5. AI AGENT"]
        H --> I[Claude/GPT Node]
        I --> J{Qualitätsprüfung}
        J -->|Bestanden| K[Strukturierter Output]
        J -->|Fehlgeschlagen| I
    end

    subgraph OUTPUT["6. OUTPUT"]
        K --> L[Notion: Seite erstellen]
        K --> M{E-Mail aktiviert?}
        M -->|Ja| N[E-Mail senden]
        M -->|Nein| O[Ende]
        L --> O
        N --> O
    end

    style TRIGGER fill:#e1f5fe
    style INPUT fill:#fff3e0
    style CONTEXT fill:#f3e5f5
    style MERGE fill:#e8f5e9
    style AI fill:#fff8e1
    style OUTPUT fill:#fce4ec
```

---

## Node-Referenz

| # | Node | Zweck | Wichtige Konfiguration |
|---|------|-------|------------------------|
| 1 | **Trigger** | Startet den Workflow | Manueller Button oder Cron-Zeitplan |
| 2 | **Input** | Empfängt Rohinhalte | Webhook, Datei-Upload oder Einfügen |
| 3 | **Notion Get** | Ruft Benutzerprofil ab | Datenbank-ID + Benutzer-ID-Filter |
| 4 | **Merge** | Kombiniert Transkript + Präferenzen | Expression: `{{ $json.transcript }}` + `{{ $('Notion').item.json }}` |
| 5 | **AI Agent** | Verarbeitet mit LLM | System-Prompt mit Persona + Benutzer-Präferenzen |
| 6a | **Notion Create** | Schreibt Zusammenfassung | Zieldatenbank + Property-Mapping |
| 6b | **Email** | Optionale Benachrichtigung | Bedingt durch Benutzerpräferenz |

---

## Konfigurationshinweise

### Notion-Integration
```
Erforderliche Datenbank-Properties:
- Title (text)
- Summary (rich_text)
- Source (select)
- Created (date)
- User (relation)
```

### AI Agent Prompt-Struktur
```
SYSTEM: Sie sind ein Zusammenfassungs-Assistent. Passen Sie Ihren Output an:
- Stil: {{ $json.user.summary_style }}
- Fokus: {{ $json.user.focus_areas }}
- Länge: {{ $json.user.preferred_length }}

USER: Fassen Sie dieses Transkript zusammen:
{{ $json.transcript }}
```

### Fehlerbehandlung
- Wiederholungsschleife am AI-Node (max. 2 Versuche)
- Fallback: Rohes Transkript schreiben, falls AI versagt
- Logging: Alle Läufe in separater Notion-DB speichern

---

## Warum dieses Pattern funktioniert

1. **Trennung der Verantwortlichkeiten** - Benutzer-Präferenzen leben in Notion, nicht hartcodiert
2. **Wiederverwendbar** - Derselbe Workflow verarbeitet jeden Dokumenttyp
3. **Auditierbar** - Jede Zusammenfassung mit Quellenreferenz gespeichert
4. **Erweiterbar** - Slack, Teams oder Webhook-Outputs einfach hinzufügen

---

*Für GAMMA-Folien: Das Mermaid-Diagramm als Visual verwenden, die Tabelle als Sprechernotizen.*
