# 🛡️ Risk2Safe — Incident Investigation Workbench

A **single-file web application** for safety professionals to conduct structured incident
investigations: build a **SnapCharT®-style timeline**, identify **Causal Factors** with
**barrier/safeguard analysis**, drill into **root causes** with the full guided questionnaire
(7 Basic Cause Categories + Equipment Difficulty + the 15-Question Human Performance
Troubleshooting Guide), classify human factors with **DoD HFACS 8.0** (active vs latent
failures), develop **SMARTER corrective actions** (with per-row AI suggestions, AI
consolidation, and Excel export), and produce a formal 8-section **investigation report** —
with optional **AI review at every step** powered by your own OpenAI API key.

> Methodology concepts referenced: SnapCharT®, Root Cause Tree®, TapRooT® are registered
> trademarks of System Improvements, Inc. DoD HFACS 8.0 per U.S. Department of Defense
> documentation. This tool is an independent aid for internal use — refer to the official
> sources and training for authoritative guidance.

---

## ✨ Workflow (7 color-coded tabs)

| # | Tab | What you do |
|---|------|-------------|
| 1 | **Plan** (teal) | Incident facts, evidence preservation, interview plan |
| 2 | **SnapCharT®** (blue) | Timeline of Events before & after the Incident, Conditions attached, dashed = unproven |
| 3 | **Causal Factors** (orange) | Mark problems, 4-Step "So what?" method, promote to ▲ CFs **+ Barrier analysis** (failed / not present / success) |
| 4 | **Root Causes** (purple) | Per CF: Level-1 → 15 Questions → categories → near-root → root causes with dictionary questions |
| 5 | **HFACS** (raspberry) | DoD HFACS 8.0: Unsafe Acts (active failures) → Preconditions → Supervision → Organizational influences (latent failures), 100 nanocodes with definitions |
| 6 | **Corrective Actions** (green) | Auto row per root cause, per-row 🤖 AI Suggest, AI Consolidate similar actions, ⬇ Excel tracker download |
| 7 | **Report** (slate) | Formal report; print or save as PDF |

## 📑 Report format

1. Executive Summary *(editable + AI draft)*
2. Incident Details
3. Incident Findings (sequence of events & problems)
4. Barrier Analysis — failed / not present / success
5. Active and Latent Failures (DoD HFACS 8.0)
6. Root Causes
7. Recommended Actions
8. Sustainability Analysis of the Recommendations *(editable + AI draft)*

## 🚀 Launch on GitHub Pages (free hosting)

1. Create a repository on github.com (e.g. `risk2safe`).
2. Upload **`index.html`** and **`README.md`** to the repository root.
3. **Settings → Pages** → Source: *Deploy from a branch* → Branch **main**, folder **/(root)** → Save.
4. Your app goes live at `https://<your-username>.github.io/risk2safe/` in ~1 minute.

Runs locally too — just open `index.html` in a browser. Everything works offline except the
AI features and the first Excel download (loads the SheetJS engine from CDN; falls back to CSV offline).

## 🤖 AI features (optional — bring your own OpenAI key)

Click **🤖 AI setup** → paste an API key from platform.openai.com (billing enabled).
Default model `gpt-4o-mini`. The key lives only in your browser's localStorage and is sent
only to api.openai.com.

- **AI Review** buttons on all 7 tabs (plan completeness, SnapCharT gaps, CF selection,
  root-cause consistency, HFACS tier coverage, SMARTER scoring, end-to-end report check)
- **Per-row action suggestions** and **consolidation of similar actions** in tab 6
- **AI draft** buttons for the Executive Summary and the Sustainability Analysis in tab 7

⚠️ Investigation text is included in AI prompts — don't use AI features for incidents whose
details may not leave your organization. AI output is advisory; the investigator owns all
conclusions. Never commit your API key to the repository.

## 💾 Data

Auto-saves in the browser (per device). **Export/Import** JSON for backup and sharing.
**⬇ Download Excel tracker** exports the corrective-action register as `.xlsx`.

## 📁 Repository contents

```
index.html   ← the entire application
README.md    ← this file
```
