# Day 19 — First Real RAGAS Scores (July 23, 2026)

## ✅ What I focused on today
- Fixed the rate-limit crash from yesterday: combined 4 
  separate judge API calls into 1 per question, added 
  retry-with-backoff on 429 errors
- Successfully ran run_ragas_eval.py end-to-end on 
  rbi_circular.pdf for all 6 questions
- Got real scores for the first time

## 📊 Results
| Metric | Score |
|---|---|
| Faithfulness | 0.32 |
| Answer Relevancy | 0.52 |
| Context Precision | 0.44 |
| Context Recall | 0.92 |

## 💡 Key insight
Retrieval is doing its job (0.92 recall — the right chunks 
are being found almost every time) but generation is where 
things break down (low faithfulness + relevancy). This 
narrows the problem significantly: it's not "fix the RAG 
pipeline," it's "fix how the model uses what it's given."

Hypothesis: my prompt explicitly asks for "economic 
implications" and "impact on India's economy" beyond the 
retrieved text — which likely invites the model to reason 
outside the document, hurting faithfulness by design.

## 🎯 Tomorrow — Day 20
- Read per-question reasons in eval_results.csv to confirm 
  the hypothesis
- Try tightening the prompt to stay grounded in context
- Re-run eval and compare faithfulness score before/after

## 📁 Files
- run_ragas_eval.py (fixed — rate limit handling, combined calls)
- eval_results.csv (new — first real output)
