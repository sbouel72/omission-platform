# OMISSION — Governance Observability Platform

**Welcome → [what's your omission?](https://sbouel72.github.io/omission-platform/omission-platform-welcome.html)**

**Live demo → [Run it now](https://sbouel72.github.io/omission-platform/omission-platform.html)**

**World Report → [31 frameworks ranked by risk delta](https://sbouel72.github.io/omission-platform/world-report.html)** · World current score 51.7 · World risk delta −33.1

**Sample report → [UNCRC 1989 — scored 62/100, Delta +36](https://raw.githubusercontent.com/sbouel72/omission-platform/main/UNCRC-omission-report.txt)**

> The Signature stage — including the UNCRC 1989 reference score — unlocks after you complete an assessment. Run the quiz or upload a document to reach it.

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
|-------|----------------|--------------------------|
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

Local file: Download and open `omission-platform.html`. OpenAI and Gemini work. Claude API requires a local server due to CORS.

Local server:
```
python3 -m http.server 8080
```
Then open: http://localhost:8080/omission-platform.html

---

## Privacy

No account required. No data sent to this site. API keys held in browser memory only.

---

## Licence

See [LICENSE](LICENSE) for full terms. In brief: the source code is MIT licensed (free to use/fork). The scoring methodology and dataset are All Rights Reserved — individual scores may be quoted with attribution; bulk access or applying the methodology requires a written licence. Enquiries: sbouel72@gmail.com

---

## Data & Methodology Usage

The OMISSION scoring methodology and World Scoring Dataset are intellectual property of Shane Bouel. The following apply:

**Free to use (no permission needed):**
Quoting individual scores (e.g. "UNCRC 1989 scored 62/100, Delta +36") in articles, reports, or social posts, with attribution to: *OMISSION Platform (sbouel72.github.io/omission-platform), Shane Bouel, [year].*

**Requires a written licence:**
- Bulk download or redistribution of the dataset
- Applying the OMISSION scoring methodology to additional frameworks for publication or commercial use
- Integrating scores or methodology into third-party tools, research outputs, or products

**To enquire about licensing:** sbouel72@gmail.com

---

## AI Training Resources

The `/AI Training Resources` folder contains the reference documents, scoring instruments, and analytical frameworks that underpin the OMISSION Platform's AI analysis layer and inform its ongoing development toward **OMISSION Platform 2.0** — a full software implementation of the governance observability engine.

The spec defines variables. The rubric makes them codeable. The scoring instrument applies the rubric. The benchmark runs the instrument on real systems. The training pairs are derived from scored cases plus forensic corrections. **Change the rubric and everything downstream re-derives.**

---

### Assessing Assistant Capabilities

A technical and evaluative resource examining how AI assistant systems process, respond to, and reason across complex governance, forensic, and socio-technical tasks. Used to benchmark and calibrate the AI analysis layer within OMISSION's Deep Scan mode — informing how AI providers are prompted, evaluated, and integrated into the scoring pipeline.

**What it does:**
- Establishes capability baselines for selecting and configuring AI providers (Claude, GPT-4o, Gemini) within the platform
- Informs prompt engineering for the Deep Scan AI analysis layer
- Supports quality assurance of evidence-based H and W score outputs
- Provides the evaluative framework for assessing reasoning quality across governance domains

**Used with OMISSION Platform:**
- Feeds directly into Deep Scan provider configuration and prompt architecture
- Supports validation of AI-generated domain scores against rubric standards
- Underpins the AI reasoning and validation architecture planned for OMISSION 2.0

---

### Systems of Representation and Omission Report

The foundational technical and governance specification report authored by Shane Paul Bouel under the Thoughtless Delineation publication framework (June 23, 2026). This document establishes the full conceptual, structural, and engineering blueprint for the OMISSION Platform — covering dialogue management theory, the architecture of institutional omission, legal accountability frameworks, multi-systemic nexus governance, and the cryptographic data schema underpinning the platform's audit ledger.

**What it does:**
- Defines the theoretical architecture of omission as an active mechanism of institutional control — not passive data decay
- Establishes the cross-domain omission framework (biological vs. governance platforms) that drives the 8-domain scoring model
- Specifies the OMISSION cryptographic data schema, Nexus Truth Engine ingestion contract, and Delta Visualizer UI state architecture
- Documents the legal accountability framework under KUH Perdata Article 1365 (Indonesian Civil Code) as a civil liability model for platform omission
- Grounds the platform's World Scoring methodology in forensic sociology and socio-technical governance theory

**Used with OMISSION Platform:**
- Primary source document for the platform's theoretical and scoring foundations
- Core reference for OMISSION 2.0 software development — database design, API contracts, and frontend state management are all specified here
- Provides the definitional basis for `omission_entropy_score`, `liability_exposure_flag`, and the governance omission ledger schema
- Contextualises the platform's adoptee rights and identity erasure focus within international legal and archival frameworks

---

### Validity caveats

- Seed codings are **illustrative**, labelled by `coding_confidence` and `evidence_basis`. They are defensible judgement calls, not authoritative measurements. Real coding requires source documents and at least two coders with an inter-rater agreement check.
- Latent inputs assigned without the rubric produce numerology. The rubric is the gate, not optional.
- Lock one log base per dataset. Mixed bases make `A_g` non-comparable across rows.

### Extending the dataset

- Add cases as new rows in the scoring instrument; benchmark and pairs regenerate from them.
- Add a second coder column and compute inter-rater agreement (Krippendorff's alpha) per variable.
- For multi-group systems, add rows sharing a `system_id`; `B(S)` and recall sum across groups.
- For AutoTrain, convert the JSONL using the `to_text` helper in the td-training-pipeline skill.

### World Scoring Dataset

**** — scored results for 31 governance frameworks across 8 domains, generated by the OMISSION Platform. Four sheets:

- **Master Rankings** — 39 frameworks ranked by Risk Delta; Current Score, True Score, Risk Delta, Blind Spots, Risk Level, Verdict
- **Domain Detail** — per-framework per-domain breakdown: W%, H%, ORI, Status (VISIBLE / ESTIMATED / BLIND SP. / OMITTED)
- **ORI Heatmap** — domain ORI values in wide format for visualisation
- **Summary** — aggregate stats: 39 total documents, avg Current Score 41.5, avg True Score 66.7, avg Risk Delta 25.2

World score (weighted by True Score, 31 valid policy docs): Current **51.7** · True **84.8** · Delta **−33.1**

Use this file to extend the platform, build training pairs from real assessment outputs, or cross-reference with the Adoptee Test scoring instrument.

### Companion pieces

- **Article** (Substack HTML): *"I Named the Silence. Now I Can Measure It."*
- **Report** (Google Doc): *"Even-Handedness Gap Measured (Adoptee Test Instrument)"*
- **Social assets** (Google Doc): thread, LinkedIn, Instagram, Note
- **Framework source**: `ethical-framework-v3.1.tex` (compiles to the v3.1 PDF)
