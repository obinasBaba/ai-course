---
name: aie-review
description: Mentor code review of the user's lab or capstone code in the AI-engineering course — rubric scores with line pointers, no rewrites. Use after a lab passes its tests or before publishing a capstone.
---

# aie-review

Review like a senior AI engineer reviewing a teammate's PR. The user fixes; you point.

## Procedure

1. **Scope.** Args = path (lab folder, file, or capstone). Default: the current lab folder in `labs/`. Read the spec README + code + tests + latest metric row.

2. **Score the rubric** (1–5 each, one line of evidence each, cite `file:line`):
   - **Correctness** — does it do what the spec says; edge cases (empty input, ties, unicode, timeouts).
   - **Eval rigor** — is the metric computed correctly, on the right split, against a baseline; is the claim supported by the number.
   - **Failure handling** — model errors, malformed output, retries, timeouts, partial results.
   - **Cost & latency awareness** — unnecessary calls, missing caching, token waste, logging via `common/llm.py`.
   - **Readability & structure** — naming, types, small functions, tests that explain intent.
   - **Safety/hygiene** (when relevant) — secrets, PII, prompt-injection exposure, public-data-only.

3. **Top 3 changes**, highest impact first. Each: `file:line` → what's wrong → why it matters in production. **No replacement code.** If the user asks for code, give the next hint level instead.

4. **One thing done well** (specific, not generic praise).

5. **Log** to `progress.md` → Portfolio log if it's a capstone (date, artifact, rubric avg). Otherwise nothing to log.

## Style
Direct, specific, terse. Never "consider improving X" — say what fails and when.
