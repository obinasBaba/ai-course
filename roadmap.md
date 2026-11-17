# Roadmap

40 weeks, 3 phases, ~7–10 h/week (1–2 h/day). Week 1 = Mon 2026-11-09. Week 0 (Nov 4–8) = setup.
Rule: **reschedule, never skip.** Buffer weeks absorb overruns first; stretch goals go second; milestones move last (and `/aie-weekly` says which).

## Phases

| Phase | Weeks | Dates | Focus | Exit criteria |
|---|---|---|---|---|
| 1 — Foundations & evals | 0–10 | 2026-11-04 → 2027-01-17 | toolchain, LLM basics, structured output, hybrid search, evals I+II, capstone C1 | C1 public with nDCG + judge TPR/TNR numbers; write-up #1 |
| 2 — Building systems + AI-103 | 11–22 | 2027-01-18 → 2027-04-11 | RAG & ingestion, extraction (C2), tools/MCP, agents; AI-103 domains paired | C2 public; agent lab passing; AI-103 practice ≥80% twice; exam weeks 20–22 if Azure access works |
| 3 — Production, security, career | 23–40 | 2027-04-12 → 2027-08-15 | shipping (FastAPI, CI eval gate, tracing, Next.js UI), security & guardrails, capstone C3, system design | C3 deployed demo + write-up #3; 3 design drills ≥4/5 |

## Week plan

| Week | Dates | Plan |
|---|---|---|
| 0–1 | Nov 4 – Nov 15 | **M00** orientation, toolchain, Python for TS devs, baselines |
| 2 | Nov 16 – 22 | **M01** LLMs as a component + structured output |
| 3–4 | Nov 23 – Dec 6 | **M02** embeddings & hybrid search · 🎯 public README with first numbers by end of week 3 |
| 5 | Dec 7 – 13 | **M03** evals I (part 1) |
| 6 | Dec 14 – 20 | 🧯 buffer |
| 7 | Dec 21 – 27 | **M03** (part 2) |
| 8 | Dec 28 – Jan 3 | **M04** evals II — LLM-as-judge |
| 9 | Jan 4 – 10 | **C1** capstone search + evals · 🎯 write-up #1 |
| 10 | Jan 11 – 17 | 🧯 buffer (Ethiopian Christmas Jan 7 falls in week 9 — use this if needed) |
| 11–12 | Jan 18 – 31 | **M05** RAG & ingestion · AI-103 A2 (GenAI apps) starts |
| 13–14 | Feb 1 – 14 | **M06** extraction & multimodal · A3 info extraction, A4 vision |
| 15 | Feb 15 – 21 | **C2** extraction capstone · 🎯 write-up #2 |
| 16 | Feb 22 – 28 | **M07** tools & MCP |
| 17–18 | Mar 1 – 14 | **M08** agents, memory, Microsoft Agent Framework · A2 agents |
| 19 | Mar 15 – 21 | A5 text & speech · A1 plan & manage Foundry |
| 20–21 | Mar 22 – Apr 4 | A6 readiness: practice assessments, weak spots, exam sandbox |
| 22 | Apr 5 – 11 | 🎓 **AI-103 exam** (gate: practice ≥80% twice; Azure labs done or consciously skipped) |
| 23–26 | Apr 12 – May 9 | **M09** shipping: FastAPI streaming, container, CI eval gate, tracing, Next.js UI |
| 27–29 | May 10 – 30 | **M10** AI security & guardrails |
| 30–33 | May 31 – Jun 27 | **C3** agent capstone, deployed · 🎯 write-up #3 |
| 34–40 | Jun 28 – Aug 15 | **M11** system design & career (ongoing) · optional M12 LoRA · spikes S1/S2 |

## Current week plan
_Updated by `/aie-weekly`._
- Week 0: finish M00 (toolchain + Python ramp + baselines).

## Weekly rhythm
- Mon–Thu: core module, 1–1.5 h.
- Fri–Sat: lab or AI-103, 1.5–2 h.
- Daily: 10 min Anki (`AIE::` decks).
- Sun: `/aie-weekly` (15 min), otherwise rest.
- **Minimum viable day** (bad day): 20 min = Anki + one lab step or one Learn unit. Counts as a session.

## Milestones
| # | Milestone | Target week | Done |
|---|---|---|---|
| 1 | M00 done, toolchain green, baselines logged | 1 | ⬜ |
| 2 | Public `labs/` README with first measured numbers | 3 | ⬜ |
| 3 | C1 published + write-up #1 | 9 | ⬜ |
| 4 | C2 published + write-up #2 | 15 | ⬜ |
| 5 | AI-103 passed | 22 | ⬜ |
| 6 | Deployed demo with CI eval gate | 26 | ⬜ |
| 7 | C3 published + write-up #3 | 33 | ⬜ |
| 8 | 3 design drills scored ≥4/5 | 40 | ⬜ |

## Budget & purchases
| Item | When | Cost | Required? |
|---|---|---|---|
| Chip Huyen, *AI Engineering* (O'Reilly, 2024; ISBN 9781098166304) — ebook or print | before M01 (week 2) | one-off book price | **Yes** |
| AI-103 exam (Pearson VUE) | week 20–22, after practice ≥80% | up to $165 US list; check your country's price; watch for vouchers | **Yes** (for cert) |
| Azure pay-as-you-go usage | once signup works (cert labs) | ~$10–40 total (estimate; free tiers + delete after labs) | For cert labs |
| Hosted LLM API credit (OpenAI or Anthropic) | M04 judge comparison | ~$10–20 | Optional |
| Alammar & Grootendorst, *Hands-On Large Language Models* | M01 if you want visual intuition | book price | Optional |
| Shankar & Husain, *Evals for AI Engineers* | when complete (after C1) | book price | Optional |
| Everything else (guide, Learn, Anthropic Academy, HF, Microsoft beginner courses, Ollama, GitHub, Anki desktop) | — | free | — |
Not needed: O'Reilly subscription, Maven/Udemy courses, paid practice-test bundles.

## Blockers
- **Azure subscription signup fails** (card/risk check; correlation IDs in `cert/ai-103.md`). Non-blocking for the core course (local models). Cert labs wait; theory proceeds.
