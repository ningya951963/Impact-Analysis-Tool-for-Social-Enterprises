# Impact Analysis Tool for Social Enterprises (NLP Final Project)

A Streamlit-based tool that helps reviewers **extract, summarize, and score** social enterprise business plans with a **rubric-driven (prompt-based) scoring system** and optional **RAG semantic search**.

> Team project repo: (link to Henry’s original repo)
> My portfolio repo focuses on: **what I built + how it works + business impact**.

---

## What this tool does
- Upload one or multiple business plan PDFs
- Extract key fields (mission, problem, description, etc.)
- Generate 3 impact scores with rationales:
  - Magnitude / Effectiveness / Efficiency
- Provide supplementary **external research snippets** to support reviewer context
- Enable Q&A via an “Analysis Agent” (RAG optional)

---

## My role (Ningya Yang) — Scoring & Research
I owned the scoring and evidence pipeline, including:
- Designed and implemented **rubric + prompt-based scoring** that returns structured JSON rationales
- Implemented **overall score calculation (0–10) with configurable weighting**
- Built **external research snippet collection** to provide supplementary citations
- Added guardrails to reduce hallucinations and enforce citation rules
- Iterated Streamlit UI to display scores + rationales clearly

---

## Technical highlights (evidence-based)
- Scoring is **prompt-based** (no fine-tuning) to keep evaluation transparent and consistent.
- Overall score = **0.4 * Magnitude + 0.4 * Effectiveness + 0.2 * Efficiency** (easy to adjust for different reviewers)  
- External research is treated as **supplementary only**; scoring is driven by business plan content.

---

## Demo screenshots
(put 3–6 key screenshots here)

---

## Tech stack
- Frontend: Streamlit
- Backend: Python
- LLM: OpenAI (structured JSON output)
- Vector store: PostgreSQL + pgvector (optional RAG search)

---

## Notes on code & data
This portfolio repo focuses on **problem framing, methodology, and product thinking**.  
The full implementation is available in the team repository (linked above).
