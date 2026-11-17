# START HERE

Private course workspace for mastering AI engineering. Mentor = Claude Code in **mentor mode** (`.claude/CLAUDE.md`). You build; the mentor scaffolds, coaches, reviews, and keeps the course alive.

## First session (M00)
```bash
cd ~/learning/ai-engineering-course
claude
```
Approve the `anki` MCP server when prompted (Anki desktop must be open with AnkiConnect). Then type:
```
/aie-start-module
```
It opens **M00 — Orientation, toolchain, Python for TS devs**. In M00 you will (yourself):
1. Turn `labs/` into a uv project + git repo and open it in PyCharm (uv interpreter).
2. Pull the remaining model: `ollama pull gpt-oss:20b` (if not already listed by `ollama list`).
3. Start Postgres + pgvector in Docker.
4. Write `labs/common/llm.py` — your provider-agnostic client that logs every call.
5. Take the AI-103 practice assessment cold (baseline) and self-rate each curriculum area.
6. Create your public GitHub repo for `labs/` and push.

## Every session after
| When | Command |
|---|---|
| Start of any session | `/aie-start-module` |
| Building | `/aie-lab` |
| Code feedback | `/aie-review` |
| Stopping mid-module | `/aie-checkpoint` |
| Module finished | `/aie-end-module` |
| Practice recall / design / cert | `/aie-quiz-me recall` · `design` · `cert` |
| AI-103 study | `/aie-cert` |
| Sunday | `/aie-weekly` |

Bad day? Do the **minimum viable day**: 10 min Anki + one lab step. It counts.

## Map
`roadmap.md` (calendar, budget) · `curriculum.md` (modules) · `resources.md` (what to read/buy) · `progress.md` (where you are) · `cert/ai-103.md` · `glossary.md` · `modules/` (your notes) · `labs/` (your public portfolio) · `references/ai-system-design-guide/` (local copy of the free guide).
