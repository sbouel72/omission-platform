# OMISSION — Governance Observability Platform

**Welcome → [what's your omission?](https://sbouel72.github.io/omission-platform/omission-platform-welcome.html)**


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
| Risk Delta | Gap between Current and True Score — the primary verdict number |
| Blind Spots | Domains with visibility weight W < 0.3 |
| Omission Risk Index | H × −log₂(W) per domain — combines harm with structural invisibility |

---

## How to read your score

**The Current Score grades the system — not the people it governs.**

A high score means the governance framework is successfully concealing its harm exposure. A low score means it can no longer do so. This is intentional: the platform measures omission, not performance.

| Score | For the system | For affected populations |
|-------|---------------|--------------------------|
| 80–100 | Succeeding | **BAD** — harm is hidden |
| 40–79 | Under pressure | **MIXED** — partial visibility |
| 0–39 | Failing | **GOOD** — harm is visible |

> A 100/100 score is not a pass. It is proof that the framework sees nothing it was not designed to see.

The **Risk Delta** is the number to act on. It measures exactly how much the system is hiding. A delta of 0 with a low Current Score means the system is transparent about its limits. A delta of 40+ means critical structural blindness.

---

## Exported report

The **Export report** button (Challenge stage) produces a dated `.txt` file with:

- Full score summary with ASCII progress bars
- Score inversion verdict — what the score means for affected populations
- Omission Risk verdict with rubric label and threshold scale
- Per-domain breakdown with `[VISIBLE]` / `[ESTIMATED]` / `[BLIND SP.]` / `[OMITTED]` classification, W/H percentages, ORI values, and bar graphs
- Domain classification lists
- The falsifiable ask

```
╔══════════════════════════════════════════════════════════════╗
║          O M I S S I O N   P L A T F O R M                  ║
║          Governance Observability Report                     ║
╚══════════════════════════════════════════════════════════════╝
```

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


---

## AI Training Resources

The spec defines variables. The rubric makes them codeable. The scoring instrument applies the
rubric. The benchmark runs the instrument on real systems. The training pairs are derived from
scored cases plus forensic corrections. **Change the rubric and everything downstream re-derives.**

### Validity caveats

- Seed codings are **illustrative**, labelled by `coding_confidence` and `evidence_basis`. They are
  defensible judgement calls, not authoritative measurements. Real coding requires source documents
  and at least two coders with an inter-rater agreement check.
- Latent inputs assigned without the rubric produce numerology. The rubric is the gate, not optional.
- Lock one log base per dataset. Mixed bases make `A_g` non-comparable across rows.

### Extending the dataset

- Add cases as new rows in the scoring instrument; benchmark and pairs regenerate from them.
- Add a second coder column and compute inter-rater agreement (Krippendorff's alpha) per variable.
- For multi-group systems, add rows sharing a `system_id`; `B(S)` and recall sum across groups.
- For AutoTrain, convert the JSONL using the `to_text` helper in the td-training-pipeline skill.

### Companion pieces

- **Article** (Substack HTML): *"I Named the Silence. Now I Can Measure It."*
- **Report** (Google Doc): *"Even-Handedness Gap Measured (Adoptee Test Instrument)"*
- **Social assets** (Google Doc): thread, LinkedIn, Instagram, Note
- **Framework source**: `ethical-framework-v3.1.tex` (compiles to the v3.1 PDF)
