# 02 — "final-sih-pgk-kit-design" repo (17–30 Sep 2026)

Path: `/Users/jagathsrujan/Documents/final-sih-pgk-kit-design` · git repo · `main` only (61 commits, 17–28 Sep).
Role: the **later, solo deep-design repo** for SIH26098 — criteria register, CAD, notes, decks and the submission package. This is where the current submission material comes from.

**Authority order (stated everywhere)**: `design/00-design-criteria-register.md` is authoritative; CAD and atlas are evidence only — *"the CAD evidences; it never decides."* Any claim in a deck must trace to a register row.

## Design version timeline

| Step | Date | What changed |
|---|---|---|
| **V0 — `[ref]` thesis architecture** | ≤ 16 Sep | Baseline inherited from the METU thesis (de-spun canard ring, alternator-as-actuator, cascade PI + DOB, brake-only rectifier). Origin of every `[ref]` value; re-scaling discipline (risks 24/32/37) |
| **V1 — parametric re-baseline** | 17 Sep | YIL data declared post-selection; `OPEN-BLOCKED` retired → `PARAMETRIC` for 25 criteria; public-data reference 155 mm model adopted (design point 45.0 kg; Ixx 0.155; Iyy 1.75); M7 re-cut to **407 m / 19.0 m/s / margin 1.11:1**; X growth block added; first commit `a0db1c8` |
| **V2 — machine sizing confirmed** | 18 Sep | 12-slot/14-pole frameless outrunner PMSM, Ø79 mid-gap, ≈0.81–0.97 kg; **2.92 kW peak / ≈121 kJ per flight** (×2.4 the reference 1.2 kW); thermal interface ≥58 W/K peak through the fuze well (bare thread only 3–16 W/K); K4 ≤ ₹6.5 lakh @ 5 000/yr; R5 two-tier Monte Carlo |
| **V3 — H block + bus re-decision** | 19–20 Sep | H1–H13 defined (dual-core M7/M4F, 1 kHz loop, ring-mounted IMU, rotary-transformer power + optical data link); **400 V → 180 V nominal bus** (H8/H12); source-register pass adds 4 criteria (M10, S8, F16, E12) + risks 40–45; novelty claims credited away to prior art; **F16 adopted 20 Sep** (withhold function when predicted miss > 150 m, latched, dud direction) |
| **V4 — CAD + manufacturing + atlas** | 20–21 Sep | `design/cad/` built (SSOT `pgk_params.py`); **Phases 0–7, every gate PASS**; first measured mass rollup (**4.839 kg steel / 2.713 kg Al** vs P9 ≤ 1.4 kg) and findings **T1–T10**; manufacturing dossier; atlas sheets (sheet `flow` replaces `sheet1` on deck slide 3) |
| **V5 — reconciliation pass (current record)** | 23 Sep | **T1–T10 all ruled**; five arithmetic errors fixed (largest: C9/C12 torque gate → **0.252 N·m transient / 0.103 continuous**); **risk 46 closed** (2.92 kW stands); T6 re-baselined ×5.2 on the 2.595 kg ring-side mass → **382 kN axial / 127 kN radial setback**, C35 → **1 911 / 635 N/µm**; **G16 added** (swerve-response phase) + risk 51; risk 52 (M7 authority transfer function) opened; P9 re-baselined → **PROPOSED** |
| **V6 — latest markers** | 29 Sep | **+G17 DEFINED**; **X2 OPEN → DEFINED** (growth ladder: beacon aiding → SAL → EO scene matching); total **197** criteria. Per-domain G/X rows not yet updated |

**Current design of record**: de-spun, fixed-canard, **one-moving-part** PGK — 12-slot/14-pole frameless outrunner PMSM as actuator + generator, 180 V nominal bus, ring-mounted IMU (rotary-transformer power / optical data link), canards span-capped at Ø151 mm with cant as the force lever, F16 predicted-miss failsafe. The CAD model has **not been re-run** against the 23 Sep rulings, and the intended P2 output `design/01-design-definition.md` **does not exist yet**.

## Artifact inventory

**`design/` — core documents** (all relative to repo root)

