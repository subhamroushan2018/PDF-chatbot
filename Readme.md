# 📄 Multi-PDF Chatbot using RAG, LangChain & Google Gemini

> An intelligent **Retrieval-Augmented Generation (RAG)** application that enables users to upload multiple PDF documents and ask natural language questions. The chatbot retrieves the most relevant information from the uploaded PDFs and generates accurate, context-aware responses using **Google Gemini 1.5 Flash**.

---

# 📌 Project Overview

This project is a **Multi-PDF Question Answering System** built using **LangChain**, **FAISS**, **Google Gemini**, and **Streamlit**.

Instead of relying on a pre-trained knowledge base, the chatbot processes user-uploaded PDF files, extracts their text, converts it into vector embeddings, stores those embeddings in a FAISS vector database, and retrieves the most relevant context to answer user queries.

The application demonstrates a complete **Retrieval-Augmented Generation (RAG)** workflow for document-based question answering.

---

# 🚀 Features

- 📄 Upload multiple PDF documents
- 🔍 Extract text from uploaded PDFs
- ✂️ Split large documents into manageable text chunks
- 🧠 Generate semantic embeddings using Google Generative AI
- 📦 Store embeddings locally using FAISS
- 🔎 Retrieve relevant document chunks using similarity search
- 🤖 Generate context-aware answers using Google Gemini 1.5 Flash
- 💬 Interactive Streamlit interface
- 🚫 Prevents hallucinations by answering only from retrieved context

---

# 🛠 Tech Stack

- Python
- Streamlit
- LangChain
- Google Gemini 1.5 Flash
- Google Generative AI Embeddings
- FAISS
- PyPDF2
- python-dotenv

---

# ⚙️ RAG Workflow

```
Upload PDF(s)
      │
      ▼
Extract Text (PyPDF2)
      │
      ▼
Split Text into Chunks
(RecursiveCharacterTextSplitter)
      │
      ▼
Generate Embeddings
(Google Generative AI)
      │
      ▼
Store Embeddings
(FAISS Vector Store)
      │
      ▼
Similarity Search
      │
      ▼
Relevant Context
      │
      ▼
Google Gemini 1.5 Flash
      │
      ▼
Final Answer
```

---

# 📂 Project Structure

```
PDF-Chatbot/
│
├── Model
|     ├── app.py
├── README.md
├── requirements.txt
├── .gitignore

```

---

# 🔍 How It Works

### 1. Upload PDF Files

Users upload one or more PDF documents through the Streamlit interface.

### 2. Text Extraction

The application extracts text from every page using **PyPDF2**.

### 3. Text Chunking

The extracted text is divided into overlapping chunks using **RecursiveCharacterTextSplitter** for efficient retrieval.

### 4. Embedding Generation

Each text chunk is converted into vector embeddings using **Google Generative AI Embeddings**.

### 5. Vector Storage

The embeddings are stored locally in a **FAISS Vector Store**.

### 6. Question Answering

When a user asks a question:

- Similarity search retrieves the most relevant text chunks.
- The retrieved context is passed to **Google Gemini 1.5 Flash**.
- Gemini generates an answer strictly based on the retrieved context.

If the required information is unavailable, the chatbot responds with:

> **"Answer is not available in context."**

---

# ▶️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/pdf-chatbot.git
```

Navigate to the project directory

```bash
cd pdf-chatbot
```

Install the required libraries

```bash
pip install -r requirements.txt
```

Create a `.env` file

```env
GOOGLE_API_KEY=YOUR_API_KEY
```

Run the application

```bash
streamlit run app.py
```

---

# 📈 Applications

- Research Paper Question Answering
- Legal Document Analysis
- Academic Notes Assistant
- Company Policy Search
- Technical Documentation Search
- Personal Knowledge Base

---

# 🔮 Future Improvements

- Conversation memory
- Chat history
- Source citation with page numbers
- OCR support for scanned PDFs
- Support for DOCX, TXT, and CSV files
- Hybrid Search (Keyword + Semantic Search)
- Deploy on Streamlit Community Cloud or Hugging Face Spaces

---

# 👨‍💻 Author

**Subham Roushan**

B.Tech, Civil Engineering  
National Institute of Technology Calicut

GitHub: https://github.com/subhamroushan2018

LinkedIn: https://www.linkedin.com/in/subham-roushan/

---

## ⭐ If you found this project useful, consider giving it a star!
