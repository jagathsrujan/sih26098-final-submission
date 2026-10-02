# 01 — "smart india hackathon" repo (25 Aug – 1 Sep 2026)

Path: `/Users/jagathsrujan/Documents/smart india hackathon` · git repo · branches: `main` + `research/*` (D_sensors, E_fuze, G_structure) + remote design branches (`design/cleansheet-rev13-20260831`, `design/cleansheet-sync-20260830`).
Role: the earlier **team working repo** — a "live research OS" with 108 cataloged ideas, an auto-generated LIVEBOARD, team branches, a clean-sheet design of record, and simulation/electronics evidence. Superseded material was archived into `legacy/` on 1 Sep.

**Hard boundary stated everywhere**: inert exhibition / analysis design only — no energetics, no live S&A. Deadline noted here: **20 Sep 2026**. Teams: 2 teams × 6 roles; branch = research role (`research/01_mech-CAA-<user>` …).

## Concepts in this repo

**Active / current at 1 Sep**
1. **Clean-sheet PGK (design of record, Rev 1.7)** — three-frame kit: S (shell) spins ~250–267 rev/s; R (rotor/canard) roll-aimed by a pancake outrunner BLDC; Ø3 balls are the de-spin joint. Threaded-race bearing-in-well; one-piece 4-fin canard shell mirrored ±3°; 24 slots / 12 pole-pair pancake machine; axial-only ignitor crossing. Docs: `cleansheet/03_DESIGN_REPORT.md` (Rev 1.7), `cleansheet/PGK_CleanSheet.FCStd`, `cleansheet/HANDOFF.md`.
2. **Reference flight software (FSW Rev 1.0)** — deterministic Python mirror of the STM32G474 deployment: 400 Hz servo / 40 Hz sensors+roll / 100 Hz EKF predict / 1 Hz GNSS / 1 Hz guidance; 33/33 tests green. On-board budget: GNC < 0.5 ms worst 1 Hz tick, RAM < 5 KB, flash < 20 KB.
3. **GNC methodology "Rev E"** — RollEKF + DragAnchor (azimuth-only R) + SlowFit (cd, wy) + adaptive mode ladder (pre→acq→guide→degraded→denied→ballistic); L0/ZEM/APN trade.
4. **Sensor selection (Rev 1.0)** — u-blox NEO-F10N (GNSS), TDK ICM-45686 (IMU; note: replaced ICM-42688-P whose ±2,000 dps fails the 4,000 °/s constant), MPS MA732 (angle), ADXL1004 (setback), RFbeam K-LD7 (prox radar). LC29H(AI) rejected (10 km ceiling < 12 km apogee).
5. **Dual-domain electronics architecture (decision 23, Rev 1.0)** — shell frame A6 board: STM32G431CBT6 + DRV8329 + 6× NVMFS5C460NL + 3× INA240A2, 15 kHz FOC; dome GNC board: STM32G474RET6; cross-frame slip ring C3 = `+5 V | GND | UART` (115.2 kBd, CRC; 100 ms loss → safe state). KiCad ERC: 0 errors / 0 warnings; 34 components / 170 nodes.
6. **Common-carrier bench demonstrator** — inert exhibition artifact (single 61811 de-spin bearing, Ø106 dome-nosed de-spun stator + 4 strakes, 12-pole ring motor, detent pawl + solenoid launch lock, Ø87 GNC PCB, 6× 14430 cells, NEO-M9N). **Not** the design of record.
7. **Flight-kit + COTS BOMs (v2.0)** — paper per-kit build and bench-demo bill.
8. **108 cataloged ideas (A–J)** — `SIH26098_Exhaustive_Ideas_Catalog.md` + `_Ideas_Database.json` + `_Ideas_Catalog.csv`.

