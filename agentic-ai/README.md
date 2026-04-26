# Agentic AI Systems

**Program:** Gen AI for Practitioners — Enterprise LLM Solutions (12-Week, 2025)  
**Topics:** Multi-agent frameworks, LangGraph, tool orchestration, autonomous workflow design

---

## Final_Project_GenAI_Agentic_RAG.ipynb

**Multi-Agent RAG Collaborative System for Competitor Analysis**

Automates end-to-end competitor analysis using a sequential multi-agent workflow built with LangGraph. The system breaks a complex research task into discrete steps handled by three specialized agents, each with its own tools and responsibilities.

**Agents:**
- **Question Generator Agent** — Validates the target company, identifies its industry sector, and generates structured analysis questions
- **Data Retrieval & Storage Agent** — Fetches answers from the web via Tavily search API and stores question-answer pairs in ChromaDB
- **Report Drafter Agent** — Queries the vector store via RAG and generates a structured competitive analysis report with sections for Executive Summary, Company Overview, Key Competitors, and Strategic Recommendations

**Architecture:**  
LangGraph `StateGraph` with sequential edges: `START → Question Generation → Data Retrieval/Storage → Report Drafting → END`

**State management:** Pydantic-based `CompetitiveAnalysisState` tracks company name, generated questions, search results, vectorstore status, and final report across agent transitions.

**Stack:** LangGraph · LangChain · ChromaDB · OpenAI GPT-4 · Tavily Search API · Pydantic

---

## Single_Agent_Systems.ipynb

**Single Agent Design Patterns**

Covers the foundational building blocks of agentic AI before composing multi-agent systems — tool definition, reasoning loops, LLM-driven decision making, and action execution. Serves as the conceptual foundation for the multi-agent final project above.

**Stack:** LangChain · OpenAI · Python
