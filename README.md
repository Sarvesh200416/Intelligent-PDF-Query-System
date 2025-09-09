# 📈 Stock Market Performance 2024 - Intelligent PDF Query System

This project implements an **Intelligent Retrieval-Augmented Generation (RAG) system** that allows users to query a PDF document containing information about **Stock Market Performance in 2024**. The system uses **LangGraph**, **Groq's LLaMA-3 model**, and **ChromaDB** to provide accurate, citation-backed answers.

---

## 📌 Project Overview

* **Goal**: Query a financial report (Stock Market Performance 2024) and retrieve precise, citation-based answers.
* **Method**: Retrieval-Augmented Generation (RAG) using PDF as the knowledge base.
* **Key Features**:

  * PDF loading and preprocessing with `PyPDFLoader`
  * Text chunking for efficient retrieval
  * Vector embeddings using `HuggingFaceEmbeddings`
  * Vector store creation with **ChromaDB**
  * LLM reasoning with **ChatGroq (LLaMA-3 70B)**
  * Retrieval pipeline orchestration via **LangGraph**

---

## 🛠️ Tech Stack

* **Python 3**
* **LangGraph** – state machine for reasoning and tool use
* **Groq API** – LLaMA-3 based inference
* **LangChain** – document processing and tools integration
* **ChromaDB** – vector store for retrieval
* **HuggingFace Embeddings** – `sentence-transformers/all-MiniLM-L6-v2`
* **PyPDFLoader** – PDF document loader
---

## ⚙️ How It Works

1. Load the PDF using **PyPDFLoader**.
2. Split text into chunks with **RecursiveCharacterTextSplitter**.
3. Create embeddings with **HuggingFace MiniLM**.
4. Store vectors in **ChromaDB**.
5. Use **LangGraph** to manage conversation and tool usage.
6. Call **ChatGroq (LLaMA-3)** to answer user queries.
7. Retrieve supporting document chunks for citation.

---

## 📊 Example Usage

```
=== RAG AGENT===

What is your question: How did the tech sector perform in 2024?

=== ANSWER ===
According to *Stock Market Performance 2024*, the tech sector showed strong growth driven by AI adoption and cloud expansion. [Document 2]
```

---

## 🔮 Future Improvements

* Add support for multiple PDFs
* Enhance retrieval with hybrid search (semantic + keyword)
* Deploy as a **Streamlit web app** for interactive querying
* Add caching to optimize repeated queries

---
