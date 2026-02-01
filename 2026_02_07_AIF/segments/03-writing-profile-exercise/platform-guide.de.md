# Schreibprofil-Interview: Plattform-Leitfaden

Führen Sie das 100-Fragen-Interview auf Ihrer bevorzugten AI-Plattform durch. Jede hat ihre Vor- und Nachteile.

---

## Schnellvergleich

| Plattform | Ideal für | Speicher | Export | Sitzungslimit |
|-----------|-----------|----------|--------|---------------|
| **Claude Pro** | Workshop-Standard | Projects (persistent) | Kopieren/Download | ~100K Tokens |
| **ChatGPT** | Bestehende Abonnenten | Begrenzter Speicher | Kopieren/Chat exportieren | ~128K Tokens |
| **Perplexity** | Schnelle Sitzungen | Keiner | Nur kopieren | ~32K Tokens |
| **Gemini** | Google-Ökosystem | Keiner | Nur kopieren | ~1M Tokens |

**Empfehlung:** Claude Pro (bester Speicher + Export), ChatGPT (solide Alternative).

---

## 1. Claude (claude.ai)

### Interview starten

**Option A: Projects (Empfohlen)**
1. Gehen Sie zu **Projects** in der linken Seitenleiste
2. Erstellen Sie ein neues Projekt: "Schreibprofil"
3. Fügen Sie den Interview-Prompt in **Project Instructions** ein
4. Starten Sie einen neuen Chat innerhalb des Projekts
5. Vorteil: Prompt bleibt über Sitzungen hinweg erhalten; Sie können morgen fortfahren

**Option B: Standard-Chat**
1. Starten Sie einen neuen Chat
2. Fügen Sie den vollständigen Interview-Prompt ein
3. Beginnen Sie mit der Beantwortung der Fragen
4. Risiko: Bei Sitzungsabbruch verlieren Sie den Kontext

### Tipps
- Verwenden Sie die **Artifacts**-Ansicht, um das kompilierte Profil als formatiertes Dokument zu sehen
- Wenn Claude ein Teilprofil mitten im Interview generiert, bitten Sie um Fortsetzung der Fragen
- Sagen Sie "Kompilieren Sie jetzt das Profil", wenn Sie fertig sind (auch vor 100 Fragen, wenn zufrieden)

### Export
- Klicken Sie auf das Profil-Artifact > **Copy** oder **Download**
- Oder wählen Sie den gesamten Text aus > kopieren Sie in Ihren Markdown-Editor
- Speichern unter: `your-repo/profiles/writing-profile.md`

### Einschränkungen
- Lange Interviews können Kontextlimits erreichen (~100K Tokens)
- Bei Kontextüberlauf: Fortschritt exportieren, neuen Chat starten, "Fortsetzen ab F45" einfügen
- Projects übertragen keine Konversationshistorie, nur Anweisungen

---

## 2. ChatGPT (chat.openai.com / Mobile App)

### Interview starten

**Web:**
1. Klicken Sie auf **New chat**
2. Fügen Sie den Interview-Prompt ein
3. Beginnen Sie mit der Beantwortung

**Mobile App:**
1. Tippen Sie auf **+** für neuen Chat
2. Fügen Sie den Prompt ein (oder nutzen Sie Spracheingabe)
3. Diktieren Sie Antworten für schnellere Fertigstellung

### Tipps
- **Memory-Funktion** (falls aktiviert): ChatGPT merkt sich möglicherweise Fragmente, aber unzuverlässig für vollständige Profile
- Verwenden Sie das **GPT-4o**-Modell (Standard für Plus-Abonnenten)
- Sprachmodus funktioniert gut für natürliche Antworten
- Fordern Sie "Erstelle ein Canvas mit dem Profil" für Seite-an-Seite-Bearbeitung

### Export
- Klicken Sie auf **Share** > **Copy link** (als Referenz)
- Oder kopieren Sie den finalen Profiltext manuell
- Für vollständigen Chat-Export: **Settings** > **Data controls** > **Export data** (dauert Stunden)

### Einschränkungen
- Kein persistenter Projektspeicher wie bei Claude
- Memory-Funktion ist unzuverlässig
- Lange Konversationen können älteren Kontext abschneiden
- Canvas nicht auf Mobile verfügbar

