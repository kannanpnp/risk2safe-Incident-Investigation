# risk2safe-Incident-Investigation
# 🛡️ Risk2Safe — Incident Investigation Workbench

A **single-file web application** for safety professionals to conduct structured incident
investigations: build a **SnapCharT®-style timeline**, identify **Causal Factors**, drill into
**root causes** with the full guided questionnaire (7 Basic Cause Categories + Equipment
Difficulty + the 15-Question Human Performance Troubleshooting Guide), develop **SMARTER
corrective actions**, and print a complete **investigation report** — with optional **AI review
at every step** powered by your own OpenAI API key.

> Methodology concepts referenced: SnapCharT®, Root Cause Tree®, TapRooT® are registered
> trademarks of System Improvements, Inc. This tool is an independent aid for internal use —
> refer to the official TapRooT® books and training for authoritative guidance.

---

## ✨ Features

| Step | Tab (own color) | What you do |
|------|------------------|-------------|
| 1 | **Plan** (teal) | Incident facts, evidence preservation list, interview plan |
| 2 | **SnapCharT®** (blue) | Timeline of Events (rectangles) before & after the Incident (circle), with Conditions (ovals) attached; dashed = unproven info |
| 3 | **Causal Factors** (orange) | Mark problems, apply the 4-Step "So what?" method, promote the true big-picture errors to ▲ CFs |
| 4 | **Root Causes** (purple) | Per CF: Level-1 classification → 15 Questions (auto-recommends categories) → near-root causes → root causes, with dictionary-style yes/no questions at every node |
| 5 | **Corrective Actions** (green) | A row auto-appears per selected root cause; SMARTER guidance, owner / due date / status tracking |
| 6 | **Report** (slate) | One-click formatted report; print or save as PDF |

Plus: multiple investigations, auto-save in the browser (localStorage), JSON export/import
to share or back up investigations, and 🤖 **AI Review** buttons on every tab.

## 🚀 Launch on GitHub Pages (free hosting)

1. Create a new repository on [github.com](https://github.com) (e.g. `risk2safe`).
2. Upload **`index.html`** and **`README.md`** to the repository root
   (*Add file → Upload files → Commit*).
3. Open **Settings → Pages**.
4. Under *Build and deployment*: Source = **Deploy from a branch**,
   Branch = **main**, Folder = **/(root)** → **Save**.
5. After ~1 minute your app is live at:
   `https://<your-username>.github.io/risk2safe/`

No build step, no dependencies, no server code — `index.html` is the whole application.

### Run locally instead
Just double-click `index.html` — it works fully offline.
(For the AI features some browsers prefer the page to be served over http(s);
GitHub Pages, or `python -m http.server` in the folder, both work.)

## 🤖 AI Review setup (optional)

1. Get an API key at **platform.openai.com → API keys** (the account needs billing/credits).
2. In the app, click **🤖 AI setup** in the top bar, paste the key, choose a model
   (default `gpt-4o-mini` — cheap and good), **Save**.
3. Click any **AI Review** button:
   - **Plan** — completeness of facts, evidence & interview plan
   - **SnapCharT®** — timeline gaps, missing Events/Conditions, wording, what to verify
   - **Causal Factors** — are the right big-picture CFs marked? Any missed?
   - **Root Causes** — are 15-Question answers & selected root causes consistent with the evidence?
   - **Corrective Actions** — SMARTER check + stronger fixes up the hierarchy of controls
   - **Report** — end-to-end consistency check + draft executive summary

**Privacy & security notes**

- The key is stored **only in your browser** (localStorage) and sent **only to `api.openai.com`**.
- The investigation text is included in the AI prompt — don't use AI review for incidents
  whose details must not leave your organization.
- AI output is **advisory only**; the investigator owns all conclusions.
- Never commit your API key to the repository.

## 💾 Data & backup

- Work auto-saves in the browser you're using (per device, per browser).
- Use **Export** to download an investigation as a `.risk2safe.json` file and
  **Import** to load it on another machine — also your backup mechanism.
- Clearing browser site data erases saved investigations: export anything important.

## 📁 Repository contents

```
index.html   ← the entire application (open this / deploy this)
README.md    ← this file
```

## ⚠️ Disclaimer

This tool supports — but does not replace — competent investigation practice and formal
training. Verify all findings against the facts. SnapCharT®, Root Cause Tree®, and TapRooT®
are registered trademarks of System Improvements, Inc., Knoxville, TN.
