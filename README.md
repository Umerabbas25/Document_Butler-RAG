# 📚 Document Butler: RAG AI Platform

A fully functional Retrieval-Augmented Generation (RAG) web application built with Python, FastAPI, and Next.js. Designed to provide a seamless document interaction experience for users, complete with file uploading, question answering with citations, and an integrated document viewer.

## 🚀 Features

### Core Platform
- **Document Processing**: Upload your files (PDF, DOCX, Markdown) and have them automatically chunked and vectorized.
- **Intelligent Q&A**: Ask context-aware questions based on your uploaded documents using state-of-the-art LLMs.
- **Exact Citations**: Quickly verify facts with exact source citations linking to the corresponding documents.
- **In-Browser File Viewer**: View your source materials side-by-side with your chat without leaving the application.

## 🛠️ Tech Stack
- **Backend**: Python, FastAPI
- **AI Framework**: LangChain
- **Vector Database**: Qdrant Cloud
- **Frontend**: Next.js, React, Tailwind CSS
- **Models**: Groq / OpenAI (LLM), HuggingFace (Embeddings)

## 💻 Local Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

### 2. Backend Setup
Make sure you have Python installed. Navigate to the backend directory:
```bash
cd backend-20260601T124647Z-3-001/backend
python -m venv venv
# On Windows
.\venv\Scripts\Activate.ps1
# On macOS/Linux
source venv/bin/activate
pip install -r requirements.txt
```

### 3. Configure Environment Variables
Create a `.env` file in the backend directory and add your Qdrant and AI credentials:
```env
OPENAI_API_KEY=your_api_key_here
QDRANT_URL=your_qdrant_cluster_url
QDRANT_API_KEY=your_qdrant_api_key
QDRANT_COLLECTION=document_butler
EMBEDDING_PROVIDER=huggingface
LLM_MODEL=llama3-8b-8192
```

### 4. Start the Backend Server
Run the following command to start the FastAPI server on port 8001:
```bash
uvicorn main:app --reload --port 8001
```

### 5. Frontend Setup
Navigate to the frontend directory:
```bash
cd frontend-next-20260601T124715Z-3-001/frontend-next
npm install
```

### 6. Start the Frontend Server
Run the following command to start the Next.js development server:
```bash
npm run dev
```

### 7. View the App
Visit [http://localhost:3000](http://localhost:3000) in your browser to start chatting with your documents!