---

## 3. Perplexity (perplexity.ai)

### Interview starten

1. Starten Sie einen neuen **Thread**
2. Fügen Sie den Interview-Prompt ein
3. Hinweis: Perplexity wird versuchen, das Web zu durchsuchen -- sagen Sie "Dies ist ein persönliches Interview, keine Websuche nötig"

### Tipps
- Am besten für schnelle, fokussierte Sitzungen
- Deaktivieren Sie **Pro Search**, um unnötige Web-Lookups zu vermeiden
- Perplexitys Stärke (Recherche) ist hier irrelevant -- Sie nutzen es als Chat-Interface

### Export
- Text manuell kopieren
- Keine native Export-Funktion
- Erwägen Sie: Screenshots wichtiger Abschnitte als Backup

### Einschränkungen
- **Kein Speicher zwischen Sitzungen** -- muss in einer Sitzung abgeschlossen werden
- Kürzeres Kontextfenster (~32K) -- kann bei vollständigen 100 Fragen Schwierigkeiten haben
- Keine Artifacts oder Seitenpanels
- Nicht empfohlen für diese Übung, ausser es ist Ihre einzige Option

---

## 4. Gemini (gemini.google.com)

### Interview starten

1. Gehen Sie zu gemini.google.com
2. Starten Sie eine neue Konversation
3. Fügen Sie den Interview-Prompt ein
4. Wählen Sie **Gemini Advanced** (1.5 Pro) für längeren Kontext

### Tipps
- **Massives Kontextfenster** (1M Tokens) -- kann sehr lange Interviews bewältigen
- Integration mit Google Docs: Bitten Sie Gemini, "Nach Google Docs exportieren" (funktioniert nicht immer)
- Gute Spracheingabe über die Mobile App

### Export
- Kopieren/Einfügen in Google Docs oder Markdown-Datei
- Keine direkte Download-Funktion
- Browser-Drucken-als-PDF als Fallback verwenden

### Einschränkungen
- **Kein Speicher zwischen Sitzungen**
- Kein Projekt-/Ordnersystem
- Antworten können weitschweifig sein -- Sie müssen möglicherweise nach prägnanter Ausgabe fragen
- Formatierung weniger zuverlässig als Claude/ChatGPT

---

## Fehlerbehebung

### "Die AI hat aufgehört, Fragen zu stellen"
Prompt: `"Setzen Sie das Interview ab Frage [X] fort. Wir haben noch [Y] vor uns."`

### "Der Kontext wird zu lang"
1. Bitten Sie um eine Zusammenfassung des aktuellen Fortschritts
2. Kopieren Sie das bisher kompilierte Profil
3. Starten Sie eine neue Sitzung
4. Einfügen: "Setzen Sie dieses Schreibprofil-Interview fort. Hier ist der bisherige Fortschritt: [Profil einfügen]"

### "Antworten werden zu stark zusammengefasst"
Prompt: `"Bewahren Sie meine exakten Worte. Paraphrasieren oder fassen Sie meine Antworten nicht zusammen."`

### "Die AI ist zu höflich / hakt nicht nach"
Prompt: `"Denken Sie daran: Haken Sie bei vagen Antworten nach. Fordern Sie mich heraus. Akzeptieren Sie keine oberflächlichen Antworten."`

---

## Schnellstart-Checkliste

- [ ] Plattform wählen
- [ ] Neuen Chat/Projekt starten
- [ ] Interview-Prompt einfügen
- [ ] 45-60 Minuten blockieren (ungestört)
- [ ] Ehrlich antworten -- die AI kann Sie nicht beurteilen
- [ ] Finales Profil als Markdown exportieren
- [ ] In Ihrem GitHub-Repo speichern

---

## Dateispeicherorte

| Was | Wo |
|-----|-----|
| Interview-Prompt | `input/me-in-a-doc.md` |
| Ihr fertiges Profil | `profiles/writing-profile.md` (erstellen Sie diese) |
| Dieser Leitfaden | `exercises/writing-profile/platform-guide.md` |

---

*Letzte Aktualisierung: 31. Januar 2026*
