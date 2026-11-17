---
name: aie-cert
description: AI-103 (Azure AI Apps and Agents Developer Associate) study session — pick a domain, map it to the user's core-module knowledge and Microsoft Learn modules, drill Azure-specific details Socratically, log weak spots and practice scores.
---

# aie-cert

Bridge general AI-engineering knowledge to Azure specifics for AI-103.

## Procedure

1. **Load** `cert/ai-103.md`. Show the domain table with weights, readiness, and the Azure-access status in one compact block.

2. **Pick domain.** Default = highest `weight × (1 − readiness)` among domains whose paired core module is done (see table). Confirm.

3. **Verify currency.** WebFetch the AI-103 study guide skills list for that domain (learn.microsoft.com) — service names change (Azure AI Studio → Foundry). Note any change in `cert/ai-103.md`.

4. **Bridge first.** Ask the user to explain the general concept from their core module (e.g. "how does hybrid search work?"), then map it to the Azure service ("in Azure AI Search, what implements that?"). Predict → check docs → explain the gap.

5. **Learn module.** Point to the exact Microsoft Learn module/unit for the domain; user reads/does exercises (labs only if Azure access works — else note "lab pending access").

6. **Drill.** 5 scenario questions (service choice, SDK/API, configuration, responsible AI/content safety, cost/limits). Score 1–5.

7. **Log** in `cert/ai-103.md`: domain readiness (0–100%), weak-spot entries (topic → doc link), Learn modules completed. Practice-assessment attempts → Practice history table (date, overall %, per-domain %).

8. **Exam gate reminder** (only when readiness ≥80% overall): exam booked only when practice ≥80% twice in a row AND Azure labs done or consciously skipped.

## Rules
- Personal Microsoft account only for Learn/exam.
- Never use exam dumps; flag any source that looks like one.
