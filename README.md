# 🥂 Penny AI Agent – Big Bang Theory RAG Personality Chatbot

This project builds an **AI agent that roleplays Penny from *The Big Bang Theory***.  
It combines **web scraping, LLM personality extraction, vector embeddings, Pinecone RAG, and LangGraph orchestration** to create a conversational agent that stays **in-character** with Penny’s witty, sarcastic, and warm personality.

---

## 🚀 Features
- **Scrapers**
  - Pulls Penny’s **quotes** from [the-big-bang-theory.com](https://the-big-bang-theory.com/quotes/character/Penny/).
  - Crawls **Fandom transcripts** to extract Penny’s full dialogues.
- **Personality Extraction**
  - Uses Groq LLM (`llama-3.1-8b-instant`) to analyze Penny’s dialogues and produce a concise list of personality traits and behaviors.
- **Knowledge Base (RAG)**
  - Embeds facts, quotes, and traits with HuggingFace embeddings.
  - Stores in **Pinecone vector database** for retrieval.
- **LangGraph Agent**
  - Responds in **Penny’s voice** with witty, sarcastic but friendly answers.
  - Supports tools:
    - `character_recall`: retrieves quotes/traits from Pinecone.
    - `save_memory` & `recall_memory`: agent memory persistence.
- **End-to-End Flow**
  1. Scrape Penny’s quotes + dialogues.
  2. Extract personality traits.
  3. Upsert into Pinecone.
  4. Deploy LangGraph agent that chats like Penny.

---

## 📦 Tech Stack
- **Python 3.10+**
- **LangChain / LangGraph** – agent orchestration
- **Groq LLM** – personality analysis & agent responses
- **Pinecone** – vector database
- **HuggingFace Embeddings** – text vectorization
- **BeautifulSoup / Requests** – scraping
- **Google Colab** – secrets + execution

---

## 🛠️ Setup

### 1. Clone Repo & Install Dependencies
```bash
pip install -q langchain langgraph pinecone-client beautifulsoup4 requests sentence-transformers
