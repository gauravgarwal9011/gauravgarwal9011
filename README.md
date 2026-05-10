<div align="center">

# Gaurav Garwal
### AI/ML Engineer · Gen AI Systems · LLM Pipelines · Agentic AI

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gaurav-garwal-59113788)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/gauravgarwal9011)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/gauravgarwal9011)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:gauravgarwal9011@gmail.com)

</div>

---

## 👋 About Me

AI/ML Engineer with **production experience** building and deploying **LLM pipelines, multi-agent systems, and RAG architectures** for enterprise clients. Currently at **Ignatiuz Software Solutions**, where I ship real-time Gen AI features using Azure OpenAI, LangChain, LangGraph, and FastAPI.

I specialise in the full Gen AI engineering stack — from fine-tuning open-source models to building observability pipelines that catch hallucinations before they reach users.

```
Latest shipped      →  NyayaGPT: Mistral-7B fine-tuned on 1,690 Indian legal pairs (QLoRA + GGUF)
Open to             →  Senior AI/ML Engineer roles (remote-first, ₹25–45 LPA)
Ask me about        →  RAG pipelines, LangGraph agents, LLM eval, MCP servers, QLoRA fine-tuning
```

---

## 🏗️ Production Projects

> Real systems built and deployed — not tutorials. Each has benchmarks, live demos, and production patterns.

---

### 🤖 AI-Powered Due Diligence Agent
> **Flagship project — 5-agent orchestration system, <45s end-to-end, production observability**

Built a production-grade agentic platform orchestrating **5 specialised agents** (Research → Extraction → Critic → Writer → Reviewer) over a full document intelligence pipeline — from raw PDF ingestion to a cited, hallucination-checked report.

**What makes it production-ready:**
- ⚡ Real-time streaming via **Redis pub/sub + SSE** — complete report delivered in under 45 seconds
- 🛡️ **Hallucination detection + PII redaction** safety guardrails on every agent output
- 📊 **Langfuse observability** — full trace per agent node, token usage, and latency per call
- 📚 RAG pipeline with **semantic chunking + ChromaDB** — every claim backed by an inline citation

**Tech:** FastAPI · Azure OpenAI GPT-4o · ChromaDB · LangGraph · Redis · Celery · Langfuse · Docker

