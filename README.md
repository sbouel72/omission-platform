# OMISSION — Governance Observability Platform

**Live demo → [Run it now](https://sbouel72.github.io/omission-platform/omission-platform.html)**

A self-contained, browser-based tool that measures what governance frameworks say they cover versus what decision-makers actually see — and surfaces the gap as a quantified risk.

No installation. No backend. No data leaves your browser.

---

## What problem does this solve?

Most governance assessments ask: "Do you have a policy for X?"

OMISSION asks a harder question: "Even if the policy exists — how visible is it to the people who need it?"

A risk that exists but is not seen is an omission. This platform measures the structural gap between documented coverage (H) and actual visibility (W) across 8 governance domains — and turns that gap into an auditable score.

---

## The two assessment modes

### Quick Assessment (10 minutes)
Rate each of the 8 domains yourself:
- H — Harm potential (0-1): How badly could this domain harm the organisation if it fails?
- W — Visibility weight (0.01-1): How well do decision-makers actually see this domain risks?

### Deep Scan — AI Analysis
Upload governance documents and an AI model reads them, returning evidence-based H and W scores per domain.

---

## Scoring

| Output | What it means |
|--------|---------------|
| Current Score | Governance health as perceived by decision-makers (0-100) |
| True Score | Governance health based on actual harm potential (0-100) |
| Risk Delta | Gap between Current and True Score |
| Omission Risk Index | 0-100 index of risk hiding in blind spots |

---

## The 8 domains

Identity, Process, Data, Risk, Compliance, Ethics, Oversight, Continuity

---

## AI providers (Deep Scan)

| Provider | Model | Key |
|----------|-------|-----|
| Claude (Anthropic) | claude-3-5-sonnet | console.anthropic.com |
| GPT-4o (OpenAI) | gpt-4o | platform.openai.com |
| Gemini (Google) | gemini-1.5-flash | aistudio.google.com |

---

## Running it

GitHub Pages (recommended): Use the live demo link above. All three AI providers work, no setup needed.

Local file: Download and open omission-platform.html. OpenAI and Gemini work. Claude API requires a local server due to CORS.

Local server:
  python3 -m http.server 8080
Then open: http://localhost:8080/omission-platform.html

---

## Privacy

No account required. No data sent to this site. API keys held in browser memory only.

---

MIT Licence
