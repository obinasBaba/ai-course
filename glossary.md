# Glossary

Terms with a source (doc, guide path, or own measurement). Appended alphabetically by `/aie-end-module`. Seeded with terms already met in real work (2026-10).

### ANN (approximate nearest neighbour)
Vector search that skips comparing against every row (HNSW, IVFFlat) — trades a little recall for speed. Only needed at scale: exact KNN over 2.4k × 1536-dim vectors measured 13 ms (own measurement, 2026-10-29).
- Source: pgvector README; guide `06-retrieval-systems/04-vector-databases.md`.

### Cosine similarity / cosine distance
Angle-based similarity between two vectors: 1 = same direction, ~0 = unrelated. pgvector's `<=>` returns cosine **distance** = 1 − similarity. OpenAI embeddings are unit-length, so cosine = dot product.
- Source: pgvector README; guide `01-foundations/05-embeddings-and-vector-spaces.md`.

### Embedding
A fixed-length list of numbers representing the meaning of a text; similar meanings land near each other. Query and documents MUST use the same model. ada-002 = 1536 dims; `nomic-embed-text` = 768 dims.
- Source: guide `01-foundations/05`; Azure OpenAI embeddings docs.

### Error analysis (open / axial coding)
Read real outputs, write free-form notes on what's wrong (open coding), then group notes into failure categories (axial coding) and count them to prioritise.
- Source: evals guide ch. 3.

### Golden set
A fixed set of inputs with trusted expected outputs/labels used to measure a system and compare versions.
- Source: evals guide ch. 4, 6.

### HNSW / IVFFlat
pgvector ANN index types. HNSW: graph-based, better recall/speed, slower build. IVFFlat: clustered lists; `lists = 1` ≈ exact scan.
- Source: pgvector README.

### Hybrid search
Combining lexical (keyword/full-text) and vector (meaning) retrieval, then fusing the ranked lists. Lexical catches exact names/codes/typos (with trigram); vector catches paraphrase.
- Source: guide `06-retrieval-systems/05-hybrid-search.md`.

### LLM-as-judge
Using an LLM to label outputs (e.g. pass/fail). Must be validated against human labels (TPR/TNR on a held-out test split) before its numbers are trusted.
- Source: evals guide ch. 4.

### MCP (Model Context Protocol)
Open protocol for exposing tools, resources and prompts to LLM applications via servers and clients.
- Source: modelcontextprotocol.io.

### nDCG@k
Normalised Discounted Cumulative Gain: rewards relevant results more the higher they rank; normalised to 0–1 against the ideal ranking. Works with graded or binary relevance.
- Source: ranx docs; evals guide ch. 6 (related: Recall@K, MRR).

### pgvector
Postgres extension adding a `vector(n)` type, distance operators (`<=>` cosine, `<->` L2, `<#>` negative inner product) and ANN indexes.
- Source: pgvector README.

### RRF (Reciprocal Rank Fusion)
Merge ranked lists by summing `1 / (k + rank)` per item (k≈60). Uses ranks, not raw scores — robust when scores aren't comparable (ada-002 cosine scores sat in a 0.76–0.85 band for relevant and junk alike, own measurement 2026-10-29).
- Source: Cormack et al. 2009 (original RRF paper); guide `06-retrieval-systems/05-hybrid-search.md`.

### TPR / TNR
True positive rate (of real passes, how many the judge calls pass) and true negative rate (of real fails, how many it calls fail). Better than raw agreement when failures are rare.
- Source: evals guide ch. 4.

### TTFT
Time to first token — the latency a user feels before streaming starts; distinct from throughput (tokens/sec).
- Source: guide `01-foundations/06-inference-pipeline.md`.
