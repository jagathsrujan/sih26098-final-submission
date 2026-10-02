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

**Next:** Round 3 — slide 4 (feasibility and viability): budget/authority/mass honesty blocks + fig2/fig3.
