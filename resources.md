# Resources

Vetted 2026-11-04. Status: ✅ verified (opened/searched) · 🔎 verify link on first use. AI moves fast — the mentor re-checks version-sensitive docs before teaching.

## Core (use these)
| Resource | Cost | Use for | Status |
|---|---|---|---|
| **Evals study guide** — `references/ai-system-design-guide/ai_evals_comprehensive_study_guide.md` ([GitHub](https://github.com/ombharatiya/ai-system-design-guide/blob/main/ai_evals_comprehensive_study_guide.md)). Unofficial distillation of Hamel Husain & Shreya Shankar's evals course; cross-check key claims with [hamel.dev](https://hamel.dev) | free | M03, M04, M05, M09 | ✅ |
| **AI System Design Guide library** — `references/ai-system-design-guide/` (numbered folders, ~130 articles, MIT). Partly AI-maintained → verify claims that matter | free | every module | ✅ |
| **Chip Huyen, *AI Engineering*** (O'Reilly, Dec 2024, ISBN 9781098166304). The field map; read selectively | buy once | M01, M05, M09, M12 | ✅ |
| **AI-103** [study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-103) · [certification page + free practice assessment](https://learn.microsoft.com/en-us/credentials/certifications/azure-ai-apps-and-agents-developer-associate/) | free (exam paid) | A0–A6 | ✅ |
| Anthropic — [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents) | free | M08 | 🔎 |
| Anthropic — [Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) | free | M01, M08 | 🔎 |
| OWASP GenAI — [Top 10 for LLM Applications 2026](https://genai.owasp.org/) + [Top 10 for Agentic Applications](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026) | free | M10 | ✅ |
| [Model Context Protocol docs](https://modelcontextprotocol.io) | free | M07 | 🔎 |

## Free courses (pick per module, not all)
| Course | Use for | Notes | Status |
|---|---|---|---|
| [Anthropic Academy](https://anthropic.skilljar.com) — "Building with the Claude API", "Introduction to Model Context Protocol" | M01, M07 | free, completion certificates | ✅ |
| [Hugging Face Agents Course](https://huggingface.co/learn/agents-course) | M08 | free certificate, ~20–30h — do selected units | 🔎 |
| [Microsoft AI Agents for Beginners](https://github.com/microsoft/ai-agents-for-beginners) (18 lessons, Agent Framework + Foundry) | M08, A2 | doubles as AI-103 prep | ✅ |
| [Microsoft Generative AI for Beginners](https://microsoft.github.io/generative-ai-for-beginners/) (21 lessons) | skim gaps | beginner-level; skip what you know | ✅ |
| DeepLearning.AI "MCP: Build Rich-Context AI Apps with Anthropic" | M07 | ~90 min, optional | 🔎 |

## Microsoft Learn paths (AI-103)
- [Get started with AI applications and agents on Azure](https://learn.microsoft.com/en-us/training/paths/get-started-ai-apps-agents/) — A0 ✅
- [Plan and Prepare to Develop AI Solutions on Azure](https://learn.microsoft.com/en-us/training/modules/prepare-azure-ai-development/) — A0/A1 ✅
- [Develop generative AI apps on Microsoft Foundry](https://learn.microsoft.com/en-us/training/paths/develop-generative-ai-apps/) — A2 ✅
- [Develop AI Agents on Azure](https://learn.microsoft.com/en-us/training/paths/develop-ai-agents-azure/) — A2 ✅
- [Develop computer vision solutions with Microsoft Foundry](https://learn.microsoft.com/en-us/training/paths/develop-computer-vision-with-foundry/) — A4 ✅
- [Azure AI Search training modules](https://learn.microsoft.com/en-us/azure/search/resource-training) — A3 ✅
- Text analysis & speech, Content Understanding — find via the study guide's links — A3/A5 🔎

## Tooling docs
[uv](https://docs.astral.sh/uv/) · [pydantic](https://docs.pydantic.dev) · [pytest](https://docs.pytest.org) · [Ollama OpenAI compatibility](https://github.com/ollama/ollama/blob/main/docs/openai.md) · [pgvector](https://github.com/pgvector/pgvector) · [ranx](https://github.com/AmenRa/ranx) · [BEIR](https://github.com/beir-cellar/beir) (SciFact) · [judgy](https://github.com/ai-evals-course/judgy) · [FastAPI](https://fastapi.tiangolo.com) · [OpenTelemetry GenAI semantic conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) · [Microsoft Agent Framework](https://learn.microsoft.com/en-us/agent-framework/) 🔎 · [mlx-lm](https://github.com/ml-explore/mlx-lm) (LoRA guide) 🔎

## Optional books
- Jay Alammar & Maarten Grootendorst, *Hands-On Large Language Models* (O'Reilly, 2024) — visual intuition, low math. M01.
- Shreya Shankar & Hamel Husain, [*Evals for AI Engineers*](https://www.oreilly.com/library/view/evals-for-ai/9798341660717/) (O'Reilly, Oct 2026; early release, ch. 6–10 not final as of 2026-11) — after C1, when complete.
- Valliappa Lakshmanan & Hannes Hapke, *Generative AI Design Patterns* (2025) — M11.

## Reading map (where each module pulls from)
| Module | Core | Optional |
|---|---|---|
| M00 | uv, pydantic, pytest, Ollama OpenAI-compat docs | — |
| M01 | Huyen ch. 1–2; guide `01-foundations/02,06`, `05-prompting-and-context/06` | Hands-On LLMs; Anthropic Academy API course |
| M02 | guide `01-foundations/05`, `06-retrieval-systems/03,04,05`; pgvector README | `16-case-studies/06-real-time-search.md` |
| M03 | evals guide ch. 1, 3, 6; `06-retrieval-systems/13` | — |
| M04 | evals guide ch. 4, 10, 11, 12 | hosted judge comparison |
| M05 | Huyen ch. 6; `06-retrieval-systems/01,02,06,10,14`; evals guide ch. 8 | `06-retrieval-systems/07,08,09` |
| M06 | `10-document-processing/01`; `16-case-studies/10` | — |
| M07 | `07-agentic-systems/03`; MCP docs; Anthropic Academy MCP | DeepLearning.AI MCP |
| M08 | Anthropic agents + context-engineering posts; `07-agentic-systems/01,02,07,08,10,11`; `08-memory-and-state/*` | HF Agents Course; MS AI Agents for Beginners |
| M09 | evals guide ch. 2, 13; `11-infrastructure-and-mlops/02,03,04`; `14-evaluation-and-observability/02`; Huyen ch. 9–10 | `16-case-studies/18-eval-gated-cicd.md` |
| M10 | `05-prompting-and-context/08`; `12-security-and-access/*`; `13-reliability-and-safety/01`; OWASP lists | `07-agentic-systems/09` |
| M11 | `00-interview-prep/*`; `15-ai-design-patterns/*`; `16-case-studies/*` | Generative AI Design Patterns |
| M12 | Huyen ch. 7–8; `03-training-and-adaptation/02,03,05,06`; mlx-lm LoRA guide | — |

## Skip
Framework deep-dive courses (LangChain/LlamaIndex-specific), math-heavy "from scratch" material (unless curious), exam dumps (never), paid bundles that duplicate the above.
