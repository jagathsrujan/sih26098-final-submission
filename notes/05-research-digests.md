# 05 — Research paper digests (walkthrough reference)

Built 2026-10-01 from four deep subagent passes over every research paper in repo 2 (`/Users/jagathsrujan/Documents/final-sih-pgk-kit-design`): the root PDFs + `notes/references/`. Purpose: proof-level answers to walkthrough questions — present and future. Nothing here is re-derived; it's what the literature already proves.

**Question bank:** QB1 mass properties · QB2 flattering inertias · QB3 stability (Sg/Sd, canard effect) · QB4 spin band & decay · QB5 canard force/torque mechanics · QB6 authority numbers · QB7 swerve phase · QB8 guidance laws · QB9 roll/attitude sensing · QB10 dispersion/CEP · QB11 bearing friction · QB12 actuator alternatives.

## Coverage & read status

| Paper | Identity | Status |
|---|---|---|
| `10463953.pdf` | Günay, METU M.Sc. 2022 (B1) | Full — text clean, verified |
| `Guidance_and_Control_Design…Spin-St.pdf` | **Yi Wang** et al., Int. J. Aerospace Eng. 2015 (C11) | Prose read; equations scrambled; NUL byte |
| `Influence_of_control_strategy…dual.pdf` | **Yu Wang** et al., Defence Technology 14 (2018) (C4) | Full |
| `Impact_point_prediction…iterativ.pdf` | Zhang, Yao, Zheng, CJA 32(8) 2019 (B2) | **Full — abstract-only † retired** |
| `1-s2.0-…3003227-main.pdf` | Karimi et al., Defence Technology 37 (2024) — MDO dual-spin vehicle | Partial; **not a rated register row (orphan)** |
| `1-s2.0-…5001722-main.pdf` | Wang Gang et al., Defence Technology 53 (2025) — CFD/RBD flight stability (B4) | **Full — abstract-only † retired** |
| `US6981672.pdf` | Clancy patent 2006 (C9) | **No text layer — claims still unread** |
| `B16-…ARL-CR-0604…pdf` | Ollerenshaw & Costello 2008, swerve response | Full |
| `W8-Costello-Peterson-2000…pdf` | JGCD 23(4) 2000 | **No text layer — reconstructed via ARL-CR-570** |
| `W26-Murphy-1963…pdf` | BRL 1216, yaw of repose / stability | Sampled (~13%) |
| `C5-Robinson-Berefelt-2011…pdf` | FOI-R-3291, guided artillery G&C | Full |
| `W17-Fresconi-Plostins-2009…pdf` | ARL-TR-4611, control mechanisms | Full |
| `W11-Corriveau…2011…pdf` | JGCD 34(4), thruster pairing | Full |
| `T22-Guan-Yi-2018…pdf` | IJAE, dual-spin UKF filtering | Full (poor extraction) |
| `W9-Yang-2001-GIF…pdf` | Not the cited AIAA 93-3786 | **No text layer — unread** |
| 3 adjacent (ADA441073 / ADA607104 / ADA462961) | swerve+pulsejets / IPP wind / gas generators | Read |

## Digests

