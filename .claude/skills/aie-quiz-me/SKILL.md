---
name: aie-quiz-me
description: Active-recall quiz for the AI-engineering course. Modes — recall (default; completed modules), design (AI system-design interview drill with rubric), cert (AI-103 domain drill). Open-ended questions, scored, logged.
---

# aie-quiz-me

Pure active recall. No teaching mid-quiz.

## Modes (first arg; default `recall`)

### recall [module|all]
1. Target: given module, or most recently completed. Load its `modules/NN-*.md`.
2. 8–10 open questions, mix: 3 recall (definitions, when-to-use) · 2 trade-offs ("hybrid vs pure vector — when does hybrid lose?") · 2 predict-the-metric ("if we double chunk size, what happens to recall@10 and why?") · 2 failure modes · 1 explain-to-PM.

### design [prompt]
1. Prompt given, or pick one fitting completed modules (e.g. "Design semantic search over 50k supplier profiles with filters", "Design an extraction pipeline for scanned invoices", "Design an agent that books travel with human approval").
2. User drives; you play interviewer: ask clarifying questions only when asked, push on weak spots.
3. Score rubric 1–5: requirements & constraints · architecture · data & ingestion · **evals** · cost/latency · safety & failure modes · iteration plan. One line of evidence each.

### cert [domain]
1. Load `cert/ai-103.md`. Target: given domain, else the weakest by weighted readiness.
2. 8–10 scenario questions in exam style ("You need X with constraint Y — which service/SDK/config?") — open-ended, user names the choice and why.
3. Verify answers against current Microsoft Learn docs before scoring when unsure.

## Run (all modes)
- One question at a time. Score 1–5 after each with one phrase naming the specific gap.
- Reveal the model answer only if score ≤2.
- Hint on request = minimum nudge.

## Wrap & log
```
Score: X/Y · Strongest: … · Weakest: … · Re-read: <module §> or <doc link>
```
Append to `progress.md` → Quiz history: `date | mode | target | score | weakest | action`.
In `cert` mode also update the domain's readiness in `cert/ai-103.md` (weakest topics → weak-spot log).
≤50% → recommend re-reading before moving on.
