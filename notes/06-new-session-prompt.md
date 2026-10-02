# 06 — New-session prompt: submission-only final design phase

**How to use:** start a **new session in THIS workspace** (`/Users/jagathsrujan/Documents/final submission sih`), set the session model to **MiMo V2.6 Pro** (`xiaomi/mimo-v2.6-pro`), and paste the block below as the first message. Research/file-reading subagents will use `deepseek/deepseek-v4.1-flash` per the prompt.

---

> **NEW SESSION — Submission-only final design phase (SIH 2026 · SIH26098 · STHIRA-PGK).**
>
> **Where to work.** Start in `/Users/jagathsrujan/Documents/final submission sih` (the resources workspace — all outputs land here). Read-only truth: `/Users/jagathsrujan/Documents/final-sih-pgk-kit-design` (design register, CAD, papers — do NOT edit). Reference: `/Users/jagathsrujan/Documents/smart india hackathon` (earlier team repo, read-only). Note: "notes/" below means THIS workspace's notes (00–05); the design repo has its own separate `notes/` folder (thesis material).
>
> **Read first, before proposing anything.** 1) `notes/00-INDEX.md` (orientation + upload traps). 2) `notes/03-submission-decisions.md` (locked decisions + outputs so far). 3) `notes/04-design-walkthrough.md` (the 11-module design walkthrough — the design story). 4) `notes/05-research-digests.md` (the proof base, question bank QB1–12). 5) `submission-resources/` (current drafts: abstract, final description, edit changelog, deck brief, QA checklist). For heavy reading or research, launch subagents with model **`deepseek/deepseek-v4.1-flash`** (explore-type, depth labels; tight budgets — never gulp a file >100 KB, never read images). Do not re-read papers wholesale; `notes/05` is the digest.
>
> **The mission.** Run a **submission-ONLY design phase**. The previous workspace tried to finish the full design (CAD, final-round engineering) and the submission at the same time — inefficient. This phase rewrites the **design definition and narrative to exactly the depth the SIH idea-submission round needs**:
> - **JUST ENOUGH:** every claim in the submission is sourced (register row / CAD evidence / paper digest), and every open item is either closed with a ruling or explicitly stated as post-selection work with a named plan. No loose ends a judge can catch.
> - **PRESERVE FREEDOM:** deliberately hold back what isn't needed now (unopened manufacturing rows, alternative mechanisms, extra novelty) in a **freedom ledger**, so the final round (if selected) can add novelty without contradicting the submission.
> - **NO SLIDE DECK PRODUCTION** — the deck is built manually by the user; this phase delivers only its **content pack** (update `submission-resources/04-deck-brief.md` if needed).
> - **No CAD work; no edits to the design repo** (propose patches instead); no new physical claims.
>
> **Submission requirements (the scope of record).** Idea Title ≤ 100 chars · Abstract ≤ 10,000 · Idea Description ≤ 50,000 · Idea Template PDF (6 slides, official template, ≤ 10 MB — content pack only here) · optional YouTube (currently skipped; revisit only if a clean capture exists) · Theme "Smart Vehicles" (confirm on the portal), Category Hardware · Team ID/Name from the portal · confirm the portal deadline.
>
> **Constraints & honesty rules (non-negotiable).** Authority order: design repo `design/00-design-criteria-register.md` ≻ evidence (CAD/atlas/sim) ≻ notes. Nothing unruled or provisional goes into printed claims (iron loss ~50–60 W uncalibrated; guided-window t ≈ 15 s placeholder; anti-jam numbers until N5 closes; unopened manufacturing claims; 400 V only ever as the "cannot store it" comparison). Derived-not-asserted; margins stated as margins; cite-and-credit the fielded kit, patent and literature where they are the lineage. Every number carries a status + closer; for any weak number use the three-part format: **value → status/source → what closes it**.
>
> **Method — step by step, with the user; log every decision.** Propose the step list first, then run ONE step per exchange, updating files as steps close:
> - **Step 0 — Intake & loose-end inventory:** use a subagent pass to inventory what the submission round requires (official format + portal fields + evaluation criteria); restate it; then inventory EVERY claim and open item across the four fields, map each to the register / `notes/05`, and list the true loose ends. Present this before anything else.
> - **Step 1 — Lock the claim set:** title (A: STHIRA-PGK), theme/team data, the canonical numbers; strip all stale values (see `notes/00` traps and the `03` changelog).
> - **Step 2 — Rewrite the design narrative step by step:** for each section of the description — purpose → claims → support → how open items are handled. The user decides anything genuinely open; you draft the words.
> - **Step 3 — Final texts:** abstract (~6–8k chars) and description (≤ 50,000 with live char math; §16 references are the trim bank).
> - **Step 4 — Template-PDF content pack** for the manual deck build + refresh the QA checklist.
> - **Step 5 — Adversarial judge pass:** act as a sceptical MoD evaluator; list every attack on every number/claim; ensure each has a register-backed answer or an explicit scope note; fix or defend.
> - **Step 6 — Freedom ledger & handoff:** what is deliberately NOT claimed now (kept for the final round), what to add post-selection; update the notes so a fresh session resumes cleanly.
>
> **Working conventions.** One step per session; the user approves before moving on. Ask real questions when a decision is genuinely the user's (options + a recommendation); otherwise decide and draft. Keep the step/decision log in `notes/` (extend `03` or start `notes/07-submission-phase-log.md`). Outputs: paste-ready, char-counted, in `submission-resources/`. The user has completed the full design walkthrough — do not re-teach the design from scratch; it is in `notes/04` and the register.
>
> **Begin with Step 0.** Present the loose-end inventory and the proposed step list, then wait for the user's go-ahead before rewriting anything.
