# Day 10 — Chunking Strategies + Retrieval (July 2, 2026)

## ✅ Topics covered
- Why documents need to be chunked before embedding
- CharacterTextSplitter — fixed character splitting
- RecursiveCharacterTextSplitter — smart hierarchical splitting
- chunk_size and chunk_overlap parameters
- Why overlap prevents information loss at boundaries
- Building retrieval chain with ChromaDB

## 💡 Key insight
Chunk overlap = rolling window in time series analysis.
Boundary information preserved intentionally.
RecursiveCharacterTextSplitter always preferred
for real documents — preserves semantic meaning.

## 😕 Confusion → clarity
Why overlap exists felt redundant at first.
Clarity: sentences at chunk boundaries would be
split and lost without overlap. Rolling window
analogy from econometrics made it click instantly
