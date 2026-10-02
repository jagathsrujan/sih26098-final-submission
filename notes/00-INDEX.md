# SIH 2026 — Final submission workspace: index & orientation

**This workspace** (`/Users/jagathsrujan/Documents/final submission sih`)
- The **resource workspace for the SIH 2026 submission round**. Submission-only design phase **complete (2026-10-02)**: portal texts final in `submission-resources/` (01 abstract · 02 description · 04 deck content pack · 05 QA · 06 judge defense); phase record in `notes/07`; freedom ledger + resume path in `notes/08`.
- The `notes/` files are working notes on the two source workspaces — context, not submission resources.

**Project**: SIH 2026 problem statement **SIH26098** — low-cost precision guidance + smart electronic fuze (PGK) kit for the 155 mm artillery shell; Ministry of Defence / Yantra India Limited. Concept name used in the decks: **STHIRA-PGK**. Targets: **CEP ≤ 30 m at ~30 km** (vs ~267 m CEP unguided), **≤ ₹6.5 lakh/kit at 5 000 kits/yr** (vs M1156 PGK ≈ US$13,541). Hard boundary repeated everywhere: **inert exhibition / analysis design only — no energetics, no live fuze/S&A.**

**Source workspaces (read-only references)**

| Repo | Path | Period | Role |
|---|---|---|---|
| "smart india hackathon" | `/Users/jagathsrujan/Documents/smart india hackathon` | 25 Aug – 1 Sep 2026 | team "research OS": cleansheet design of record (Rev 1.7), simulation evidence (Rev E CEP 21.5 m), electronics + flight-software baseline, 6-slide submitted deck |
| "final-sih-pgk-kit-design" | `/Users/jagathsrujan/Documents/final-sih-pgk-kit-design` | 17–30 Sep 2026 | solo deep design: criteria register (197 rows), CAD phases 0–7, briefing/deck suite, canonical 6-slide submission deck + portal text |

**Version story in one screen**
- 25 Aug — repo 1 starts (108-idea catalog, team branches, auto-updating LIVEBOARD).
- 28 Aug — bench demonstrator switches to the "common carrier" concept.
- 30 Aug — clean-sheet design track **Rev 1.1** declared design of record.
- 31 Aug — **Rev 1.3** + "Rev E" GNC Monte Carlo → CEP50 **21.5 m** (gate ≤ 30 m; 250/250 end in guidance).
- 1 Sep — superseded work archived under `legacy/`; design report **Rev 1.7**; electronics + flight software baseline; 6-slide deck submitted (ppt + pdf at repo root).
- 17 Sep — repo 2 starts (initial import; parametric design basis; YIL data declared post-selection only).
- 18–20 Sep — criteria register grows (196→197 rows); PMSM sizing (2.92 kW / 121 kJ finding); source register; **CAD Phases 0–7 all gates PASS**, findings **T1–T10**; manufacturing dossier.
- 21–23 Sep — atlas sheets built; **23 Sep reconciliation pass**: T1–T10 ruled, G16 + risks 51/52 added, risk 46 closed, five arithmetic errors fixed.
- 22–28 Sep — deck suite (48-pp briefing, 20-slide deck, canonical 6-slide `deck.html`); system architecture sheet (28 Sep, extra pass 30 Sep).
- 29 Sep — G17 + X2 DEFINED; portal form content re-measured (description 49,924 / 50,000 chars).
- 1 Oct (now) — final submission round; gather resources here.

**Where the canonical versions live**

| What | Where |
|---|---|
| Design truth | repo 2 `design/00-design-criteria-register.md` — **197 criteria** (49 DEFINED / 37 DERIVED / 24 PARAMETRIC / 86 OPEN + P9 PROPOSED), updated 29 Sep. Authority order: **register ≻ CAD/atlas evidence** ("the CAD evidences; it never decides") |
| CAD | repo 2 `design/cad/` (phases 0–7; gates PASS; `VERIFICATION-LOG.md`); findings T1–T10 → `design/07-cad-evidence.md` (ruled 23 Sep) |
| Simulations | repo 1 `cleansheet/out_sim/` (`RESULTS.md`, `RESULTS_GNC.md` = Rev E, `RESULTS_FSW.md`, `RESULTS_SENSORS.md`) + `cleansheet/flight_sw/` (33 tests green) |
| Canonical submission deck | repo 2 `submission/deck/deck.html` — print to PDF = the submission file. `SIH26098-Idea-Template-6Slides.pdf` on disk is from a **superseded** HTML |
| Portal text | repo 2 `submission/SIH26098-form-content.md` + `submission/SIH26098-idea-description-paste-ready.txt` |
| Official format | repo 2 `submission/SIH2026-IDEA-Presentation-Format.pdf` — max **6 slides incl. title**; use the provided template; save as **PDF**; do not change the idea-detail pointers |

