# 03 — Description edits (changelog + how to apply)

The final description text is `02-description-FINAL.txt` — it was produced from `SIH26098-form-content.md` FIELD 4 by applying the six edits below. Net result at that pass: **49,903 / 50,000 chars (headroom 97)**, all stale numbers removed. **Superseded by the Steps 2–3 addendum at the end of this file: 49,843 / 50,000 (headroom 157).**

## What changed (vs the repo2 draft)

| # | Where | Change | Δ chars |
|---|---|---|---|
| 1 | §11.1 body | Replaced the loose authority narrative ("~85 N transient, 15–25 N band, 20 N on a 43 kg shell, ~18 m/s") with the register form: band + ≥ 18.1 N minimum over the guided window, 45.0 kg design point, 450 m vs 407 m, **1.11:1 stated as a margin** | −42 |
| 2 | §11.2 budget table | Guidance 15 → **17 m**, meteorological 10 → **5 m**, RSS 20.4 → **20.3 m**, CEP ~24 → **~23.9 m** | +2 |
| 3 | §15 mass bullet | Replaced "1.4–1.7 kg class / 1.0–1.21× / 1.55–2.2×" with the honest re-baseline: **≈2.7 kg aluminium analysis** (4.8 kg steel), **+1.7 kg net ≈ 3.9 % of the 45 kg round**, 1.4 kg target **not yet met**, levers named (material, axial-flux, ring diameter, retention, make-vs-buy; spigot −0.59 kg banked), gate = **> 90 % range retention** | +303 |
| 4 | §12 (retention line) | "the **74 kN** setback load" → "the **382 kN axial** setback load" (T6-ruled value) | +7 |
| 5 | §2 opening | "The kit replaces…" → "**STHIRA-PGK** replaces…" (the description never named the product) | +3 |
| 6 | §16 references | Cut **entries 7** (Khalil 2009) and **8** (Spagni 2009) — uncited in the body, least load-bearing; renumbered 9–24 → 7–22; in-text citations updated: `[2, 24]` → `[2, 22]`, `[23]` → `[21]` | ≈ −290 |

**Total: −22 chars** (measured in Python; the portal's live counter is the final authority — expect ±1 depending on newline convention).

## How to apply to repo 2 (keep the source repo consistent)

1. Replace the fenced FIELD 4 block in `SIH26098-form-content.md` with the full content of `02-description-FINAL.txt`.
2. Replace `SIH26098-idea-description-paste-ready.txt` with the same text (the old twin is ≈ identical, and the "named STHIRA-PGK in §2" insertion is now part of the canonical text).
3. Doc hygiene (outside the pasted text, optional but recommended):
   - Update the "Character count verification" table with a new row: description **49,903**, abstract **6,639** (re-measured 2026-10-01).
   - The post-fence note below §16 still cites old item numbers: "Items 2, 5, 13, 14, 15 and 16" → now **2, 5, 11, 12, 13, 14**; "Entries 1–8" → **1–6**.

## Re-measure command (run from repo2/submission)

```bash
python3 - <<'EOF'
from pathlib import Path
t = Path("SIH26098-form-content.md").read_text(encoding="utf-8")
i = t.index("## FIELD 4"); a = t.index("```", i)+3; a = t.index("\n", a)+1
b = t.index("```", a)
print("FIELD 4 chars:", len(t[a:b]))
EOF
```

## Addendum — Steps 2–3 (2026-10-02, submission-phase; log: `notes/07-submission-phase-log.md`)

Second pass applied on top of the six edits above:

- §1 dispersion sourced to published fielded-class figures [4]; service firing tables deferred post-selection.
- §4.3 MEMS wording → range statement; §4.4 GNSS-denial outage tolerance gets its closer (§10.3).
- §10.1 roll-through-resonance scope note: span-capped-canard disposition, evidence named in §10.3 — an open evidence item, not a settled result.
- **New §11.5 status block** — three-part format (value → status/source → closer) for every weak number.
- §12: cost objective stated (₹6.5 lakh @ 5,000/yr vs published US$13,541, development + tooling excluded); unopened manufacturing numbers stripped (98 % IACS / 368 W/mK, 79 %/87 %, −⅓ winding head, ~1 % mass) → freedom ledger; digital-cell paragraph tightened.
- §15: patent credit sharpened to the actual claims (US 6,981,672, 2006, expired — two-pair split + alternator-as-actuator = lineage); "no published treatment" → search-scoped; roll-sensing claim honest ("ours to prove"); "defined module interface" → "a reserved module interface — definition is post-selection work".
- §16: 22 → **12 references**, compact format; in-text citations renumbered ([4] ATK · [2, 12] Zhang + IEEE · [11] NATO STO).
- Abstract (`01-abstract.txt`) synchronised: published-record attribution, requirement wording ("30 m … at full charge and long range"), authority/cost/machine closers, patent lineage sentence, X18 fix.

**Current baselines:** description **49,850 / 50,000** (headroom 150) · abstract **7,079 / 10,000** · title **84 / 100**. Both texts final and paste-ready; the "How to apply to repo 2" steps above still stand (replace FIELD 4 + the paste-ready twin with `02-description-FINAL.txt`).

**Step 5 judge-pass fixes (2026-10-02):** §4.3 "largest sensing risk into a **solved item**" → "**bench-verifiable item**" (removed the §4.3-vs-§15 contradiction) · §15 estimator bullet gains "Bias estimation per se is established practice; the integration is the contribution." (novelty over-claim closed) · §6.5 AOP-22 tail trimmed to fund it ("…message-rejection criteria" clause removed). Net +7 chars → 49,850.