| File | Purpose | Status |
|---|---|---|
| `00-design-criteria-register.md` | Working record of every criterion + decision log (~88 entries) + risks 1–52 | **CURRENT, authoritative.** ~433 KB; 632 lines; 197 rows (49 DEFINED / 37 DERIVED / 24 PARAMETRIC / 86 OPEN + P9 PROPOSED) |
| `02-reference-155mm-model.md` | Public-data platform substitute (M795 / M549A1 → design point 45.0 kg, 855 mm, Ø154.89); MIL-STD-333B 2″-12 UNS-2A; intrusion ≤124.7 mm; kit 1.4 kg = +0.42 kg net; Sg 1.37–3.55 (design point 1.83) | CURRENT basis; retired at P6 |
| `03-caa-machine-sizing.md` + `03a-machine-sizing-model.py` | PMSM sizing (C14–C20, C34–C43); the kilowatt finding | CURRENT; superseded in part (400 V → 180 V; hold 2.36 → 2.28 N·m; Kt 0.716 void — use C14's 0.362); script still has `T_CONT = 2.36` (~3.5 % high) |
| `05-source-register.md` | Rated sources (Cite 1–5 / Adopt 1–5 + read-depth), claim corrections, gap list | CURRENT (19 Sep + J section 20 Sep); corrections not fully propagated into submission |
| `06-manufacturing-and-process.md` | Process/cost dossier + digital hybrid cell at 5 000 kits/yr ("no register value changed by this file"; proposals K7/K8/C46/C47/H14/H15 + risks 47–50 unopened) | CURRENT research pass |
| `07-cad-evidence.md` | CAD proofs (gates) + findings T1–T10 | CURRENT; findings ruled 23 Sep |
| `08-atlas.md` | Number ledger for the atlas sheets (every number vs its criterion) | CURRENT; `sheet1` superseded on the slide by `flow` |
| `ROADMAP-and-prompts.md` | Phase plan (P0–P7) + master session prompt + carried items 1–20 | CURRENT; counts lag register (196/87 vs 197/86) |
| `START-HERE-session-prompt.md` | Old interview protocol (define criteria one question at a time) | SUPERSEDED as entry point by the roadmap's master prompt |
| `04-caa-dual-spin-interface.html` | Interactive three.js visualisation of the two interfaces | Current but carries flagged stale numbers (73.5 kN setback, 400 V); **only artifact needing network (three.js CDN)** |
| `09-professor-briefing.html` (+ `09a-briefing-build.py`) | 48-page technical briefing (the full design record; nothing asserted in the decks that isn't argued here) | CURRENT; build embeds figures as data URIs, hard-fails on external refs |
| `09b-slides.html` (+ `09b-slides-build.py`) | 20-slide present-from deck (2026-09-23) | CURRENT; bundled fonts in `design/fonts/` (6 WOFF2 subsets: Deck Sans/Serif/Mono) |
| `10-canard-aim-matrix.html` | Four cannard-command panels; "the four canards never move — only the ring rotates"; φ_d (G16) open | Current reference figure |
| `11-system-architecture.html` (+ `11a-architecture-scene.py` → `.excalidraw` mirror) | Detailed system architecture sheet (3 tiers), updated 30 Sep (flight-computer strip, bias estimator, diode-OR, chopper dump; N5 amber) | CURRENT |
| `design/cad/` | SSOT `pgk_params.py`, `macros/00…95_phase*.py` (Phases 0–7), `out/` (9 FCStd + 18 screenshots + 22 deck-renders), generated docs (`PARAMETERS.txt`, `PARTS.md`, `TRACEABILITY.md`), hand-kept `VERIFICATION-LOG.md` | CURRENT; verified numbers: intrusion 124.70 mm, 0.0000 mm³ shell interference, air gap 0.400 mm, cant 10.0000°, tips Ø151.00, machine 1.018 kg, rotating assembly 1.876 kg |
| `design/atlas/` | `atlas_scene.py` (SSOT) → `render_svg.py --all --png --strict` → 6 sheets (`flow` + sheet1–5) in svg/png/excalidraw; gates: check_fit / check_overlap / check_routes | CURRENT; `flow` = deck slide 3 figure |
| `design/fonts/` | 6 WOFF2 subsets (Source Sans / Source Serif / DejaVu Mono) embedded in 09b slides | cache for reproducible builds (`--fonts` regenerates) |

**`notes/` — reference distillation**

| File | Purpose |
|---|---|
| `00-PGK-thesis-working-notes.md` | Distils METU/Günay 2022 thesis (`10463953.pdf`, 169 pp) — the `[ref]` authority: torque ledger `T = Talt + Tf − Taero`; authority criteria `Taero ≤ (Talt_max+Tf)/2 = 2.93 N·m`, `Taero > Tf = 0.10 N·m`; Taero min 0.1706 N·m @ 41.16 s; cascade PI `0.29 + 7.82/s` over P `29.7`; DOB `Ĝ = 588.4/(s+1.04)`, `Q = 1/(0.5s+1)`; loss of control t = 30–50 s in the reference |
| `01-thesis-full-text-extracted.txt` | Raw pdftotext layer (5 234 lines) — evidence file; **no verbatim sentences allowed in the submission** (similarity screen) |
| `02-PGK-SIH-design-brief.md` | Thesis→SIH bridge: R1–R12 requirements, D1–D7 architecture decisions, CEP error-budget skeleton (RSS 20.4 → ~24 m), [verify] on M1156 unit price |
| `03-wang2015-gnc-application.md` | The closest external paper (register C11): swerve phase ≈172° launch → 146–149° near apogee; authority vs correction-start time; perturbation IPP cross-check; created G16 + risk 51 |
| `04-workspace-pdf-references.md` | On-disk reference ledger (11 PDFs in `notes/references/`); recommends 6 register additions (W4, W8, W17, W21, W22, W25) — **not executed** |
| `notes/figures/` | 18 page-anchored thesis crops + 9 Wang crops + `extract.py`; 5 thesis figures used live in the deep-dive deck |
| `notes/references/` | 11 PDFs (8 literal refs of the two source papers + 3 flagged adjacent), incl. B16 Ollerenshaw & Costello (register row, created risk 52) |

**`submission/` — versions (oldest → newest; canonical in bold)**

| # | Artifact | Status |
|---|---|---|
| 1 | `SIH26098-abstract-draft.txt` | SUPERSEDED (pre-F16, pre-estimator) |
| 2 | `SIH26098-draft-from-register.md` | Internal draft; carries stale ⟨DECISION REQUIRED — F16⟩ + raw criterion IDs — do not paste |
| 3 | `SIH26098-verified-source-audit.md` (19 Sep) | Evidence check on the public record; current reference |
| 4 | `SIH26098-judge-and-competitor-dossier.md` (19–20 Sep) | Judge/competitor strategy, novelty ledger, the "no verbatim thesis" rule |
| 5 | `SIH26098-template-slides.md` | 6-slide content plan; carries the F16 placeholder (decision since made) |
| 6 | `SIH26098-idea-presentation.html` | First 6-slide HTML — superseded |
| 7 | `SIH26098-idea-template-6slides.html` → `SIH26098-Idea-Template-6Slides.pdf` | Second 6-slide HTML + its PDF export — superseded by the deck below, but is the PDF on disk |
| 8 | `SIH26098-form-content.md` | Portal field content (title options, 3,948-char abstract, 49,924-char description, char-count log). **§11.2 error budget is stale (20.4/24); deck uses 20.3/23.9** |
| 9 | `SIH26098-idea-description-paste-ready.txt` | Standalone description ≈ FIELD 4 + product name; paste-ready |
| 10 | **`deck/deck.html`** | **CANONICAL 6-slide deck.** Self-contained (fonts/figures inline), 1280×720 slides; browser Print → Save as PDF = the submission file. Team ID/Name still placeholders; guided-window t≈15 s is a placeholder |
| 11 | `deck/deep-dive.html` | Long-form internal review "for the professor" — explicitly NOT the submission |
| 12 | `deck/figures/` | figlib.py + fig1–3 generators; **fig4-system-flowchart** (PS "electronics block diagram" deliverable) exists but **not embedded** in deck.html; `embed_cad.py`; `cad/` 21 renders; `market/` + `thesis/` credited figures |

## Official submission format (from `SIH2026-IDEA-Presentation-Format.pdf`)

- **Max 6 slides including title.** Sections: (1) Title (PS ID/title, theme, category, Team ID, Team Name, IDEA TITLE); (2) Proposed Solution; (3) Technical Approach; (4) Feasibility & Viability; (5) Impact & Benefits; (6) Research & References.
- Points/diagrams/infographics — no paragraphs; keep it precise; **use only the provided template** and do not change the idea-detail pointers; **save as PDF and upload** (delete the instructions slide).
- Evaluation (from SIH guidelines, via the dossier): novelty, complexity, clarity & detail, feasibility, practicability, sustainability, scale of impact, UX, future-work potential; business potential gets extra weight; prototype preferable but not mandatory for Hardware Edition; 500-idea cap per PS; **deadline 30 Sep 2026** (conflicts with repo 1's 20 Sep tracker — confirm on portal).

## Key numbers & decisions (register-backed)

- **Platform**: 45.0 kg design point (43–47 kg envelope); Ixx 0.155 (0.144–0.167); Iyy 1.75 (1.22–1.81); 855 mm; Ø154.89; spin 1 108–1 912 rad/s; 15 000 g / 5 000 g.
- **Dispersion/authority**: CEP 267 m → σ 227 m; M7 = 407 m @ 80 % capture / 19.0 m/s / T 42.8 s / margin 1.11:1; C8 force ≥ 18.1 N; 450 m available vs 407 m required.
- **Machine**: 2.92 kW peak (×2.4 reference); ≈121 kJ/flight; hold 2.28 N·m; slew 5.76 N·m; 15.9 / 6.5 A rms; 2 130 Hz; bus 180 V nominal (≈150–200 V); gate Tf 0.252 N·m transient / 0.103 continuous.
- **Error budget (current)**: nav 5 / G&C 17 / meteo 5 / aero-ballistic 8 / fuze 3 → RSS 20.3 → **CEP 23.9 m** (~20 % under the 30 m claim). Verified in `deck.html`; stale form-content §11.2 still says 20.4/~24.
- **Mass reality check**: CAD 4.839 kg steel / 2.713 kg Al vs P9 ≤ 1.4 kg (+94 % in Al; P9 now PROPOSED); net platform effect +3.9 %; machine 1.018 kg (C40 +5 %); setbacks 223.4–275.8 kN measured → re-baselined 382 kN axial / 127 kN radial.
- **Cost/volume**: K4 ≤ ₹6.5 lakh (≈ US$7,800) @ 5 000 kits/yr vs M1156 US$13,541 (FY2013, >100k units).
- **Setter**: AOP-22 — 100 ± 0.01 kHz, 1 000 ± 10 bit/s, FMW 275 ± 5 ms, ≈550 bits for a CCF package (risk 44 owns the bit budget).
- **F16 (adopted)**: withhold function when predicted miss > 150 m; latched; dud-direction.

## Open items / gaps (repo 2)

1. **86 OPEN of 197 rows** + P9 PROPOSED; F16's dud contribution must land on F10.
2. **Risk 8 — the aerodynamic coefficient set (with Magnus, both parts)**: the binding blocker on P3 and the long pole.
3. **Mass (P9) is the biggest written-down gap**; levers are material, ring diameter (T8 ↔ C44 ↔ M10) and retention hardware — a user decision (carried item 20).
4. Carried items still open: 13 (ring-hold duty trade, risk 37), 14 (RocketPy scope vs R5), 16 (manufacturing rows K7/K8/C46/C47/H14/H15 + risks 47–50 unopened — if unopened, the deck must not carry the claims), 17 (rehearsal), 19 (Wang items: G16, risk 10 sweep, S4 vs ≈10°, Magnus for risk 8), 20 (P9 ruling, C9/C12 duty, C26/C32/C35, C44↔M10, risk 52).
5. Consistency debt: CAD not re-run vs the T-rulings; `03a` stale `T_CONT`; ROADMAP counts lag; register G/X cells lag; `01-design-definition.md` missing; P5 deck "not built" per roadmap though decks exist.
6. Submission blockers: Team ID/Name placeholders; theme bucket conflict (Smart Vehicles vs Defence and Security vs Miscellaneous); stale form-content §11.2; 76-char headroom; guided-window placeholder; fig4 not embedded; the on-disk PDF is from a superseded HTML (regenerate from `deck.html`).
7. `04-caa-dual-spin-interface.html` retains stale numbers in prose (flagged in its own reconcile panel) and is the only artifact needing network; CAD `out/` has a stray `product 2.FCStd` + 2 gitignored `.FCBak`.
