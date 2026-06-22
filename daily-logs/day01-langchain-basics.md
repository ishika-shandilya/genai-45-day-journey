# Day 1 — LangChain Basics (June 22, 2026)

## ✅ What I covered today
- LangChain library setup — langchain, langchain-openai, langchain-groq, langchain-google-genai
- ChatPromptTemplate — from_template, from_messages
- System messages, Human messages, AI messages
- LLM invocation — Groq (llama), Gemini, OpenAI
- StrOutputParser — parsing LLM output to clean string
- Chains using | pipe operator
- Runnables — RunnableLambda, RunnablePassthrough, RunnableSequence, RunnableParallel

## 💡 Key insight
The | pipe operator chains components like an assembly line.
prompt | llm | parser = clean, readable pipeline

## 😕 What was confusing
- RunnableParallel output structure (nested dict)

## 🎯 Tomorrow — Day 2
- RAG pipeline fundamentals
- Document loading, chunking, embedding, retrieval

## 📁 Files
- Revised LangChain basics notebook
