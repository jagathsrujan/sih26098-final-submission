# 04 — Design walkthrough (understanding sessions)

Goal: **your understanding of the design and its decisions** — the thing the previous versions lacked. One aspect at a time, at whatever depth you ask. Not a resource dump; each module is a sit-down.

Per-module format (the default):
1. I explain the slice: **what was decided → why → what was rejected → the evidence → what's still open.**
2. You explain it back / answer 3–5 judge-style questions (this is the actual test of understanding).
3. You raise improvements or challenges → logged below → routed into the register/resources once settled.

Rules: one module per sitting (say "deeper" or "next"); every number is traceable (register row / CAD / sim) and anything unruled is flagged as open; say "I don't follow" anywhere and I'll re-explain differently. **Walkthrough closed 2026-10-01 (all 11 modules taught; user cancelled the catch-up round). Follow-on phase: submission-only final design — starter prompt in `notes/06-new-session-prompt.md`.**

Sources I'll pull from as needed: repo 2 `design/00-design-criteria-register.md` (authority), `design/03/05/06/07/08` docs, `design/cad/` + `VERIFICATION-LOG.md`, repo 1 `cleansheet/out_sim/*` + `04_GNC_METHODOLOGY.md`, `notes/00–04` from repo 2.

## Modules

- [x] **1. Why this kit exists** — problem, requirements, dispersion math, SWaP-C constraints (register M, PS) — *taught 2026-10-01; teach-back done (gaps filled: σ math, YIL-specific reasons, cost benchmark)*
- [x] **2. Platform & envelope** — no YIL data pre-selection, parametric design, 45 kg reference, stability margins (P, S) — *taught 2026-10-01; Q1–2 checked; Q3–5 re-taught with paper evidence (see `notes/05-research-digests.md`, QB1–4)*
- [x] **3. Concept & mechanism** — de-spun ring, fixed canards, steering vs control pairs, one actuating axis (C) — *taught 2026-10-01; teach-back done (gaps filled: pair roles, the two torques, rejection reasons sharpened)*
- [x] **4. The machine** — alternator-as-actuator, 12s/14p sizing, the 2.92 kW / 121 kJ loaded-generator finding, torque gates (C14–C43) — *taught + re-taught 2026-10-01 (dual-role physics, P = torque × spin, hold-duty breakdown, iron-loss caveat); revisit numbers in module 5*
- [x] **5. Power & thermal** — 180 V bus, reserve battery + alternator, energy ledger, >90 % range-retention cost, ≥58 W/K thermal path (W, P6) — *taught 2026-10-01; teach-back skipped (user moved on); "canards as radiators" idea evaluated + logged (#4); 4-way thermal trade table is the spine if revisited*
- [x] **6. Guidance & control** — IPP law, swerve-response phase, authority window + adaptive limits, cascade loop, degradation ladder (G) — *taught 2026-10-01; teach-back skipped (user moved on); G16/risk 51 + guided-window placeholder flagged as the open items*
- [x] **7. Navigation & sensing** — ring as inertial platform, roll estimation, GNSS aperture, the sensor set (N) — *taught 2026-10-01; teach-back deferred to end catch-up round (sweep plan)*
- [x] **8. Fuze, safety & setter** — multi-mode fuze, S&A interlocks, AOP-22, F16 150 m failsafe, standards (F) — *taught 2026-10-01; teach-back deferred to end catch-up round (sweep plan)*
- [x] **9. Electronics & flight software** — dual-domain split, slip-ring link, FSW mirrors + test evidence (H) — *taught 2026-10-01; teach-back deferred to end catch-up round (sweep plan)*
- [x] **10. Mass, manufacturing & cost** — CAD mass reality + levers, two-tier process plan, ₹6.5 L lane at 5,000/yr (K, J) — *taught 2026-10-01; teach-back deferred to end catch-up round (sweep plan)*
- [x] **11. Evidence & open risks** — T1–T10 rulings, Rev E sim, 86 OPEN rows, risk 8, honest-uncertainty playbook (R, X) — *taught 2026-10-01; catch-up cancelled — walkthrough closed; follow-on phase prompt in `notes/06-new-session-prompt.md`*

## Improvements raised (log)

| # | Module | Idea / challenge | Status |
|---|---|---|---|
| 1 | 1 | Wants the envelope specifics for "fuze can be bigger, but must fit shell + barrel" — state the exact limits (thread, intrusion, in-bore clearance) | carry to module 3 |
| 2 | 1 | Pricing is the point: manufacturing/assembly must be cheaper to hit the lane; expects the GNC + manufacturing to carry the "unique/novel" burden | carry to modules 6 & 10 |
| 3 | 3 | Keep the two ring-opposing torques distinct (aerodynamic torque vs bearing friction — not body load-path transfer) and reinforce the PMSM dual role (motor + generator in one device) | carry to module 4 |
| 4 | 5 | **Canards as radiators** — use the canard surfaces to dump the absorbed heat | evaluated in-session: matches the design's own 4-way trade; "reject to airstream" is already *partial* (~350 W from 0.05 m²). Canards ≈0.002–0.004 m² → tens of W; adding area costs drag (range gate) + the stability allowance. Interface path (fuze well) stands | closed 2026-10-01 |
