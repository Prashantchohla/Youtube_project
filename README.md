# 🎥 YouTube Transcript Q&A System using LangChain and Hugging Face

This project implements an intelligent Q&A system over YouTube video transcripts using **LangChain**, **Hugging Face Transformers**, and **semantic search** powered by **ChromaDB**. Given a YouTube video URL, the system fetches its transcript, embeds it, stores it in a vector database, and allows users to ask contextual questions based on the content.

---

## 📌 Key Features

- 🔗 Fetches YouTube video transcripts using `youtube-transcript-api`
- ✂️ Splits long transcripts into manageable chunks using LangChain's `RecursiveCharacterTextSplitter`
- 💬 Embeds text using `sentence-transformers` and stores in `Chroma` vector database
- ❓ Enables semantic Q&A via Hugging Face LLMs with contextual chunk retrieval
- ⚙️ Built using modular LangChain components (embedding, retriever, prompt, parser)

---

## 🧠 Tech Stack

- **LangChain** (core, community, text-splitters)
- **Hugging Face Transformers** (`sentence-transformers`, `huggingface_hub`)
- **ChromaDB** (vector store)
- **YouTube Transcript API**
- Python (Jupyter Notebook)

---

## 🗂️ Project Workflow

1. **Transcript Ingestion**:
   - Extracts transcript for a given `video_id` using `YouTubeTranscriptApi`
2. **Document Chunking**:
   - Splits the transcript into overlapping chunks (`chunk_size=1000`, `overlap=200`)
3. **Embedding & Vector Store**:
   - Uses `HuggingFaceEmbeddings` to convert chunks into vectors
   - Stores them in a persistent ChromaDB vector store
4. **Query & Answer Generation**:
   - User inputs a question
   - Top relevant transcript chunks are retrieved
   - A prompt template and HuggingFace LLM (`HuggingFaceEndpoint`) generate the final answer

---

## 📁 File Overview

| File                          | Description |
|-------------------------------|-------------|
| `YouTube_Project.ipynb`       | Complete code in notebook format including setup, ingestion, vectorization, and Q&A |


