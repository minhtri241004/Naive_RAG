# 🛒 E-commerce RAG Shopping Assistant

An intelligent shopping assistant pipeline built with **Retrieval-Augmented Generation (RAG)**. This project retrieves relevant product information from a custom catalog and uses a Large Language Model (LLM) to generate personalized, format-specific recommendations for users.

## 🌟 Key Features

* **Vector Search Engine:** Utilizes `FAISS` for fast and efficient similarity search.
* **Multilingual Embeddings:** Powered by `sentence-transformers` (`paraphrase-multilingual-MiniLM-L12-v2`) to handle diverse queries accurately.
* **Generative AI Integration:** Uses Google's `Gemini` API to synthesize retrieved context into natural, helpful, and strictly formatted recommendations.
* **Secure Configuration:** Implements `python-dotenv` for safe API key management.
* **Modular Architecture:** Clean separation of concerns between data indexing (offline) and querying (online).

## 📂 Project Structure

```text
📦 RAG-Shopping-Assistant
 ┣ 📂 data/
 ┃ ┣ 📜 rag_dataset.csv        # Raw product catalog dataset
 ┃ ┣ 📜 product_index.faiss    # Compiled FAISS vector index
 ┃ ┗ 📜 documents.pkl          # Pickled document store for retrieval
 ┣ 📜 build_index.py           # Script to encode text and build FAISS index
 ┣ 📜 query.py                 # Script to test vector retrieval directly
 ┣ 📜 rag_pipeline.py          # Main pipeline integrating FAISS and Gemini LLM
 ┣ 📜 .env                     # Environment variables (API Keys) - NOT tracked by git
 ┣ 📜 .gitignore               # Git ignore rules
 ┗ 📜 README.md                # Project documentation