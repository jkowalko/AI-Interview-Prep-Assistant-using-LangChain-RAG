# AI Interview Prep Assistant (LangChain RAG)

A lightweight Retrieval-Augmented Generation (RAG) app that helps you prepare grounded, professional interview answers using **your resume + job description + company notes**.

**What this notebook demonstrates:**
- Document ingestion (PDF + TXT)
- Chunking + embeddings
- FAISS vector search
- Context-grounded answers with source attribution
- Clean, production-style code structure

**How it works:**
1. Load documents from `/data`
2. Split → embed → store in FAISS
3. Retrieve relevant chunks
4. LLM answers using **only** the retrieved context (no hallucinations)
