# 03 — Submission decision session (log)

Purpose: a resumable Q&A log — each answer drives the submission resources (title, abstract, description edits, deck brief, video plan, upload QA). Draft resources will be built in this workspace under `submission-resources/`; the two source repos stay untouched (read-only references).

## Round 1 — 2026-10-01

| # | Decision | Answer | What it drives |
|---|---|---|---|
| 1 | Idea Title | **A — STHIRA-PGK** (85/100 chars) | Portal title, deck slide 1, all references to the product name |
| 2 | Mass framing | **Re-baseline honestly** — state ≈2.7 kg aluminium analysis, +3.9 % platform effect; ≤1.4 kg target framed as the open trade with named levers (material, ring diameter, banked spigot −0.586 kg) | Description §15 rewrite + (light) abstract line; replaces the stale "1.4–1.7 kg class" text |
| 3 | Deck tool | **Figma or Canva** (manual build, later) | Deck brief must be tool-neutral: figure list, locked numbers, slide map, export checklist |
| 4 | Abstract depth | **~6–8k with hard numbers** | Abstract expansion pass (currently 3,948 chars; cap 10,000) |

## Round 2 — 2026-10-01

| # | Decision | Answer | Notes |
|---|---|---|---|
| 5 | YouTube video | **Skip for now** | Revisit only if a clean capture exists; optional field |
| 6 | Portal theme | **Smart Vehicles** | Copy verbatim into slides/portal |
| 7 | Deck figure set | **Flow charts + CAD pics** (user words) | Brief specs: flow/architecture diagrams (atlas `flow`, system architecture, fig4 flowchart) + CAD renders as primary; fig1–3 data charts optional spares |
| 8 | Char budget policy | **Trim §16 refs as needed** | Only the amount needed; deck slide 6 keeps a curated list |

## Outputs (built 2026-10-01)

- `submission-resources/01-abstract.txt` — expanded abstract, **6,639 chars** (decision: ~6–8k with hard numbers).
- `submission-resources/02-description-FINAL.txt` — full description, **49,903 / 50,000** (headroom 97): §11.1 authority rewrite, §11.2 budget 5/17/5/8/3 → 20.3 → 23.9, §15 honest mass re-baseline, 74 kN → 382 kN axial, STHIRA-PGK named in §2, §16 cut refs 7–8 + renumbered 1–22 + citations updated.
- `submission-resources/03-description-edits.md` — changelog + apply-to-repo2 instructions.
- `submission-resources/04-deck-brief.md` — Figma/Canva build brief (flowcharts + CAD figure set).
- `submission-resources/05-upload-qa-checklist.md` — pre-upload checks + locked numbers + forbidden stale values.

## Open decision queue

- [ ] Team ID + Team Name: paste from portal (blocker for slide 1 + portal)
- [ ] Review/approve the drafted texts (abstract, description changes, deck brief)
- [ ] Build + export the deck PDF (manual, Figma/Canva) — then run QA checklist
- [ ] Optionally sync FINAL description back into repo2 (`form-content.md` FIELD 4 + paste-ready twin)
- [ ] Final portal upload

## Locked numbers (source of truth for all resources)

CEP target ≤30 m; budget closes **RSS 20.3 → CEP 23.9 m** (nav 5 / G&C 17 / meteo 5 / aero 8 / fuze 3) · authority **≥18.1 N**, 450 m available vs 407 m required (1.11:1) · machine **2.92 kW peak / ≈121 kJ** · bus **180 V nominal** · mass **≈2.7 kg Al analysis, +3.9 % platform effect** (P9 PROPOSED) · design point **45.0 kg** platform · cost **≤ ₹6.5 lakh @ 5 000/yr** vs M1156 US$13,541 · setter AOP-22 ≈550 bits · F16 failsafe: withhold when predicted miss >150 m (latched, dud direction).

Nothing unruled/provisional goes into any resource (atlas rule: amber = open; e.g. guided-window t≈15 s must not be printed).

**Errata (2026-10-02, Step 1):** the Idea Title is **84** chars (not 85 — measured in Python). The authoritative claim set with statuses/closers now lives in `notes/07-submission-phase-log.md` (Step 1 section); the submission-phase log is in the same file.
