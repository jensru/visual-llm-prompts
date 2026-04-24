# visual-llm-prompts

> System prompts that make Claude, ChatGPT, Claude Code, and other LLMs answer with **diagrams, tables, and structured output** instead of prose walls. Built for **designers, visual thinkers, and anyone with dyslexia or a reading difficulty**.

🇩🇪 [Deutsche Version: README.de.md](./README.de.md)

---

## 🎯 The problem in one picture

```
   STANDARD LLM                WITH THESE PROMPTS
   ════════════                ═══════════════════

   📄📄📄📄📄 Prose             🎯 Core message
   📄📄📄📄📄                   • Bullet
   📄📄📄📄📄                   • Bullet
   📄📄📄📄📄                   📊 [Diagram]
   📄📄📄📄📄                   ❓ Does this fit?

        ↓                            ↓

   😵 overwhelmed               😊 grasped
```

---

## 🧠 Why this exists

Designers are the profession with the **highest documented prevalence of dyslexia**. In art and design education up to **4× higher** than in the general population. Individual cohorts reach 30 %. Nearly half of all creative professionals identify as neurodivergent (Understood.org + 4A's, 2025).

Meanwhile every LLM's primary interface is: **text in, text out**.

And the best practice for effective use — reviewing the concept the model proposes before it builds — assumes fluent, fast reading. That's a structural mismatch, and it's barely named in the industry debate.

**Voice input is solved. Reading is the wall.**

These prompts tear down that wall. By making the model output visual, structured, and dialog-oriented — so visual thinkers get answers in the format their brains already prefer.

---

## 📦 What's inside

Five tested system prompts, each in English and German:

| # | Prompt | What it forces | When to use |
|---|--------|----------------|-------------|
| 01 | **Hard / Visual-First** | At least one visual element per answer + few-shot examples | Daily driver, strict output |
| 02 | **Soft / Structured** | Guide rails, structure over prose | First experiment, lightweight |
| 03 | **Mermaid Focus** | Mermaid diagrams for flows, states, architecture | Claude Artifacts, GitHub, Notion |
| 04 | **ASCII User Flows** | ASCII wireframes and flows | Terminal, Claude Code, plain Markdown |
| 05 | **Audio Loop** | TTS-friendly, short sentences, no visual clutter | Voice-in, speech-out workflow |

See [`prompts/en/`](./prompts/en/) and [`prompts/de/`](./prompts/de/) for the full prompt files.

---

## 🚀 Quick start

### 1. Pick a variant

```
  Undecided?           →  02 Soft / Structured
  Visual-heavy daily?  →  01 Hard / Visual-First
  In a Markdown tool?  →  03 Mermaid Focus
  In terminal / CLI?   →  04 ASCII User Flows
  Going hands-free?    →  05 Audio Loop
```

### 2. Paste it where you work

| Environment | Where |
|-------------|-------|
| 🟣 Claude (web) | Settings → Personalization → Custom Instructions |
| 🟢 ChatGPT | Settings → Personalization → Custom Instructions |
| ⚫ Claude Code | Drop into `CLAUDE.md` in your project folder |
| 💬 Single chat | Send as the first message |
| 🟠 Claude Skills | Use as a skill file |

### 3. Test it

Ask the same question before and after. Suggested tests:

- "Explain MVC."
- "How would you structure a login form?"
- "Build me a plan for an onboarding flow with email confirmation."

Notice the difference in how the model answers.

---

## 🎧 Bonus: audio loop

```
   🎤                              🔊
    │                               ▲
    ▼                               │
   ┌─────────────────────────────────┐
   │      🤖  LLM (with prompt)      │
   └─────────────────────────────────┘
    voice in             speech out
    no typing            no reading
```

**Tools:**
- macOS: Select text → `⌥ Esc`
- iOS: Settings → Accessibility → "Speak Screen"
- Pro: ElevenLabs Reader, Speechify
- Voice input: Whisper, Superwhisper, MacWhisper

Combine with prompt `05-audio-loop` for a pure audio workflow.

---

## 📊 Compatibility

| Prompt | Claude Web | ChatGPT | Claude Code CLI | GitHub/Notion | Slack |
|--------|:----------:|:-------:|:---------------:|:-------------:|:-----:|
| 01 Hard | ✅ | ✅ | ⚠️ emojis vary | ✅ | ⚠️ |
| 02 Soft | ✅ | ✅ | ✅ | ✅ | ✅ |
| 03 Mermaid | ✅ | ✅ | ❌ (no render) | ✅ | ❌ |
| 04 ASCII | ✅ | ✅ | ✅ best | ✅ | ✅ |
| 05 Audio | ✅ | ✅ | ⚠️ needs TTS | ✅ | ✅ |

**Rule of thumb:**
- Terminal / CLI environments → **04 ASCII**
- Rendered Markdown tools → **03 Mermaid** or **01 Hard**
- Audio workflow → **05 Audio**
- Not sure yet → **02 Soft**

---

## 🤝 Contributing

These prompts are opinionated starting points. They will get better with feedback from the people who need them most.

**Useful contributions:**
- Report how a variant works with your model / tool
- Suggest a new variant for a specific use case (code review, meeting notes, research summaries)
- Translate to additional languages
- Add screenshots showing before/after outputs

Open an issue or PR. Clear titles help.

---

## 📜 License

MIT — use, remix, share. Attribution appreciated.

---

## ❤️ About

Built by **Jens Rusitschka** at [kick & boost](https://kickboost.io).

I design AI workflows for product teams that actually hold up in real work. Masterclass, workshops, engagements. Design professional for 20+ years. Two sons with their own reading challenges. This topic, I understood before I had to research it.

- 🌐 [kickboost.io](https://kickboost.io)
- 💼 [LinkedIn](https://www.linkedin.com/in/jensrusitschka/)

If these prompts changed how you work with AI, I'd love to hear about it.

---

## 🔖 Keywords

`llm prompts` · `system prompts` · `claude` · `chatgpt` · `claude code` · `dyslexia` · `neurodivergent` · `accessibility` · `visual thinking` · `designers and ai` · `inclusive ai` · `ascii diagrams` · `mermaid diagrams` · `custom instructions` · `prompt engineering`
