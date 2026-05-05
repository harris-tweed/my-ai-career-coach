# My AI Career Coach

A personal career coach that runs locally on your computer, powered by Claude. It learns who you are, remembers your sessions, and gets more useful over time — without any of your data leaving your machine.

---

## Prerequisites

- **A Claude subscription** — [claude.ai/upgrade](https://claude.ai/upgrade). The Pro plan is sufficient.
- **Claude Code** — Anthropic's CLI that lets Claude work with files on your computer. Install it by running:
  ```bash
  npm install -g @anthropic-ai/claude-code
  ```
  Full installation guide: [docs.anthropic.com/claude-code](https://docs.anthropic.com/en/docs/claude-code/getting-started)
- **Node.js 18+** — required by Claude Code. Download from [nodejs.org](https://nodejs.org).
- Basic comfort with a terminal.

---

## Setup

**1. Clone this repository**

```bash
git clone https://github.com/harris-tweed/my-ai-career-coach.git
cd my-ai-career-coach
```

**2. Create the folder structure**

```bash
mkdir -p sessions context skills
```

- `sessions/` — one file per coaching session, written automatically
- `context/` — documents you share with your coach (assessments, reviews, etc.)
- `skills/` — optional session-type guides you can add over time

**3. Start Claude Code in the project folder**

```bash
claude
```

That's it. The coach will take it from there.

---

## First session

When you open the project for the first time, the coach will:

1. **Brief you** on how the coaching relationship works — what to expect, how sessions are structured, how memory works.
2. **Ask you to share documents** — anything you'd give a human coach: personality assessments (DiSC, Myers-Briggs, Gallup, etc.), performance reviews, peer feedback, a CV, a LinkedIn export. Drop files into the `context/` folder and the coach will read them.
3. **Fill gaps with questions** — if documents don't cover everything, the coach will ask a small number of targeted questions.
4. **Generate your setup** — it writes two files tailored to you: `coach.md` (the coach's persona and approach) and `me.md` (your profile). You can review and edit both.

After that, every session picks up from where the last one ended.

---

## Day-to-day use

Open a session any time by running `claude` from the project folder. The coach will read your recent session summaries and open with something relevant.

Bring something real — a situation you're navigating, a decision you're sitting with, a pattern you've noticed. This works best as a thinking space, not a status update.

To end a session, say *"let's close"* or *"wrap up"* and the coach will close cleanly and write a summary.

---

## Your data

Everything stays on your computer. Session notes, documents, your profile — all of it lives in this folder as plain markdown files. Nothing is sent to an external service or stored anywhere outside your machine. You can read, edit, or delete any file at any time.

---

## Adding context over time

Drop files into `context/` whenever you want — a new performance review, an org chart, stakeholder notes. The coach will draw on them when relevant and can dive into them in more detail when a session calls for it.

---

## Customising your coach

Once set up, your coach lives in `coach.md`. You can edit it directly if you want to adjust the tone, add something you've learned about how you work best, or rename your coach. `me.md` is your profile — keep it current as your situation evolves.
