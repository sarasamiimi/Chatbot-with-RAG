
This project is a simple but complete chatbot built in three steps. It starts with a basic Streamlit interface, then connects to Groq’s LLaMA models, and finally adds RAG so the chatbot can answer questions based on a PDF file.

Phase 1 – Basic Streamlit Chat 

File: phase_1.py
The first version introduces the chat interface. Messages are saved in session state and the bot returns a placeholder response.

Phase 2 – Groq LLaMA Integration 

File: phase_2.py
Here the placeholder reply is replaced with real output from Groq’s llama3-8b-8192 model. A custom system prompt helps the model respond clearly and directly.

Phase 3 – PDF RAG System 

File: phase_3.py
This phase adds Retrieval-Augmented Generation. The app loads a PDF (reflexion.pdf), splits it into chunks, creates embeddings, and uses a retriever to ground answers in the document.

Installation 

pip install streamlit langchain langchain-groq langchain-community chromadb sentence-transformers 

Or with Pipenv:

pipenv install 

Running the App 

Set your Groq API key:

export GROQ_API_KEY="your_key" 

Start the application:

streamlit run phase_3.py 

phase_1.py phase_2.py phase_3.py Pipfile Pipfile.lock reflexion.pdf README.md 

This project demonstrates how to combine Streamlit, Groq LLMs, and a lightweight RAG pipeline to build a document-aware conversational app.
