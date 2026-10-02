# 05 — Upload QA checklist

Work top to bottom once the manual deck PDF exists. Anything marked ⛔ blocks the upload.

## 0. Files in this folder

- `01-abstract.txt` — paste into **Abstract/Summary** (7,079 / 10,000 chars; repo2's `SIH26098-abstract-draft.txt` is superseded — don't use it).
- `02-description-FINAL.txt` — paste into **Idea Description** (49,850 / 50,000; headroom 150).
- `04-deck-brief.md` — content pack for the deck build.

## 1. Portal fields

| Field | Value | Check |
|---|---|---|
| Idea Title | `STHIRA-PGK: De-Spun Canard Guidance Kit with Multi-Mode Smart Fuze for 155 mm Shells` | 84/100 chars (max 100); portal counter confirms ✔ |
| Abstract / Summary | `01-abstract.txt` | portal counter ≤ 10,000 (7,079) ✔ |
| Idea Description | `02-description-FINAL.txt` | portal counter ≤ 50,000 (49,850) — **read the live counter, not our number** |
| Theme bucket | **Smart Vehicles** | ⛔ copy the portal value character-for-character at paste time |
| Category | **Hardware** | ✔ |
| Team ID / Team Name | ⟨from portal⟩ | ⛔ currently placeholders everywhere — fill on slide 1 before export |
| YouTube link | skipped | optional field left empty |
| Deadline | **5 Oct 2026** (exact time on the portal) | ⛔ the 02–05 Oct one-time edit window covers Team Name / Consent / PPT only |

## 2. Template PDF (PDF only; verify the portal's size cap — "≤ 10 MB" is unconfirmed)

- [ ] Built from the **downloaded official template**; section headings / idea-detail pointers unchanged
- [ ] Exactly **6 pages incl. the title page**; **instructions slide deleted**; points/diagrams only, no paragraphs
- [ ] Title-page fields complete: PS ID · PS title (verbatim) · theme · category · Team ID · Team Name · idea title
- [ ] **fig4-system-flowchart embedded** (the PS's electronics block-diagram deliverable)
- [ ] Fonts embedded; opens offline; size within the portal's cap

## 3. Consistency pass (PDF ↔ abstract ↔ description)

Locked values: **CEP ≈ 23.9 m** (budget nav 5 / G&C 17 / meteo 5 / aero 8 / fuze 3 → RSS 20.3) · authority **≥ 18.1 N**, **450 vs 407 m**, **1.11:1** · machine **2.92 kW / ≈ 121 kJ** · bus **180 V** · mass **≈ 2.7 kg Al (4.8 kg steel)**, net **+1.7 kg ≈ 3.9 %**, **1.4 kg target not met**, gate **> 90 % retention** · cost **≤ ₹6.5 lakh (~US$7,800) @ 5,000/yr** vs **US$13,541** (priced roll-up post-selection) · design point **45.0 kg** · F16 **150 m** failsafe · dispersion **94/125/150/267 m** ("published record for the fielded class") · spin band **10,000–20,000 rpm** · setback **382 kN axial**.

⛔ **Must not appear anywhere:** `20.4` / `~24 m` budget · `1.4-1.7 kg class` · `1.0-1.21` / `1.55-2.2` ratios · `74 kN` setback · `400 V` (unless as the deliberate "cannot store it" comparison) · `15,000–20,000 rpm` · "defined module interface" · "no published treatment … reports" as an absolute · "resonance dispositioned" as settled · unopened process numbers (`79%`/`87% IACS`, `98% IACS`, `368 W/mK`, "third of the winding-head", "one per cent of the kit's mass") · guided-window `t ≈ 15 s` · iron-loss `50–60 W` · criterion IDs (`[G4]`, "risk 46", "PARAMETRIC") · placeholders (`⟨…⟩`, "to be filled") · "the reference has no guidance law" style novelty claims.

**Credit-line rule:** wherever the two-pair canard split or the alternator-as-actuator appears, it is credited as lineage (fielded M1156 / US 6,981,672, 2006, expired). Only the sizing, thermal path, ring sensing, spin-axis aperture, error estimator, authority gate and F16 failsafe are claimed as ours.

## 4. Final steps

- [ ] Re-read the title page against the portal (PS ID, PS title verbatim, theme, category, Team ID/Name)
- [ ] Upload PDF → confirm the portal preview renders all 6 pages
- [ ] Paste title / abstract / description → confirm live counters and no truncation (our counts: 84 / 7,079 / 49,850)
- [ ] Save a copy of the uploaded PDF into this workspace and note the upload time in `notes/03-submission-decisions.md`
- [ ] If using the 02–05 Oct edit window: **one-time only** — Team Name, Consent, PPT
