# 🍎 From Zero to a Strategy Explainer Video: Using NotebookLM Like a Product Manager

**Audience:** Anyone — no technical background, no prior PM experience required.
**What you'll walk away with:** A real, finished product strategy document (an "Apple Ecosystem Lock-In" strategy) that you built almost entirely by talking to two free AI tools: **NotebookLM** and **Gemini**.

This repo is a step-by-step replay of a real strategy exercise. Every prompt used is copy-paste ready in the [`/prompts`](./prompts) folder, and every AI response we got back is saved in [`/reference-outputs`](./reference-outputs) so you can compare your results as you go. If something looks different for you, that's fine — AI answers vary slightly each time. The goal is to learn the *process*, not to match the output word-for-word.

📸 **Screenshots:** Wherever you see an image placeholder below (`screenshots/step-X.png`), that's a real screenshot from the NotebookLM notebook used to build this — showing exactly what the screen looked like at that step.

---

## 🔄 The paradigm shift this repo demonstrates

| Era | How strategy used to get made |
|---|---|
| **The Old Way** | Strategy relied on manual research, static financial models, isolated focus groups, and slow, monolithic planning cycles taking months. |
| **The GenAI Era** | Generative AI accelerates the planning phase — synthesizing massive datasets, drafting content, and speeding up ideation. |
| **The Agentic Era** | Autonomous agents execute multi-step plans, interact with live tools, test hypotheses, and output validated recommendations. |

This exercise sits at the GenAI stage of that shift: you'll use **NotebookLM** (for grounded research) and **Gemini** (for strategic reasoning) together, the same two-tool loop strategists use to move from raw information to a boardroom-ready pitch.

---

## 🎯 Your role & the challenge

> **Your role: Product Strategist at Apple.**
> You are tasked with defending Apple's hardware ecosystem from commoditization, as proprietary AI models from competitors threaten to become the primary user interface people rely on.

**The strategic context:** The rapid rise of LLMs from OpenAI, Google, and Microsoft presents a critical shift — hardware runs the risk of becoming commoditized if AI agents bypass traditional operating systems and device-native ecosystems entirely. Apple's counter-bet is **extreme cross-device personalization** built on a **privacy-first, on-device architecture** that cloud-only competitors can't easily replicate.

This workshop simulates how Apple could use integrated local silicon and private cloud infrastructure to build what the strategy calls an **indefensible AI-hardware moat.**

---

## 🧠 Before you start: What even is NotebookLM?

