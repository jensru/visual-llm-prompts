# visual-llm-prompts

> System-Prompts, die Claude, ChatGPT, Claude Code und andere LLMs dazu bringen, mit **Diagrammen, Tabellen und strukturiertem Output** zu antworten statt mit Prosa-Wänden. Gebaut für **Designer, visuell denkende Menschen und alle mit Legasthenie oder Leseschwäche**.

🇬🇧 [English version: README.md](./README.md)

---

## 🎯 Das Problem in einem Bild

```
   STANDARD-LLM                MIT DIESEN PROMPTS
   ════════════                ═══════════════════

   📄📄📄📄📄 Prosa             🎯 Kernaussage
   📄📄📄📄📄                   • Bullet
   📄📄📄📄📄                   • Bullet
   📄📄📄📄📄                   📊 [Diagramm]
   📄📄📄📄📄                   ❓ Passt das?

        ↓                            ↓

   😵 überfordert               😊 erfasst
```

---

## 🧠 Warum es das gibt

Designer sind die Berufsgruppe mit der **höchsten Prävalenz von Legasthenie**. In Kunst- und Designausbildung bis zu **4× so häufig** wie in der Allgemeinbevölkerung. Einzelne Kohorten erreichen 30 %. Fast die Hälfte aller Kreativprofis identifiziert sich als neurodivergent (Understood.org + 4A's, 2025).

Gleichzeitig ist das primäre Interface zu jedem LLM: **Text rein, Text raus**.

Und die beste Nutzung, die zuverlässig funktioniert, setzt flüssiges, schnelles Lesen voraus: Konzepte prüfen, bevor die KI baut. Das ist ein strukturelles Mismatch und wird in der Debatte fast nie benannt.

**Voice rein ist gelöst. Lesen ist die Bremse.**

Diese Prompts reißen die Bremse raus. Sie zwingen das Modell, visuell, strukturiert und dialogisch zu antworten, damit visuell Denkende Antworten im Format bekommen, das ihr Gehirn ohnehin bevorzugt.

---

## 📦 Was drin ist

Fünf getestete System-Prompts, jeweils auf Englisch und Deutsch:

| # | Prompt | Was erzwungen wird | Wann nutzen |
|---|--------|---------------------|-------------|
| 01 | **Hart / Visuell-First** | Mindestens ein visuelles Element pro Antwort + Few-Shot-Beispiele | Daily Driver, strenger Output |
| 02 | **Weich / Strukturiert** | Leitplanken, Struktur statt Prosa | Erstes Experiment, lightweight |
| 03 | **Mermaid-Fokus** | Mermaid-Diagramme für Flows, States, Architektur | Claude Artifacts, GitHub, Notion |
| 04 | **ASCII-UserFlows** | ASCII-Wireframes und Flows | Terminal, Claude Code, plain Markdown |
| 05 | **Audio-Loop** | TTS-freundlich, kurze Sätze, keine visuellen Störer | Voice-in, Sprache-out Workflow |

Die vollständigen Prompt-Files in [`prompts/de/`](./prompts/de/) und [`prompts/en/`](./prompts/en/).

---

## 🚀 Schnellstart

### 1. Variante wählen

```
  Unsicher?                →  02 Weich / Strukturiert
  Visuell-heavy täglich?   →  01 Hart / Visuell-First
  In Markdown-Tool?        →  03 Mermaid-Fokus
  In Terminal / CLI?       →  04 ASCII-UserFlows
  Hands-free?              →  05 Audio-Loop
```

### 2. Einkleben wo du arbeitest

| Umgebung | Wo |
|----------|-----|
| 🟣 Claude (Web) | Einstellungen → Personalisierung → Custom Instructions |
| 🟢 ChatGPT | Einstellungen → Personalisierung → Custom Instructions |
| ⚫ Claude Code | In `CLAUDE.md` im Projekt-Ordner |
| 💬 Einzelchat | Als erste Nachricht schicken |
| 🟠 Claude Skills | Als Skill-File |

### 3. Testen

Stell dieselbe Frage vorher und nachher. Test-Vorschläge:

- "Erklär mir MVC."
- "Wie würdest du ein Login-Formular strukturieren?"
- "Baue mir einen Plan für einen Onboarding-Flow mit Email-Bestätigung."

Du wirst den Unterschied spüren.

---

## 🎧 Bonus: Audio-Loop

```
   🎤                              🔊
    │                               ▲
    ▼                               │
   ┌─────────────────────────────────┐
   │      🤖  LLM (mit Prompt)       │
   └─────────────────────────────────┘
    Sprache rein           Sprache raus
    kein Tippen            kein Lesen
```

**Tools:**
- macOS: Text markieren → `⌥ Esc`
- iOS: Einstellungen → Bedienungshilfen → "Bildschirm sprechen"
- Pro: ElevenLabs Reader, Speechify
- Voice-Input: Whisper, Superwhisper, MacWhisper

Kombiniert mit Prompt `05-audio-loop` für einen reinen Audio-Workflow.

---

## 📊 Kompatibilität

| Prompt | Claude Web | ChatGPT | Claude Code CLI | GitHub/Notion | Slack |
|--------|:----------:|:-------:|:---------------:|:-------------:|:-----:|
| 01 Hart | ✅ | ✅ | ⚠️ Emojis variieren | ✅ | ⚠️ |
| 02 Weich | ✅ | ✅ | ✅ | ✅ | ✅ |
| 03 Mermaid | ✅ | ✅ | ❌ (kein Render) | ✅ | ❌ |
| 04 ASCII | ✅ | ✅ | ✅ beste Wahl | ✅ | ✅ |
| 05 Audio | ✅ | ✅ | ⚠️ externe TTS | ✅ | ✅ |

**Faustregel:**
- Terminal / CLI → **04 ASCII**
- Gerenderte Markdown-Tools → **03 Mermaid** oder **01 Hart**
- Audio-Workflow → **05 Audio**
- Unsicher → **02 Weich**

---

## 🤝 Mitmachen

Diese Prompts sind opinionated Startpunkte. Sie werden besser mit Feedback von den Leuten, die sie am meisten brauchen.

**Nützliche Beiträge:**
- Berichten, wie eine Variante mit deinem Modell / Tool läuft
- Neue Variante vorschlagen für einen spezifischen Use Case (Code-Review, Meeting-Notes, Research-Summaries)
- Übersetzung in weitere Sprachen
- Screenshots mit Vorher/Nachher-Output

Issue oder PR öffnen. Klare Titel helfen.

---

## 📜 Lizenz

MIT. Nutzen, remixen, teilen. Attribution wird geschätzt.

---

## ❤️ Über den Autor

Gebaut von **Jens Rusitschka** bei [kick & boost](https://kickboost.io).

Ich baue AI-Workflows für Produktteams, die im echten Arbeiten tragen. Masterclass, Workshops, Begleitung. Teil der Design-Community seit 20 Jahren, eigene Erfahrungen mit Schreibschwächen. Dieses Thema hab ich verstanden, bevor ich es überhaupt recherchieren musste.

- 🌐 [kickboost.io](https://kickboost.io)
- 💼 [LinkedIn](https://www.linkedin.com/in/jensrusitschka/)

Wenn diese Prompts verändert haben, wie du mit KI arbeitest, würde ich es gern hören.

---

## 🔖 Keywords

`llm prompts` · `system prompts` · `claude` · `chatgpt` · `claude code` · `legasthenie` · `dyslexie` · `neurodivergent` · `barrierefrei` · `visuelles denken` · `designer und ki` · `inclusive ai` · `ascii diagramme` · `mermaid` · `custom instructions` · `prompt engineering`
