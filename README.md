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

<img width="1512" alt="Screenshot 2025-05-04 at 1 17 08 PM" src="https://github.com/user-attachments/assets/cf341410-f07f-48c9-9608-7a0cd64aeb44" />

<img width="1512" alt="Screenshot 2025-05-04 at 1 17 12 PM" src="https://github.com/user-attachments/assets/2edce3ff-9a0e-4115-a354-9266f1d0e611" />

<img width="1512" alt="Screenshot 2025-05-04 at 1 17 49 PM" src="https://github.com/user-attachments/assets/e023e7d4-6a33-4f67-b2c3-28125baf4e43" />

![Screenshot 2025-05-04 at 1 18 02 PM](https://github.com/user-attachments/assets/114796aa-cc83-4e60-933f-6d11c0a18755)

<img width="1512" alt="Screenshot 2025-05-04 at 1 18 13 PM" src="https://github.com/user-attachments/assets/41204ffb-c5c4-4e28-b8c0-efcdda294293" />


<img width="1512" alt="Screenshot 2025-05-04 at 1 17 22 PM" src="https://github.com/user-attachments/assets/5d9b67ec-2ac4-4127-8264-78a9f8b557af" />

<img width="1512" alt="Screenshot 2025-05-04 at 1 17 22 PM" src="https://github.com/user-attachments/assets/aa549899-24e1-4a5b-b3b0-0d021307ea6d" />



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


