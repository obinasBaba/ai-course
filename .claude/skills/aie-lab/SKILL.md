---
name: aie-lab
description: Run a hands-on lab for the current AI-engineering module — write the spec, acceptance criteria and test scaffold, coach the user through implementing the core logic with a time-boxed hint ladder, run tests, and log the resulting metric with provenance.
---

# aie-lab

The user builds. You scaffold, coach, verify, record.

## Procedure

1. **Identify lab.** Current module from `progress.md`; lab summary from `curriculum.md`. Confirm: "Lab `<mNN-slug>`: <one-line goal>. Go?"

2. **Verify versions.** Before writing anything, check current docs for any library/API the lab touches (WebSearch/WebFetch). Note the versions used in the spec.

3. **Write the spec** → `labs/mNN-<slug>/README.md`:
   - Goal (1–2 sentences, real-product framing)
   - Inputs (dataset + licence; public data only — never company data)
   - Tasks (numbered, small; each one testable)
   - Acceptance criteria (checkboxes; each maps to a test)
   - **The metric** to report + how to compute it + baseline to compare against
   - Stretch goals (optional)
   - Reading pointers (exact sections)

4. **Write the scaffold** (allowed): `tests/` with failing tests that encode the acceptance criteria, fixtures, data download/loader scripts, config, typed function **signatures with `raise NotImplementedError`** in `src/`. Do NOT implement AI/system logic. Python idioms may be shown freely when asked.

5. **Coach.** User implements. When stuck:
   - L1 concept nudge → L2 exact doc/guide pointer → L3 pseudocode. Never runnable logic.
   - Track time per step; >25 min stuck → offer the next level unprompted.
   - When they ask "is this right?", run the tests; let tests answer first.

6. **Run & measure.** `uv run pytest` (and the lab's metric script). Ask the user to **predict the metric before running**. Then compare prediction vs result in one line.

7. **Record** in `progress.md` → Lab metrics:
   `date | lab | metric | value | dataset | model+quant | params | labs SHA | baseline | note`
   Ask the user to commit in `labs/` first (they type the commit), then record the SHA.

8. **Close.** One-line takeaway from the user ("what surprised you?"). Suggest `/aie-review` for a code review, or continue the module.

## Rules
- Public data only. No company code/data/names in `labs/`.
- Prefer the user's `labs/common/llm.py` client; local Ollama by default.
- Keep each lab finishable in ≤2 sessions; split if bigger.
