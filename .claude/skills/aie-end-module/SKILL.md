---
name: aie-end-module
description: Close out an AI-engineering course module — user's Feynman summary first, then deep-dive notes, glossary, progress with spaced-review dates, 15–20 Anki flashcards (or .tsv fallback), portfolio log and next-module hint. Use at the end of every module.
---

# aie-end-module

Consolidate. No new learning.

## Procedure

1. **Identify module** from `progress.md`; confirm with the user.

2. **Feynman summary (user first).** Ask: "Explain this module in 5 sentences to a senior dev who hasn't done it — include one number you measured." Wait. Score clarity 1–5 and name the one gap. Their text goes verbatim into the deep dive.

3. **Write** `modules/NN-<slug>.md`:
   ```markdown
   # NN — <Module>
   ## In my words (user's Feynman summary, verbatim)
   ## Core concepts (each with source: book §, doc URL, or references/… path)
   ## What I built (lab path in labs/, commit SHA)
   ## Results (metrics table with provenance; baseline vs result; what surprised me)
   ## Gotchas & failure modes (from the lab, with evidence)
   ## Decision rules (when to use X vs Y — terse)
   ## Concept link (optional: how this maps to a real system the user knows, e.g. GTCOne — concepts only)
   ## Open questions
   ## Cross-references
   ```

4. **Glossary.** Append new terms to `glossary.md` (alphabetical, no duplicates, each with a source).

5. **Progress.** In `progress.md` → Modules: status ✅, completed date, self-assessment (ask 1–5), total hours (sum Session log), `Next review` = today + 7 days. Clear the Checkpoint section.

6. **Flashcards (15–20).** Mix: ~5 concepts · ~4 decision rules/trade-offs · ~3 predict-the-metric · ~3 failure modes · ~2 "write the formula as code" (front: task; back: the user's own ~5 lines from the lab) · ~2 explain-to-PM.
   Colorization (HTML): citations/paths → `<span style="color:#888">…</span>`; answer kernel → `<b style="color:#2563eb">…</b>`; failure-mode cards → back wrapped in `<div style="border-left:3px solid #dc2626;padding-left:8px">…</div>`. Max these three roles.
   Delivery:
   - Anki MCP available (`list_decks` works) → deck `AIE::<NN Module>`; `batch_create_notes` (Basic, Front/Back), ≤20 per batch. Confirm before writing.
   - Else → `flashcards/NN-<slug>.tsv` (`front<TAB>back`, HTML inline, no literal tabs/newlines). Import: Anki → File → Import → deck `AIE::<NN Module>`, tick "Allow HTML in fields".

7. **Portfolio log.** If the module produced something publishable (README metrics, chart, write-up), add a row to `progress.md` → Portfolio log and suggest one sentence for the labs README.

8. **Next hint.** One sentence: the next module per the dependency graph (and the paired AI-103 domain if any). Stop.
