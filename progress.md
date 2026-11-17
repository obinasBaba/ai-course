# Progress

Updated by the `aie-*` skills. Self-assessment: 1 = lost · 3 = can build it with notes · 5 = could teach it and defend the trade-offs in an interview.
Review intervals after completion: +1w → +3w → +2m → +4m (warm-ups in `/aie-start-module`).

## Modules
| # | Module | Status | Started | Completed | Self (1-5) | Hours | Next review | Notes |
|---|---|---|---|---|---|---|---|---|
| M00 | Orientation, toolchain, Python for TS devs | 🔄 | 2026-11-05 | — | — | — | — | |
| M01 | LLMs as a component + structured output | ⬜ | — | — | — | — | — | |
| M02 | Embeddings & hybrid search | ⬜ | — | — | — | — | — | Prior exposure: GTCOne PR1 (2026-10) |
| M03 | Evals I: retrieval metrics | ⬜ | — | — | — | — | — | |
| M04 | Evals II: LLM-as-judge | ⬜ | — | — | — | — | — | |
| C1 | Capstone: search + evals | ⬜ | — | — | — | — | — | |
| M05 | RAG & ingestion | ⬜ | — | — | — | — | — | |
| M06 | Extraction & multimodal | ⬜ | — | — | — | — | — | |
| C2 | Capstone: extraction | ⬜ | — | — | — | — | — | |
| M07 | Tools & MCP | ⬜ | — | — | — | — | — | |
| M08 | Agents, memory, frameworks | ⬜ | — | — | — | — | — | |
| M09 | Shipping | ⬜ | — | — | — | — | — | |
| M10 | Security & guardrails | ⬜ | — | — | — | — | — | |
| C3 | Capstone: agent, deployed | ⬜ | — | — | — | — | — | |
| M11 | System design & career | ⬜ | — | — | — | — | — | ongoing |
| M12 | LoRA (optional) | ⬜ | — | — | — | — | — | |

Status: ⬜ todo · 🔄 in progress · ✅ done · 🔁 needs revisit

## Checkpoint
_Overwritten by `/aie-checkpoint`; cleared by `/aie-end-module`._
- None yet.

## Session log
| Date | Module | Minutes | What moved |
|---|---|---|---|

## Lab metrics
Provenance is mandatory — a number without dataset/model/SHA/baseline doesn't count.
| Date | Lab | Metric | Value | Dataset | Model + quant | Params | Labs SHA | Baseline | Note |
|---|---|---|---|---|---|---|---|---|---|

## Quiz history
| Date | Mode | Target | Score | Weakest | Action |
|---|---|---|---|---|---|

## Weekly retros
| Week | Planned h | Actual h | Moved | Blocker | Next-week focus |
|---|---|---|---|---|---|

## Open questions
| Opened | Question | Status | Answer |
|---|---|---|---|

## Ideas backlog
Project ideas to fold into labs/capstones later (concepts only; no company code/data).
| Added | Idea | Fits module | Notes |
|---|---|---|---|
| 2026-11-04 | Relationship-aware search: a query matching a related record (destination, promotion, brand) returns linked entities, with "matched via" reasons | M05 / S1 | from GTCOne PR2 discussion; public-data version possible (e.g. Wikivoyage places ↔ listings) |
| 2026-11-04 | Place recognition (gazetteer + geo radius) for queries naming places that aren't records | S1 | GeoNames (CC-BY) |
| 2026-11-04 | Extraction confidence calibration study | M06 / C2 | |

## Portfolio log
| Date | Artifact | Link | Rubric avg | Note |
|---|---|---|---|---|

## Prior experience (context, not course credit)
- 2026-10 (work): supplier hybrid search — ada-002 embeddings, pgvector cosine, RRF fusion, category prefilter, 800 ms embedding budget + cache; measured exact KNN 13 ms / 2.4k rows; Azure embed warm call ~250 ms from laptop (~180 ms RTT). Basis for M02 concept link.