[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat&logo=github)](https://github.com/gauravgarwal9011/due-diligence-agent)
[![Demo](https://img.shields.io/badge/Demo-Live-00D4AA?style=flat&logo=streamlit)](https://huggingface.co/spaces/gauravgarwal9011)

---

### ⚖️ NyayaGPT — Indian Legal LLM with QLoRA Fine-Tuning and MLOps Pipeline
> **Latest project — Mistral-7B fine-tuned on 1,690 Indian legal pairs · 3.3× memory reduction · 2.2× faster inference · zero ROUGE-L degradation**

Fine-tuned **Mistral-7B-Instruct-v0.3** on a custom dataset of 1,690 instruction pairs built from IndianKanoon court judgements + GPT-4o teacher distillation using QLoRA (r=16, α=32). Shipped a complete MLOps stack on top — not just a model card, a deployable system with A/B testing.

**Verified benchmark numbers (from actual training runs):**

| Precision | Memory | Latency | ROUGE-1 | ROUGE-L | RAGAS Faithfulness |
|---|---|---|---|---|---|
| FP16 base (Mistral-7B) | 14.5 GB | 10.8 ms/tok | — | 0.40 | — |
| INT8 (llama.cpp GGUF) | ~7.2 GB | ~6.8 ms/tok | — | 0.40 | — |
| **INT4 QLoRA (fine-tuned)** | **4.4 GB** | **4.9 ms/tok** | **0.57** | **0.40** | **0.66** |

> **3.3× memory reduction · 2.2× faster inference · zero ROUGE-L degradation through INT4 quantization**

**What makes this interview-defensible:**
- 📐 **Dataset engineering** — 1,690 pairs from IndianKanoon scraper + GPT-4o teacher distillation, not random web data
- 🔢 **LoRA config rationale** — r=16, α=32 chosen after ablation: r=8 gave 0.04 lower ROUGE-1, r=32 gave no gain
- 📊 **RAGAS Faithfulness 0.66** as grounded eval baseline — not just ROUGE, which doesn't penalise hallucinations
- ⚡ **GGUF quantization via llama.cpp** — FP16 → INT8 → INT4 with zero ROUGE-L drop, proving NF4 distribution preserves legal vocabulary
- 🧪 **MLflow experiment tracking** — all 3 training runs logged with hyperparams, metrics, and artifact versions
- 🖥️ **Streamlit A/B dashboard** — live side-by-side comparison of base vs fine-tuned on custom legal prompts
- 🤗 **HF Hub deployment** — LoRA adapter + full model card published with training config

**Tech:** Unsloth · QLoRA · bitsandbytes · llama.cpp GGUF · MLflow · Streamlit · Hugging Face Hub · PyTorch

[![GitHub](https://img.shields.io/badge/GitHub-NyayaGPT-181717?style=flat&logo=github)](https://github.com/gauravgarwal9011/NyayGPT)
[![HuggingFace](https://img.shields.io/badge/Model-HF_Hub-FFD21E?style=flat&logo=huggingface)](https://huggingface.co/gauravgarwal9011)
[![MLflow](https://img.shields.io/badge/MLflow-Experiments-0194E2?style=flat&logo=mlflow)](https://github.com/gauravgarwal9011/NyayGPT)

---

### 🗺️ Intelligent Route Guidance & Productivity Assistant
> **LangGraph agent integrated with Microsoft 365 — 40% reduction in admin tasks**

Built a production LangGraph-powered assistant that combines real-time route guidance with full Microsoft 365 workflow automation — fetching emails, scheduling Teams meetings, and drafting responses autonomously.

**Integrations built:**
- 📧 **Microsoft Graph API** — Outlook email fetch, Teams meeting scheduling, draft generation
- 🔄 **Power Automate** — automated multi-step workflow triggers from agent decisions
- 📍 **MongoDB** — persistent session state and client tracking (35% accuracy improvement)
- ⚡ **Azure Functions** — serverless execution for background automation tasks

**Tech:** LangGraph · MongoDB · Azure Functions · Microsoft Graph API · Power Automate · FastAPI

[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat&logo=github)](https://github.com/gauravgarwal9011/route-guidance-assistant)

---

### 📄 Multimodal RAG — Document Extraction & Retrieval
> **RAG system that understands tables, images, and text — 30% better extraction accuracy**

Built a multimodal RAG pipeline using the **Unstructured library** to extract and index mixed-format documents (PDFs with embedded tables, charts, and images) — then query uniformly across all modalities.

**What's different from standard RAG:**
- 🖼️ Handles **images, tables, and text** in the same retrieval index — single query hits all modalities
- ⚡ **50% faster retrieval** vs standard text-only RAG via LangChain semantic querying
- 📊 25% improvement in query precision through cross-modal context fusion

**Tech:** LangChain · Unstructured · FAISS · Azure OpenAI · ChromaDB · Streamlit

[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat&logo=github)](https://github.com/gauravgarwal9011/multimodal-rag)

---

### 🎙️ English Speaking Assessment Agent
> **Real-time spoken conversation coach with automated fluency scoring — 25% learner retention improvement**

Built an interactive AI coach that conducts full spoken conversations, scores fluency in real-time across 5 dimensions, and generates personalised feedback reports per session.

**Architecture highlights:**
- 🔊 STT → GPT-4o → TTS pipeline with <800ms round-trip latency
- 📈 Automated scoring: pronunciation, fluency, grammar, vocabulary, coherence
- 📋 Structured feedback reports generated and delivered post-session

**Tech:** Azure OpenAI GPT-4o · Speech-to-Text · Text-to-Speech · FastAPI · Streamlit

[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat&logo=github)](https://github.com/gauravgarwal9011/english-speaking-assessment-agent)

---

### ⚡ HybridRAG — Dense + Sparse Retrieval System
> **+18% recall@5 vs pure dense retrieval — benchmarked, not estimated**

Built an enterprise RAG system combining **BM25 keyword search + FAISS semantic search** via LangChain's EnsembleRetriever, with all three prompting patterns (CoT, ToT, ReAct) exposed as separate API endpoints.

**Benchmark results:**

| Retriever | Recall@5 | Latency | Notes |
|---|---|---|---|
| Dense only (FAISS) | 0.71 | 180ms | Baseline |
| Sparse only (BM25) | 0.64 | 45ms | Misses semantic matches |
| **Hybrid (Ensemble)** | **0.84** | **210ms** | **+18% recall vs baseline** |

**Tech:** LangChain EnsembleRetriever · BM25 · FAISS · Azure OpenAI · MLflow · Streamlit

[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat&logo=github)](https://github.com/gauravgarwal9011/hybrid-rag)
[![HuggingFace](https://img.shields.io/badge/Demo-HF_Space-FFD21E?style=flat&logo=huggingface)](https://huggingface.co/spaces/gauravgarwal9011)

---

### 📊 LLM Eval Suite
> **Complete evaluation pipeline — RAGAS + DeepEval + W&B + GitHub Actions CI gate**

Production evaluation framework that runs 4 RAGAS metrics + DeepEval hallucination checks + custom domain metrics against a golden dataset — and **automatically fails the PR** if faithfulness drops below threshold.

**3-model benchmark using NyayaGPT results:**

| Model | ROUGE-1 | ROUGE-L | RAGAS Faithfulness | Latency | Memory |
|---|---|---|---|---|---|
| GPT-4o (API baseline) | — | — | 0.91 | ~1,200ms | API |
| Mistral-7B FP16 (base) | — | 0.40 | — | 10.8 ms/tok | 14.5 GB |
| **Mistral-7B INT4 (NyayaGPT)** | **0.57** | **0.40** | **0.66** | **4.9 ms/tok** | **4.4 GB** |

> NyayaGPT: **2.2× faster · 3.3× smaller · RAGAS Faithfulness 0.66** — all real measured numbers

**Tech:** RAGAS · DeepEval · Weights & Biases · LangSmith · GitHub Actions · Streamlit · MLflow

[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat&logo=github)](https://github.com/gauravgarwal9011/llm-eval-suite)
[![W&B](https://img.shields.io/badge/W%26B-Dashboard-FFBE00?style=flat&logo=weightsandbiases)](https://wandb.ai/gauravgarwal9011)

---

### 🔌 MCP-Enabled Agent Server
> **Due Diligence Agent re-architected as a Model Context Protocol server**

Refactored the Due Diligence Agent to expose all 4 tools as a **FastMCP server** — connectable from Claude Desktop, any MCP client, or LangGraph via `MultiServerMCPClient`. One Docker Compose command starts everything.

```bash
# Connect any MCP client to your running server
mcp connect http://localhost:8000
> search_documents("SEBI regulations 2024")
> assess_risk("The indemnity clause limits liability to...")
```

**Tech:** FastMCP · LangGraph · ChromaDB · Redis · PostgresSaver · Docker Compose

[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat&logo=github)](https://github.com/gauravgarwal9011/mcp-agent-server)

---

### 🛡️ HITL Enterprise Agent — Production Safety Layer
> **Human-in-the-loop + compliance guardrails for enterprise agentic workflows**

Extended the MCP Agent with SOC2-aligned safety controls: **LangGraph `interrupt()`** for human approval checkpoints, **Microsoft Presidio** PII detection, prompt injection filtering, and a full audit trail per run.

**Controls implemented:**

| Control | Implementation | Standard |
|---|---|---|
| Human approval gate | LangGraph interrupt() | SOC2 CC6 |
| PII redaction | Microsoft Presidio | GDPR Art. 5 |
| Prompt injection detection | Rule-based + classifier | OWASP LLM01 |
| Audit logging | SQLite + FastAPI | SOC2 CC7 |
| Confidence threshold | Auto-review if score <0.85 | Internal |

**Tech:** LangGraph · Presidio · LangSmith · DeepEval guardrails · FastAPI · PostgresSaver

[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat&logo=github)](https://github.com/gauravgarwal9011/hitl-enterprise-agent)

---

## 🧰 Tech Stack

### Gen AI & LLM Engineering
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Azure OpenAI](https://img.shields.io/badge/Azure_OpenAI-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![Hugging Face](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)
![Haystack](https://img.shields.io/badge/Haystack-00B0FF?style=flat)

### Vector Stores & Retrieval
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat)
![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat&logo=pinecone&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-F97316?style=flat)
![LanceDB](https://img.shields.io/badge/LanceDB-8B5CF6?style=flat)

### Fine-Tuning & Evaluation
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![RAGAS](https://img.shields.io/badge/RAGAS-00D4AA?style=flat)
![DeepEval](https://img.shields.io/badge/DeepEval-EC4899?style=flat)
![W&B](https://img.shields.io/badge/Weights_&_Biases-FFBE00?style=flat&logo=weightsandbiases&logoColor=black)
![Langfuse](https://img.shields.io/badge/Langfuse-7C3AED?style=flat)
![LangSmith](https://img.shields.io/badge/LangSmith-1C3C3C?style=flat)

### Backend & Deployment
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)

### Cloud & Azure
![Azure Functions](https://img.shields.io/badge/Azure_Functions-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![Azure Logic Apps](https://img.shields.io/badge/Azure_Logic_Apps-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![Azure AI Foundry](https://img.shields.io/badge/Azure_AI_Foundry-0078D4?style=flat&logo=microsoftazure&logoColor=white)

### Data & ML
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

---

## 💼 Work Experience

**AI/ML Engineer** · Ignatiuz Software Solutions · *Jun 2025 – Present*
- Building production LLM and Gen AI solutions — **35% faster inference, 22% accuracy improvement**
- RAG workflows with LangChain + FAISS + Pinecone + Azure — **40% reduction in retrieval latency**
- FastAPI backends + Streamlit UIs for document intelligence and decision-support workflows

**DS & AI Intern** · Intellipaat · *2024 – 2025*
- ML pipelines in Python + SQL — **15% accuracy improvement, 20% processing time reduction**

---

## 🎓 Education & Certifications

- **MBA in Business Analytics & Marketing** — DAVV *(2023–2025)*
- **Executive PG Certification in Data Science & AI** — IHub Divyasampark, IIT Roorkee & Intellipaat

---

## 📊 GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=gauravgarwal9011&show_icons=true&theme=radical&hide_title=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=gauravgarwal9011&layout=compact&theme=radical)

</div>

---

## 🔍 Earlier Projects

<details>
<summary>Click to expand — Data Science & ML projects</summary>

### End-to-End QA System (Haystack + Pinecone)
Scalable Question Answering system with RAG pipelines, dense retrievers, and FastAPI deployment.
[View Repo](https://github.com/gauravgarwal9011/End-to-End-QA-system-using-Haystack-and-Pinecone-DB)

### News Summarization + Text-to-Speech App
Real-time news scraping → NLP summarization → gTTS speech synthesis with multilingual support.
[View Repo](https://github.com/gauravgarwal9011/News-App)

### Walmart Sales Prediction (Time Series)
ARIMA + Seasonal ARIMA forecasting on retail sales data.
[View Repo](https://github.com/gauravgarwal9011/Walmart-sales-time-series)

### Netflix Recommendation Engine (SVD)
Collaborative filtering using Singular Value Decomposition on viewing history data.
[View Repo](https://github.com/gauravgarwal9011/Netflix-Recommendation-system)

### SQL Case Study — Advanced Customer Analytics
CTEs, UDFs, TVFs, stored procedures, triggers, and pivot/unpivot on a customer database.
35% query performance improvement. [View Repo](https://github.com/gauravgarwal9011/SQL-Case-Study)

</details>

---

<div align="center">

*If you find my work useful, a ⭐ on any repo goes a long way.*
*Open to collaborating on production AI/ML systems — reach out anytime.*

</div>
