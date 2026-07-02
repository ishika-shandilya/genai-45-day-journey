# Day 9 — RAG Architecture Deep Dive (July 1, 2026)

## ✅ Topics covered
- What RAG is and why it exists
- RAG pipeline: Load → Chunk → Embed → Store → Retrieve → Generate
- Document loaders — PyPDFLoader, TextLoader
- Why LLMs hallucinate without grounding
- How RAG controls hallucination through context injection
- ChromaDB as vector store for retrieved chunks

## 💡 Key insight
RAG = specification correction for LLMs.
Same as using verified data sources in econometrics
instead of estimated figures.
Grounded answers only — no hallucination.

## 😕 Confusion → clarity
Hallucination control felt vague at first.
Clarity: LLM only answers from retrieved context.
If answer isn't in the document — it says so.
RAG disciplines the LLM like data disciplines a model.
