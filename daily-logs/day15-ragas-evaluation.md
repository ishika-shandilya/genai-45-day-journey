# Day 15 — RAGAS Evaluation (July 8, 2026)

## ✅ What I did today
- Read about RAGAS evaluation framework
- Understood the 4 core metrics:
  - Faithfulness (0-1) — hallucination control
  - Context Precision (0-1) — retrieval quality
  - Context Recall (0-1) — information coverage
  - Answer Relevance (0-1) — response quality
- Planned RAGAS integration for RBI Policy Analyser

## 💡 Key insight
RAGAS = R² and RMSE for RAG systems.
"Looks good" is never acceptable in Economics research.
Same discipline applies to AI evaluation.
Numbers don't lie — scores between 0 and 1 
tell the real story of RAG quality.

## 😕 What I want to implement tomorrow
- pip install ragas
- Create evaluation dataset with questions + ground truth
- Run RAGAS on RBI Policy Analyser
- Get actual faithfulness and precision scores
