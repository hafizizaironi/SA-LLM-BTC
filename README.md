# SA-LLM-BTC

**SA-LLM-BTC** is a sentiment analysis system for Bitcoin news headlines using Large Language Models (LLMs).

## 🔍 Features

- Analyzes cryptocurrency news headlines using multiple LLMs
- Models used: LLaMA, Qwen, BERT, Gemma, and VADER (lexicon-based)
- Converts model outputs into JSON sentiment format
- Frontend built with React for interactive visualization
- Backend powered by FastAPI and supports multiple model endpoints

## 📁 Project Structure

- `frontend/`: React-based interface for input, result visualization, and interaction
- `backend/`: FastAPI server with sentiment analysis APIs
- `models/`: Not included due to size — see below

## 📦 Models

The `.gguf` model files are **not included** in this repo due to GitHub file size limits.

📥 **You can download them from [Google Drive / Hugging Face](#)**  
📝 Place them inside: `backend/app/models/`

## ⚙️ Setup

```bash
# Frontend
cd frontend
npm install
npm run dev

# Backend
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
