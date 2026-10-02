# 08 — Freedom ledger & handoff (Step 6, 2026-10-02)

Two jobs: (1) record what the submission **deliberately does not claim**, so the final round (if selected) can add novelty without contradicting anything we printed; (2) hand the workspace to a fresh session. Phase record: `notes/07-submission-phase-log.md`. Source repos stay read-only — the register patches below are **proposals only**.

---

## A. Freedom ledger — held back, claimable later

### A1. Unopened manufacturing numbers (moved out of description §12 in Step 2)
Printed-copper **79 % slot fill / 87 % IACS** after heat treatment · cold-sprayed copper **98 % IACS / 368 W/mK** as-sprayed · printed hybrid end-winding **−⅓ winding-head height** · modular sensor channel **≈1 % of kit mass** · **printed-in conductors / components-in-structure** (harness elimination) · the digital-cell **"variant in days"** growth story.
- Why held: they sit on register rows **C46/C47/H14/H15/K7/K8 + risks 47–50**, which are not opened; unopened rows may not print as claims.
- Where they return: description §12 and deck slide 4 in the final round, as **measured/qualified** values after first articles — never as dossier estimates.
- The submission already names the processes (MIM, cold-spray, printed windings, digital cell) as candidate tools "validated post-selection", so adding the numbers later upgrades the claim without contradicting it.

### A2. Extra novelty held back (the final-round headline material)
- **The ring-as-inertial-platform proof**: the submission claims the arrangement as "ours to prove, bench-verifiable". The **bench data** (ring-angle tracking under applied torque and spin) is the final-round headline — keep it unshown until then.
- **Estimator performance**: bias-convergence rates and the measured shrink of the two largest budget terms — quantifies the G17 integration claim.
- **F16 dud-rate allocation** (F10) — becomes a safety-case number.
- **Anti-jam sizing** (N5: null depth, J/S margin, bandwidth) — the "table stakes" line becomes a capability claim.
- **Growth module specifics**: beacon-fix link budget, SAL seeker integration — only after **X18** defines the interface.
- **Rejected-alternative depth** (final-round "we did the homework"): the cold-gas RCS physics rejection (repo1, 300 bar → 3.3 L tank, 72 % of requirement), the two-motor face-gas legacy design — usable as *rejected* alternatives, never as ours.
- **Realised mass reduction**: spigot hollowing **−0.586 kg** banked, the axial-flux trade outcome, make-vs-buy decision — the P9 closure story.
- **Platform-matched Monte Carlo output** (the new CEP number) — supersedes both 23.9 m (budget) and 21.5 m (methodology-vintage) as the headline when it exists.

### A3. Internal figures never printed (quote only with status if asked live)
Sg envelope **1.37–3.55**, design point ≈ **1.83** (PARAMETRIC) · iron-loss estimator **~50–60 W** (uncalibrated) · guided-window **t ≈ 15 s** (placeholder) · torque gates **0.252 N·m transient / 0.103 continuous** (C9/C12 ruled) · **Tf ≤ 0.10 N·m**, Taero_min **0.1706 N·m** [ref] · Rev E MC **CEP50 21.5 m**, 250/250 in guidance (methodology-vintage; see defense brief R1).

### A4. References dropped from §16 (restore to final-round research section if space allows)
Wernert & Theodoulis 2013 · Wang et al. 2018 (Defence Technology) · Robinson & Berefelt 2011 (FOI) · DOT&E FY2015 · Norris et al. 2020 · DT 2025 flight-stability (B4) · Guo et al. 2026 resonance · Hasselstrom & Nilsson 2012 · NSWC Indian Head 2021 · DT 2026 damage tolerance. (Slide 6 / description §16 keep the curated 12.)

---

## B. Post-selection adds, in value order (each unlocks printed claims)

