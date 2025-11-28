A modular, end-to-end RAG system designed for document-aware question answering.

The project integrates Groq LLaMA, semantic embeddings, vector-based retrieval, and a Streamlit interface to deliver fast and context-grounded responses.

Features
• Multi-phase pipeline
– Phase 1: Streamlit chatbot UI
– Phase 2: Integration with Groq LLaMA 

API
– Phase 3: Full RAG pipeline (PDF ingestion → chunking → embeddings → retrieval → generation)

• Document-aware answering
Upload a PDF, convert it to text chunks, embed them, and ask questions grounded in the uploaded content.

• Fast inference
Powered by Groq’s accelerated LLaMA models for low-latency generation.

• Modular architecture
All phases implemented separately to show learning progression and system design clarity.

 System Architecture
1) Document Loader
PDF files are parsed and chunked into manageable segments.
2) Embedding Generator
Text chunks are converted into semantic vectors using an embedding model.
3) Vector Store / Retriever
Embeddings are indexed and used for similarity search.
4) LLM Layer
Groq LLaMA processes retrieved context and generates grounded answers.
5) User Interface
Streamlit frontend for uploading files and chatting with the model.




   Project Structure
├── phase_1.py # Basic Streamlit chatbot ├── phase_2.py # LLaMA chatbot via Groq API ├── phase_3.py # Full RAG pipeline ├── reflexion.pdf # Self-reflection report ├── Pipfile # Dependencies └── README.md # (This file) 



How to Run
1. Install dependencies
pip install -r requirements.txt 
2. Add your Groq API key
Create a .env file:
GROQ_API_KEY=your_key_here 
3. Run the Streamlit RAG app
streamlit run phase_3.py 


Example Usage
Upload a PDF (e.g., research paper, notes, documentation)
The system automatically:
extracts text
chunks it
creates embeddings
stores them in memory
Ask questions like:
“What does the paper say about the training methodology?”
The model answers using ONLY the content of your file.


Future Improvements (To-Do)
• Add vector store persistence (FAISS / ChromaDB)
• Add evaluation metrics for retrieval quality
• Support multi-PDF knowledge bases
• Add chat history memory
• Deploy a cloud demo version


Why This Project Matters
RAG is one of the most in-demand skills in today’s AI world—combining LLMs with real data.
This project demonstrates practical experience in:
• LLM prompting
• Embedding models
• Information retrieval
• End-to-end ML system design
• UX for ML applications
