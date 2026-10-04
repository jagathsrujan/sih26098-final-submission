# 07 — Deck slide content (6-slide official template, manual Figma/Canva build)

Living content file — grown one slide per approved round (2 → 3 → 4 → 5 → QA). Numbers are the locked canonical set (`notes/07` Step 1) with inline honesty wording. Companion: `08-flowchart-spec.md` (the centerpiece chart) · `05-upload-qa-checklist.md` · `06-judge-defense-brief.md`. Character counts python-verified 2026-10-02.

**Ground rules (every slide):** only canonical numbers with honesty wording · never-say list (`06`) · nothing from `notes/08` section A · credit lineage (M1156 / US 6,981,672, 2006, expired) wherever two-pair canards or alternator-as-actuator appear · **no criterion IDs or status tags — including "F16"** (register row ID → printed as "predicted-miss withhold") · only placeholder anywhere = `⟨Team ID/Name⟩` (slide 1) · points/diagrams only, no paragraphs · template section headings / idea-detail pointers unchanged · exactly 6 pages, instructions slide deleted.

---

## Master figure plan

| Figure (repo2, read-only) | Slide | Role |
|---|---|---|
| Centerpiece flowchart (redraw per `08`) | 3, tall left column ≈600×648 | Full trajectory timeline + in-flight functioning in one read; slide 2 carries the pointer chip |
| `fig4-system-flowchart.svg/.png` (660×518 native) | 3, top-right ≈620×487 | **REQUIRED** PS electronics block-diagram deliverable (flight chain / power / fuze lanes + computer strip) |
| `cad/14-part-ring-canards.png` + `15` inset | 2, hero | Force pair vs torque pair roles |
| `cad/18-part-bearing-path.png` | 2 | Bearing-isolated de-spin + setback load path |
| `cad/16-part-stator-windings.png` + `17-part-rotor-magnets.png` | 2 | Rotor/stator = generator & actuator (fallback: `11-section-machine`) |
| `cad/05-shell-kit-section.png` | 3, thumb strip | Thermal path through the fuze well |
| `cad/21-part-fuze-train.png` | 3, thumb strip | Fuze train + out-of-line S&A |
| `cad/19-part-electronics-stack.png` | 3, thumb strip | Electronics stack |
| Spares: `fig2-error-budget`, `fig3-canard-authority`, `fig1-dispersion`, `01/04-assembly` | 5, trim bank | slide 4 = tables 1–3 + `10-section-through-axis` (permanent, round 4 — fig2/fig3 retired) · slide 5 = 04 or 01 |

CAD PNGs: 16:9 ~2400×1350, white background, gate-checked solids. Numbers visible in renders (124.70 mm intrusion, 0.400 mm air gap, cant) are interface verifications — **none print**.

---

## Slide 1 — TITLE PAGE (fill-in card only — no design)

PS ID `SIH26098` · PS title (verbatim from portal) · Theme `Smart Vehicles` · Category `Hardware` · Team ID / Team Name `⟨from portal⟩` · Idea Title `STHIRA-PGK: De-Spun Canard Guidance Kit with Multi-Mode Smart Fuze for 155 mm Shells` (84/100).

---

## Slide 2 — IDEA TITLE & PROPOSED SOLUTION *(status: DELIVERED round 1, approved plan)*

### Bullet text (paste-ready; counts python-verified)

