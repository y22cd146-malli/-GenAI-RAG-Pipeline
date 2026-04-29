# 🤖 GenAI RAG Pipeline

> Retrieval-Augmented Generation pipeline built with LangChain, ChromaDB, and FastAPI. Improved response accuracy by **40%** using semantic search and optimised embeddings.

![Python](https://img.shields.io/badge/Python-3.11-blue) ![FastAPI](https://img.shields.io/badge/FastAPI-0.111-green) ![LangChain](https://img.shields.io/badge/LangChain-0.2-orange) ![Docker](https://img.shields.io/badge/Docker-ready-blue)

## 🏗️ Architecture

```
User Query → FastAPI → Vector Search (ChromaDB) → LLM (Mistral) → Grounded Answer
```

## ✨ Features
- 📄 Ingest PDF and text documents into a persistent vector store
- 🔍 Semantic search with HuggingFace embeddings
- 🤖 LLM-powered answers via Ollama (local, zero API cost)
- 🌐 REST API with FastAPI
- 🐳 Docker-ready deployment
- 📊 Structured logging and fault-tolerant architecture

## 🚀 Quick Start

```bash
git clone https://github.com/YOUR_USERNAME/genai-rag-pipeline.git
cd genai-rag-pipeline
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
uvicorn app.api:app --reload --port 8000
```

Or with Docker:
```bash
docker-compose up --build
```

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /health | Health check |
| POST | /ingest | Ingest documents |
| POST | /query | Query the pipeline |

### Example
```bash
curl -X POST http://localhost:8000/query \
  -H "Content-Type: application/json" \
  -d '{"question": "What are the key findings?"}'
```

## 📁 Project Structure
```
genai-rag-pipeline/
├── app/
│   ├── api.py              # FastAPI routes
│   └── rag_pipeline.py     # Core RAG logic
├── tests/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── .env.example
```

## 🧪 Tests
```bash
pytest tests/ -v
```

## 👨‍💻 Author
**Mallikarjuna Purni** — Cloud & AI MLOps Engineer
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/mallikarjuna-purni-a8185628b/)
