# 🚀 n8n RAG Automation using Ollama & Pinecone

A fully automated **Retrieval-Augmented Generation (RAG)** pipeline built with **n8n**, **Ollama (local LLMs)**, and **Pinecone Vector Database**.

This project demonstrates how to ingest documents, generate embeddings, store them in a vector database, and query them using an AI Agent with real context.

---

## ✨ Features

- 📁 Automated document ingestion from Google Drive
- ✂️ Intelligent document chunking
- 🧠 Embedding generation using local Ollama models
- 📦 Scalable vector storage with Pinecone
- 💬 Context-aware chat using n8n AI Agent
- 🔒 Runs locally with no external LLM dependency

---
## 📂 Folder Structure

```
n8n-rag-automation-ollama-pinecone/
│
├── workflows/
│   ├── file-ingestion-pipeline.json
│   └── rag-chat-automation.json
│
├── screenshots/
│   ├── file-ingestion-workflow.png
│   └── rag-chat-workflow.png
│
├── .env.example
├── .gitignore
└── README.md
```
---

## 🏗️ Architecture Overview

**File Ingestion Pipeline**
- Google Drive Trigger (file added/updated)
- File download
- Recursive Character Text Splitter
- Embeddings via `nomic-embed-text`
- Store vectors in Pinecone

**RAG Chat Pipeline**
- Chat trigger
- AI Agent (tool-enabled)
- Semantic search from Pinecone
- Context-aware responses using Llama 3.2

---

## 🧠 Models Used

| Purpose | Model |
|------|------|
| Chat / Agent | `llama3.2:latest` |
| Embeddings | `nomic-embed-text` |
| Embedding Dimension | `768` |
| Similarity Metric | `cosine` |

---

## ⚙️ Prerequisites

- n8n (local or Docker)
- Ollama installed
- Pinecone account
- Google Drive credentials (for ingestion)

---

## 🚀 Setup Instructions

### 1️⃣ Install Ollama Models
```bash
ollama pull llama3.2
ollama pull nomic-embed-text

 ```



---
## 🌟 Final Notes

This project was built to explore how **automation, local LLMs, and vector databases** come together to form real-world AI systems.  
Everything here is designed to be **practical, transparent, and extensible**.

If this repository helps you learn, build, or experiment with **RAG pipelines**, feel free to fork it, adapt it, or improve it.

Contributions, suggestions, and discussions are always welcome.

⭐ If you found this useful, consider starring the repo — it really helps!

Happy building 🚀
---