### Core trio — architecture, guidance, stability
**Günay thesis (B1).** Architecture = ours: bearing-isolated fixed-canard ring, alternator actuator, single control axis = ring roll. Canard pairs (Fig 2.4): 0°/180° equal cant → net force 2F; 90°/−90° opposite cant → net roll torque. Torque ledger `T = Talt + Tf − Taero`; criteria **Taero ≤ (Talt_max+Tf)/2 = 2.93 N·m**, minimum authority **> Tf = 0.10**; Taero min **0.1706 @ 41.16 s**, 2.119 @ 86.5 s; Talt_max **5.76** (Kt 0.716 × 8 A). Vehicle (Table 5.1): **43 kg, Ixx 0.144, Iyy 1.216**, V₀ 800, p₀ 1600 rad/s, 63°; rig spin 1623→1050 rad/s; launch **15 000 g / 5 000 g**. Control: cascade PI 0.29+7.82/s + P 29.7 @ 1 kHz; DOB 588.4/(s+1.04), Q 1/(0.5s+1). **Failure t = 30–50 s**: fixed saturation limits fail because alternator current falls 10→5 A with relative speed → fix = DOB + dynamic limits. **No guidance law at all**; aero comes from refs (Wang 2018 / Khalil), sparse 5-point Mach table.
**Yi Wang 2015 (C11).** Swerve phase: ≈172° at launch → min 146–149° near apogee → ≈163° at 85 s; with Mach 149→167°; four command angles within ≈3° (max at t = 42.6 s); command must lead by φ_d (their eq. 38). Correction authority vs start time: ≈540 m span at a 30 s start → a point by 80 s. Perturbation IPP: 75+20 rows, ≤5 kB, steps 2 m/s / 5 m; interpolation <0.8/<0.1 m; vs 0.5° elevation error ≤2/≤15 m; fading-memory filter; 10 Hz loop. MC: **CEP ≤30 m @ ≈27 km** (their disturbance set). **No angular feedback (~10° sideslip)**; carries Magnus force+moment terms. Caveats: eq. (30) as printed is defective (returns ≈517–1210°, not 149–168°) — never transcribe; single flight condition; nothing on power/thermal/sensors.
**Yu Wang 2018 (C4).** What it proves: a nose control torque changes dual-spin stability, and the trend is predictable from a closed-form criterion — control strategy can be designed to protect stability. Criterion (eq. 11, Hurwitz): p₁=2(H−2g*)>0, p₂>0, **C_dyna = S̃d² − S̃d − S̃g > 0** (dual-spin-modified static/dynamic factors). Design rules: minimize canard roll moment `Mrc`; hold lower forward-body spin during roll-speed keeping; ΔMmo sign rules per phase; roll-angle-switching stability bounds. Bearing friction model: `Mrb = cV(pA−pF) + cR|FN|·sign(...)`, **cV=0.002, cR=4e-5**. Vehicle: 41.3+1.5 kg, IxA 0.133, pA 1277 rad/s; aero table = **the same sparse 5-point Mach table the thesis uses** (C_Nδ 0.172/0.195/0.170/0.076/0.092).

### Guidance / aero / patent
**Zhang 2019 (B2, CJA).** The two-pair split stated as prior art ("differential canards 1&3 opposite → roll of forward body; steering canards 2&4 same → control force"); force magnitude fixed by cant, **direction set only by forward-body roll angle** (eqs. 11/17/18). IPP method: corrected modified linear theory + iterative impact-point controller (J = φ_d,n², seed φ_F,0 = Δ₀ + π/2, exit J<J_th or N). Sim: 155 mm, 41.316+0.235 kg, θ 47.5°, u 860 m/s, p_A 1445, p_F 125.66 rad/s; 50 MC runs; guidance from 40 s; max 6 iterations; **uncontrolled CEP 206 m → 1.17 m IPP (ideal)**; same airframe with phase-lag law = **24.73 m**; authority at 40 s start ≈570/620/600 m. Caveats: ideal full-state sensors; 1.17 m never quotable as achievable; no N/N·m numbers.
**Karimi 2024 (DT, orphan).** MDO (Simulated Annealing + Minimax): 46.76 → 37.5 kg; **S_G 2.24–2.31** (criterion >1), **S_D 0.66** (0–2); critical roll band **415–1419 rad/s** at n=20 rifling; capture zone MD<5 m: 1055→2404→2960/5000; structural limits steel 1100 MPa, boards 120 MPa. Not rated in the register — decide: add row or drop.
**Wang Gang 2025 (B4, DT).** CFD/RBD coupled; **the resonance failure mode with numbers**: damping term H minimized when forward-body spin ω_f = −(fast-mode frequency) — **128 rad/s forbidden; 0 or 192 rad/s safe** (their airframe); S_g = P²/4M, S_d = (2T−H)/H criterion; aft body ≈1571 rad/s. All results at apex (subsonic) — instability domain not mapped over full flight. This is what S8 / risk 41 carry.
**US 6,981,672 (C9).** **Unread** (scanned, no text layer). Credited in-project for: fixed-canard 2-D geometry and "2-D steering from one actuation axis" (defeats that novelty claim). The steering/control pair split is credited to B3 (Jaiswal AIAA 2024-1105). Action: pull claim text from Google Patents/Espacenet before citing further.

