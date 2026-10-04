# 09 — Deck build log (slide content + figure plan session, 2026-10-02)

Running log for the deck-content session (one slide per round; user approves before the next). Plan of record: `~/.commandcode/plans/sthira-pgk-deck-slide-content-and-figure-plan.md`. Deliverables: `submission-resources/07-deck-slide-content.md` · `08-flowchart-spec.md` · `09-deck-export-qa.md` (round 5). Portal texts untouched. Repo2/repo1 read-only.

## Round 0 — exploration + decisions (2026-10-02)

Sources read (text only, no images): `notes/00-INDEX.md` · `notes/08-freedom-ledger.md` · `submission-resources/04/05/06` · `notes/07` (canonical numbers) · repo2 `fig4_system_flowchart.py` (fig4 = 3-lane architecture block diagram, 660×518, built for the template's ≈616×483 box) · `cad/README.md` (render map + colour key + "interface verifications only" rule) · atlas `scenes.json` (flow = phase-activation sheet) · `notes/02` (deck.html = 1280×720).

**User decisions (question round):**
1. Centerpiece flowchart = **ONE figure on slide 3** (tall column recommended; wide-band variant specced). Slide 2 carries a pointer chip only.
2. Flowchart grammar = **pure node/edge flow** + thin time-phase strip (no trajectory curve, no swimlanes).
3. Honesty wording = **inline canonical phrases** attached to each number.
4. CAD split = **3+3 by role**: slide 2 = 14+15 ring/canard roles, 18 bearing, 16+17 rotor/stator · slide 3 = 05 thermal, 21 fuze train, 19 electronics.

**Rulings this round:** "F16" is a register criterion ID → never prints on slides; behaviour printed as "predicted-miss withhold" (user's own ground rule "no criterion IDs"). Chart numbers limited to 150 m / 1 kHz / ≈ 90 s (+ spin band with "class band" tag if used).

## Round 1 — slide 2 + flowchart spec (2026-10-02)

- Slide 2 text delivered char-counted (python-verified): bullets 1,587 · header+credit+pointer 314 · callouts 645 · total 2,546.
- Wireframe (1280×720) + 3 labelled-CAD figure specs (F2-1 hero 14+15, F2-2 18, F2-3 16+17) with 10 callout labels written to teach functioning.
- Centerpiece flowchart node/edge spec (15 nodes, 20 edges) + mermaid draft + redraw notes → `08-flowchart-spec.md`.
- Forbidden-value scan run on the new files: clean (see command in plan §5.2).

## Round 2 — slide 3 (2026-10-02)

- **Density choice (user):** option (a) — thumbs 205×104 strip + fig4 ~0.9×, everything stays on slide 3.
- Slide 3 text delivered char-counted (python-verified): 11 bullets = 1,041 chars (S1–S5 technologies · S6–S11 methodology, honesty phrases inline) · 6 thumb callouts = 264 · total 1,305.
- Wireframe adjusted to real heights: chart 600×528 tall-left (08-spec variant), fig4 561×440 (0.85× nominal, grow to 0.94× as text allows), bullets x632–1264 y506–704, thumbs strip bottom-left. Trim ladder recorded in 07.
- Figure specs F3-0…F3-4 written (chart, fig4 REQUIRED, 05/21/19 thumbs with h1–h6 callouts).

## Round 3 — slide 4 + figure scrub (2026-10-02)

- **Figure-integrity finding → decision (user): scrubbed SVG copies.** fig2 audited clean (canonical numbers only). fig3 and fig4 broke the deck rules *inside the image*: fig3 printed `14.1 N on the gated phase` (contradicting the printed ≥ 18.1 N claim), `apogee t ≈ 41 s`, `impact t ≈ 86 s`, a fixed 15 s window start (against "gate-computed, not timed"); fig4 carried criterion IDs (`[H1, G17]`-style), `OPEN` status tags, and non-canonical numbers (275 ms, 231 V, 24 GHz, 480/240 MHz, 150–200 J, ≈20:1, ≈12 W, 0.5–1.5 W, ≥1 J, +5.8 K, 10°, Ø30 mm, 0.1–199.9 s).
- Clean copies built from modified generator copies (repo2 untouched) → `submission-resources/deck-assets/fig3-canard-authority-clean.svg` + `fig4-system-flowchart-clean.svg` (fig4 also got the mandatory lineage credit footer). fig2 used as-is. Slide-3 mockup rebuilt on the clean fig4; scrub scan of both SVGs clean.
- Slide 4 text delivered (python-verified): 14 bullets = 1,708 chars (F1–F10 feasibility · R1–R4 challenges→strategies) + captions/callouts 229 = 1,937. Wireframe: bullets left x20–660 · fig2 + fig3-clean stacked right at native 1.0× · optional F4-3 (10-section) zone.

**Repo2 patch proposals (propose-only — repo2 never edited):**
1. `fig3_canard_authority.py`: cut the `14.1 N` legend variant → `dashed: 18.1 N required over the guided window`; time ticks → phase labels (`launch / mid-flight / impact`) with axis `flight phase — the window opens and closes by the authority gate`; `apogee t ≈ 41 s` → `apogee`; `impact t ≈ 86 s` → `impact — ≈ 90 s`; `inhibited band` → `gate limits command`; add footnote `Derived figures; the guided-window analysis re-quantifies them.`; open_svg height 216 → 232.
2. `fig4_system_flowchart.py`: apply the scrub list above (IDs, status tags, non-canonical numbers) + the lineage credit line before `close_svg()`. Full replacement map = `deck-assets/fig4_system_flowchart.py` (the modified copy).

**Next:** Round 4 — slide 5 (impact and benefits): cost honesty block, rounds/charges, growth wording.

## Round 4 — figure-direction revision: slide 4 re-cut (2026-10-04)

Trigger: user marked up the mockups — figure zones read **cluttered**, the charts **"feel AI generated"**. Direction: fewer graphs, tables / other data representation, **more CAD + research-paper tables & figures with references**.

**User decisions (question round):**
1. Slide 4 visuals = **tables + CAD, zero synthetic graphs** — fig2 + fig3 retired from the deck.
2. Research-paper figures, when used, = **redrawn clean `after Author year`** with credit captions — never scanned crops (foreign numbers cannot be scrubbed).
3. **The table owns the numbers** — bullets trim to honesty framing; every number prints once.

**Rulings this round:** third-party published figures print with "published" status + author-year credit (table 3: `206 → 24.73 m` Zhang/Yao/Zheng CJA 2019 · `CEP ≤ 30 m at ≈ 27 km` Yi Wang IJAE 2015) · old F1/F2/F3/F5 numbers → tables 1–2 · old F4 → table 2 "Correction" row (`a margin, not comfort` stays attached to 1.11:1) · old F6 levers → table 2 "Target class" row · sub-allocation (3.7/3.0/2.0/1.0) = table 1 footnote (old F2 cut) · gate (90 %) stays in F4 bullet only (R2 echo, approved round 3) · `cad/10-section-through-axis.png` promoted from trim bank to **permanent** (more CAD per direction) · **fig2/fig3 retired** (repo2 untouched; `deck-assets/fig3-canard-authority-clean.svg` kept as a spare).

Deliverables: `07` slide 4 re-cut — python-verified: bullets 1,352 (12) · table rows 753 (14) · titles + captions + footnote + callouts 517 · **total 2,622** (round 3: 1,937; prose fell 1,708 → 1,352, numbers live in typeset rows) · wireframe + specs F4-1…F4-4 (tables = typeset text, redraw policy recorded) · `mockups/slide4-mockup.src.html` rebuilt (tables as live HTML text) → `slide4-mockup.html` + `slide4-mockup.png` 2560×1440.

Render note: Chrome headless hung twice (fresh + named profile) — the mockup was rendered with agent-browser instead. Reusable line: `agent-browser set viewport 1280 720 2` → `open file://…/slideX-mockup.html` → `screenshot …png` → `close`.

Forbidden-value + ID scan: slide-4 generator + print strings clean (residual `07` hits are rule/history lines only: ground rules, slide-1 `⟨from portal⟩`, slide-2 honesty map).

**Slide-6 patch proposal (propose-only):** add *Yi Wang et al., Int. J. Aerospace Eng., 2015* to the curated 12 — it now carries table 3; funded by `04`'s trim order (3) drop entry 10 (PS implicit).

**Round-4 hotfix (2026-10-04, user review: "fix the spacing of the table and the image cut off"):** table rhythm evened to 50 px (DOM eval measured: blocks 56–262 / 312–487 / 537–652, slack 52) · CAD figure moved to the bottom-left band (620×284, x20 y420) with `object-fit:contain` — full 2334×1313 canvas, machine never cropped (the 566×88 `cover` letterbox sliced it; canvas is 16:9 with the machine drawn tall in the centre) · first hotfix attempt put the figure at y352 and hid R3/R4 behind it — bullets measured to y404, figure now starts y420 · **print-integrity bug found by reading the render:** CSS `text-transform:uppercase` turned the `1σ (m)` header into `1Σ (M)` — headers now print exactly as listed (rule recorded in `07`). `07` wireframe + F4-4 spec updated to the measured layout.

**Next:** Round 5 — slide 5 (impact and benefits) under the same direction: rounds/charges + unit economics as tables, CAD hero (`04`/`01`), published figures credited per ruling 2.
