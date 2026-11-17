# Decisions

Date, decision, why. Newest at the bottom.

---

**2026-11-17 — Local first, one interface for all models.**
Every model call goes through `llm.py`; provider and model names live in `.env`.
Why: near-zero budget means local Ollama models today, but swapping to an API model later
must be a config change, not a rewrite.

**2026-11-17 — Extraction model is provisional (`qwen3:4b`).**
Why: 4B fits comfortably in 16 GB RAM alongside Postgres; strong at structured JSON output.
The final pick will be decided by the extraction eval, not by popularity.
