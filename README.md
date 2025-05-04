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

## the models that we are using:


---------this is for qwen2.5 model-------
from llama_cpp import Llama

llm = Llama.from_pretrained(
	repo_id="lmstudio-community/Qwen2.5-7B-Instruct-1M-GGUF",
	filename="Qwen2.5-7B-Instruct-1M-Q4_K_M.gguf",
)

---------this is for gemma -------
from llama_cpp import Llama

llm = Llama.from_pretrained(
	repo_id="lmstudio-community/gemma-3-4b-it-GGUF",
	filename="gemma-3-4b-it-Q4_K_M.gguf",
)
---------this is for base-model-llama -------
from llama_cpp import Llama

llm = Llama.from_pretrained(
	repo_id="lmstudio-community/Meta-Llama-3.1-8B-Instruct-GGUF",
	filename="Meta-Llama-3.1-8B-Instruct-Q4_K_M.gguf",
)
---------this is for fine-tune llama ( model A ) -------

from llama_cpp import Llama

llm = Llama.from_pretrained(
	repo_id="hafizizaironi/crypto_llama3.1_8b_q4_k_m_mzas_selfannotated",
	filename="unsloth.Q4_K_M.gguf",
)
---------this is for fine-tune llama ( model B ) -------

from llama_cpp import Llama

llm = Llama.from_pretrained(
	repo_id="lmstudio-community/Llama-3.2-3B-Instruct-GGUF",
	filename="Llama-3.2-3B-Instruct-Q4_K_M.gguf",
)

## Images

<img width="1512" alt="Screenshot 2025-05-04 at 1 17 22 PM" src="https://github.com/user-attachments/assets/5d9b67ec-2ac4-4127-8264-78a9f8b557af" />



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


