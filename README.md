# 🚀 Financial AI Agent: 2009 Accounting & Finance Expert

A production-focused Financial AI Agent built inside n8n using Retrieval-Augmented Generation (RAG), OpenAI, and Supabase Vector Database.

This project is designed to retrieve and answer finance and accounting-related questions from Pakistan financial regulatory documentation (2009 dataset) using semantic vector search and AI-powered reasoning.

The workflow combines document ingestion, vector embeddings, conversational memory, and live retrieval to create an intelligent finance assistant capable of answering complex accounting and compliance-related queries directly from uploaded documentation.

*📌 Project Overview*

This system was developed as a complete RAG-based AI automation workflow using n8n.

The AI Agent is capable of:
* Reading large financial PDF documents
* Processing and chunking financial data
* Creating vector embeddings using OpenAI
* Storing vectors inside Supabase
* Performing semantic document retrieval
* Answering finance-related queries in natural language
* Maintaining conversational memory during live chat sessions

The workflow demonstrates how AI automation can be integrated into finance, accounting, compliance, and document retrieval systems using modern AI infrastructure.

*🛠️ Complete Workflow Architecture*

The workflow contains 10 interconnected nodes divided into two primary pipelines:

*1️⃣ Live Chat & AI Interaction Pipeline*

* *When Chat Message Received:* This node acts as the primary live chat trigger. It listens for incoming user queries and routes them directly to the AI Agent.
* *Advanced AI Agent:* The central orchestration engine responsible for reasoning, retrieval decisions, and response handling.
* *OpenAI Chat Model:* Provides natural language understanding and generates finance-related conversational responses.
* *Simple Memory:* Stores previous chat interactions locally to maintain conversational continuity and follow-up context.
* *Supabase Vector Store (Tool):* Connected directly to the AI Agent to perform semantic vector search and retrieve relevant financial information from the uploaded dataset.

*2️⃣ Document Ingestion & Vector Pipeline*

* *When Clicking “Execute Workflow”:* Manual execution trigger used to start the document ingestion process.
* *Download File (Google Drive):* Downloads the uploaded financial PDF file directly from Google Drive.
* *Supabase Vector Store:* Initial database connection responsible for handling vector storage.
* *Default Data Loader:* Processes and chunks large PDF content into smaller structured sections for embedding generation.
* *OpenAI Embeddings:* Converts processed text chunks into vector embeddings for semantic search and retrieval.

*📊 Technology Stack*

* n8n
* OpenAI
* Supabase
* Retrieval-Augmented Generation (RAG)
* OpenAI Embeddings
* Vector Database
* Semantic Search
* Google Drive Integration
* Conversational AI

*⚙️ Installation & Setup Guide*

*Step 1 — Import Workflow*
* Download the workflow JSON file from this repository.
* Open your local n8n dashboard.
* Click: Import Workflow -> Upload File.
* Select the workflow JSON file.
* The complete workflow architecture will automatically appear on your canvas.

*Step 2 — Configure Google Drive*
* Upload your finance PDF document to Google Drive.
* Open the Download File node.
* Connect your Google account.
* Select the uploaded PDF file.

*Step 3 — Configure Supabase*
* Create a project on Supabase.
* Open both Supabase nodes inside n8n.
* Add: Supabase URL & Service Role Key.
* Important: Use only the main project URL.
* Example: https://your-project.supabase.co (Do NOT add /rest/v1/).

*Step 4 — Configure OpenAI*
* Open the following nodes: OpenAI Chat Model & OpenAI Embeddings.
* Add your OpenAI API Key credentials.

*Step 5 — Run Vector Ingestion Pipeline*
* Click the: "When Clicking 'Execute Workflow'" node.
* Start execution.
* The workflow will automatically download the PDF, process document text, generate embeddings, and store vectors inside Supabase.

*Step 6 — Start Live Chat*
* Open the: "When Chat Message Received" node.
* Launch the chat interface.
* Ask finance or accounting-related questions.
* The AI Agent will retrieve relevant information directly from the uploaded financial dataset and generate contextual responses.

*📸 Workflow Screenshots*

*1️⃣ Complete Workflow Architecture*
[Screenshot RAG finance.png]

*2️⃣ Live Query & AI Response*
[Screenshot RAG finance (2).png]

*📈 Performance Notes*

* Responses are generated using semantic vector retrieval.
* Accuracy depends on uploaded document quality and chunk structure.
* The workflow is optimized for finance and accounting document retrieval tasks.
* Conversational memory helps maintain contextual follow-up interactions.

*🧠 Learning Purpose*

This project demonstrates:
* RAG implementation inside n8n
* AI workflow automation
* OpenAI embeddings pipeline
* Vector database integration
* Financial document retrieval
* Conversational AI architecture
* Semantic search systems

The workflow is structured in a beginner-friendly format so users can run it locally on their own PC with minimal setup.

*📂 Repository Files*

* Workflow JSON:pakistan finance accounting 2009 data.json 
* Screenshot 1: Screenshot RAG finance.png
* Screenshot 2: Screenshot RAG finance (2).png

*🚀 Future Improvements*

Potential future upgrades include:
* Multi-document support
* OCR integration for scanned files
* Advanced citation and source-linking system
* Real-time database synchronization
* Multi-user authentication
* Dashboard analytics

*📄 License*

This project is provided for educational, learning, and portfolio demonstration purposes.
