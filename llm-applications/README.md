# LLM Applications & Agent Foundations

**Programs:** Generative AI for NLP (2024) · Gen AI for Practitioners (2025)  
**Topics:** Prompt engineering, LLM classification, agent architecture, tool use, reasoning loops

---

## M6_Introduction_to_Agents.ipynb

**Agent Architecture Fundamentals**

Covers the core building blocks of LLM-powered agents — how agents perceive inputs, select tools, reason about actions, and execute in loops. Foundational module from the 2025 program that precedes multi-agent system design.

**Concepts covered:**
- Tool definition and binding to LLMs
- ReAct (Reasoning + Acting) pattern
- Agent executor loops and stopping conditions
- Memory and state across agent turns

**Stack:** LangChain · OpenAI · Python

---

## llm_finetuning_lora_aspect_sentiment.ipynb

**LLM Fine-Tuning with LoRA — Aspect-Based Sentiment Analysis**

Fine-tunes a Llama model for aspect-based sentiment analysis on customer reviews using LoRA (Low-Rank Adaptation) via the Unsloth library and PEFT. Specifically targets the Query, Key, and Value projection matrices (`q_proj`, `k_proj`, `v_proj`) in the transformer attention layers — the most parameter-efficient approach to adapting large language models for downstream tasks.

**Key implementation details:**
- LoRA rank `r=16`, `lora_alpha=16` applied to attention KQV + FFN projection layers
- Quantized model loading with `bitsandbytes` for memory-efficient fine-tuning on consumer GPU
- Gradient checkpointing enabled for large sequence lengths
- Fine-tuned adapter saved as `dialogue-summarizer-llama` and persisted to Drive

**Stack:** Unsloth · PEFT · TRL · bitsandbytes · Hugging Face Transformers · Python

---

## customer_support_llm_classification.ipynb

**LLM-Based Customer Support Ticket Classification**

Applies large language models to classify customer support tickets by intent and sentiment. Demonstrates practical NLP for enterprise automation using zero-shot and few-shot prompting strategies.

**Stack:** Hugging Face Transformers · OpenAI · LangChain · Python

> **Note:** API tokens used during development have been redacted. Replace `YOUR_HF_TOKEN_HERE` with your own Hugging Face token to run.
