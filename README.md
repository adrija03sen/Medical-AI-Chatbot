#  Medical AI Chatbot

An AI-powered medical question-answering chatbot built using **Retrieval-Augmented Generation (RAG)**. It retrieves relevant information from a medical knowledge base and uses an LLM to generate contextual responses.

##  Problem Statement

General-purpose LLMs may generate answers that are not grounded in a specific medical knowledge source. Searching medical documents manually can also be time-consuming.

This project solves this by combining **semantic search + medical documents + LLMs** to provide more relevant, context-based answers.

##  How It Works

```text
Medical PDFs
     ↓
Text Extraction & Chunking
     ↓
Sentence Embeddings
     ↓
Pinecone Vector Database
     ↓
User Question
     ↓
Semantic Similarity Search
     ↓
Relevant Medical Context
     ↓
OpenAI LLM
     ↓
Generated Answer
```

The application uses **RAG**, meaning the LLM receives relevant information retrieved from the medical knowledge base before generating the response.

##  Tech Stack

* **Python** — Core development
* **Flask** — Backend/web application
* **LangChain** — RAG pipeline and LLM orchestration
* **OpenAI** — LLM for response generation
* **Pinecone** — Vector database
* **Sentence Transformers** — Text embeddings
* **PyPDF** — PDF processing
* **python-dotenv** — Environment variable management

##  Project Structure

```text
Medical-AI-Chatbot/
├── research/
├── src/
│   ├── helper.py
│   └── prompt.py
├── app.py
├── requirements.txt
├── setup.py
├── .env
└── README.md
```

##  Setup

### 1. Clone the repository

```bash
git clone https://github.com/adrija03sen/Medical-AI-Chatbot.git
cd Medical-AI-Chatbot
```

### 2. Create virtual environment

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API keys

Create a `.env` file:

```env
OPENAI_API_KEY=your_openai_api_key
PINECONE_API_KEY=your_pinecone_api_key
PINECONE_INDEX_NAME=your_index_name
```

### 5. Run the application

```bash
python app.py
```

##  What Makes It Different?

Unlike a basic chatbot that directly sends questions to an LLM:

```text
Basic Chatbot:
User → LLM → Answer
```

this project uses:

```text
User → Semantic Search → Medical Context → LLM → Answer
```

This allows the model to generate responses using information retrieved from a **specific medical knowledge base**.

##  Key Concepts

* Retrieval-Augmented Generation (RAG)
* Generative AI
* Large Language Models
* Vector Databases
* Semantic Search
* Text Embeddings
* Prompt Engineering
* Flask Backend

##  Disclaimer

This project is for **educational and informational purposes only**. It is not intended to diagnose, treat, or replace professional medical advice.

##  Author

**Adrija Sen**
NIT Silchar

[GitHub Repository](https://github.com/adrija03sen/Medical-AI-Chatbot)