| Zone | # | Text | chars |
|---|---|---|---|
| Header | — | `STHIRA-PGK — a de-spun canard guidance kit with an integrated multi-mode fuze` | 77 |
| **The problem** | A1 | `Dispersion grows with range — published record for the fielded class: 94 / 125 / 150 → 267 m CEP against the ≤ 30 m the requirement demands` | 139 |
| | A2 | `Volume fire costs rounds, time on station, collateral exposure and battery time` | 79 |
| | A3 | `YIL already manufactures the shell hardware — the missing capability is the kit` | 79 |
| | A4 | `Retrofit only: fuze well + forward ogive — no shell re-qualification` | 68 |
| **The solution** | B1 | `Four fixed canards on a bearing-isolated de-spun ring — zero moving control surfaces` | 84 |
| | B2 | `0°/180° equal-cant pair: net guidance force = 2× one canard; roll torques cancel` | 80 |
| | B3 | `90°/−90° opposite-cant pair: net roll torque; zero net force` | 60 |
| | B4 | `Ring roll angle aims the force vector — 2-D steering from one actuation axis` | 76 |
| | B5 | `The alternator is the actuator (magnets on ring, coils on body) — no servos, gearboxes or linkages` | 98 |
| | B6 | `No flight battery — the alternator powers the flight; supercapacitor buffer for motoring bursts; reserve battery for pre-launch and safe state only` | 147 |
| | B7 | `Multi-mode fuze (proximity / time / impact) set over the existing AOP-22 inductive setter` | 89 |
| **Innovation and uniqueness** | C1 | `Loaded-generator sizing: 2.92 kW peak / ≈121 kJ per flight — derived sizing figures; the rig confirms them` | 106 |
| | C2 | `Declared thermal path through the fuze well: ≥58 W/K needed vs 3–16 W/K bare thread — a designed interface; the rig closes it` | 125 |
| | C3 | `The de-spun ring is the inertial platform — pickoff + magnetometer; spin-axis GNSS aperture` | 91 |
| | C4 | `In-flight error estimator — bias estimation is established; the integration is ours` | 83 |
| | C5 | `State-dependent authority gate — turns the apogee torque collapse into a designed constraint` | 92 |
| | C6 | `Predicted-miss withhold: predicted miss > 150 m → function withheld, latched, dud-direction` | 91 |
| Credit block | — | `Lineage, credited — the two-pair canard split and the alternator-as-actuator are the fielded M1156 specification, claimed in US 6,981,672 (2006, expired). The engineering that makes it close is ours.` | 199 |
| Pointer chip | — | `▸ full flight-function chart — slide 3` | 38 |

Bullets A–C = 1,587 chars · header+credit+pointer = 314 · callouts = 645 · **slide 2 total = 2,546**.

Number honesty map: 94/125/150/267 m + ≤30 m → "published record for the fielded class" (never YIL) · 2× and 0°/180°/90°/−90° → geometry, credited via credit block · 2.92 kW/≈121 kJ → "derived sizing figures; the rig confirms them" · ≥58 W/K vs 3–16 W/K → "a designed interface; the rig closes it" · 150 m → decided figure, printed plain (label "F16" forbidden) · 10,000–20,000 rpm (callout k5) → "(class band)".

### Wireframe (1280×720)

```
┌────────────────────────────────────────────────────────────────────────┐
│ HEADER: title line (77 ch)                     [▸ chart — slide 3]     │ y 0–48
├───────────────────────────────┬────────────────────────────────────────┤
│ THE PROBLEM   A1 A2 A3 A4     │ HERO: 14-part-ring-canards (~3:2)      │ y 56–350
│ THE SOLUTION  B1 … B7         │ callouts k1 k2 k3 · [15-inset: k4]     │
│ INNOVATION AND UNIQUENESS     ├───────────────────────┬────────────────┤
│                 C1 … C6       │ 18-bearing-path (4:3) │ 16 stator +    │ y 362–580
│                               │ callouts k5 k6 k7     │ 17 rotor       │
│                               │                       │ k8 k9 k10      │
├───────────────────────────────┴───────────────────────┴────────────────┤
│ CREDIT BLOCK (ruled box)                                              │ y 590–704
└────────────────────────────────────────────────────────────────────────┘
Left col x 20–628 (bullets, ~13 px, mono for numbers) · Right col x 644–1260 (CAD) · hero 620×290 · insets 302×218.
```

### Figure specs — slide 2

**F2-1 hero — `cad/14-part-ring-canards.png` + `15-part-canard.png` inset.** Crop: ring group centred, ~3:2, 8% margin. Teaches: the two-pair role split on one physical part.
- k1 (80) `Steering pair 0°/180° — equal cant: net force 2× one canard, roll torques cancel`
- k2 (70) `Control pair 90°/−90° — opposite cant: net roll torque, zero net force`
- k3 (66) `Ring carrier — rotates to aim the force vector; one actuation axis`
- k4 (35, on 15-inset) `cant angle splits force from torque`