**Known traps before upload** (all verified in repo 2)
- **Trap status (2026-10-02, submission phase closed):** theme resolved = **Smart Vehicles** · deadline resolved = **5 Oct 2026** (+ 02–05 Oct one-time Team Name/Consent/PPT window) · error budget fixed everywhere to 5/17/5/8/3 → RSS 20.3 → CEP 23.9 · abstract spin band fixed to 10,000–20,000 rpm · title = **84** chars · §16 = 12 references. Still live: Team ID/Name placeholders · repo2 `form-content.md` §11.2 still stale · the on-disk Idea-Template PDF is superseded (build from the official template + `submission-resources/04`) · fig4-system-flowchart must be embedded · PDF size cap unconfirmed.
- **Team ID + Team Name are placeholders** in `deck.html` / the old PDF / HTML templates — take them from the portal.
- **Theme/bucket conflict**: deck + form-content say **Smart Vehicles**; `draft-from-register.md` says Defence and Security; analyst data says Miscellaneous. Copy the portal value character-for-character.
- **Stale error budget**: `deck.html` uses the corrected **nav 5 / G&C 17 / meteo 5 / aero 8 / fuze 3 → RSS 20.3 → CEP 23.9 m** (verified); `form-content.md` §11.2 still shows the OLD split (RSS 20.4 → ~24 m). Fix before upload.
- **Description at 49,924 / 50,000 chars** — 76 chars headroom; §16 reference list (~3,200 chars) is the designated trim candidate.
- **Deadline conflict**: repo 1 tracker says 20 Sep (kit deadline); repo 2 roadmap + SIH guidelines say **30 Sep 2026**. Confirm on the portal.
- Old drafts (`draft-from-register.md`, `template-slides.md`) still carry ⟨DECISION REQUIRED — F16⟩ and raw `[criterion]` IDs — **do not paste from them verbatim**.
- `submission/deck/figures/fig4-system-flowchart.*` (the PS's "electronics block diagram" deliverable) exists but is **not embedded** in `deck.html`.

**Starter prompt for the next session (copy-paste)**
> Read `notes/00-INDEX.md` and `notes/08-freedom-ledger.md`. The SIH 2026 idea submission is text-final (`submission-resources/01` + `02`, paste-ready); the 6-slide PDF is built manually from the content pack `submission-resources/04`, and the Q&A armoury is `06-judge-defense-brief.md`. Read-only source repos: `/Users/jagathsrujan/Documents/smart india hackathon` and `/Users/jagathsrujan/Documents/final-sih-pgk-kit-design`. Help me <task>.

**Notes map**
- `notes/00-INDEX.md` — this file (orientation + canonical pointers + traps).
- `notes/01-smart-india-hackathon-repo.md` — deep notes on the earlier team repo (concepts, Rev 1.1→1.7, Rev E numbers, directories, tooling, superseded map, open threads).
- `notes/02-final-sih-pgk-kit-design-repo.md` — deep notes on the later design repo (design timeline V0–V6, artifact inventory, key numbers, submission versions + official format, gaps).
- `notes/03-submission-decisions.md` — locked decisions (title, mass framing, deck tool, abstract depth) + built resources + errata.
- `notes/04-design-walkthrough.md` — the 11-module design walkthrough record (closed 2026-10-01).
- `notes/05-research-digests.md` — paper digests + question bank QB1–12 (the proof base).
- `notes/06-new-session-prompt.md` — starter prompt that opened the submission-only phase (historical).
- `notes/07-submission-phase-log.md` — submission-phase record: requirements inventory, 203-claim source map, canonical number table (Step 1), Steps 0–5 logs.
- `notes/08-freedom-ledger.md` — freedom ledger (held-back claims), post-selection adds, register patch proposals, resume path.
