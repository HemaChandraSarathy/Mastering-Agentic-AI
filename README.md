# Mastering Agentic AI

### [MoveIt](./moveit)
A Streamlit + LangChain fitness accountability app with AI-powered companions.
Users pick a personality (Simon Sinek, Gordon Ramsay, Golden Retriever, etc.) or
create a custom one, then get personalised motivation throughout their day.

- **Stack:** Streamlit · LangChain · ChatAnthropic (Claude)
- **Run it:** `pip install -r requirements.txt`, add your `ANTHROPIC_API_KEY` to
  `.streamlit/secrets.toml`, then `streamlit run app.py`
- See [`moveit/README.md`](./moveit/README.md) for details.

### [Financial Document Intelligence (RAG)](./financial-doc-rag)
A two-pipeline RAG system that turns a portfolio company's document folder into a cited,
analyst-confirmed insights one-pager. **Numbers are extracted deterministically** (Excel cells,
text-PDF tables, and image-PDF OCR via LiteParse) — never from a vector search — then validated and
reconciled; **narrative is answered by RAG** (hybrid retrieval + rerank over Supabase pgvector) with a
refusal path. Includes two golden eval sets (retrieval quality + extraction accuracy).

- **Stack:** LangChain + LangGraph · Supabase pgvector · Nebius (embeddings) · Anthropic `claude-sonnet-4-6` ·
  pdfplumber / pandas / LiteParse OCR (extraction) · Streamlit (UI)
- **Run it:** `pip install -r requirements.txt`, copy `.env.example` → `.env` and fill keys, then
  `streamlit run app.py`
- See [`financial-doc-rag/README.md`](./financial-doc-rag/README.md) for details.

### [Unburden](./smart-receipt-assistant)
An agentic household mental-inbox assistant that captures bills, promos, invites, repairs, returns,
and other tasks living in your head. An LLM agent extracts the details, assigns ownership
(Mom / Dad / Either), schedules tasks on Google Calendar, and follows up so nothing slips.
Includes human-in-the-loop approvals, Gmail fallback for promo and coupon questions,
LangSmith-traced agent runs, and golden examples for evaluation.

- **Stack:** TanStack Start (React 19) · LangGraph · Lovable Cloud · Gemini 2.5 Flash ·
  Google Calendar + Gmail APIs · Tailwind CSS + shadcn/ui
- **Run it:** `bun install`, then `bun dev`
- See [`smart-receipt-assistant/README.md`](./smart-receipt-assistant/README.md) for details.