**F2-2 — `cad/18-part-bearing-path.png`.** Crop: bearing stack + retention collar, 4:3. Teaches: bearing-isolated de-spin and the setback load path.
- k5 (86) `Flight bearings isolate the de-spun ring from 10,000–20,000 rpm body spin (class band)`
- k6 (63) `Setback load path routes around the bearings — continuous metal`
- k7 (63) `Retention collar — one rotating assembly; no servos or linkages`

**F2-3 — `cad/16-part-stator-windings.png` + `17-part-rotor-magnets.png` side by side** (fallback `11-section-machine.png`). Teaches: the machine is generator and actuator.
- k8 (50) `Rotor — magnets carried by the rotating ring group`
- k9 (71) `Stator — coils on the body: generates to the bus and drives ring torque`
- k10 (61) `generator and actuator in one — lineage: M1156 / US 6,981,672`

---

## Slide 3 — TECHNICAL APPROACH *(status: DELIVERED round 2; density decision = thumbs 205×104 strip + fig4 ~0.9×)*

### Bullet text (paste-ready; python-verified)

S1–S5 under the template pointer **"technologies used"** · S6–S11 under **"methodology and process of implementation"**.

| # | Text | chars |
|---|---|---|
| S1 | `Flight computer: STM32-class dual MCU — one core bare-metal at 1 kHz control; second core nav + GNSS` | 100 |
| S2 | `Sensing: GNSS + IMU + baro + ring angle (pickoff + magnetometer)` | 64 |
| S3 | `Power: three-phase rectification + four-quadrant stage · supercapacitor buffer · 180 V bus` | 90 |
| S4 | `Setting: the existing AOP-22 inductive chain — mode, ToF, target, MV, met` | 73 |
| S5 | `Build tools: FreeCAD CAD (gate-checked) · embedded C · 7-DOF simulation · HIL · dynamometer rig` | 95 |
| S6 | `IPP guidance — propagate → compare → command ring angle — credited to published work` | 84 |
| S7 | `Ours in the loop: the state-dependent authority gate + error-estimator integration` | 82 |
| S8 | `The ring is the inertial platform — ours to prove; the bench programme is tasked with proving it` | 96 |
| S9 | `Span-capped canard ring: resonance is an open item — evidence closes in the 7-DOF campaign` | 90 |
| S10 | `Process: 7-DOF Monte Carlo with guidance in the loop → HIL → rotating dynamometer rig (plan, not an asset) → integration demonstrator` | 133 |
| S11 | `GNSS-denied: coast on inertial to the drift limit (outage tolerance set in the campaign); anti-jam GNSS is a module-level substitution` | 134 |

Bullets = 1,041 chars (11) · callouts = 264 (6) · **slide 3 total = 1,305**.

Number honesty map: 1 kHz and 180 V → canonical, printed plain · ≥58 W/K vs 3–16 W/K → "designed interface, rig closes it" (callout h2) · 7-DOF = method name · no MC run counts on this slide (they live slide 4) · no ring-sensing "solved" claims (S8 carries "ours to prove") · resonance never "solved" (S9).

### Wireframe (1280×720)

```
┌────────────────────────┬─────────────────────────────┐
│ CHART (per 08-spec,    │ fig4-system-flowchart        │
│ tall variant)          │ 561×440 (0.85×; grow toward  │
│ 600×528                │ 620×487 as text allows;      │
│ x 16–616 y 56–584      │ never upscale > 1.0×)        │
│                        │ x 632–1193 y 56–496          │
│                        ├─────────────────────────────┤
│                        │ bullets S1–S11               │
├───────┬──────┬─────────┤ x 632–1264 y 506–704        │
│ 05    │ 21   │ 19      │ 12–12.5 px, mono for numbers │
│ 205×104 thumbs          │ two groups under the         │
│ x 16–640 y 596–700      │ template's two pointers      │
└───────┴──────┴─────────┴─────────────────────────────┘
```

Trim ladder if it doesn't fit at export: (1) drop S10's parenthetical to "rig (plan, not asset)", (2) fig4 stays 0.85×, (3) merge S6+S7 into one line, (4) last resort: move 05+19 to slide 4, keep 21.

### Figure specs — slide 3

