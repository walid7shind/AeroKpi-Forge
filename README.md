# 🚀 AeroMind
### Multimodal KPI Extraction & Validation Engine

---

## 🧠 Overview

AeroMind is a production-grade AI system that transforms unstructured documents (PDFs, tables, graphs) into **structured, validated KPIs**.

**Documents → Structured KPIs → Validated Outputs**

Unlike standard RAG pipelines, AeroMind integrates:
- multimodal processing
- custom retrieval logic
- dependency-aware computation
- constraint-based validation

---

## 🏗️ System Architecture

![Main Architecture](docs/main_architecture.png)

### Pipeline

PDF → Vision Processing → Retrieval System → Extraction → KPI Engine → Validation → Output

---

## 🗂️ Data Architecture

![Data Architecture](docs/data_architecture.png)

The system follows a layered data lifecycle:

- **Input Layer** → raw documents (PDFs)
- **Processing Layer** → OCR + vision parsing
- **Retrieval Layer** → chunking, embeddings, ranking
- **KPI Layer** → structured + computed metrics
- **Output Layer** → datasets & reports
- **Observability Layer** → logs, metrics, validation

---

## ⚙️ Core Logic

### 🔹 Custom Retrieval

score = importance + λ × cosine_similarity

- semantic similarity
- domain-aware ranking
- multi-query retrieval (paraphrases + HyDE)

---

### 🔹 KPI Computation

KPI = f(dependencies, history, extracted values)

- reconstruct missing KPIs
- use historical data
- apply deterministic formulas

---

### 🔹 Validation

total = sum(components)

- cross-KPI consistency
- anomaly detection
- confidence scoring

---

## 📊 Example

### Input

Airline financial report (PDF)

### Output

```json
{
  "revenue": "12.3B",
  "growth": "5.2%",
  "operating_margin": "18%",
  "confidence": 0.87,
  "status": "validated"
}
```

---

## ⚡ Key Features

- Multimodal document understanding
- Custom retrieval scoring (beyond standard RAG)
- Dependency-aware KPI reconstruction
- Constraint-based validation
- Production-level observability (latency, cost, logs)

---

## 🧪 Challenges Solved

- Noisy and inconsistent PDFs
- Missing or partial KPIs
- Complex metric dependencies
- Hallucination control in LLM outputs
- Trade-off between cost, latency, and accuracy

---

## 🛠️ Tech Stack

- **Backend**: FastAPI
- **LLMs / Embeddings**: OpenAI
- **Vector Store**: Qdrant
- **PDF Processing**: PyMuPDF
- **Frontend**: React (streaming UI)

---

## 🔄 Pipeline Execution

The system processes documents through:

1. PDF → JSON conversion
2. JSON enrichment
3. Embedding generation
4. Vector store indexing
5. Retrieval + reasoning

Orchestrated via batch processing and async execution.

---

## 📡 API

### Upload PDFs
POST /api/upload-pdfs

### Query System
POST /ask

### Streaming
- Server-Sent Events (SSE)

---

## 📈 Positioning

This project demonstrates:

- AI system design (not just model usage)
- Integration of AI + data engineering + LLMOps
- Production-aware architecture

---

## ⚠️ Disclaimer

This is a generalized system inspired by real-world constraints.
No proprietary data or internal company logic is exposed.

---

## ⭐ Takeaway

AeroMind is not a chatbot.

It is a **decision-grade AI system** that transforms unstructured data into reliable, structured intelligence.

