# 04 — Template-PDF content pack (manual 6-slide build, Figma/Canva)

Content only — you lay it out. Build on the **downloaded official SIH 2026 Idea Presentation template** (repo2 `submission/SIH2026-IDEA-Presentation-Format.*`). Numbers are the locked canonical set (`notes/07` Step 1); where a number prints, its honesty wording prints with it. Tags in [brackets] are for you as builder/defender — **no criterion IDs or status tags print on the slides themselves**.

**Hard rules (official template):** exactly **6 slides incl. the title page** · keep the template's idea-detail pointers / section headings verbatim · points/diagrams/infographics only, no paragraphs · **delete the instructions slide** · export **PDF** (verify the portal's size cap — "≤ 10 MB" is unconfirmed third-party info) · clock: idea submission due **5 Oct 2026** (exact time on the portal); the **02–05 Oct one-time edit window** covers Team Name / Consent / PPT only.

## Locked facts (title page + portal)

- **Idea Title (84/100 chars):** `STHIRA-PGK: De-Spun Canard Guidance Kit with Multi-Mode Smart Fuze for 155 mm Shells`
- **PS:** SIH26098 — copy the PS title verbatim from the portal/PS page (working paraphrase: low-cost precision guidance + smart electronic fuze kit for the 155 mm shell; MoD / Yantra India Limited)
- **Theme:** **Smart Vehicles** · **Category:** **Hardware** — copy the portal values character-for-character
- **Team ID / Team Name:** ⟨from portal⟩ — the only permitted placeholder; fill before export
- Title-page field order (per the template): PS ID · PS title · Theme · PS Category · Team ID · Team Name · Idea Title

## Slide 1 — TITLE PAGE

