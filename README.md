# AI Interview Prep Assistant (LangChain RAG)

A lightweight Retrieval-Augmented Generation (RAG) app that helps you prepare grounded, professional interview answers using **your resume + job description + company notes**.

**What this notebook demonstrates:**
- Document ingestion (PDF + TXT)
- Chunking + embeddings
- FAISS vector search
- Context-grounded answers with source attribution
- Clean, production-style code structure
- Gradio for evaluation  interactive UI

**How it works:**
1. Load documents from `/data`
  a. FIRST: Create a /data directory and upload your 3 - TXT files - Resume, Job Description, Company notes your interviewing
2. Using an OPENAI_API_KEY of your choice
3. Split → embed → store in FAISS
4. Retrieve relevant chunks
5. LLM answers using **only** the retrieved context (no hallucinations)
6. Gradio UI to display LLM-as-Judge results


This includes an LLM-as-Judge evaluator with clear scores and explanation on 3 key areas: Groundedness, Relevance, and Professionalism. 
![EvalLLMJudge](EvalLLLasJudge.png)
