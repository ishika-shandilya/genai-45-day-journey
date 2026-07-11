# Day 17 — RAGAS Implementation Attempt (July 11, 2026)

## ✅ What I focused on today
- Wrote eval_dataset.py — 6 Q&A pairs grounded in a mock 
  RBI circular, manually verified as ground truth
- Wrote run_ragas_eval.py using the ragas package, wrapped 
  Gemini via LangchainLLMWrapper
- Hit ModuleNotFoundError on ragas import — traced it to a 
  broken upstream dependency (ragas still imports ChatVertexAI 
  from a langchain-community path that's been removed)
- Confirmed via multiple open GitHub issues — not my config
- Tried pinning ragas<0.4, then langchain-community==0.3.27 — 
  each fix broke a different package
- Recreated venv from scratch — same conflict resurfaced
- Decision: dropped ragas package entirely, rebuilt all 4 
  metrics (faithfulness, answer relevancy, context precision, 
  context recall) manually as LLM-as-judge functions using 
  Gemini directly

## 💡 Key insight
Not every bug is a config issue.
When a well-known package has multiple open GitHub issues 
describing your exact error, the fix is routing around the 
dependency, not debugging harder against it.

## 🎯 Tomorrow — Day 18
- Run the custom eval script end-to-end
- Report real faithfulness/relevancy/precision/recall scores
- Fix any remaining errors in the ragas-free version