**F3-0 — the centerpiece chart:** `08-flowchart-spec.md`, tall variant at 600×528 (tight vs the 648 target: fold N1/N2 into one launch-and-de-spin band or take sub-notes to 7.5 px — edge labels carry the detail). This is where "launch → … → impact" is read in one pass; slide 2's pointer chip leads here.

**F3-1 — `fig4-system-flowchart.svg/.png`:** REQUIRED (the PS's electronics block-diagram deliverable). 660×518 native, no cropping, its own title and lane labels stay. Nominal 0.85× (561×440); grow toward 0.94× if the bullets trim. Embed the scrubbed `../deck-assets/fig4-system-flowchart-clean.svg`, never the repo2 original.

**F3-2 — thumb `cad/05-shell-kit-section.png`** (crop: fuze-well/thread region). Teaches: the declared thermal path into the shell.
- h1 (36) `heat path: fuze-well threads → shell`
- h2 (67) `≥58 W/K vs 3–16 W/K bare thread — designed interface, rig closes it`

**F3-3 — thumb `cad/21-part-fuze-train.png`** (crop: the on-axis train). Teaches: S&A logic, not decoration.
- h3 (46) `out-of-line S&A: rotor in line only when armed`
- h4 (31) `dual interlocks: setback + spin`

**F3-4 — thumb `cad/19-part-electronics-stack.png`** (crop: stack as laid out). Teaches: what the electronics physically contain and the one-way fuze link.
- h5 (47) `avionics · dump resistor · buffer · setter coil`
- h6 (37) `one-way arming-gated link to the fuze`

## Slide 4 — FEASIBILITY AND VIABILITY *(status: REVISED round 4 — figure direction: tables + CAD, no synthetic charts; fig2/fig3 retired)*

### Bullet text (paste-ready; python-verified)

F1–F8 under the template pointer **"feasibility analysis"** · R1–R4 under **"potential challenges and risks · strategies for overcoming them"**. Round-4 ruling: **the tables own the numbers** — bullets carry framing and honesty only; every number prints once.

| # | Text | chars |
|---|---|---|
| F1 | `Error budget closes under the requirement — derived terms, combined in RSS (table 1)` | 84 |
| F2 | `Guidance margin — derived figures; the guided-window analysis re-quantifies them (table 2)` | 90 |
| F3 | `Mass — CAD analysis, not a weighed article; the target class is not yet met (table 2)` | 85 |
| F4 | `Gate: retain > 90 % of the conventional round's maximum range` | 61 |
| F5 | `Validation: 7-DOF Monte Carlo — 5,000 design + 5×1,000 corners, worst-corner 95 % bound — then HIL, rotating dynamometer rig (plan, not an asset), integration demonstrator` | 171 |
| F6 | `Standards: MIL-STD-1316 · 331C · 810F · 461 · AOP-22 Ed B Ver 1 · STANAG 4369/AOP-39 · 4439 · 9216/MIL-STD-333B` | 111 |
| F7 | `Manufacturing: two-tier process at 5,000 kits/yr — one moving assembly, no shell re-qualification, tooling amortised; candidate processes validated post-selection` | 162 |
| F8 | `Published precedent sits beside ours in table 3 — credited results; full references on slide 6` | 94 |
| R1 | `Aerodynamic coefficient set is the acknowledged long pole → published data + CFD fill the gaps, uncertainty carried into the CEP budget` | 135 |
| R2 | `Mass trade → named levers; the > 90 % range-retention gate decides` | 66 |
| R3 | `GNSS contested → inertial coast to the drift limit; anti-jam GNSS as a module substitution; growth modules are options, never delivered capability` | 146 |
| R4 | `Thermal duty — 2.92 kW peak / ≈ 121 kJ per flight (derived sizing figures) → designed interface ≥ 58 W/K vs 3–16 W/K bare thread; the rig closes it` | 147 |

Bullets = 1,352 chars (12) · table rows = 753 (14) · titles + captions + footnote + callouts = 517 · **slide 4 total = 2,622** (round 3: 1,937 — the numbers moved from prose into typeset rows; prose fell 1,708 → 1,352).

Cut/merge record vs round 3: old F1/F2/F3/F5 numbers → tables 1–2 · old F4 → table 2 "Correction" row (`a margin, not comfort` stays attached to 1.11:1) · old F6 levers → table 2 "Target class" row · gate stays in F4 only (R2 echo, approved round 3) · **fig2 + fig3 retired from the deck** (repo2 untouched; `deck-assets/fig3-canard-authority-clean.svg` kept as a spare).

Number honesty map: 5/17/5/8/3 → 20.3 → 23.9 vs ≤ 30 → table 1 caption `derived budget — the 7-DOF Monte Carlo produces the flight CEP` · 3.7/3.0/2.0/1.0 → table 1 footnote `derived sub-allocation` · ≥ 18.1 N · 450/407/80 %/1.11:1 → table 2 (`derived figures — the guided-window analysis re-quantifies them`; `a margin, not comfort`) · 2.7/4.8 kg · +1.7 kg · 3.9 % · 45.0 kg → `CAD analysis, not a weighed article` · 1.4 kg · −0.59 kg → `not yet met — levers named` · > 90 % = requirement gate (plain) · MC counts = plan values ("worst-corner 95 % bound") · 2.92 kW / ≈121 kJ → "derived sizing figures" · 58/3–16 W/K → "designed interface; the rig closes it" · 382 kN → "(derived)" (c10a) · 206 m / 24.73 m / 50-run / ≈ 27 km → **published third-party figures, cited in table 3** (status "published" printed in its caption). **No time values anywhere** — the guided window is gate-computed.

### Wireframe (1280×720)

```
┌────────────────────────────────────┬──────────────────────────────┐
│ FEASIBILITY ANALYSIS               │ T1 — error budget (2-col)     │
│   F1 … F8                          │  7 rows · x676–1242 y56–262  │
│ POTENTIAL CHALLENGES AND RISKS →   ├──────────────────────────────┤
│   R1 … R4                          │ T2 — guidance margin & mass   │
│ x20–660 y56–405 (12–12.5 px,       │  3-col · 5 rows y312–487     │
│ mono for numbers, hyphen bullets)  ├──────────────────────────────┤
│                                    │ T3 — published precedent      │
│ 10-section CAD (contain — never    │  3-col · 2 rows y537–652     │
│  cropped) 620×284 · x20 y420       │  credits in the ref column    │
│  callouts c10a c10b in the margin  │  50 px rhythm between blocks  │
└────────────────────────────────────┴──────────────────────────────┘
```

Positions measured (DOM eval, round-4 hotfix): bullets end y404 · figure y420–704 · table blocks 56–262 / 312–487 / 537–652 (gaps 50/50, bottom slack 52). Trim ladder: (1) T3 collapses to two credited lines under table 1 (grid dropped), (2) the CAD figure trims in height to 620×220 (contain — never cropped), (3) F5 parenthetical → "rig (plan, not asset)", (4) last resort: merge F2+F3.

### Figure / table specs — slide 4

**F4-1 — Table 1 "error budget" (replaces `fig2-error-budget`; fig2 retired).** Typeset text — no image file. 2 columns (Term | 1σ (m)), mono for numbers, thin rules top / under header / above RSS only.
- Rows: `Navigation | 5` (14) · `Guidance & control | 17` (23) · `Meteorology | 5` (15) · `Aero-ballistic | 8` (18) · `Fuze | 3` (8) · `RSS | 20.3` (10) · `CEP | ≈ 23.9 vs ≤ 30 m required` (31)
- Title (49): `Table 1 — error budget — 1σ terms combined in RSS`
- Caption (62): `derived budget — the 7-DOF Monte Carlo produces the flight CEP`
- Footnote (100): `navigation carries a derived 3.7 m sub-allocation — GNSS 3.0 / IMU + filter 2.0 / timing + lever 1.0`

**F4-2 — Table 2 "guidance margin & mass" (replaces `fig3-canard-authority`; fig3 retired).** 3 columns (Check | Figure | Note), mono for numbers.
- Rows: `Guidance force | ≥ 18.1 N minimum over the guided window` (56) · `Correction | 450 m available vs 407 m required (80 % capture) → 1.11:1 | a margin, not comfort` (94) · `Kit mass | ≈ 2.7 kg aluminium (4.8 kg steel) | CAD analysis, not a weighed article` (82) · `Round effect | +1.7 kg ≈ 3.9 % of the 45.0 kg round | CAD analysis` (66) · `Target class | 1.4 kg | not yet met — levers: material, ring diameter, retention (spigot −0.59 kg banked)` (105)
- Title (32): `Table 2 — guidance margin & mass`
- Caption (63): `derived figures — the guided-window analysis re-quantifies them`

**F4-3 — Table 3 "published precedent (credited)" (new — the research-paper element).** 3 columns (Published result | Figure | Reference), reference column 8–9 px italic.
- Rows: `IPP-corrected 155 mm — 50-run Monte Carlo | uncontrolled 206 m → 24.73 m CEP | Zhang, Yao & Zheng, Chin. J. Aeronaut., 2019` (123) · `Perturbation-IPP 155 mm — Monte Carlo | CEP ≤ 30 m at ≈ 27 km | Yi Wang et al., Int. J. Aerospace Eng., 2015` (108)
- Title (40): `Table 3 — published precedent (credited)`
- Caption (66): `the ≤ 30 m claim has published precedent — cited results, not ours`
- **Redraw policy (round-4 ruling):** tables print as typeset text; any future research **curve** (slide 5 candidates) is redrawn as clean vector `after Author year` with a credit caption — never a scanned crop (foreign numbers cannot be scrubbed).

**F4-4 — `cad/10-section-through-axis.png`, full canvas (2334×1313) contained at 620×284, x20 y420 — never cropped** (round-4 hotfix; the earlier 566×88 cover strip sliced the machine). The machine sits tall in the canvas centre; callouts sit in the left white margin, clear of the part. Permanent since round 4 (was trim bank). Teaches: the setback load path and the single-axis stack (machine · bearing · train bore · buffer).
- c10a (54) `382 kN axial setback (derived) — continuous metal path`
- c10b (51) `machine · bearing · train bore · buffer on one axis`

**Print note (all tables):** headers print exactly as listed — no case transform anywhere (CSS uppercase renders `1σ (m)` as `1Σ (M)`, a print-integrity break; found and fixed in the round-4 hotfix).

**Slide-3 figure note (updated):** embed `../deck-assets/fig4-system-flowchart-clean.svg` — scrub applied: criterion IDs (`[H1, G17]`-style) out · `F7 / F8 thresholds OPEN` → `thresholds at hardware definition` · `≥58 W/K at the well — OPEN` → `… rig closes it` · non-canonical numbers cut (275 ms, 231 V, 24 GHz, 480/240 MHz, 150–200 J, ≈20:1, ≈12 W, 0.5–1.5 W, ≥1 J, +5.8 K, 10°, Ø30 mm, 0.1–199.9 s) · lineage credit footer added. Never embed the repo2 original on a slide. Repo2 untouched; patch proposals in `notes/09`.

## Slide 5 — IMPACT AND BENEFITS *(status: skeleton — text delivered round 4)*

- Business first: ≤ ₹6.5 lakh (≈ US$7,800) recurring per kit at 5,000/yr vs fielded US$13,541 (≈ 40 % below) — development + tooling excluded; "the priced cost roll-up follows selection"; volume gap disclosed (fielded > 100,000 units at scale; 5,000/yr is the certified-volume assumption).
- Operational: 301 → 77 rounds and 959 → 208 charges per target (fielded programme's published figures); our derived ≈ 23.9 m beside these; no adjustment fire; less collateral, less battery exposure.
- Buyer = existing shell procurer — existing channel, no new platform, no new training. Indigenous content: YIL mechanical core (ring + canards one datum, stator, winding, housing; MIM candidates); GBD magnets = less heavy rare earth, not more.
- Safety: predicted-miss withhold — "where it was not aimed, it does not function".
- Future progression — "options, never delivered capability": anti-jam GNSS module · cooperative beacon fix · fielded-type SAL seeker · other calibres, via a reserved module interface (its mechanical and electrical definition is post-selection work).
- Figures: 04-shell-kit-iso (installed on the ghosted shell) or 01-assembly-iso; unit-economics bar; rounds/charges before-after.

## Slide 6 — RESEARCH AND REFERENCES *(status: keep as-is)*

The curated 12 from `04-deck-brief.md`, two columns, no IDs, no status tags. Trim order only if space forces: (1) compress entry 9 (standards) to one line, (2) merge 4+5, (3) drop 10 (PS reference implicit).
