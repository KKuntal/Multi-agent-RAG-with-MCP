# Agentic RAG Chatbot

Agentic RAG Chatbot is an intelligent system for answering questions over multi-format documents using Retrieval-Augmented Generation (RAG) and a multi-agent architecture. It supports PDF, Word, PowerPoint, CSV, and text/markdown files. The system parses documents, splits them into chunks, generates embeddings with SentenceTransformers, and stores them in a FAISS vector index for semantic search.

When a user asks a question via the Streamlit web interface, the system retrieves relevant document chunks and uses Google Gemini 2.0 Flash to generate answers based strictly on the retrieved context, with source attribution. Agents communicate using a custom Model Context Protocol (MCP) for traceable and robust coordination.

## Features
- Multi-format document support (PDF, PPTX, DOCX, CSV, TXT/MD)
- Semantic search with FAISS and SentenceTransformers
- Context-aware answers with source references
- Modular agentic architecture and traceable communication
- Streamlit chat interface for document upload and Q&A

## Quick Start
1. Install Python 3.8+ and get a Google Gemini API key
2. Clone the repository and install dependencies:
  ```bash
  git clone "repo link"
  cd agentic-rag-chatbot
  pip install -r requirements.txt
  ```
3. Add your API key to a `.env` file:
  ```env
  GEMINI_API_KEY=your_gemini_api_key_here
  ```
4. Run the app:
  ```bash
  streamlit run ui/streamlit_app.py
  ```