- Fill the seven fields above.
- Optional problem hook (only if the template's slide 1 has content space; otherwise it lives on slide 2):
  *"155 mm artillery is unguided at long range — 94 m to 267 m CEP in the published record for the fielded class, against the 30 m the requirement demands."*

## Slide 2 — IDEA TITLE & PROPOSED SOLUTION

**Title line:** *STHIRA-PGK — a de-spun canard guidance kit with an integrated multi-mode fuze*

- **Problem (points):** dispersion grows with range — published record **94 / 125 / 150 → 267 m** vs **≤ 30 m** required at full charge and long range [M6 class-anchor: fielded-class figures, never YIL data] · volume fire costs rounds, time, collateral, battery exposure · YIL already manufactures the shell hardware — the missing capability is the kit · retrofit: fuze well + forward ogive only, no shell re-qualification.
- **Solution:** four fixed canards on a bearing-isolated de-spun ring · **0°/180° equal-cant pair** = net guidance force (2× one canard), roll torques cancel · **90°/−90° opposite-cant pair** = net roll torque, zero force · ring roll angle aims the force vector → **2-D steering from one actuation axis, zero moving control surfaces**.
- **Actuation economy:** **the alternator is the actuator** (magnets on ring, coils on body) — no servos, gearboxes or linkages · **no flight battery**: alternator in flight · supercapacitor buffer for motoring bursts · reserve battery pre-launch and safe state only.
- **Fuze:** multi-mode (proximity / time / impact) configured over the **existing inductive setter** (AOP-22) — integrates with current firing procedure.
- **Credit block (must say):** the architecture is the fielded **M1156** specification and is claimed in **US 6,981,672 (2006, expired)** — the two-pair split and the alternator-as-actuator are **lineage, not our invention**. Ours is the engineering that makes it close: loaded-generator sizing (**2.92 kW peak / ≈ 121 kJ per flight** — sizing figures, dynamometer rig confirms), the declared thermal path, the ring as inertial platform, the spin-axis GNSS aperture, the in-flight error estimator, the state-dependent authority gate, the F16 predicted-miss failsafe.
- **Visual:** annotated exploded CAD (01-assembly-iso / 05-shell-kit-section / 12-exploded-stack / 14-part-ring-canards) + canard force inset; thermal path through the fuze-well threads if it fits.

## Slide 3 — TECHNICAL APPROACH

- **Guidance:** impact-point-prediction (propagate → compare → command ring angle → recompute) — credited to published work [ref Zhang 2019]; ours is the **state-dependent authority gate**. Authority is high early and late and collapses at apogee; the gate turns that collapse into a designed constraint.
- **Navigation:** GNSS + IMU + baro + ring-angle fusion · **the ring is the inertial platform** — spin removed, standard IMU suffices (pickoff relative to body + magnetometer absolute) — *ours to prove; the bench programme is tasked with proving it* · **spin-axis GNSS aperture** (elements combined, no spin-frequency modulation).
- **GNSS-denied:** coasts on inertial to the drift limit; anti-jam GNSS is a **module-level substitution** (capability only — no null-depth or margin numbers, those are not set). Outage tolerance is set and verified in the Monte Carlo campaign.
- **Control:** cascade **P outer / PI inner**, disturbance observer, **state-dependent current and velocity limits**, anti-windup, **1 kHz** loop. Stability: the **span-capped canard ring (Ø151 mm tips)** is the resonance disposition — *evidence closes in the 7-DOF campaign (open item, not a settled result)*.
- **Fuze & safety:** RF Doppler proximity (selectable burst height) / crystal time / impact crush-inertial (selectable delay) · out-of-line S&A, dual environmental interlocks (setback + spin) · **F16 one-liner: if the predicted impact lands more than 150 m from the loaded target, the fuze withholds function — latched, dud-direction** (AOP-22 command mode).
- **Visual (required):** **fig4-system-flowchart** — the PS's electronics block-diagram deliverable, must be embedded — plus the atlas `flow` sheet or the system-architecture sheet for the three-tier layout.

## Slide 4 — FEASIBILITY AND VIABILITY

- **Error budget (locked):** nav **5** / G&C **17** / meteo **5** / aero **8** / fuze **3** → **RSS 20.3 m → CEP ≈ 23.9 m** vs ≤ 30 m — *derived budget; the 7-DOF Monte Carlo produces the flight CEP* (nav line carries a derived 3.7 m sub-allocation).
- **Authority (derived figures):** ≥ **18.1 N** minimum over the guided window · **450 m** available vs **407 m** required (80 % capture) → **1.11:1 — a margin, not comfort**; re-quantified in the guided-window analysis.
- **Mass (honest framing — approved):** aluminium analysis **≈ 2.7 kg** (same model 4.8 kg steel), net **+1.7 kg ≈ 3.9 %** of the 45 kg round · **1.4 kg target class not yet met** · levers named (material, ring diameter, retention; spigot −0.59 kg banked) · gate **> 90 % range retention** · *CAD analysis, not a weighed article*.
- **Challenges → mitigations (the template asks for them):** aerodynamic coefficient set is the acknowledged long pole → published data + CFD + uncertainty carried into CEP · mass → named levers + range-retention gate · GNSS contested → degradation ladder + beacon/seeker options · thermal → designed interface (**≥ 58 W/K** need vs bare thread **3–16 W/K**), rig closes it.
- **Validation plan:** 7-DOF simulation + Monte Carlo (**5,000 design + 5×1,000 corners, worst-corner 95 % bound**) · hardware-in-the-loop · rotating dynamometer rig (**plan, not an asset**) · integration demonstrator.
- **Standards:** MIL-STD-1316 · 331C · 810F · 461 · AOP-22 Ed B Ver 1 · STANAG 4369/AOP-39 · 4439 · 9216/MIL-STD-333B.
- **Manufacturability:** two-tier process at **5,000 kits/yr** · one moving assembly · no shell re-qualification · tooling amortisation stated; candidate processes live in the process dossier and are **validated post-selection** (no process numbers on the slide).
- **Visual:** error-budget waterfall (fig2-error-budget.svg) + authority chart (fig3-canard-authority.svg) + a CAD section (10/11).

## Slide 5 — IMPACT AND BENEFITS

- **Business first (SIH weights business potential):** **≤ ₹6.5 lakh (≈ US$7,800)** recurring per kit at 5,000/yr vs the fielded **US$13,541** (≈ 40 % below) — development and tooling excluded; **the priced cost roll-up follows selection**. Volume basis stated honestly (fielded > 100,000 units; 5,000/yr is the certified-volume assumption).
- **Operational payoff:** **301 → 77 rounds** and **959 → 208 charges** per target (the fielded programme's published figures); no adjustment fire; less collateral and less battery exposure; our derived **≈ 23.9 m** sits beside these.
- **Buyer = existing shell procurer** — existing channel, no new platform, no new training.
- **Indigenous content:** YIL mechanical core (ring + canards one datum, stator, winding, housing; MIM candidates) · bounded additions · GBD magnets = less heavy rare earth, not more.
- **Safety:** F16 predicted-miss discipline — where it was not aimed, it does not function.
- **Future progression — options, never delivered capability:** anti-jam GNSS module · cooperative beacon fix · fielded-type SAL seeker · other calibres, via a **reserved module interface (its mechanical and electrical definition is post-selection work)**.
- **Visual:** unit-economics bar · rounds/charges before-after · production/supply picture.

## Slide 6 — RESEARCH AND REFERENCES

Curated two-column list (no criterion IDs, no status tags). Credits the lineage:

1. G. Gunay, M.Sc. thesis, METU, 2022 — de-spun alternator-actuator architecture.
2. X. Zhang, X. Yao, Q. Zheng, Chinese J. Aeronautics, 2019 — IPP for dual-spin fixed canards.
3. G. Clancy, T. Bybee, W. Friedrich, **US Patent 6,981,672**, 2006 (expired) — fixed-canard 2-D guidance.
4. Orbital ATK, NDIA Armament Systems Forum, 2015 — fielded PGK program update + dispersion record.
5. M1156 Precision Guidance Kit — public programme record (US Army PM-CAS).
6. Elbit Systems, Silver Bullet II brochure — three-mode fuzing at parity.
7. R. Jaiswal, M. Kothari, A. Abhishek, AIAA 2024-1105 — canard-guided fuze two-pair arrangement.
8. NATO AOP-22 Ed B Ver 1, 2018 — inductive setting + command mode.
9. MIL-STD-1316 / 331C / 810F / 461 · STANAG 4369/AOP-39 · 4439 · 9216/MIL-STD-333B.
10. Problem statement SIH26098 (MoD / Yantra India Limited), SIH 2026.
11. NATO STO-EN-SET-197-08 — beacon / pseudolite aiding.
12. IEEE 2018 — approximate statistical moments for impact-point prediction.

## Figure set (flowcharts + CAD — your chosen set)

| Type | File | Use |
|---|---|---|
| Flow / block | `submission/deck/figures/fig4-system-flowchart.svg`/.png | **REQUIRED — the PS's electronics block-diagram deliverable**; slide 3 |
| Flow / block | `design/atlas/out/flow.svg` (also .png) | systems flow — slide 2 or 3 |
| Flow / block | `design/11-system-architecture.html` | redraw/screenshot, three tiers — slide 3 |
| CAD | `submission/deck/figures/cad/` — 01, 04, 05, 10, 11, 12, 14, 16, 17, 18, 19, 21 | slides 2–4 (assembly, sections, exploded, ring+canards, bearing path, electronics stack, fuze train) |
| Spares (data) | `fig1-dispersion.svg`, `fig2-error-budget.svg`, `fig3-canard-authority.svg` | slides 1/4 if a chart is wanted |

## Style + export

- Two typefaces: one sans for prose, one **mono for every number/unit**.
- Three colours + greys (old palette accent `#0b5cad` if you want continuity).
- Fonts embedded on export; **PDF, exactly 6 pages, within the portal's size cap**.

## Pre-export checklist

- [ ] Title-page fields filled (PS ID · PS title verbatim · theme · category · Team ID · Team Name · idea title)
- [ ] Template section headings / idea-detail pointers unchanged; **instructions slide deleted**; exactly 6 pages
- [ ] **fig4-system-flowchart embedded**
- [ ] No placeholders (`⟨…⟩`) · no criterion IDs · no status tags on slides (honesty stays in words: "derived", "target", "not yet met", "follows selection")
- [ ] Forbidden values absent everywhere: `20.4` / `~24 m` budget · `1.4-1.7 kg class` · `1.0-1.21` / `1.55-2.2` ratios · `74 kN` · `400 V` (except the "cannot store it" comparison) · `15,000–20,000 rpm` · "defined module interface" · unopened process numbers (`79%`/`87% IACS`, `98% IACS`, `368 W/mK`, "third of the winding-head", "one per cent of the kit's mass") · "resonance dispositioned" as settled · t ≈ 15 s · iron-loss 50–60 W
- [ ] Credit rule: the two-pair split and the alternator-as-actuator credited as lineage (M1156 / US 6,981,672) wherever they appear
- [ ] Every number matches the canonical table (`notes/07` Step 1) and the QA consistency list