### Dual-spin theory / swerve
**B16 Ollerenshaw & Costello 2008.** Canonical swerve results: any control = no-roll-frame force or moment at offset Δ_SLC; **spin-stabilised: force forward of the COP responds ≈180° out of phase**; force behind CG ≈ in phase; pure moment −90° (fin-stab) / opposite (spin-stab); Magnus acts 90° off AoA and is the only swerve driver when applying at the COP; use atan2. M549 params (Table 1): **V₀ ≈ 826 m/s, p₀ = 1674.1 rad/s, m ≈ 42.95 kg, C_NA 2.6314, C_YPA −0.96, C_MQ −27.7**; inertias ≈0.147/1.89 kg·m² flagged (scrambled table — verify against image before use). Validity: V, p frozen → local result, update downrange.
**W8 Costello & Peterson 2000.** No text layer; via ARL-CR-570: the 7-DOF dual-spin model (three translations + yaw/pitch + two separate roll states, bearing-coupled H,J,T,L,M,N); **gyroscopic term F = D(I_xx^F p_F + I_xx^A p_A)/(V I_yy)** — the ring's spin directly enters stability; two distinct spin-decay rates; example spin pair 7.3→6.7 / −10.1→−83.8 rad/s; swerve closed forms; model update at least once per 4000 cal of range.
**W26 Murphy 1963.** The definitions to teach from: **Sg = P²/4M; Sg > 1 required**; statically stable (M<0) is always gyroscopically stable; **dynamic stability band Sg ∈ (0,2)**; (1) dynamically stable ⇒ gyroscopically stable; (2) inside (0,2) high spin stabilises an unstable body and a stable body is dynamically stable; (3) outside, spin can destabilise; **resonance when spin = fast-mode frequency → catastrophic yaw** (roll-through-resonance is the failure of the constant-coefficient model); slow mode = precession (sets swerve spiral), fast mode = nutation; **yaw of repose → the classic right-hand drift**; roll decay closed form φ″+Kpφ′ = Kc and the C_lp↔C_f skin-friction relation.
**C5 Robinson & Berefelt 2011.** Flight-phase authority (supersonic/summit/terminal — terminal limited by gyroscopic stability, spin decay); tip-mounted control cannot synthesise dynamics, only trajectory-correct; "few tenths of a g" achievable with fuze canards (Lloyd–Brown); mechanism taxonomy incl. **ATK PGK: 4 de-spun fixed canards + bearing brake = bank-to-turn** (the Clancy patent); brakes are 1-D and irreversible; crossrange needs a free-spinning fuze, limited by max AoA before instability; PG vs PFG trade table; CEP context: CCF ~50 m, Excalibur <10 m, IGS spec <5 m; **error sensitivities: 1 °C → >50 m, 1 m/s wind → ≈50 m, 1 m/s muzzle velocity → ≈25 m at 25 km; downrange-dominant ellipse**; without IMU use yaw-of-repose upfinding; inner/outer loop recommended.

