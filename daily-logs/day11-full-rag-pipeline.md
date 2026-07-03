# Day 11 — Full RAG Pipeline End-to-End (July 3, 2026)

## ✅ Topics covered
- PyPDFLoader — loading PDF documents
- RecursiveCharacterTextSplitter — chunking with overlap
- OpenAIEmbeddings — converting chunks to vectors
- ChromaDB — storing and searching embeddings
- RetrievalQA chain — connecting retriever to LLM
- k parameter — how many chunks to retrieve
- Full pipeline: PDF → chunks → embed → store → retrieve → answer

## 💡 Key insight
k parameter controls retrieval quality.
Too few chunks = incomplete answers
Too many chunks = noise confusion for LLM
k=3 is the sweet spot for most documents.

## 😕 Confusion → clarity
Assumed more chunks = better answers.
Wrong. Too many chunks = multicollinearity for LLMs.
Same problem as adding too many variables in
gravity model regression — signal drowns in noise.
