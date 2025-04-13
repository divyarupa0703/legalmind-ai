# 🧠 Legal Gemini QA System

This repository provides a powerful pipeline for processing, chunking, embedding, and querying **Indian legal court documents (PDFs)** using **Google Gemini**, **ChromaDB**, and **PyMuPDF**. It enables both **standard legal QA** and **chain-of-law reasoning** using LLMs.

---

## 📂 Features

- 🔍 **PDF Parsing** – Extracts text from Indian court judgments using `PyMuPDF`.
- 🧩 **Legal-Aware Chunking** – Splits text into meaningful sections like case info, petitioner arguments, and final order.
- 🧠 **Embeddings via Gemini** – Embeds document chunks using Google's `embedding-001` model.
- 💾 **Vector Storage** – Stores chunks and embeddings with `ChromaDB`.
- 🧑‍⚖️ **Metadata Extraction** – Extracts court name, judge, case number, petitioner names, and IPC sections.
- 🤖 **Legal QA** – Asks questions about judgments using standard or step-by-step legal reasoning (Chain-of-Law).

---

## 🛠️ Requirements

- Python 3.8+
- Google Generative AI SDK
- ChromaDB
- PyMuPDF (`fitz`)

```bash
pip install chromadb PyMuPDF google-generativeai