**Evaluated / parked**
- **Cold-gas (or hypergolic) RCS PGK** — fixed canard ring doubling as RCS: 24 nozzle exits, 8 channels, one rotating metering disk; no de-spin motor. **Rejected by physics eval**: 300 bar cold gas needs a 3.3 L tank (22× the Ø35 bore); opposite-face firing cancels force into torque; best case is a solid gas-generator terminal trim at 10.8 m/s (72 % of the 15 m/s requirement). Docs: `SIH26098_COLDGAS_PGK.md`, `SIH26098_COLDGAS_PHYSICS_EVAL.md`; scripts in `scratchpad/`.

**Archived**
- Two-motor N20 + face-gear design, earlier common-carrier demo, Ø155×778 printed shell mockup, electronics block-diagram example, letter-folder research (A–J) — all in `legacy/` (commit 85b9508: "archive superseded artifacts under legacy/ — main = cleansheet+electronics+active research"). `legacy/README.md` explains each archive reason.

## Version timeline (this repo)

| Mark | Date | What |
|---|---|---|
| initial | 25 Aug | "live research OS" repo: idea catalog, team structure, LIVEBOARD, branch-based research onboarding |
| switch | 28 Aug | active PGK demo → common carrier |
| Rev 1.1 | 30 Aug | clean-sheet design track: native FreeCAD Assembly (24 links / 23 joints) + 122-frame kinematic Simulation; declared design of record |
| Rev 1.2 | 30–31 Aug | steering-effect sim; de-spin re-spec 10 s/60 A regen-dominant → **15 s @ ≤40 A boost-sourced + brake chopper**; GNSS lock 35 → 45 s; mass 1.77 → 1.84 kg; energy ≤ 0.9 Wh worst case |
| Rev 1.3 | 31 Aug | GNC pass: roll-reference corrected (collar↔bell angle sensor is relative-only; absolute nose roll acquired post-de-spin via drag referencing); fin authority restated **q-scaled** (60 N = q at 70 s, ~0.5 N at lock); electrical frequency 1.25 → **3 kHz**; de-spin re-specced |
| Rev E | 31 Aug | GNC methodology + Monte Carlo (seed 20260901): **CEP50 21.5 m** (gate ≤ 30 m), 233 guide + 17 degraded, 0 denied; 9.9× vs unguided 212.3 m. Fixes the Rev D rad/deg unit bug (~3283× anchor R error) + settled-window anchoring + adaptive-R ladder |
| Rev 1.4–1.7 | 1 Sep | Rev 1.4 Rev E terminal accuracy; 1.5 `flight_sw/`; 1.6 sensor selection; 1.7 dual-domain electronics |
| archive | 1 Sep | `legacy/` freeze + refined design/submission artifacts; submitted 6-slide deck `SIH26098_PGK_Bharat_SIH_2026.pptx/.pdf` |

**Rev E key numbers** (250 primary + 80×5 secondary MC): unguided 212.3 · legacy windowed (idealized) 8.9 · **Rev E L0 21.5** (mean 22.1, p90 33.1) · ZEM 21.5 · APN 148.6 (rejected) · GNSS outage 60–70 s 17.6 · BLIND 115.2 · never-lock fail-safe 209.7. Deterministic spot checks: nominal 12.5, mount-bias 5° 18.1, crosswind 9.4, headwind 13.7, Cd+5 % 104.5 (authority-limited stress), BLIND 91.4. Predecessor Rev 1.2 numbers (guided 6.9 m) are flagged dishonest — constant 60 N + earth-referenced sensor.

## Directory inventory

