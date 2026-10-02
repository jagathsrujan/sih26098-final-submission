# 07 — Submission phase log (submission-only final design, Steps 0–6)

Running log for the submission-only design phase (started 2026-10-02). One step per exchange; the user approves before the next step. Authority order: repo2 `design/00-design-criteria-register.md` ≻ evidence (CAD/atlas/sim) ≻ notes. Nothing unruled or provisional prints as fact; every number carries value → status/source → closer. No CAD work; no edits to the design repo (patch proposals only); no new physical claims; no deck production (content pack only).

Companion files: `notes/03-submission-decisions.md` (locked decisions + built resources) · `notes/00-INDEX.md` (traps) · `notes/05-research-digests.md` (paper digests QB1–12).

---

## Step 0 — 2026-10-02 — intake & loose-end inventory

Run as two parallel deepseek subagent passes (requirements research; claim-to-source mapping) plus direct reads of `notes/00–05` and `submission-resources/`. Status: **closed — user approved with "go" on 2026-10-02; no objections to rulings R1–R9.**

### A. Submission-round requirements (restated, verified where possible)

**Fields and limits**

| Field | Limit | Verdict |
|---|---|---|
| Idea Title | ≤ 100 characters | Corroborated (portal-enforced; not in official docs) |
| Abstract / Summary | ≤ 10,000 characters | Corroborated |
| Idea Description | ≤ 50,000 characters | Corroborated |
| Idea Template | Official template, **max 6 slides incl. title**, **PDF only** (no PPT/Word), delete the 7th instructions slide, don't alter idea-detail pointers | **Confirmed** (official template instructions) |
| Template file size | "≤ 10 MB" | **UNCONFIRMED** — third-party figure only; verify on portal |
| YouTube link | Optional | Corroborated — currently **skipped** (decision #5) |

**Official template slide map (in order):** 1 TITLE PAGE (PS ID, PS title, theme, PS category, Team ID, Team Name, Idea Title) · 2 IDEA TITLE & PROPOSED SOLUTION (solution, how it addresses the problem, innovation/uniqueness) · 3 TECHNICAL APPROACH (technologies, methodology/process) · 4 FEASIBILITY AND VIABILITY (feasibility, challenges/risks, mitigation) · 5 IMPACT AND BENEFITS (impact on target audience, benefits) · 6 RESEARCH AND REFERENCES (reference/research details and links). Points/diagrams/infographics only — no paragraphs. (Team's `form-content.md` labels the six as Problem Statement / Proposed Solution / Technical Approach / Feasibility Analysis / Impact Assessment / References — functionally identical.)

**Portal fields:** PS selection (SIH26098) · theme/technology bucket · Idea Title · Abstract · Idea Description · template PDF upload · optional YouTube. Team ID / Team Name / members pre-filled via College SPOC; leader verifies team name, authorization letter, member details. Only confirmable on the portal: exact char counters, upload size cap, bucket dropdown contents, editable-vs-display-only fields, exact cut-off time.

**Evaluation criteria (official, SIH 2026 Guidelines):** "novelty of the idea, complexity, clarity and details in the prescribed format, feasibility, practicability, sustainability, scale of impact, user experience and potential for future work progression." **No official weightages published** (circulating rubrics are third-party and one is wrong on slide count — ignore). Business potential carries extra weight (per the internal judge dossier). ~4–5 teams per PS shortlisted; PS org not obliged to declare a winner. Rules: 500-idea cap per PS (SIH26098 at ~109/500 on a 1 Oct mirror), max 2 PS per team, SPOC/leader submits.

**Deadline (time-critical):** extended to **5 October 2026** (was 30 Sep; repo1's 20 Sep tracker is stale). **02–05 Oct one-time edit window** for Team Name, Consent, and the PPT only — not the abstract/description text. Exact cut-off time not published — **confirm on portal**. Today = 2 Oct → Steps 1–5 are pre-upload work.

**Theme conflict resolved:** "Smart Vehicles" is an official SIH 2026 theme (17-theme list) and SIH26098 is listed as **Hardware / Smart Vehicles** → `draft-from-register.md` ("Defence and Security") and the analyst's "Miscellaneous" are wrong. Copy the portal value character-for-character at upload regardless.

**Sources (condensed):** sih.gov.in/letters/2026/SIH 2026 Guidelines.pdf · sih.gov.in homepage banner (extension) · sih.gov.in/letters/2026/SIH2026-IDEA-Presentation-Format.pptx · MOE Innovation Cell announcement · mirrors: sih2026.vuce.in/ps/SIH26098 + /themes, github.com/AyushPatel-Hub/SIH, sih-lemon-eight.vercel.app/rules. sih.gov.in itself was 504-ing during research; facts came from official-URL snippets + mirrors — re-verify on the portal.

### B. Claim inventory — four fields (203 claims; every numeric claim mapped)

Authority shorthand: `reg <ID>` = register row + status (DEFINED / DERIVED / PARAMETRIC / OPEN / PROPOSED); `SR <id>` = `design/05-source-register.md`; `T1–T10` = `design/07-cad-evidence.md`; digest = `notes/05-research-digests.md`; `mfg` = `design/06-manufacturing-and-process.md`; `sim` = repo1 `cleansheet/out_sim/RESULTS_GNC.md`.

Counts: Title 2 · Abstract 48 · Description 104 · Deck+QA 49.

#### B1 — Idea Title
| # | Claim | Value | Source + status | Closer |
|---|---|---|---|---|
| 1.1 | Title string (option A) | `STHIRA-PGK: De-Spun Canard Guidance Kit with Multi-Mode Smart Fuze for 155 mm Shells` | notes/03 decision R1 #1 (locked) | Portal title field |
| 1.2 | Title length | 85 (deck brief) vs ~84 (QA) | internal | Portal counter; store one number in Step 1 |

#### B2 — Abstract (`01-abstract.txt`)
| # | Claim (exact) | Source + status | Closer |
|---|---|---|---|
| 2.1 | 94 m CEP at intermediate ranges | SR A1 (Orbital ATK NDIA 2015; Cite 5 / Adopt 4) | — |
| 2.2 | 267 m at maximum range | reg M6 PARAMETRIC (≈227 m σ); SR A1 | YIL firing tables (post-sel 3) |
| 2.3 | 30 m guided | reg M4/M5 (PS requirement) | — |
| 2.4 | YIL makes the mechanical hardware | SR A8 + PS | post-selection |
| 2.5 | Four fixed canards on de-spun ring, two bearings | reg C1, C31, G2 DEFINED | — |
| 2.6 | 0°/180° equal cant → net force 2× single, roll torques cancel | reg C1 DEFINED (2·F·sin δ_s), C9 | — |
| 2.7 | 90°/−90° opposite cant → zero net force, net roll torque | reg C1 DEFINED | — |
| 2.8 | Ring rotation aims force vector anywhere in-plane → 2-D steering, one axis | reg G2, C1 DEFINED | — |
| 2.9 | Magnets on ring, coils on body (alternator = actuator) | reg C34, C9 | — |
| 2.10 | No servos/gearboxes/linkages; no flight battery | reg C1 DEFINED, W4/W5 | — |
| 2.11 | Supercapacitor buffer for motoring bursts | reg W4 DERIVED | — |
| 2.12 | Reserve battery pre-launch + safe state only | reg W5 OPEN (scope fixed) | chemistry P4 |
| 2.13 | IPP guidance (propagate → compare → command) | reg G1 DEFINED | — |
| 2.14 | GNSS/INS + baro + onboard aero model | reg N1, N3, N6, N11 | N11 OPEN (baro) |
| 2.15 | "15,000–20,000 rpm … no flight-representative MEMS gyroscope can measure" | reg S6 PARAMETRIC = 10,578–18,264 rpm | **contradiction → fix** |
| 2.16 | In-flight estimator learns MV error, drag bias, wind | reg G17 DEFINED (29 Sep) | P3/R5 |
| 2.17 | Multi-mode fuze: proximity, time, impact | reg F1 DEFINED | — |
| 2.18 | Out-of-line S&A interlocked on setback and spin | reg F6 DEFINED | — |
| 2.19 | Set over existing inductive setter | reg F11 PARAMETRIC, F12 DEFINED | risk 44 (H11) |
| 2.20 | Withhold when predicted miss > 150 m | reg F16 DEFINED (20 Sep) | — |
| 2.21 | Budget closes 20.3 m RSS | reg G4 DEFINED | R5 |
| 2.22 | nav 5 / G&C 17 / meteo 5 / aero 8 / fuze 3 | reg G4 DEFINED (√(25+289+25+64+9)) | R5 |
| 2.23 | CEP ≈ 23.9 m (1.1774 × 20.3) vs 30 m | reg G4, M5 | R5 |
| 2.24 | ≥ 18.1 N across guided window | reg C8 DERIVED (provisional) | R5 |
| 2.25 | 450 m of impact correction | reg M7 DERIVED (provisional) | R5 |
| 2.26 | 407 m required, 80 % capture | reg M7 DERIVED | R5 |
| 2.27 | Margin 1.11:1 | reg M7 DERIVED | R5 |
| 2.28 | Verification L1: 7-DOF sim, guidance in the loop | reg R5/§10.1 | P3 |
| 2.29 | MC dispersion analysis produces the CEP | reg R5 DEFINED | P3 |
| 2.30 | HIL bench, rotating dynamometer rig | reg R7 DEFINED (rig parked) | P7 |
| 2.31 | PoC ring-angle tracking under load | reg R7/§14 | P7 |
| 2.32 | Mass ≈ 2.7 kg (Cu-and-Al analysis) | reg P9 PROPOSED + CAD T5 (2.713 kg Al) | T4/T5/P9 joint |
| 2.33 | Net + ≈ 1.7 kg over fuze replaced | reg P9 PROPOSED (+1.74) | P9 |
| 2.34 | = 3.9 % of the 45 kg round | reg P9 PROPOSED | P9 |
| 2.35 | 1.4 kg target class not yet met | reg P9 PROPOSED | P9 route a/b/c |
| 2.36 | Levers: material, ring diameter, retention hardware | reg P9/T5/T8/C44 | P3/P4 |
| 2.37 | Gate: retain > 90 % of max range | reg M10 DEFINED | P3 |
| 2.38 | ₹6.5 lakh (≈US$7,800) recurring at 5,000/yr | reg K4 DEFINED | **K5 OPEN** |
| 2.39 | ≈ 40 % below US$13,541 | reg K4; SR A2 | K5 |
| 2.40 | Development + tooling excluded | reg K4 DEFINED | — |
| 2.41 | Architecture = fielded M1156 spec | SR A1/A2; reg C1/C34 | — |
| 2.42 | 2.92 kW peak | reg C42 DERIVED (provisional on aero set) | risk 8 / P3 |
| 2.43 | ≈ 121 kJ per flight | reg C42/W7 DERIVED | risk 8 |
| 2.44 | Through a declared thermal interface | reg W7/W12, P6 DERIVED | rig R7 |
| 2.45 | Ring as inertial platform when GNSS contested | reg N6 DEFINED, X17 DEFINED | — |
| 2.46 | Spin-axis GNSS aperture | reg N3 DEFINED | — |
| 2.47 | In-flight error estimator | reg G17 DEFINED | P3/R5 |
| 2.48 | State-dependent authority gate | reg G3/G15 DERIVED/DEFINED | — |
| 2.49 | Module interface for beacon / laser seeker ("options, never delivered capability") | reg X1, X2 DEFINED; **X18 OPEN** | X18 defines interface |

#### B3 — Idea Description (`02-description-FINAL.txt`)
| # | § | Claim (value) | Source + status | Closer |
|---|---|---|---|---|
| 3.1 | 1 | Unguided long-range CEP "hundreds of metres" | reg M6 PARAMETRIC | YIL tables |
| 3.2 | 1 | Requirement CEP 30 m or better | reg M4 PARAMETRIC | M4 confirm |
| 3.3 | 1 | Launch spin 10,000–20,000 rpm | reg S6 PARAMETRIC (10,578–18,264 rpm) | — |
| 3.4 | 1 | Flight duration 90 s | reg G3 (t ≈ 86 s), C21/W1 | — |
| 3.5 | 1 | High axial/radial shock (qualitative) | reg E1/E2 OPEN [ref] 15,000 g / 5,000 g | YIL data |
| 3.6 | 1 | Retrofit = fuze well + forward ogive only | reg P12/P13 PARAMETRIC | — |
| 3.7–3.9 | 3 | Canard pairs (as 2.6/2.7) | reg C1/C9 | — |
| 3.10 | 3 | Symmetric authority: peak aero torque ≤ ½(max alternator torque + friction) | reg C9 DERIVED | C14 |
| 3.11 | 3 | Min controllability: aero torque > friction | reg **C10 OPEN** | C22/C25 |
| 3.12 | 3 | Aero torque rises to "a few newton-metres" (≈2.2 N·m [ref]) | reg **C11 OPEN** | risk 8 |
| 3.13 | 3 | Friction "fraction of a newton-metre" (Tf ≤ 0.10 N·m) | reg C13 DERIVED | C25 / R7 |
| 3.14 | 3 | Margin thinnest near apogee (Taero_min 0.1706 N·m) | reg C12 DERIVED | R5 |
| 3.15 | 3 | 2 mm/side clearance; canard tips Ø151 mm | reg C31 DEFINED | — |
| 3.16 | 3 | Fielded kit carries four fixed external canards | SR A2; reg C1 | — |
| 3.17 | 4 | IPP law | reg G1 DEFINED | — |
| 3.18 | 4 | Authority high early+late, vanishes at apogee | reg G3 DERIVED | aero set |
| 3.19 | 4 | Nav fuses GNSS + IMU + baro + ring angle | reg N1/N3/N6/N11/N10 | N11/N10 OPEN |
| 3.20 | 4 | Body rotates 10,000–20,000 rpm | reg S6 PARAMETRIC | — |
| 3.21 | 4 | Ring angle: pickoff (relative) + magnetometer (absolute) | reg N10/N12/G6 | N12 OPEN |
| 3.22 | 4 | GNSS denial → inertial coast, degrades to drift | reg **N4 OPEN** | N4 |
| 3.23 | 5 | Cascade outer P / inner PI | reg G8/G9 DERIVED | — |
| 3.24 | 5 | Inner ≥ 5× faster (5.4×: 33.6/6.2) | reg G9 DERIVED | — |
| 3.25 | 5 | Disturbance observer Q(s) = 1/(0.5s+1) | reg G14 DERIVED | 2× bound |
| 3.26 | 5 | State-dependent limits | reg G15 DEFINED | — |
| 3.27 | 5 | Aero torque varies > order of magnitude (ratio 12.4) | reg C12 DERIVED | risk 8 |
| 3.28 | 5 | Loop rate 1 kHz | reg G13 DEFINED | R7 jitter |
| 3.29 | 5 | Guidance bandwidth "a few hertz" (6.2 Hz outer) | reg G8 DERIVED | — |
| 3.30 | 6 | Proximity RF Doppler, burst height selectable (2–15 m) | reg F2/F1 DEFINED | F3 |
| 3.31 | 6 | Time mode, crystal timer 0.1–199.9 s | reg F1/F4 | F4 OPEN |
| 3.32 | 6 | Impact crush/inertial switch, selectable delay | reg F1/F5 | F5 OPEN |
| 3.33 | 6 | Out-of-line S&A, setback + spin interlocks (15,000 g / 176.3–304.4 Hz) | reg F6 DEFINED | — |
| 3.34 | 6 | Arming delay after muzzle exit (no value printed) | reg **F8 OPEN** | F7/F8 |
| 3.35 | 6 | Setter package (mode, ToF, target, MV, met) | reg F12 DEFINED | risk 44 |
| 3.36 | 6 | > 150 m → withhold, latched irrevocable | reg F16 DEFINED | — |
| 3.37 | 6 | AOP-22 command mode / safety-unacceptable patterns | reg F11 PARAMETRIC | YIL setter |
| 3.38 | 6 | Fuze + guidance share processor and rail | reg H10/H5 DEFINED | — |
| 3.39–3.41 | 8 | Dual-domain MCUs; 1 kHz loop; three-phase rectification + controlled current sink | reg H1/G13, H8 DEFINED | — |
| 3.42 | 9 | Alternator powers the whole flight | reg C42/W1 | risk 8 |
| 3.43 | 9 | Reserve battery activated by launch environment | reg W5 OPEN (scope fixed) | W5 chemistry |
| 3.44 | 9 | Active dissipation; optional recovery | reg W7/W12/W4 DERIVED | rig |
| 3.45 | 9 | Standards: MIL-STD-331C, 810F, 1316, 461; STANAG 4369/AOP-39, 4439, 9216/MIL-STD-333B; AOP-22 Ed B Ver 1 | reg E10/E11/F13/F6/F11/P6 | E-domain mostly OPEN |
| 3.46 | 9 | HERO/EMR/ESD requirement (standards fixed at hardware-definition) | reg **E12 OPEN** | P4 (risk 42) |
| 3.47 | 10 | 6-DOF extended to 7-DOF (ring as independent roll body) | reg R5/§10.1 | P3 |
| 3.48 | 10 | Aero coefficients vs Mach/α/β (not sparse table) | **risk 8 OPEN** | aero set |
| 3.49 | 10 | CFD fills gaps / verifies canard interference | reg §10.2 | P3 |
| 3.50 | 10 | MC varies MV/charge temp, met, target location, launch perturbations, aero coeffs, sensor noise | reg R5 DEFINED | P3 |
| 3.51 | 10 | HIL ring loop vs live trajectory | reg R7/§10.4 | R8 OPEN |
| 3.52 | 10 | Dynamometer bench (torque motor + speed motor) | reg R7/§10.5 | rig parked |
| 3.53 | 11 | Force band 15–25 N mid-flight, ≈85 N launch transient, →0 apogee | reg G3 DERIVED, **C28 OPEN** (±85 N) | risk 8 |
| 3.54 | 11 | ≥ 18.1 N min over guided window | reg C8 DERIVED | R5 |
| 3.55 | 11 | Design point 45.0 kg | reg M7/P2 PARAMETRIC | YIL data |
| 3.56–3.59 | 11 | 80 % capture; 450 m available; 407 m required; 1.11:1 | reg M7 DERIVED | R5 |
| 3.60 | 11 | Budget 5/17/5/8/3 → RSS 20.3 m | reg G4 DEFINED | R5 |
| 3.61–3.62 | 11 | CEP ≈ 23.9 m; closes under 30 m with margin | reg G4/M5 | R5 |
| 3.63 | 11 | Graceful degradation (fuze functions on set mode) | reg R4 DEFINED / N4 OPEN | N4 |
| 3.64 | 12 | 5,000 kits/year | reg K4 DEFINED | K5/YIL |
| 3.65 | 12 | 382 kN axial setback through continuous metal | reg C26 DERIVED (T6 re-baseline) | C32/P9 |
| 3.66 | 12 | Stator 0.1–0.2 mm laminations or SMC | reg **C39 OPEN** | iron-loss calc |
| 3.67 | 12 | Core loss ≈ 83 W/kg at 1 T / 1 kHz, to 5 kHz | mfg §50 (J1 Somaloy 700 7P) | C39 |
| 3.68 | 12 | Electrical frequency 2,130 Hz | reg C39 | — |
| 3.69 | 12 | Copper skin depth ≈ 1.4 mm (1.43 mm @ 2,130 Hz) | mfg / SR | — |
| 3.70 | 12 | 736 N shear per magnet at launch accel (5 g × 15,000 g) | reg **C38 OPEN** | CAD load case |
| 3.71 | 12 | GBD magnets (heavy RE at grain boundaries only) | mfg | K6 OPEN |
| 3.72 | 12 | Cold-sprayed copper 98 % IACS, 368 W/mK as-sprayed | mfg §136 (J9) | **unopened rows** |
| 3.73 | 12 | Indium foil + compliant sleeve + cold-spray mating surface | mfg / reg P6 PARAMETRIC | rig |
| 3.74 | 12 | AlN thick-film dump resistor + graphite spreader | mfg | — |
| 3.75 | 12 | MIM for small fuze parts | mfg | K6 |
| 3.76 | 12 | Spin-axis GNSS aperture = laser-direct-structured traces | mfg / reg N3 DEFINED | — |
| 3.77 | 12 | Printed copper 79 % slot fill, 87 % IACS after heat treatment | mfg §95 (J4) | **C46/C47 not opened** |
| 3.78 | 12 | Printed hybrid end-winding removes ≈ ⅓ winding-head height | mfg | **not opened** |
| 3.79 | 12 | 2nd sensor channel ≈ 1 % of kit mass | mfg | **not opened** |
| 3.80 | 12 | Two-tier production/development strategy | mfg | **K7/K8/H14/H15 not opened** |
| 3.81 | 12 | No shell re-qualification | reg P13 PARAMETRIC / M10 | — |
| 3.82 | 15 | M1156 = de-spun canards, no actuators, one moving part, self-generating, no battery | SR A2/A1; reg C1/C34 | — |
| 3.83 | 15 | US 6,981,672 covers fixed-canard 2-D guidance | reg ref 5 / **SR C9 — patent UNREAD (no text layer)** | pull claims externally |
| 3.84 | 15 | AIAA 2024-1105 covers two-pair arrangement | SR B3 (Jaiswal) | — |
| 3.85 | 15 | IPP for dual-spin fixed canards established | digest QB8 / B2 Zhang 2019 | — |
| 3.86 | 15 | AOP-22 registers XM8 course-correction time fuze | reg F1 / AOP-22 Annex E.16 | — |
| 3.87 | 15 | Israeli kit: PD + PDD + airburst | SR A4 (Elbit Silver Bullet II) | — |
| 3.88 | 15 | Machine 2.92 kW peak / ≈ 121 kJ per flight | reg C42 DERIVED | risk 8 |
| 3.89 | 15 | "no published treatment … reports" | **UNSOURCED absolute** | rephrase/cut |
| 3.90 | 15 | Bare 2″-12 UNS thread ≈ 3–16 W/K vs peak 58 W/K | reg P6 PARAMETRIC / W7 | rig R7 |
| 3.91 | 15 | Ring removes 1,107–1,912 rad/s of spin | reg S6 PARAMETRIC | — |
| 3.92 | 15 | Published work names in-flight ring-angle feedback as largest unresolved problem | digest QB9 (gap) | — |
| 3.93 | 15 | Fielded kit determines roll from GNSS, no inertial sensors | SR A2 | — |
| 3.94 | 15 | Spin-invariant GNSS aperture | reg N3 DEFINED | — |
| 3.95 | 15 | State-dependent gate makes 1.11:1 usable | reg G3/G15/M7 | R5 |
| 3.96 | 15 | Estimator targets two largest budget terms [2, 22] | reg G17; M5/G4 | P3/R5 |
| 3.97 | 15 | Three-mode fuze matches Indian Army RFI categories | SR A8 | — |
| 3.98 | 15 | Time mode corrected in flight by own nav | reg F1 (credited AOP-22 XM8) | — |
| 3.99 | 15 | Retain > 90 % range | reg M10 DEFINED | P3 |
| 3.100 | 15 | Mass ≈ 2.7 kg (4.8 kg steel), ~2× fielded total, ~4× net penalty | reg P9 PROPOSED + T5 | P9 |
| 3.101 | 15 | Net +1.7 kg = 3.9 % of 45 kg | reg P9 PROPOSED | P9 |
| 3.102 | 15 | 1.4 kg target not met; spigot −0.59 kg banked; make-vs-buy open | reg P9/T9/C44/C45 | P3/P4 |
| 3.103 | 15 | Module interface → beacon [21] / SAL seeker ("not fitted, funded or flown") | reg X1/X2 DEFINED; **X18 OPEN** | X18 |
| — | 16 | 22 references (7–8 cut, renumbered) | reg/SR-mapped | trim bank |

#### B4 — Deck (6 slides) + upload QA
| # | Claim (value) | Where | Source + status | Closer |
|---|---|---|---|---|
| 4.1–4.3 | Dispersion 94 / 125 / 150 → 267 m CEP vs ≤ 30 m; attributed "Orbital ATK NDIA 2015" | slide 1 | SR A1 (Cite 5/Adopt 4); reg M6 PARAMETRIC | YIL tables |
| 4.4–4.7 | Fuze-well kit; canard split → 2-D steering; alternator = actuator; fuze over inductive setter | slide 2 | reg C1/C31/G2/C34/F1/F11/F12 | — |
| 4.8 | Architecture = fielded M1156 spec (credit block) | slide 2 | SR A2 | — |
| 4.9 | 2.92 kW peak, ≈ 121 kJ/flight, declared thermal interface | slide 2 | reg C42/W7/W12 | risk 8 |
| 4.10 | No flight battery; supercap buffer; reserve pre-launch/safe only | slide 2 | reg W4/W5 | W5 |
| 4.11 | IPP credited; claim only the state-dependent gate | slide 3 | reg G1/G3/G15 | — |
| 4.12 | Ring inertial platform; pickoff + magnetometer; GNSS+IMU+baro | slide 3 | reg N6/N10/N12/N3 | N12 OPEN |
| 4.13 | Anti-jam GNSS + INS coasting + spin-axis aperture ("table stakes") | slide 3 | reg X17/N3; **N5 OPEN** | N5 |
| 4.14 | Cascade PI/P, DOB, adaptive limits, 1 kHz | slide 3 | reg G8/G9/G14/G15/G13 | — |
| 4.15 | "resonance dispositioned via span-capped canard" | slide 3 | reg **S8 OPEN** (asks evidence) | P3 |
| 4.16 | S&A, dual interlocks, ESD/EM qual; power chain | slide 3 | reg F6/E12/W5/W7 | E12 P4 |
| 4.17 | F16 150 m withhold (decided one-liner) | slide 3 | reg F16 DEFINED | — |
| 4.18 | Budget 5/17/5/8/3 → RSS 20.3 → CEP ≈ 23.9 m | slide 4 | reg G4 DEFINED | R5 |
| 4.19 | Nav 3.7 m sub-allocation (GNSS 3.0 + IMU/filter 2.0 + time/lever 1.0) | slide 4 | reg N1 DERIVED (prov. N3/N8) | N8/R5 |
| 4.20–4.21 | ≥ 18.1 N; 450 vs 407 m (80 % capture) → 1.11:1 | slide 4 | reg C8/M7 DERIVED | R5 |
| 4.22 | Standards list (as 3.45) | slide 4 | reg E/F domain | mostly OPEN |
| 4.23 | MC 5,000 design + 5×1,000 corners, worst-corner 95 % bound | slide 4 | reg R5 DEFINED | P3 |
| 4.24 | HIL + rotating dynamometer rig (plan, not asset) | slide 4 | reg R7 | P7 |
| 4.25 | Two-tier process; no shell re-qual; tooling amortisation | slide 4 | reg K4 / mfg | K5/K6 |
| 4.26 | Mass ≈ 2.7 kg Al (4.8 kg steel), +1.7 kg ≈ 3.9 %, 1.4 kg not met, gate > 90 % | slide 4 | reg P9/T5 PROPOSED + M10 | P9 |
| 4.27 | Aero coefficient set = acknowledged long pole | slide 4 | risk 8 OPEN | P3 |
| 4.28–4.29 | ≤ ₹6.5 lakh (≈US$7,800)/kit @ 5,000/yr vs US$13,541 | slide 5 | reg K4 / SR A2 | K5 |
| 4.30 | Fielded > 100,000 units | slide 5 | SR A2/S4 | — |
| 4.31 | 301→77 rounds / 959→208 charges (fielded published) | slide 5 | SR A1; verified-source-audit L70 | — |
| 4.32 | Our derived 23.9 m beside these | slide 5 | reg G4 | R5 |
| 4.33 | YIL mechanical core; GBD = less heavy RE | slide 5 | SR A8 / mfg | K6 |
| 4.34 | Growth: anti-jam, module interface, other calibres | slide 5 | reg X17/X1/X18 | N5/X18 |
| 4.35–4.43 | QA locked set (as notes/03): 23.9 m budget · authority · machine · bus 180 V · mass · cost · 45.0 kg · F16 150 m · dispersion | QA §3 | reg G4/C8/M7/C41/P9/K4/P2/F16 + SR A1 | — |
| 4.44–4.49 | Chars 6,639 / 49,903 / title ~84–85; theme Smart Vehicles; Team ⟨portal⟩; Hardware; PDF 6 pp; YouTube skipped | QA §1–2 | notes/03 + official format | portal counters |

### C. Stale / contradicted scan

- **Found (must fix):** abstract "15,000–20,000 rpm" (2.15) contradicts reg S6 (10,578–18,264 rpm) and the description's own "10,000–20,000 rpm" (3.3/3.20).
- **Found (internal):** title length 85 vs ~84 across our own files.
- **Clean (verified absent from all four fields):** old budget 20.4 / ~24 m · "1.4–1.7 kg class" · 1.0–1.21× / 1.55–2.2× · 74 kN · ⟨DECISION REQUIRED — F16⟩ · raw [criterion] IDs · unframed 400 V · guided-window t ≈ 15 s · iron-loss ~50–60 W.
- **Not printed (open conflicts, portal-side):** deadline 20 vs 30 Sep → research resolves to **5 Oct**; theme conflict → research resolves to **Smart Vehicles**.
- **Latent (not in the four fields, defend in Step 5):** repo1 Rev E MC CEP50 21.5 m vs printed 23.9 m (different vintage/method — reconciliation line drafted in E-R10).

### D. Open items printed as fact today (qualify with value → status → closer in Steps 2–3)

1. Mass ≈ 2.7 kg / +3.9 % — P9 **PROPOSED** (framing approved: honest open trade).
2. 94/125/150/267 m — M6 **PARAMETRIC**; must read as published fielded-class figures (SR A1), never YIL.
3. Anti-jam GNSS — **N5 OPEN** (no numbers may print).
4. Outage/degradation behaviour — **N4 OPEN** (scope note).
5. 2.92 kW / 121 kJ (C42, provisional on risk 8) · 18.1 N / 450 vs 407 / 1.11:1 (C8/M7, provisional on M6) · nav 5 m (N1, provisional on N3/N8).
6. ₹6.5 lakh target — K4 DEFINED but K5 (cost evidence) **OPEN**.
7. Manufacturing processes §12 — named candidates rest on **unopened rows C46/C47/H14/H15/K7/K8 + risks 47–50** (3.67–3.80).
8. "resonance dispositioned" (deck s3) — **S8 OPEN**. 9. "defined module interface" (§15) — **X18 OPEN**.

### E. True loose ends

**(a) Claimed without ruling/evidence — fix in Steps 1–2:**
1. Abstract rpm band (see C) — align to "10,000–20,000 rpm" + soften the MEMS sentence to a range statement.
2. Deck s3 "resonance dispositioned" → "designed against; evidence closes in the 7-DOF campaign" (S8 scope note).
3. §15 "the defined module interface" → "a reserved growth-module interface; definition is post-selection work" (X18) + freedom-ledger entry.
4. US 6,981,672 credited but the on-disk PDF has no text layer = **unread (Rule-1 defect)** → pull claim text (Google Patents/Espacenet) in Step 1; cite precisely or credit generally.
5. §15 "no published treatment … reports" — unsourced absolute → "we have found no published treatment…" or cut.
6. §12 manufacturing numbers (3.72/3.77–3.80) on unopened rows → hold the numbers in the freedom ledger; keep named candidates as "studied in the process dossier; validation post-selection"; propose register patches at Step 6 (no repo edits).

**(b) Open but printed as settled — qualify, don't delete:** items D1–D6 above (three-part format).

**(c) Missing data:**
7. Team ID + Team Name (portal) — blocker for slide 1 + fields.
8. Portal-side: exact live counters (title 85 vs ~84), PDF size cap ("10 MB" unconfirmed), exact cut-off time on 5 Oct, bucket-dropdown value, editable-vs-display-only fields.
9. Deck PDF build (manual Figma/Canva) from the official template; ensure **fig4-system-flowchart** (the PS's electronics block-diagram deliverable) lands in the new deck; repo2's on-disk `SIH26098-Idea-Template-6Slides.pdf` is superseded — build fresh.
10. Post-selection closers: YIL shell/fuze-well drawings + firing tables + setter data (retire M3/M4/M6/M7 chain) · aero coefficient set (risk 8 — the long pole) · K5 cost roll-up · X18 interface definition · rig (R7).

### F. Proposed step list (one step per exchange; user approves before moving on)

- **Step 0** — Intake & loose-end inventory ← this file (presented 2026-10-02).
- **Step 1** — Lock the claim set: title A, theme/team data, canonical numbers; strip all stale values; patent pull; ruling sheet.
- **Step 2** — Rewrite the design narrative section by section: purpose → claims → support → how open items are handled (user decides anything genuinely open; agent drafts).
- **Step 3** — Final texts: abstract (~6–8k chars) + description (≤ 50,000 with live char math; §16 refs = trim bank).
- **Step 4** — Template-PDF content pack for the manual 6-slide build + refresh QA checklist (no deck production).
- **Step 5** — Adversarial judge pass: attack every number/claim; register-backed answer or explicit scope note; fix or defend.
- **Step 6** — Freedom ledger & handoff: held-back items, post-selection adds, register patch proposals, fresh-session notes.

Clock: portal deadline 5 Oct 2026 (exact time TBC); one-time PPT/Team-Name edit window 02–05 Oct → Steps 1–5 are pre-upload; Step 6 is post-upload bookkeeping (can run in parallel).

### G. Proposed rulings for Step 1 (pending user objection at go-ahead)

- **R1** Title A locked as-is; re-measure length once and store one number.
- **R2** Theme "Smart Vehicles" verbatim; category Hardware; Team ID/Name from portal.
- **R3** Spin band printed as "10,000–20,000 rpm" (class envelope; register S6 = 10,578–18,264 rpm rounded outward, stated as such); MEMS sentence reworded to a range statement ("beyond the range of flight-representative MEMS rate sensors").
- **R4** Patent US 6,981,672: fetch claim text; credit precisely (fixed canards + 2-D steering from one actuation axis) or generally if the pull fails.
- **R5** §12: named candidate processes stay ("studied in the process dossier; validation post-selection"); unopened numeric claims (79 %/87 %, 98 % IACS/368 W/mK, −⅓ head, 1 % mass) move to the freedom ledger; register patch proposals for C46/C47/H14/H15/K7/K8 + risks 47–50 at Step 6.
- **R6** Three-part format (value → status/source → closer) applied to: P9 mass, M6 dispersion attribution, C42 machine, C8/M7 authority, N1 nav line, K4 cost, N4/N5, S8, X18.
- **R7** "no published treatment reports" → search-scoped wording.
- **R8** Rev E 21.5 m is not printed; reconciliation line held for the judge pass: *the submission's claim of record is the derived budget CEP ≈ 23.9 m; the 7-DOF Monte Carlo (planned) produces the flight CEP — earlier methodology-MC results on predecessor GNC are superseded by that plan.*
- **R9** Char discipline: description ≤ 50,000 (97 headroom) — three-part lines funded by the §16 trim bank (~2.9 k chars); abstract 6.5–8 k.

### H. Portal checklist (user-side, before/at upload)

1. Team ID + Team Name (also feeds slide 1).
2. Theme/bucket dropdown value copied character-for-character (expected "Smart Vehicles"); category "Hardware".
3. Exact char counters for title / abstract / description (title 85-vs-84 reconciliation happens here).
4. Template PDF upload size cap (verify "≤ 10 MB" or replace the rule in QA).
5. Exact submission cut-off time on 5 Oct 2026; confirm the 02–05 Oct one-time edit window covers the PPT as announced.
6. Whether PS ID/title/theme/category are display-only.
7. YouTube field presence (leave empty).

---

## Step 1 — 2026-10-02 — locked claim set + stale strip

Rulings R1–R9 accepted (user "go", no objections). Status: **closed; claim set locked below. Awaiting go-ahead for Step 2 (narrative rewrite).**

### Identity block (locked)

- **Idea Title (A):** `STHIRA-PGK: De-Spun Canard Guidance Kit with Multi-Mode Smart Fuze for 155 mm Shells` — **84/100 chars** (measured in Python; corrects the "85" in notes/03 #1 and the old deck brief). Portal counter is final authority at paste time.
- **Theme:** **Smart Vehicles** (official SIH 2026 theme; copy the portal value verbatim) · **Category:** Hardware · **PS:** SIH26098 (MoD / Yantra India Limited).
- **Team ID / Team Name:** ⟨from portal⟩ — the only permitted placeholder; must be filled on slide 1 and the portal before upload.
- Product name in-text: **STHIRA-PGK** (named from §2 onward). YouTube: skipped. Slides: exactly 6, official template, PDF.

### Canonical numbers (value → status/source → closer) — single source for abstract, description, deck

| # | Value as printed | Status / source | What closes it |
|---|---|---|---|
| 1 | CEP ≤ 30 m at long range (requirement) | M4/M5 — PS requirement | — |
| 2 | CEP ≈ **23.9 m** from budget nav 5 / G&C 17 / meteo 5 / aero 8 / fuze 3 → RSS **20.3 m** | G4 DEFINED (derived, 1.1774 × σ) | R5: 7-DOF MC produces the flight CEP |
| 3 | Unguided dispersion **94 / 125 / 150 → 267 m** CEP | M6 PARAMETRIC + SR A1 — **published fielded-class figures (Orbital ATK NDIA 2015), never YIL data** | YIL firing tables (post-selection) |
| 4 | Authority **≥ 18.1 N** minimum over the guided window | C8 DERIVED (provisional on the M6 anchor) | R5 gated-window quantification |
| 5 | **450 m** available vs **407 m** required (80 % capture) → **1.11:1**, stated as a margin | M7 DERIVED (provisional on M6) | R5 |
| 6 | Machine **2.92 kW peak / ≈121 kJ per flight** | C42 DERIVED (provisional on risk 8 aero set) | P3 aero coefficient set |
| 7 | Bus **180 V nominal** | C41/W8/H12 DEFINED | — (prints only if needed; 400 V only ever as the "cannot store it" comparison) |
| 8 | Mass **≈2.7 kg** aluminium analysis (4.8 kg steel), net **+1.7 kg ≈ 3.9 %** of the 45 kg round; **1.4 kg target not yet met** | P9 PROPOSED + CAD T5 (2.713 kg Al) | P9 joint ruling (material, ring diameter T8↔C44↔M10, retention; spigot −0.586 kg banked) |
| 9 | Design point **45.0 kg** platform | P2/M7 PARAMETRIC | YIL data (post-selection) |
| 10 | Gate: retain **> 90 %** of the conventional round's maximum range | M10 DEFINED (requirement) | P3 achieved retention |
| 11 | Cost **≤ ₹6.5 lakh (≈ US$7,800)** recurring per kit @ **5,000/yr** vs M1156 **US$13,541** (≈40 % below); development + tooling excluded | K4 DEFINED (target); **K5 OPEN** (cost evidence) | K5 ranked + priced drivers |
| 12 | Setter **AOP-22**, ≈550 bits for a CCF package | F11 PARAMETRIC / risk 44 | YIL setter data |
| 13 | F16: withhold function when predicted miss **> 150 m**, latched, dud-direction | F16 DEFINED (20 Sep) | F10 dud-rate allocation |
| 14 | Spin band **10,000–20,000 rpm** (class envelope; S6 = 10,578–18,264 rpm rounded outward — stated as a band, not a measurement) | S6 PARAMETRIC | YIL data (post-selection) |
| 15 | Setback **382 kN axial / 127 kN radial** (T6 re-baselined; the 74 kN value is dead) | C26/C35 DERIVED | C32/P9 load path |
| 16 | Thermal: peak need **≥58 W/K** through the fuze-well interface vs bare thread **3–16 W/K** | W7/P6 PARAMETRIC | Rig (R7) + P6 drawing |
| 17 | Guided window: **no time value prints** (t ≈ 15 s is a placeholder) | G3 DERIVED | R5 |

### Patent lineage — credit line locked (R4 closed)

US **6,981,672** B2 "Fixed canard 2-D guidance of artillery projectiles" (Clancy, Bybee & Friedrich; Alliant Techsystems; filed 17 Sep 2003; granted 3 Jan 2006; **expired**). Claims 1–13 + description read in full via Google Patents on 2026-10-02 — the on-disk scan PDF's Rule-1 defect (unread citation) is **closed**.

- **What it claims:** nose portion on a spin-control coupling counter-rotating to the body; one fixed canard pair (0°/180°, differentially canted) that re-spins the de-spun nose; a second fixed pair (90°/270°, same cant) that, when the nose is de-spun, induces both a moment and a lateral force → trajectory change; steering by de-spinning and holding the nose at a commanded roll attitude (bank-to-turn); de-spin by **alternator + variable-resistance load** (armature on sleeve, magnets on nose); threaded fuze-well retrofit of legacy projectiles; GPS/INS navigation; RF proximity height-of-burst fuze described.
- **Locked credit line** (for description §15 + deck slide 6): *the fixed-canard two-pair architecture — a bearing-isolated counter-rotating nose, one pair for net roll torque and one for net guidance force, steered by holding the de-spun nose at a commanded roll attitude, with the alternator as the de-spin actuator — is claimed in US Patent 6,981,672 (2006, expired) and is the published specification of the fielded M1156 kit.*
- **Consequence:** alternator-as-actuator and the two-pair split are **lineage, never our novelty**. Ours = loaded-generator sizing (2.92 kW / 121 kJ), declared thermal path, ring as inertial platform, spin-axis GNSS aperture, in-flight error estimator (G17), state-dependent authority gate, F16 predicted-miss failsafe, span-capped canard/resonance discipline, honest SWaP-C + cost engineering. (Abstract ¶8 already carries this structure — keep it.)
- **Pair-position note:** our description puts the equal-cant (force) pair at 0°/180° and the torque pair at 90°/−90°; the patent swaps roles between positions. Positions are equivalent up to a command-angle phase offset — never claim positional novelty.

### Stale strip record (Step 1 edits)

| Fix | File | Before → after | Δ chars |
|---|---|---|---|
| Spin band + MEMS sentence (R3) | `submission-resources/01-abstract.txt` | "15,000–20,000 rpm rotation that no flight-representative MEMS gyroscope can measure" → "10,000–20,000 rpm rotation beyond the range of flight-representative MEMS rate sensors" | +3 (6,639 → **6,642**) |
| Title count (R1) | `submission-resources/04-deck-brief.md` | 85/100 → 84/100 | 0 |
| Title count (R1) | `submission-resources/05-upload-qa-checklist.md` | "~84 (max 100)" → "84/100 chars (max 100)" | 0 |
| Errata + pointer | `notes/03` | title count corrected; authoritative set pointed here | +~250 |

Post-strip verification (Python + grep, 2026-10-02): **zero** occurrences of 15,000–20,000 rpm · 20.4 / ~24 budget · 1.4–1.7 kg class · 1.0–1.21× / 1.55–2.2× · 74 kN · ⟨DECISION REQUIRED — F16⟩ · criterion IDs · unframed 400 V · t ≈ 15 s · iron-loss 50–60 W in any submission field.

**Live baselines:** abstract **6,642 / 10,000** · description **49,903 / 50,000** (headroom 97) · title **84 / 100**.

### Ruling register status

R1 locked (84 chars) · R2 locked (theme/category/team) · R3 applied · R4 closed (patent read; credit line above) · **R5–R9 locked as policy for Steps 2–3**: §12 manufacturing downgraded to named candidate processes ("studied in the process dossier; validation is post-selection work") with unopened numbers (79 %/87 % slot fill & IACS, 98 % IACS / 368 W/mK cold-spray, −⅓ winding head, 1 % mass channel) moved to the freedom ledger · three-part format (value → status/source → closer) on P9 mass, M6 dispersion, C42 machine, C8/M7 authority, N1 nav line, K4 cost, N4/N5, S8, X18 · "no published treatment reports" → search-scoped wording ("we have found no published treatment…") · Rev E 21.5 m not printed; reconciliation line held for Step 5 · char discipline: §16 references are the trim bank.

---

## Step 2 — 2026-10-02 — description narrative rewrite (R5–R9 applied)

Status: **closed. `02-description-FINAL.txt` rewritten in place — 49,843 / 50,000 chars (headroom 157).** Section-by-section: purpose unchanged (§1–2); claims re-sourced and status-qualified (§3–11); open items now each carry status + named closer; §12 downgraded; §15 credit structure sharpened; §16 trimmed.

### Edit ledger (description)

| # | Section | Change | Δ chars |
|---|---|---|---|
| 1 | §1 | Dispersion claim sourced: "published figures for the fielded class run from about 94 m to 267 m across the range envelope [4]; service firing tables follow after selection" (M6 class-anchor rule) | +150 |
| 2 | §4.3 | "No flight-representative MEMS gyroscope measures that rate" → "a band beyond the range of flight-representative MEMS rate sensors" (R3) | −15 |
| 3 | §4.4 | N4 closer added: outage tolerance "set and verified in the §10.3 campaign rather than assumed here" | +110 |
| 4 | §10.1 | S8 scope note: model resolves dual-spin modes incl. roll-through-resonance; "design's disposition is the span-capped canard ring, and the quantitative evidence is a named task of §10.3 — an open evidence item, not a settled result" | +215 |
| 5 | §11.2→ new §11.5 | **Three-part status block for every weak number** (budget/CEP → §10.3 MC; authority set + force band → sizing on parametric 45.0 kg public-data platform, provisional on §10.2; 2.92 kW/121 kJ → §10.5 rig; nav 5 m (3.7 m sub-allocation) → §10.3; mass → CAD analysis, closes at detailed design vs >90 % gate; cost → objective, priced roll-up post-selection; 382 kN/736 N → structural analysis) | +960 |
| 6 | §12 | Cost objective stated with status: ₹6.5 lakh (~US$7,800) @5,000/yr vs published US$13,541, development + tooling excluded | +165 |
| 7 | §12 | R5 downgrade: cold-spray numbers (98 % IACS / 368 W/mK) stripped | −38 |
| 8 | §12 | R5 downgrade: dev-tier numbers (79 %/87 %, −⅓ head) stripped → "bounded by published process data held in the manufacturing dossier … validation is post-selection first-article work" | −40 |
| 9 | §12 | R5 downgrade: "about one per cent of the kit's mass" stripped | −51 |
| 10 | §12 | Freedom-ledger move: printed-in conductors / in-structure components claim removed from the "keeps improving" paragraph | −390 |
| 11 | §12 | Digital-cell paragraph tightened (post-treatment chain kept, named) | −120 |
| 12 | §15 | R4: patent credit sharpened to the actual claims (counter-rotating nose on bearings, torque pair + force pair, roll-angle hold steering, alternator as de-spin actuator) + "credited lineage, not contributions of this design" | +185 |
| 13 | §15 | R7: "no published treatment … reports" → "we have found no published treatment … reporting" | +13 |
| 14 | §15 | Roll-sensing claim made honest: "published work … assumes in-flight roll knowledge rather than solving it … the ring-as-platform and its pickoff are ours to prove, and proving them is a named task of the bench programme" | +105 |
| 15 | §15 | X18: "the defined module interface" → "a reserved module interface - whose mechanical and electrical definition is post-selection work" | +65 |
| 16 | §16 | Trim bank cut 22 → **12 entries**, compact one-line format; in-text citations renumbered: [5]→[4] ATK, [2, 22]→[2, 12] Zhang+IEEE, [21]→[11] NATO STO | −1,250 |

**Baselines after Step 2:** description **49,843 / 50,000** (headroom 157) · abstract **6,642 / 10,000** · title **84 / 100**. Verified: zero stale markers; citations ⊆ {1..12}; no criterion IDs; no unopened manufacturing numbers.

### References dropped from §16 (candidates for deck slide 6 / final-round restore)
Wernert & Theodoulis 2013 · Wang et al. 2018 (Defence Technology) · Robinson & Berefelt 2011 (FOI) · DOT&E FY2015 · Norris et al. 2020 review · DT 2025 flight-stability (B4) · Guo et al. 2026 resonance · Hasselstrom & Nilsson 2012 (thermal contact) · NSWC Indian Head 2021 (high shock) · DT 2026 damage tolerance. Kept 12: Gunay thesis · Zhang 2019 CJA · Clancy patent · Orbital ATK 2015 · M1156 record · Elbit Silver Bullet II · Jaiswal AIAA 2024-1105 · AOP-22 · standards bundle · SIH26098 PS · NATO STO beacon · IEEE IPP.

### Freedom-ledger seeds (formalised at Step 6)
Printed-copper 79 %/87 % IACS · cold-spray 98 % IACS / 368 W/mK · hybrid end-winding −⅓ head · sensor-channel ~1 % mass · printed-in conductors / in-structure components · printed digital-cell growth story (variant-in-days) · Elbit brochure year and full bib data · dropped §16 entries above.

---

## Step 3 — 2026-10-02 — final texts (char-mathed)

Status: **closed. Paste-ready pair = `01-abstract.txt` (7,079 / 10,000 — inside the 6–8k decision band) + `02-description-FINAL.txt` (49,843 / 50,000, headroom 157). Title 84/100.**

Abstract edits (6, Δ +437 from 6,642): dispersion attributed to "the published record for the fielded class" + requirement wording corrected to "the 30 m the requirement demands at full charge and long range" (M4 exact) · authority-set closer ("derived figures … the guided-window analysis in the verification campaign re-quantifies them") · machine-figure closer ("the dynamometer rig to confirm the figures") · cost closer ("the priced cost roll-up follows selection") · patent lineage sentence ("the two-pair arrangement with the alternator as de-spin actuator is also claimed in a 2006 US patent, now expired") · X18 fix ("a reserved module interface — its mechanical and electrical definition is post-selection work").

Description unchanged in Step 3 (final since Step 2). Verified in both texts: zero weak/stale markers; the abstract carries every locked number (94/267 m, 150 m, 20.3 → 23.9 m, 18.1 N, 450/407 m, 1.11:1, 2.7/1.7 kg, 3.9 %, ₹6.5 lakh / US$13,541, 2.92 kW / 121 kJ); the §11.5 status block covers every weak number's status + closer. **§16 trim bank is now exhausted** — description headroom is 157 chars, so any later addition must be funded by a cut.

Counts synced to `00-README.md`, `05-upload-qa-checklist.md` §1, and the `03-description-edits.md` addendum (Steps 2–3 changelog).

Next: Step 4 — template-PDF content pack (6 slides) + QA checklist refresh.

---

## Step 4 — 2026-10-02 — template-PDF content pack + QA refresh

Status: **closed. `04-deck-brief.md` rebuilt as the content pack; `05-upload-qa-checklist.md` refreshed.** No deck production (user builds manually in Figma/Canva).

### What the pack fixes vs the old brief
- **Slide map re-mapped to the official template headings**: 1 TITLE PAGE (the seven fields: PS ID · PS title · theme · category · Team ID · Team Name · idea title) · 2 IDEA TITLE & PROPOSED SOLUTION · 3 TECHNICAL APPROACH · 4 FEASIBILITY AND VIABILITY · 5 IMPACT AND BENEFITS · 6 RESEARCH AND REFERENCES. Ruling: the old "slide 1 = Problem Statement content" mapping is folded into slide 2; a compact problem hook is offered for slide 1 only if the template's title page has content space. (Template rule: don't change the idea-detail pointers.)
- **Credit block mandated on slide 2**: M1156 + US 6,981,672 (2006, expired) — two-pair split and alternator-as-actuator = lineage; ours = sizing / thermal / ring sensing / spin-axis aperture / estimator / authority gate / F16.
- **Honesty wording on-slide**: budget "derived; MC produces the flight CEP" · authority "derived figures…re-quantified in the guided-window analysis" · mass "CAD analysis, not a weighed article" · cost "the priced roll-up follows selection" · resonance "evidence closes in the 7-DOF campaign (open item, not settled)" · anti-jam capability-only (no N5 numbers) · growth "reserved module interface — definition is post-selection work".
- **fig4-system-flowchart marked REQUIRED** (the PS's electronics block-diagram deliverable — the loose end from Step 0).
- **Slide 6 = the canonical 12 references** (the kept §16 list) — no criterion IDs, no status tags.
- Pre-export checklist extended with the new forbidden values (15,000–20,000 rpm · "defined module interface" · unopened process numbers · "resonance dispositioned" as settled) and the credit-line rule.
- Clock lines added: due **5 Oct 2026** (time on portal); 02–05 Oct one-time edit window (Team Name/Consent/PPT only); PDF size cap flagged unconfirmed.

### QA refresh (05)
§1 deadline row added · §2 template checks rebuilt (pointers unchanged, instructions slide deleted, fig4 embedded, size cap unconfirmed) · §3 locked-values list extended (spin band, dispersion phrasing, cost closer) and ⛔ list extended (new stale values + "no published treatment" absolute + credit-line rule) · §4 upload steps keep the live-counter and upload-time discipline.

Next: Step 5 — adversarial judge pass.

---

## Step 5 — 2026-10-02 — adversarial judge pass

Status: **closed. Every claim attacked as a sceptical MoD evaluator; all attacks now carry a register-backed answer or an explicit scope note. Deliverable: `submission-resources/06-judge-defense-brief.md` (attack → answer ledger A–J, 4 prepared reconciliations, 10-item never-say list).**

### Loose ends the pass caught (fixed)
1. **Internal contradiction:** §4.3 called the ring-sensing chain "a solved item" while §15 (correctly) says it is "ours to prove" → fixed to "**bench-verifiable item**" (+6).
2. **Novelty over-claim:** §15 listed the in-flight error estimator as a contribution without scoping it — a specialist would cite classic adaptive/bump-up estimation → added "**Bias estimation per se is established practice; the integration is the contribution**" (+93), funded by trimming §6.5's AOP-22 tail (−89).
3. **Deck pack wording:** slide 3 "the bench programme proves it" → "is tasked with proving it".

### Everything else: defended (no text change needed)
36 attacks across ten groups (accuracy/budget, authority, machine/thermal, mass/SWaP-C, cost, fuze/F16, guidance/nav, stability/structures, manufacturing, embedded/verification) — each maps to a printed status line (§11.5 block, §6.5 honesty paragraphs, slide-4/5 wording) or a scope note (S8, N4/N5, F7/F8, K5, X18, C39). Key prepared answers: 2.92 kW is burst duty with a declared ≥58 W/K interface (rig closes) · 2.7 kg answered with the honest re-baseline + named levers + >90 % gate · F16 dud cost stated openly (F10) · IPP/estimator novelty credited away.

### Prepared reconciliations (in 06)
R1 Rev E 21.5 m vs printed 23.9 m (methodology-vintage result vs budgeted claim; the MC arbitrates — never present 21.5 as the claim) · R2 PS dispersion figures vs class-record figures (lead with the PS's) · R3 guided-window duration (never quote t ≈ 15 s) · R4 theme question.

**Baselines after Step 5:** description **49,850 / 50,000** (headroom 150) · abstract **7,079 / 10,000** · title **84 / 100**.

Next: Step 6 — freedom ledger & handoff.

---

## Step 6 — 2026-10-02 — freedom ledger & handoff · PHASE CLOSED

Status: **closed — the submission-only design phase is complete.** Deliverable: **`notes/08-freedom-ledger.md`** (freedom ledger · post-selection adds · register patch proposals · resume path + starter prompt). `notes/00-INDEX.md` updated: state banner, trap-status line, notes map 00–08, new starter prompt.

**What is deliberately NOT claimed** (the final-round ammunition, all logged in 08-A): the unopened manufacturing numbers (79 %/87 %, 98 % IACS / 368 W/mK, −⅓ head, ~1 % mass, printed-in conductors, variant-in-days) · bench-proof and estimator-performance results · F10 dud-rate · N5 anti-jam sizing · X18-gated growth specifics · rejected-alternative depth (cold-gas RCS, two-motor legacy) · realised mass reduction · internal figures (Sg envelope, iron-loss estimator, t ≈ 15 s, torque gates, Rev E 21.5 m) · the 10 dropped §16 references.

**Post-selection adds in value order** (08-B): YIL platform data → aero coefficient set (risk 8) → bench rig results → mass closure (P9) → K5 cost roll-up → manufacturing first articles → fuze/electronics closures → the MC campaign outputs. **Register patch proposals** (08-C, propose-only): open C46/C47/H14/H15/K7/K8 + risks 47–50 · P9 route + spigot banking · C38 · C39 calibrated iron loss · F10 · N4/N5/N11/N12 · X18 · S8/G16/risks 51–52 · consistency debt · source-register hygiene.

**Final submission state:** paste-ready `01-abstract.txt` (7,079 / 10,000) + `02-description-FINAL.txt` (49,850 / 50,000) + Idea Title (84/100) · build source `04-deck-brief.md` (fig4 REQUIRED) · `05-upload-qa-checklist.md` · `06-judge-defense-brief.md`. Remaining work is user-side: Team ID/Name + portal verbatim values + cut-off time + PDF size cap + live counters, the manual deck build/export, and the upload (then save the PDF here and log the time in `notes/03`). Deadline **5 Oct 2026**; 02–05 Oct one-time Team Name/Consent/PPT window.