### Control mechanisms / sensing / adjacent
**W17 Fresconi & Plostins 2009.** The architecture's quantified justification: **despinning the control mechanism returns ≈10× authority vs body-fixed pulsing** (continuous footprint ≈12.5 km vs ~1.2 km at 50 N; pulsed at φC=180° has P̄=0.31; φC=30° = 9 % as effective). Authority linear in force, quadratic in footprint; axial location is the dominant lever: behind CG best; **at the CP → zero manoeuvre**; **nose canard (forward of CP) → authority reversed vs commanded roll** — exactly why ring roll angle must be right. Effector L/D: blades ~10, tabs ≤1, thrusters >10. Baseline: 46.17 kg, Ix 0.1706, Iy 2.034, 263 Hz spin, >500 m yaw-of-repose drift, AOA ≈1.1° near apogee. Roll signal assumed perfect (the sensing gap is explicit).
**W11 Corriveau 2011.** Authority = ‖J+J_L+J_Y‖/(mV); rules (fire behind CG for spin-stab; same roll orientation; second impulse Δs = k·2π/(ωF±ωS) cancels the epicyclic); numbers: 105 mm M1 α=3.0 mrad, J=10 N·s; 30 mm GSP 25.6 mrad. **Verdict: pairing is "not that effective" on spin-stabilised bodies** (L score 0.33) → aerodynamic continuous route is the right architecture.
**T22 Guan & Yi 2018.** 7-DOF plant with separate fore/aft rolls + bearing friction (eq. 16); **eq. 17: canard command defined in the de-spun forebody roll frame — the formal statement of the roll-angle dependency**; forebody spin decays fast after canards open while aft body keeps spinning (stability preserved); UKF observes **position only — does NOT observe roll** (don't cite it as a roll observer).
**W9 Yang GIF 2001.** Unread (no text layer; also not the cited 1993 AIAA paper). Only secondary GIF precedents (IAI TopGun 20 m CEP claim) can stand in meanwhile.
**Adjacent.** ADA441073: 17 ft crossrange change at 3750 ft; <10 ft IPP error with model refresh ≤4000 cal; authority ↓ with range-to-go. ADA607104: radar IPP benchmarks — RMS ≈718 m @OT 15% → ≈55 m @OT 50% (120 mm); design rule OT ≥ 20%, sensor ≤10 m / ≤5 mrad, IPP RMS ≤10% of range; drag-vs-thrust ambiguity (same class as our alternator-thrust modelling). ADA462961: gas-generator arrays ~1 N·ms, <4 ms, 250 mN — five to seven orders below an alternator's continuous envelope.

## Cross-paper findings (new, not in the earlier notes)

1. **Two "Wang" papers, two different groups** — Yi Wang (2015, Shijiazhuang) and Yu Wang (2018, Nanjing). "Wang et al." is ambiguous in any citation.
2. **Aero independence is illusory** — the thesis's coefficients come from Wang 2018, whose Table 2 *is* the same sparse 5-point Mach table the thesis flags for non-physical jumps. One source seen twice → **risk 8 (aero set) is even more the long pole**.
3. **Roll sensing is a genuine gap in the literature** — B16, C5, W17 assume a perfect roll signal; T22 doesn't observe it. Our ring-as-inertial-platform + pickoff approach is genuinely ours to prove (supports the novelty stance).
4. **The resonance failure mode now has numbers** (DT 2025: forbidden ω_f = 128 rad/s, safe 0/192) — teach it alongside Sg, never instead of it.
5. **The architecture choice is evidence-backed**: despun ≈10× pulsed (W17); thrusters ineffective on spin (W11); PGK's own published spec = de-spun fixed canards + bearing brake (C5).
6. **Class brackets from the papers**: mass 41.3–46.8 kg; Iy ≈ 1.2 (thesis) → 2.0 (ARL baseline). Our 45.0 kg / 0.155 / 1.75 sits mid-bracket, deliberately not the flattering end.

## Register consequences / actions

- B2 and B4: **full reads done → retire the abstract-only `†` flags**; B4's row can now carry the 128/192 rad/s numbers.
- C9 (patent): Cite-4 with unread text remains a Rule-1 defect — pull claims externally, then update.
- Karimi DT 2024: unrated orphan — add Cite/Adopt rating or drop.
- W8/W9: no text layers — note in `notes/04`; W8 theory reachable via ARL-CR-570.
- B16 Table 1 inertia/AoA pairings need image verification before use as design inputs.
- The description's claim #4 ("continuous IPP is new") remains uncorrected in the draft — it is not new (Zhang 2019 full read confirms).

## QB → paper map (condensed)

| QB | Primary | Secondary |
|---|---|---|
| QB1 mass | Thesis Table 5.1; CJA Table 1; DT2024 Table 6 | W17 baseline; B16 M549 |
| QB2 flattering numbers | — (cross-check only; class bracket above) | — |
| QB3 stability | **W26 (Sg = P²/4M, bands, resonance)**; DT2025 (S_g/S_d criterion, 128 rad/s) | DT2024 Table 6; C5 (margins/degradation) |
| QB4 spin | **B16 (M549 p₀ 1674); DT2024 (415–1419 rad/s); W26 §5.5 (decay)** | Thesis 1623→1050; CJA 1445; T22 |
| QB5 pair mechanics | **CJA §2 eqs 11/17/18**; Thesis Fig 2.4; W17 Table 4 | C5 taxonomy; patent (credited) |
| QB6 authority | W17 (≈10×, footprints); C5 (few tenths g; Bakken) | CJA 570–620 m; B16 per-lbf |
| QB7 swerve | **B16 eqs 45–50**; W26 §6.9 | C11 (§03 notes); ARL-CR-570 eqs 57–62 |
| QB8 guidance | CJA (IPP method); C5 (PG vs PFG) | W11 rules |
| QB9 sensing | **gap in literature** — W17 assumes perfect roll; T22 position-only UKF; C5 upfinding options | — |
| QB10 CEP | C5 (50 m/<10 m/<5 m; sensitivities); CJA (206→1.17→24.73 m) | ADA607104 IPP RMS; B16 5280 ft |
| QB11 friction | Wang 2018 eq. 7 (cV, cR); ARL-CR-570 bearing coefficient | Thesis Tf = 0.1 N·m |
| QB12 alternatives | W11 (thrusters); ADA462961 (gas generators); W17 (taxonomy) | Thesis alternator (the chosen one) |
