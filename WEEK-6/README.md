# Week 6 - Golden Question Set & Baseline Run (Release v0.1)

## Prerequisites
1. Install Ollama and check: `ollama --version`
2. Download the model: `ollama pull llama3.2`
3. Make sure Ollama is running (the desktop app or `ollama serve`) - it listens on http://localhost:11434

## Setup (inside this folder)
```powershell
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

## Run
```
python main.py
```
Creates `baseline_results.csv` (30 questions, keyword score, PASS/REVIEW/ERROR, Release v0.1).
