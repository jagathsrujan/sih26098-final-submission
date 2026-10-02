# 06 — Judge defense brief (adversarial pass, Step 5)

Internal Q&A armoury for the idea round (and the final round if selected). Rule of engagement: answer in the printed discipline — **value → status/source → what closes it** — and never claim one inch beyond the submission's text. Where an answer quotes an internal figure that is NOT printed, it is tagged *(internal — quote only with its status)*.

---

## A. Accuracy and the CEP budget

**A1. "Your 23.9 m is a spreadsheet number."**
A: Correct — and we say so in the text: it is a derived one-sigma budget (nav 5 / G&C 17 / meteo 5 / aero 8 / fuze 3 → RSS 20.3 m, CEP = 1.1774 σ), ~20 % inside the 30 m requirement. The seven-degree-of-freedom Monte Carlo with the guidance loop in the loop **produces** the flight CEP — it is the first deliverable of the validation plan, not an afterthought. We assert the method, not the outcome. [G4 DEFINED · closer: R5/§10.3]

**A2. "Why those five allocations? 17 m for guidance and control looks invented."**
A: They are design budgets from the sizing and error analysis, and the Monte Carlo traces every error source to its contribution so the budget is managed rather than asserted. The guidance-and-control line is deliberately dominant: it carries the impact-prediction residual — the drag, muzzle-velocity and wind biases — which is exactly what the in-flight estimator attacks, targeting the budget's two largest terms. The navigation line itself carries a derived 3.7 m sub-allocation (GNSS 3.0, inertial/filter 2.0, timing/lever 1.0).

**A3. "Where do 94/125/150/267 m come from? Those are not Indian figures."**
A: They are the published record for the fielded class (the PGK programme's own published figures, NDIA 2015) — we attribute them as such and never as service data. YIL firing tables are post-selection documents; the parametric design basis exists precisely because platform data is not ours to hold before selection. *(If the PS text quotes different figures: lead with the PS's own numbers and keep ours only as the published class record.)* [M6 PARAMETRIC · closer: YIL tables]

**A4. "CEP = 1.1774 σ — justify."**
A: The standard circular relationship for a zero-mean circular normal miss distribution. The Monte Carlo produces the two-dimensional impact distribution and reads CEP directly, so the conversion factor is a presentational bridge, not a hidden assumption.

**A5. "Your budget closes at 20.3 but you print 23.9 — which is the claim?"**
A: Both, with distinct meanings: 20.3 m is the one-sigma radial RSS; 23.9 m is the implied CEP (50 % circle). The requirement is stated in CEP, so the claim of record is CEP ≈ 23.9 m against 30 m.

**A6. "Have you run any simulation at all?"** → see **Prepared reconciliation R1** below.

## B. Authority and margins

**B1. "Where does 18.1 N come from?"**
A: The canard sizing analysis on the parametric 45.0 kg public-data reference platform, taken as a minimum across the guided window. It is a derived figure, provisional on the aerodynamic coefficient set — the acknowledged long pole — and the guided-window analysis in the Monte Carlo campaign re-quantifies it. The force band (15–25 N mid-flight, ~85 N transient) comes from the same derivation. [C8/M7 DERIVED · closer: R5]

**B2. "407 m required — prove it."**
A: It is the correction span needed to capture 80 % of the unguided population given the class dispersion anchor; 450 m is what the canard force integrates to over the guided window. Both are derived, both re-quantify with the platform data and the aero set.

**B3. "1.11:1 is a thin margin."**
A: Agreed — and the text says it plainly: a margin stated as a margin, not as comfort. Two things make it usable: the state-dependent authority gate (current and velocity limits scheduled from the observed disturbance, so authority is never lost where the torque collapses at apogee) and the error estimator that shrinks the correction demand. The accuracy claim does not lean on the margin — the CEP budget has its own ~20 % headroom.

## C. Machine, power and thermal

**C1. "121 kJ through a fuze well in 90 seconds — that is a blowtorch."**
A: The figure is honest and printed with its cost: 2.92 kW peak, ~121 kJ per flight, leaving through a declared thermal interface rather than a hidden loss. The interface requirement is ≥ 58 W/K peak against a bare 2″-12 UNS thread at 3–16 W/K; the closing route — contacting radial path through the well bore, conductance-specified joint, peak/average split, active dissipation stage with a graphite spreader and AlN dump resistor — is designed (not assumed) and confirmed on the rotating dynamometer rig. The peak is burst duty, not continuous dissipation. [W7/P6 · closer: R7 rig]