1. **YIL platform data** (shell drawing, fuze-well drawing, firing tables, setter logs) → re-baseline M3/M4/M6/M7 + the P/S sizing chain; PARAMETRIC → service-anchored; closes "94/267 m" attribution to Indian figures.
2. **Aerodynamic coefficient set (risk 8 — the long pole)** → re-quantifies 18.1 N, 450/407 m, 2.92 kW / 121 kJ and the CEP budget; unlocks the produced (not asserted) CEP.
3. **Bench rig results (R7)**: ring-angle tracking under load · measured alternator constant + friction · thermal-path conductance (P6) → "ours to prove" becomes "proven on the bench".
4. **Mass closure (P9 ruling + levers + realised spigot)** → next mass statement; the YIL acceptable-mass question answered.
5. **K5 priced cost roll-up** at certified volume → target becomes estimate.
6. **Manufacturing first articles** (after opening the rows) → A1 numbers become printable as measured.
7. **Fuze/electronics closures**: F10 dud allocation · F7/F8 arming thresholds · N5 anti-jam sizing · N4 outage tolerance · X18 interface definition · E-domain standards set (P4, risk 42).
8. **Simulation campaign (R5)** outputs: CEP · guided-window duration · swerve phase (G16) · stability/resonance evidence (S8) · M7 authority transfer function (risk 52).

## C. Register patch proposals (design repo — propose, never edit from here)

1. Open/rule **C46, C47, H14, H15, K7, K8 + risks 47–50** (the manufacturing dossier's proposals).
2. **P9** mass: decide route (material / ring diameter / both), land the banked spigot −0.586 kg, raise the YIL acceptable-mass question (post-sel item 4).
3. **C38** magnet retention: close on the CAD load case (736 N per magnet).
4. **C39**: calibrated iron-loss calculation (retires the 50–60 W estimator).
5. **F10**: allocate F16's deliberate dud contribution.
6. **N5** (null depth / J-S margin / bandwidth) · **N4** (bounded outage) · **N11** (baro justification) · **N12** (absolute ring-angle method).
7. **X18**: define the reserved module interface (mechanical + electrical).
8. **S8 / G16 / risks 51–52**: name-vehicle evidence at P3.
9. Consistency debt: register per-domain G/X cells, ROADMAP counts (196/87 → 197/86), `03a` stale T_CONT 2.36 → 2.28 N·m, missing `01-design-definition.md`.
10. Source-register hygiene: Karimi DT 2024 orphan (add rating or drop) · W8/W9 no-text-layer notes · B16 Table 1 inertia/AoA verification before use as design inputs · C9 patent text now read (update the Rule-1 note).

## D. Submission state at handoff

- **Paste-ready:** `submission-resources/01-abstract.txt` (**7,079 / 10,000**) · `02-description-FINAL.txt` (**49,850 / 50,000**, headroom 150) · Idea Title **84/100** (`STHIRA-PGK: De-Spun Canard Guidance Kit with Multi-Mode Smart Fuze for 155 mm Shells`).
- **Build/defense:** `04-deck-brief.md` (content pack; fig4-system-flowchart REQUIRED) · `05-upload-qa-checklist.md` · `06-judge-defense-brief.md`.
- **User-side blockers:** Team ID / Team Name from the portal · portal verbatim values (theme bucket, PS title) · exact cut-off time on 5 Oct · PDF size cap · live char counters · manual deck build + export · upload, then save the PDF here and log the time in `notes/03`.
- **Clock:** idea submission **5 Oct 2026**; the 02–05 Oct one-time edit window covers Team Name / Consent / PPT only.
- **Optional repo2 sync (patches, when the user chooses):** replace `SIH26098-form-content.md` FIELD 4 + the paste-ready twin with `02-description-FINAL.txt`; regenerate the template PDF from the official template (the on-disk `SIH26098-Idea-Template-6Slides.pdf` is superseded); fix form-content §11.2's stale budget (20.4/24); refresh its char-count log (7,079 / 49,850).

## E. Fresh-session resume path

1. `notes/00-INDEX.md` — orientation (updated 2026-10-02).
2. `notes/07-submission-phase-log.md` — the full phase record: submission requirements, the 203-claim source map, the **canonical number table** (Step 1), Steps 0–5 logs.
3. This file — what is held back and what happens post-selection.
4. `submission-resources/` — everything paste-ready or build-ready.

**Starter prompt (copy-paste):**
> Read `notes/00-INDEX.md` and `notes/08-freedom-ledger.md`. The SIH 2026 idea submission is text-final (`submission-resources/01` + `02`); the 6-slide PDF is built manually from the content pack `submission-resources/04`, and Q&A armoury is `06-judge-defense-brief.md`. Read-only source repos: `/Users/jagathsrujan/Documents/smart india hackathon` and `/Users/jagathsrujan/Documents/final-sih-pgk-kit-design`. Help me <task>.