[NotebookLM](https://notebooklm.google.com/) is a free Google tool that works like a research assistant with a photographic memory. Here's the only vocabulary you need:

| Term | What it means |
|---|---|
| **Notebook** | A folder-like workspace where you keep everything related to one project (here: "Apple Strategy") |
| **Source** | Any document you feed it — a PDF, a pasted article, a website link. NotebookLM *only* uses what you give it, so its answers stay grounded in real material instead of making things up |
| **Note** | A piece of text you write or generate inside the notebook (like a sticky note). Notes can themselves be turned into sources for later questions — this is the trick this whole exercise is built on |
| **Report** | A longer, structured write-up NotebookLM generates for you from selected sources/notes |

Full glossary with more terms: [`GLOSSARY.md`](./GLOSSARY.md)

---

## 🗺️ The whole workflow at a glance

```
 1. Perform live Market Research inside NotebookLM. You could alternatively add raw research on 3 companies (sources) manually.
          ↓
 2. Ask 3 strategic questions → save each answer as a Note
          ↓
 3. Turn those 3 Notes into sources → generate one Strategic Comparison Report
          ↓
 4. Hand that Report to Gemini with a role-play prompt → get a full strategy blueprint
          ↓
 5. Ask Gemini to turn the blueprint into a "day in the life" story
          ↓
 6. Feed that story back into NotebookLM as a Note/Source → generate a video overview
```

Six steps. Zero code. Let's go.

---

## Step 1 — Load NotebookLM with raw research (the "sources")

**What you're doing:** Decoding scattered, unstructured information so its opinions are grounded in facts instead of guesses — the same way real strategists work from messy real-world inputs instead of a clean brief.

1. Go to [notebooklm.google.com](https://notebooklm.google.com/) and sign in with any Google account (it's free).
2. Click **New Notebook** and name it something like `Apple Ecosystem Strategy`.
3. Click **Add Source** and upload or paste in 2–3 short recent items — articles, keynote recaps, filings, or Wikipedia sections — covering:
   - **Microsoft** — enterprise Copilot adoption and software pipelines
   - **Google** — Gemini integrations across consumer apps & Workspace
   - **Apple** — Apple Intelligence, on-device chips, and privacy positioning

> 💡 If you don't want to hunt for articles yourself, click **Add Sources**, which opens a pop-up. You can enter the Part 1 prompt from [`01-market-research-questions.md`](./prompts/01-market-research-questions.md), choose the **Web** and **Fast Search/Deep Search** menu options, and press the right-arrow icon in the pop-up to add live sources via Google Search.

![Step 1 - Adding sources to a NotebookLM notebook](./screenshots/step-1-add-sources.png)
*(Screenshot placeholder — add yours here)*

- [ ] I have a notebook with at least 3 sources (one per company)

---

## Step 2 — Ask 3 strategic questions and save each answer as a "Note"

This is the step most people skip — and it's the most important one. Instead of asking one big question, you ask three *focused* questions and **save each answer as a Note**. This turns a simple Q&A tool into a strategy-building tool.

Open the copy-paste-ready prompts here: [`prompts/01-market-research-questions.md`](./prompts/01-market-research-questions.md)

For **each** of the 3 prompts from Part 2 — Prompts:
1. Paste it into NotebookLM's chat box.
2. Read the answer.
3. Click **Save as Note** (or the equivalent "save to notebook" button).
4. Once the saved note is visible, right-click it and select **Save to Source**.
5. Repeat for all 3 prompts — you should end up with 3 separate Notes *and* 3 added sources listed in the left pane alongside your original sources.

![Step 2 - Saving an AI answer as a Note](./screenshots/step-2-save-as-note.png)
*(Screenshot placeholder — add yours here)*

- [ ] I have 3 saved Notes: Compute Philosophy, Ecosystem Vulnerabilities, and a SWOT Matrix

---

## Step 3 — Turn your Notes into a single Market Outlook Report

**What you're doing:** NotebookLM lets you promote a Note into a Source. This means your *own* AI-generated analysis can now be combined with the original research to build something bigger.

1. In your notebook's source list, find the 3 Notes you just created.
2. Select **only** those 3 Notes as active sources (deselect the raw articles for this step).
3. Use NotebookLM's reports feature and ask it to produce a **Market Outlook Report** combining all 3.

![Step 3 - Selecting Notes as sources to generate a report](./screenshots/step-3-generate-report.png)
*(Screenshot placeholder — add yours here)*

- [ ] I generated one combined Market Outlook Report from my 3 Notes

This Report is your evidence base. Everything from here on is opinion and design *built on top of* this evidence — which is exactly how real strategy work is supposed to flow.

---

## Step 4 — Hand the Report to Gemini and ask it to think like a Product Manager

**What you're doing:** Switching tools. NotebookLM is great at grounded research; [Gemini](https://gemini.google.com/) is great at creative, structured thinking. Real strategists move work between tools like this all the time.

1. Copy your Market Outlook Report out of NotebookLM by saving it as a Google Doc, then downloading it.
2. Open [Gemini](https://gemini.google.com/) and paste in the downloaded report as an attachment — this serves as the context for your prompt.
3. Immediately follow it with this prompt (also saved in [`prompts/02-strategy-analysis-prompt.md`](./prompts/02-strategy-analysis-prompt.md)):

```
Act as a Lead Product Manager at Apple. Our strategy is to use Apple
Intelligence to create 'sticky' experiences that require a user to
own an iPhone, an Apple Watch, and a Mac. The AI must act as a
continuous, private context layer across all three.
```

Compare what you get back to our reference run: [`reference-outputs/01-strategic-blueprint.md`](./reference-outputs/01-strategic-blueprint.md)

![Step 4 - Feeding the report into Gemini](./screenshots/step-4-gemini-prompt.png)
*(Screenshot placeholder — add yours here)*

- [ ] I have a full strategy blueprint back from Gemini (it should include product pillars, architecture ideas, and a "why users won't leave" argument)

---

## Step 5 — Turn the strategy into a story a whole team could understand

**What you're doing:** A wall of strategy bullet points doesn't convince anyone. A *story* does. This is how PMs pitch ideas to non-technical stakeholders and executives.

Paste this follow-up into the same Gemini conversation (also in [`prompts/03-day-in-the-life-prompt.md`](./prompts/03-day-in-the-life-prompt.md)):

```
Design a specific, day-in-the-life user journey for a busy
professional. Show me a seamless AI-driven workflow that starts on
the Apple Watch in the morning, transitions to the Mac during the
workday, and ends on the iPhone at night. The workflow should involve
managing an unexpected flight cancellation and rescheduling meetings.
Highlight exactly how the 'On-Device Context' makes this better than
a generic cloud AI.
```

Compare your story to our reference run: [`reference-outputs/02-day-in-the-life-journey.md`](./reference-outputs/02-day-in-the-life-journey.md) — ours follows "Sarah, VP of Product" through a cancelled flight, from Watch → Mac → iPhone.

**Optional stress-test follow-up** — push your own idea further:

```
Critique this workflow. If a competitor (like Google on Android)
tried to copy this, what specific Apple hardware integration makes
ours impossible to replicate perfectly?
```

![Step 5 - Gemini's day-in-the-life story](./screenshots/step-5-day-in-life-story.png)
*(Screenshot placeholder — add yours here)*

- [ ] I have a full narrative walking through morning → workday → evening
- [ ] I identified one specific hardware integration a competitor couldn't easily copy

---

## Step 6 — Close the loop: turn your story into a video overview

**What you're doing:** Bringing your finished thinking back into NotebookLM, which can turn a Note into a short narrated video/audio overview — a genuinely useful way to share strategy work with people who'd rather watch than read.

1. Copy Gemini's day-in-the-life story.
2. Paste it into your NotebookLM notebook as a new **Note**.
3. Save that Note as a **Source**.
4. Use NotebookLM's **video overview** (or **audio overview**) feature on that source.

![Step 6 - Generating a video overview in NotebookLM](./screenshots/step-6-video-overview.png)
*(Screenshot placeholder — add yours here)*

- [ ] I generated a video or audio overview of my finished strategy story

---

## 🏛️ Boardroom discussion

Once you've finished, sit with this question — it's the one this exercise is actually testing:

> **How does generating a concrete, multi-device user journey change the way you'd argue for a high-level corporate strategy in a boardroom?**

Real strategy pitches don't win on abstract market definitions. They win when you can force alignment around something specific and hard to dismiss — in this case, an indefensible hardware-software integration story that a competitor genuinely can't copy.

---

## 🏁 What you just proved to yourself

In under an hour, with no coding and no formal PM training, you:
1. Turned scattered raw research into structured evidence
2. Combined AI-generated analysis with real sources (a technique real strategists use constantly)
3. Produced a full strategic blueprint
4. Translated that blueprint into a story non-technical stakeholders could actually follow
5. Packaged it into a shareable video

That entire loop — **research → synthesize → analyze → storytell → package** — is the actual day-to-day work of product strategy. The tools just made it fast.

---

## 📁 What's in this repo

```
notebooklm-pm-strategy-walkthrough/
├── README.md                 ← you are here
├── GLOSSARY.md                ← plain-English definitions of every tool/term used
├── CHECKLIST.md                ← one-page tracker of all 6 steps
├── prompts/                   ← every copy-paste-ready prompt, in order
└── reference-outputs/          ← the actual AI responses from our run-through, for comparison
```

## 🙋 Adding your own scenarios

---

Want to try this same 6-step loop on a different company or product? Swap Step 1's sources for a different set of competitors and re-run the exact same prompts — that's the whole point of a repeatable strategy process.