| Dir | Purpose | Status | Key files |
|---|---|---|---|
| `cleansheet/` | Design of record: requirements → BOM → design report Rev 1.7 → GNC Rev E → sensors → electronics → FSW + sims + CAD | ACTIVE | `00_REQUIREMENTS.md`, `02_BOM_…` (Rev 1.4), `03_DESIGN_REPORT.md` (Rev 1.7; decisions 1–23, REQ-1…8, risks), `04_GNC_METHODOLOGY.md`, `05_SENSOR_SELECTION.md`, `06_ELECTRONICS_ARCHITECTURE.md`, `HANDOFF.md`, `PGK_CleanSheet.FCStd`, `flight_sw/`, `out_sim/`, `scripts/` |
| `cleansheet/scripts/` | Headless FreeCAD build + both trajectory sims | ACTIVE | `sim_gnc_check.py` (revC/revD/**revE**), `sim_guidance_check.py` (Rev 1.2 predecessor); CAD: `verify.py`, `build_bearing.py`, `bearing_piecewise2.py`, `build_thread_full3.py`; README marks older thread/bearing scripts superseded |
| `cleansheet/flight_sw/` | Reference flight software + co-sim + C header contract | ACTIVE | `fsw/` (config, dynamics, timebase, modes, sensors, nav, guide, ctrl), `cosim/` (`run_cosim.py`, `run_sensors.py`, `gen_golden.py`), `tests/` 33 green, `board/board_config.h` |
| `cleansheet/out_sim/` | Machine-generated evidence | ACTIVE | `RESULTS.md`, `RESULTS_GNC.md`, `RESULTS_FSW.md`, `RESULTS_SENSORS.md`, run logs, `steering_*.png` |
| `electronics/` | KiCad dome GNC schematic skeleton + generator | ACTIVE | `gnc_board.kicad_pro`, 4 sheets, `gen_gnc_schematic.py` (rerun == identical), `gnc_board.net` (34 comps / 170 nodes), `erc.rpt` (0/0) |
| `research/` | 6 PS-driven role folders + D_sensors + templates + merger | ACTIVE, lopsided | `06_electronics-embedded-power/` 8 entries, `D_sensors/` 6+1 entries; folders 01–05 README-only; `templates/`, `merge.py` |
| `legacy/` | Frozen archive ("new work never goes here") | ARCHIVED | `old_two_motor_design/`, `old_common_carrier_demo/`, `old_shell_mockup/`, `docs/archive/`, `output/electronics_example/`, `research-A-J/` |
| `cad_models/` | Bench demonstrator ("not the design of record") | separate | `PGK_155MM_ASSEMBLY.md`, `render_pgk_155mm.py`, `simulate_trajectory_155.py` (independent 3DOF M107), `out_pgk/` (STEP/STL/previews), stray `TwoCyl_Engine.*` |
| `tmp/` | Working artifacts | ambient | `viewer_template.html` → root `pgk_3d_viewer.html`; `gen_bom_csvs.py`; `deck/` pitch-deck pipeline (Node `create_ppt.mjs`); `pdfs/` rendered PS/format pages |
| `scratchpad/` | Parked cold-gas concept scripts | parked | `pgk_coldgas_physics.py`, `pgk_nozzle_sizing.py`, `pgk_solid_sizing.py` |
| `thesis_images/` | 95 figure crops from `10463953.pdf` (Günay, METU 2022) | reference | page-named PNGs |
| `.github/` | one workflow | ACTIVE | `workflows/research-sync.yml` — runs `research/merge.py`, commits LIVEBOARD `[skip ci]`; no test/CI gates |

Root artifacts: `README.md`, `SIH26098_TEAM_BRIEFING.md`, `TEAM_STRUCTURE.md`, `UNIVERSAL_PROMPT.md`, `SIH26098_LIVEBOARD.md`, idea catalog trio, `SIH26098_FLIGHT_KIT_BOM.md/.csv`, `SIH26098_COTS_BOM.md/.csv`, `SIH26098_PGK_KIT_DEEP_DIVE.md` (28 Aug bench design v1.0, superseded), `SIH26098_PGK_Bharat_SIH_2026.pptx/.pdf` (submitted 6-slide deck), `GuidanceKit_Thesis_Explainer.html`, `SIH26098_PS_Infographic.html`, `PGK_155mm.FCStd` + `COTS_Library.FCStd` (pre-cleansheet baseline; gitignored), `SIH2026_Hardware_PS.{md,json,csv}`.

## Tooling / how to run the evidence

- `python3 cleansheet/scripts/sim_guidance_check.py` → `out_sim/RESULTS.md`.
- `python3 cleansheet/scripts/sim_gnc_check.py revE` → `out_sim/RESULTS_GNC.md`, `revE_full_run.log`.
- `python3 cleansheet/flight_sw/cosim/run_cosim.py` / `run_sensors.py` / `gen_golden.py`; `pytest cleansheet/flight_sw/tests/ -q` (33 tests, run from `flight_sw/`).
- `python3 research/merge.py` → rebuilds LIVEBOARD.
- `python3 cad_models/simulate_trajectory_155.py` (independent 3DOF M107 study).
- `~/.local/bin/kicad-cli sch erc electronics/gnc_board.kicad_sch` → `erc.rpt`.
- FreeCAD: headless `freecadcmd` only (GUI booleans/helical sweeps crash it); entry scripts in `cleansheet/scripts/`.
- No `requirements.txt` / `pyproject.toml` anywhere — deps are implicit (numpy, matplotlib, pytest, FreeCAD 1.1.3, KiCad 10.x, Node, LibreOffice).

## Superseded → current map (top items)

| Superseded | Current |
|---|---|
| `legacy/old_two_motor_design/` (2× N20 + face gears) | `cad_models/` common carrier → `cleansheet/` |
| `legacy/old_common_carrier_demo/` | `cad_models/render_pgk_155mm.py` + `out_pgk/` |
| `legacy/old_shell_mockup/` (printed shell) | `Projectile_Body` in `PGK_155mm.FCStd` |
| `legacy/output/electronics_example/` (block diagram) | `cleansheet/06_ELECTRONICS_ARCHITECTURE.md` + `electronics/gnc_board` |
| root `PGK_155mm.FCStd` (strake/de-spun stator baseline) | `cleansheet/PGK_CleanSheet.FCStd` (design of record) — root file stays as the `cad_models/` bench source |
| `legacy/research-A-J/{A,B,C,E,G,I}` letter folders | `research/01–06` role folders (`D_sensors` was promoted, not archived) |
| `sim_guidance_check.py` (Rev A/B idealized) | `sim_gnc_check.py` revC→revD→revE |
| `out_sim/RESULTS.md` (6.9 m, "dishonest") | `RESULTS_GNC.md` (21.5 m) → `RESULTS_FSW.md` → `RESULTS_SENSORS.md` |

## Open threads (top)

1. Doc-lag: `cad_models/PGK_155MM_ASSEMBLY.md` still calls root `PGK_155mm.FCStd` the "active baseline" while `cleansheet/HANDOFF.md` names `PGK_CleanSheet.FCStd` the design of record.
2. Root CAD `.FCStd/.step/.stl` gitignored → a fresh clone cannot regenerate `cad_models/out_pgk/`; much on-disk legacy output untracked. `legacy/attachments/` referenced by `legacy/README.md` does not exist.
3. `merge.py` never writes the ideas DB ("next step" TODO); LIVEBOARD still flags 3 missing URLs; research folders 01–05 have 0 entries (only 06 + D_sensors populated).
4. Naming drift: `HANDOFF.md` title says "Rev D" but body says Rev 1.7; env paths still Linux; `board_config.h` comments TLV7011 where BOM says TLV7031.
5. Engineering rungs still open: 6DOF truth (Magnus, spin decay) + ≥1,000-run MC for the formal CEP; dome Ø62 4-layer PCB layout; bench bring-up B1–B4; C port of `flight_sw/` + 15 kHz FOC ISR timing; REQ-1 retention lip / REQ-2 shear pins designed-not-modeled; magnet-ring pole change 24→12; mass optimisation to 1.58 kg; radome RF re-verification ≥85 %.
6. Repo hygiene: `.playwright-mcp/`, `.pytest_cache/`, `excalidraw.log`, `tmp/`, `thesis_images/` not fully gitignored.

Details beyond these notes live in the repo itself — start at `README.md`, `SIH26098_LIVEBOARD.md`, `cleansheet/HANDOFF.md`.
