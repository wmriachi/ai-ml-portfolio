# Retrieval-Augmented Generation (RAG) Systems

**Program:** Generative AI for NLP — Transformers, LLMs, Semantic Search, Conversational AI (2024)  
**Topics:** RAG architecture, vector databases, document ingestion, embedding models, semantic search

---

## Power_BI_RAG_System.ipynb

**RAG System for Power BI Documentation**

Builds a production-ready RAG pipeline that enables analysts to query Power BI's official documentation using natural language. Designed to solve the real problem of analysts misinterpreting or missing features due to the breadth and complexity of technical documentation.

**Pipeline:**
1. **Document Ingestion** — Loads Power BI PDF documentation using `PyPDFDirectoryLoader`
2. **Chunking** — Splits documents using `RecursiveCharacterTextSplitter` with tiktoken encoder for token-aware chunking
3. **Embedding & Storage** — Generates OpenAI embeddings and stores document chunks in a persistent ChromaDB vector database
4. **Retrieval** — Semantic similarity search retrieves relevant chunks for a given user query
5. **Generation** — OpenAI GPT model synthesizes a grounded, context-aware answer from retrieved chunks

**Key design decisions:**
- Token-aware chunking (tiktoken) avoids context window violations
- Persistent ChromaDB avoids re-embedding on every session
- Batch processing handles large documentation sets without memory overflow

**Stack:** LangChain · ChromaDB · OpenAI Embeddings · GPT-4 · PyPDF · tiktoken · Python