**C2. "Iron losses at 2,130 Hz?"**
A: The stator trade is thin laminations versus soft-magnetic composite on published loss data (≈83 W/kg at 1 T/1 kHz, material characterised to 5 kHz — the machine's electrical frequency range). *(Internal: a rough estimator puts iron loss in the tens of watts; it is deliberately NOT claimed until the calibrated loss model closes — never quote 50–60 W as a result.)* [C39 OPEN · closer: calibrated iron-loss calculation]

**C3. "Why not just use a battery?"**
A: The alternator-as-actuator is the fielded architecture (M1156 specification, claimed in US 6,981,672) — we credit it. Its economy is the product premise: no flight battery to qualify for a 90 s high-g flight, one moving assembly, and the de-spin machine doubles as the generator. A reserve battery exists for pre-launch and the safe state only — which is also the safety story: unpowered in storage means no arming path.

## D. Mass and SWaP-C

**D1. "2.7 kg is roughly double the fielded kit — you fail SWaP-C."**
A: Stated openly in the submission: ≈2.7 kg aluminium analysis (4.8 kg steel), net +1.7 kg ≈ 3.9 % of the 45 kg all-up round — roughly 2× the fielded total and ~4× its net penalty. The 1.4 kg target class is not met and we do not pretend otherwise. The levers are named (material, ring diameter, retention hardware — spigot −0.59 kg already banked) and the gate the mass must close against is the requirement that actually binds: **better than 90 % range retention**. These are CAD figures, not a weighed article; the trade closes at detailed design. [P9 PROPOSED · closer: P9 ruling + YIL acceptable-mass, post-selection]

**D2. "Then re-baseline the design at 1.4 kg."**
A: That is the open trade, and it is engineering, not slideware: every lever is a real design variable with a cost on the other side (ring diameter fights the T8↔C44↔M10 triangle; retention fights the 382 kN load path). We would rather present a measured 2.7 kg with named levers than an aspirational 1.4 kg.

**D3. "+3.9 % mass — what does that do to range?"**
A: That is precisely the >90 % range-retention gate, computed against drag and mass effects on the trajectory model; achieved retention is a P3 output once the coefficient set lands.

## E. Cost

**E1. "₹6.5 lakh is a wish."**
A: It is labelled a target in the text, with its exclusions (development and tooling) and its volume assumption (5,000/yr, to be confirmed with the procurer) — a like-for-like comparison against the fielded kit's published US$13,541 recurring price. The priced, ranked cost roll-up is a named post-selection deliverable; the two-tier process strategy (no new tooling, or dies shared across part families) is what makes the target credible at that volume. [K4 DEFINED · closer: K5]

**E2. "US$13,541 is a 2013 price at >100,000 units — unfair comparison."**
A: Which is why we print the volume gap ourselves (slide 5): the fielded figure is published, at scale; ours is a certified-volume assumption at 5,000/yr. The comparison is disclosed, not hidden — and the direction of the gap favours honesty, not us.

## F. Fuze, safety and F16

**F1. "The 150 m withhold is copied."**
A: Adopted rather than invented — it is the fielded kit's published figure and we credit it, with the AOP-22 command mode as the standards basis. The contribution is its integration: the kit's own impact prediction doing the deciding, latched and irrevocable.

**F2. "F16 turns near-misses into duds. Is that acceptable?"**
A: The cost is stated in the submission, not hidden: the decision is a prediction, so a prediction error can withhold function on a round that would have landed acceptably. The exposure is bounded by propagation error over the remaining flight, which is why the decision is taken as late as the authority allows. The deliberate dud-rate contribution is an explicit open item with a named closer. [F10 OPEN]

**F3. "What stops the veto being spoofed, or failing the round safe-open?"**
A: It is absent by default: the veto travels the same bounded, one-way, arming-gated path as the time correction — if the kit says nothing, the fuze arms and functions on its own pre-set terms. The failsafe is the withholding of a command; the rotor never goes in line, so there is no new element in the explosive train and no new function path.

**F4. "Setback and spin interlock thresholds?"**
A: Interlocks are dual and independent (setback + spin) with an out-of-line S&A; threshold values are fixed at the hardware-definition phase against YIL data and standard practice and are deliberately not claimed before that. [F7/F8 OPEN]

## G. Guidance, navigation and sensing

**G1. "Impact-point prediction is not new."**
A: Agreed, and the submission credits it to the published literature (Zhang et al. 2019 and the fielded practice). What is ours is stated narrowly: the state-dependent authority gate, the estimator integration, the sensing arrangement and the fuze discipline.

**G2. "Adaptive bias estimation is not new either."**
A: Correct — and the text now says so: bias estimation per se is established practice; the contribution is its integration with the impact-point loop, aimed at the budget's two largest terms (prediction and meteorological residuals).

**G3. "The de-spun ring as inertial platform — you say it is 'ours to prove'."**
A: Yes, and we say it first. The published work assumes in-flight roll knowledge rather than solving it (the analyses take the roll signal as given). Removing 1,107–1,912 rad/s of spin turns the hardest sensing problem into a conventional low-rate measurement; the ring-angle chain (relative pickoff + magnetometer absolute) is a bench-verifiable item and proving it is a named task of the bench programme.

**G4. "A barometric sensor at Mach 2?"**
A: An aiding channel only — for altitude and air-density estimation — not the primary navigation source; GNSS/INS carries the solution. Its selection closes with the sensor verification item. [N11 OPEN]

**G5. "GNSS is jammed — then what?"**
A: Three answers, in order: the solution coasts on inertial to the drift limit (the tolerated outage duration is set and verified in the Monte Carlo campaign — not asserted); anti-jam GNSS is a module-level substitution (we quote no null-depth or margin figures, because none are set — that is an open sizing item); and the growth path (cooperative beacon fix, fielded-type SAL seeker) is a reserved module interface described as options, never as delivered capability.

**G6. "The spin-axis GNSS aperture — antennas on spinning bodies exist."**
A: The claim is the specific arrangement for this kit — elements combined rather than switched on the spin axis, so there is no spin-frequency modulation to track out and a standard receiver stays usable — not antenna theory. It is stated narrowly and checkable.

## H. Stability and structures

**H1. "Roll-through resonance — you have no evidence."**
A: The submission agrees with you in advance: the design's disposition is the span-capped canard ring (tips at Ø151 mm), and the quantitative evidence is a named task of the 7-DOF campaign — an open evidence item, not a settled result. *(Internal: the design point sits near Sg ≈ 1.8 across a parametric envelope — quote only as parametric, never as measured.)* [S8 OPEN · closer: P3]

**H2. "382 kN setback — where did 74 kN go?"**
A: 74 kN was a superseded estimate and appears nowhere in the submission; 382 kN axial / 127 kN radial is the re-baselined figure (measured in the CAD load cases, ×5.2 correction on the ring-side mass) carried through continuous metal in the retention path, routed around the flight bearings. [C26/C35 DERIVED · closer: C32 structural analysis]

**H3. "2 mm per side clearance — will it survive the bore?"**
A: The clearance budget caps the canard tips at Ø151 mm so the assembly cannot foul the bore or the rammer; permanently exposed canards mean in-bore safety is a static clearance question, not a mechanism-safety argument — the same choice the fielded kit makes. Magazine and handling constraints apply to a fixed envelope.

## I. Manufacturing and production

**I1. "The digital-cell and printing story is hand-waving."**
A: It is labelled in the text for what it is: development and first-article tooling, not production assumptions, bounded by published process data held in the dossier, carrying their own qualification cost outside the recurring unit — validation is post-selection first-article work. The production tier is deliberately boring: machined one-datum ring, conventional concentrated winding (skin depth ~1.4 mm at 2,130 Hz — no printed conductor needed on loss grounds), MIM where the family justifies the tooling. *(Never quote the dossier's process numbers — 79 %/87 %, 98 % IACS, 368 W/mK, −⅓ head — they sit on unopened register rows.)*

**I2. "5,000 kits a year — who certified that?"**
A: Nobody yet: it is the stated production volume assumption for this class, and the procurer confirms the share of consumption post-selection. The process strategy is sized to it and the cost comparison discloses it.

## J. Embedded, verification and format

**J1. "1 kHz control on a spinning projectile — timing and jitter under launch?"**
A: Deterministic by construction — bare-metal or fixed-priority RTOS on the control core, navigation and guidance on the second core — with jitter an explicit verification item of the bench rig. [G13/H1 · closer: R7]

**J2. "How does data cross from the de-spun ring?"**
A: The cross-frame link is a defined interface decision at hardware definition — contactless coupling across the bearing gap (inductive/short-range optical alongside a magnetic pickoff), with the slip-ring/rotary-transformer options held in the design register. No number is claimed before that decision.

**J3. "No prototype — why should we believe a paper design?"**
A: The format makes the prototype preferred, not mandatory, for Hardware Edition; our proof-of-concept plan buys information per rupee in order — 7-DOF Monte Carlo, then the rotating dynamometer bench (the PoC that the constraints hold in hardware: ring-angle tracking under applied disturbance torque and spin), then the integration demonstrator with the inductive programming chain end to end and the safe-and-arm logic under simulated setback and spin. The deliverables list matches the PS's own.

**J4. "5,000 + 5×1,000 Monte Carlo runs is still simulation."**
A: Yes — with hardware-in-the-loop closing the one loop pure simulation leaves open (real ring hardware in the attitude loop) and the rig producing the measured alternator constant and friction data that close the design. Simulation is where a CEP claim is legitimately produced.

---

## Prepared reconciliations

**R1 — "Have you run any simulation?" / the 21.5 m question.**
A: Yes — earlier methodology runs on a predecessor guidance configuration produced CEP50 ≈ 21.5 m with every run terminating in guidance. Those are methodology-vintage results on a superseded configuration, so the submission's claim of record is the conservative derived budget: CEP ≈ 23.9 m. The platform-matched seven-degree-of-freedom campaign re-quantifies both. *(Internal: never present 21.5 m as the submission's claim; never let it "disagree" with 23.9 m — one is a superseded-methodology result, the other the budgeted claim, and the planned MC arbitrates.)*

**R2 — PS dispersion figures differ from 94/125/150/267 m.**
A: Lead with the PS's own figures; ours are the published fielded-class record, cited and attributed. Requirement is unchanged: CEP ≤ 30 m at full charge and long range.

**R3 — Guided-window duration ("isn't it about 15 seconds?").**
A: The window is defined by the authority gate, not a fixed clock — the gate opens where dynamic pressure gives authority and closes where it does not; its duration is a quantified output of the guided-window analysis. *(Never print or quote t ≈ 15 s — it is an unvalidated placeholder.)*

**R4 — "Smart Vehicles? This is a munition."**
A: The theme is the portal's bucket for SIH26098 (listed Hardware / Smart Vehicles); we copy the portal value character-for-character. The innovation content — guidance, navigation, smart fuze, embedded flight software — is exactly the PS's scope.

## Never-say list (would contradict the submission)

1. Never claim the two-pair canard split or the alternator-as-actuator as ours — they are M1156/US 6,981,672 lineage (expired patent, published spec).
2. Never claim the estimator mathematics as novel — integration only.
3. Never quote 21.5 m as the submission's accuracy claim (see R1).
4. Never quote iron loss 50–60 W as a result (uncalibrated estimator), t ≈ 15 s as the guided window, or any unopened process number (79 %/87 %, 98 % IACS, 368 W/mK, −⅓ head, ~1 % mass).
5. Never say resonance is "solved/dispositioned/verified" — disposition designed, evidence open (§10.3).
6. Never say the growth-module interface is "defined" — reserved, definition post-selection.
7. Never present the mass as meeting the 1.4 kg class, or the cost as more than a target.
8. Never imply YIL service data (firing tables, drawings, setter logs) is in hand — all post-selection.
9. Never claim anti-jam performance numbers (N5 sets null depth / margin / bandwidth later).
10. Never let a degradation mode sound worse than unguided — the governing rule is that no failure mode degrades below the unguided round; the F16 withhold is a separate, deliberate safety decision.
