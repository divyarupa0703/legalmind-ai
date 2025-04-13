 Legal Document QA Pipeline
A powerful legal question-answering system that processes legal PDFs, extracts key sections, stores embeddings using ChromaDB, and answers queries using Gemini's LLM.

🚀 Features
✅ Text Extraction from PDF files using PyMuPDF.

🧩 Contextual Chunking of legal sections (case info, arguments, court orders, etc.)

🧠 Embeddings via Gemini's Embedding API.

🗄️ Storage & Retrieval with ChromaDB.

📚 Legal Metadata Extraction (judge, IPC sections, petitioners, etc.)

🧑‍⚖️ Legal QA using Gemini with:

Standard answers

Chain-of-Law Reasoning (structured legal reasoning)

📦 Dependencies
bash
Copy
Edit
pip install pymupdf chromadb google-generativeai
🧠 Powered By
PyMuPDF – for parsing PDFs

ChromaDB – vector store

Google Generative AI (Gemini) – for embeddings & answers

🧪 Example Usage
python
Copy
Edit
if __name__ == "__main__":
    pdf_path = "path/to/legal_document.pdf"
    
    full_text, chunks = process_and_store_pdf(pdf_path)
    metadata = extract_metadata(full_text)

    question = "What was the final order of the court?"
    result = legal_qa(question, full_text, reasoning=True)

    print("[Metadata]", metadata)
    print("[Answer]", result["answer"])
📂 File Structure
bash
Copy
Edit
legal_qa_pipeline.py  # Main script
README.md             # This file
chroma_db/            # Vector DB folder (auto-created)
⚖️ Legal-Specific Chunking Includes:
Case Information

Representation (Advocates)

Charges/Allegations

Petitioner's Arguments

State's Response

Final Court Order

🤖 Modes of Answering
Mode	Description
Standard	Direct QA based on context
Chain-of-Law	Step-by-step legal reasoning
