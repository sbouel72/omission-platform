# OMISSION Platform 2.2.1

**Live demo → [Run it now](https://sbouel72.github.io/omission-platform/)**

A self-contained, browser-based tool that measures what governance frameworks say they cover versus what decision-makers actually see — and surfaces the gap as a quantified risk.

No installation. No backend. No data leaves your browser.

---

## Pages

| File | Role |
| :--- | :--- |
| [index.html](https://github.com/sbouel72/omission-platform/blob/main/index.html) | Landing page — explainer, scored UNCRC sample, methodology overview |
| [omission-platform-welcome.html](https://github.com/sbouel72/omission-platform/blob/main/omission-platform-welcome.html) | Canonical alias — redirects to index.html |
| [omission-platform.html](https://github.com/sbouel72/omission-platform/blob/main/omission-platform.html) | Core assessment tool — 7-stage flow, Quick Assessment, Deep Scan AI |
| [world-report.html](https://github.com/sbouel72/omission-platform/blob/main/world-report.html) | World Report 2026 — compare your score against 31 frameworks across 16 jurisdictions |
| [nexus-observatory.html](https://github.com/sbouel72/omission-platform/blob/main/nexus-observatory.html) | Pattern Observatory — systemic domain-level omission rankings across 39 frameworks |

---

## The OMISSION Standard

The **OMISSION Standard** is the theoretical and operational backbone of this Platform. It provides the epistemological framework, domain definitions, proxy indicators, scoring methodology, and evidentiary weighting rules that underpin the Platform's H×W scoring model.

| Version | Status | Document |
| :--- | :--- | :--- |
| **v2.2.1** | ✅ **Current active standard** | [OMISSION_Standard_v2.2.1.docx](./OMISSION_Standard_v2.2.1.docx) |
| v2.2 | Superseded | [OMISSION_Standard_v2.2.docx](./OMISSION_Standard_v2.2.docx) |
| v2.1 | Superseded | [OMISSION_Standard_v2.1.docx](./OMISSION_Standard_v2.1.docx) |

**v2.2.1 patch notes:** Aggregate weighting formula made explicit for non-Platform auditors. Platform sync protocol now names the responsible maintainer and notification mechanism.

**v2.2 release notes:** Domain taxonomy shifted from institutional accountability domains to the eight survivor-centred rights domains used by the Platform. Process, Compliance, and Oversight reclassified as cross-cutting audit infrastructure. Scoring outputs (Visibility Deficit H, Disclosure Score W, Omission Risk Index H×(1−W)) fully aligned with Platform formula.

---

## What problem does this solve?

Most governance assessments ask: "Do you have a policy for X?"

OMISSION asks a harder question: "Even if the policy exists — how visible is it to the people who need it?"

A risk that exists but is not seen is an omission. This Platform measures the structural gap between documented coverage (H) and actual visibility (W) across 8 governance domains — and turns that gap into an auditable score.

---

## The two assessment modes

### Quick Assessment (10 minutes)

Rate each of the 8 domains yourself:

- **H** — Harm potential (0–1): How badly could this domain harm the people it governs if it fails?
- - **W** — Visibility weight (0.01–1): How well do decision-makers actually see this domain's risks?
 
  - ### Deep Scan — AI Analysis
 
  - Upload governance documents and an AI model reads them, returning evidence-based H and W scores per domain. For fully evidenced scores, use the OMISSION Standard v2.2.1 to conduct an auditor-verified assessment — the Standard produces H and W scores per domain that import directly into the Platform.
 
  - ---

  ## Scoring

  | Output | What it means |
  | :--- | :--- |
  | **Visibility Deficit (H)** | Harm potential per domain — what the institution is not disclosing or not seeing (0–1) |
  | **Disclosure Score (W)** | How well the institution makes risks visible to decision-makers (0.01–1) |
  | **Omission Risk Index** | H × (1−W) — risk hiding in blind spots per domain |
  | **Current Score** | Governance health as perceived by decision-makers (0–100) |
  | **True Score** | Governance health based on actual harm potential (0–100) |
  | **Risk Delta** | Gap between Current and True Score |

  **Aggregate Score formula:**

  ```
  Aggregate Score = Σ(Domain_Score_d × H_d) / Σ(H_d)

  Where: Domain_Score_d = 100 − (H_d × (1 − W_d) × 100)
  ```

  ---

  ## The 8 domains

  | Domain | What It Protects |
  | :--- | :--- |
  | **Identity Continuity** | The right to know and maintain one's own name, origin, and legal identity |
  | **Family Integrity** | The right to preserve family relationships and connections |
  | **Cultural Continuity** | The right to retain access to language, culture, and community |
  | **Information Rights** | The right to access records and decisions concerning oneself |
  | **Agency** | The right to participate meaningfully in decisions affecting oneself |
  | **Consent** | The right to informed, voluntary, and ongoing agreement |
  | **Self-Determination** | The right to shape the rules and policies that govern one's life |
  | **Memory Preservation** | The right to an accurate, accessible, and complete historical record |

  ---

  ## AI providers (Deep Scan)

  | Provider | Model | Key |
  | :--- | :--- | :--- |
  | Claude (Anthropic) | claude-opus-4-6 (recommended) · claude-sonnet-4-6 (fast) | console.anthropic.com |
  | GPT-4o (OpenAI) | gpt-4o | platform.openai.com |
  | Gemini (Google) | gemini-1.5-flash | aistudio.google.com |

  ---

  ## Running it

  **GitHub Pages (recommended):** Use the live demo link above.

  **Local server:**
  ```
  python3 -m http.server 8080
  ```
  Then open: http://localhost:8080/omission-platform.html

  ---

  ## Privacy

  No account required. No data sent to this site. API keys held in browser memory only.

  ---

  MIT Licence
