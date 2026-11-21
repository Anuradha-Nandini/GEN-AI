# TOKENIZER LAB — Comparison of BPE, WordPiece and SentencePiece (English • Telugu • Hindi)

## 1. Aim
Implement and compare three subword tokenization approaches — BPE, WordPiece and SentencePiece — using English, Telugu and Hindi text, and observe how each splits text and how many tokens it produces.

## 2. Learning Objectives
- Understand why tokenization is required before text is processed by a language model.
- Observe the difference between word-level and subword-level splitting.
- Run pretrained tokenizers representing BPE, WordPiece and SentencePiece.
- Compare token pieces and token counts for English, Telugu and Hindi.
- Explain why token counts differ across tokenizer vocabularies and training data.

## 3. Short Theory
A tokenizer converts text into smaller units called tokens (a word, part of a word, punctuation, or a byte/character-related unit) and maps them to numeric token IDs.

| Tokenizer | Basic idea | Model used |
| --- | --- | --- |
| BPE | Repeatedly merges frequent adjacent symbol pairs. GPT-2 uses byte-level BPE. | `gpt2` |
| WordPiece | Learned subword vocabulary; words not in the vocabulary are split into pieces. | `bert-base-multilingual-cased` |
| SentencePiece | Language-independent framework learning subwords from raw text. XLM-R uses SentencePiece with a BPE model. | `xlm-roberta-base` |

**Note:** This compares real pretrained tokenizers, not three algorithms trained on the same data with the same vocabulary size. GPT-2 is mainly English-trained; mBERT and XLM-R are multilingual. So count differences reflect both method and vocabulary/training data. SentencePiece is a framework, not one single algorithm.

## 4. Requirements
Python 3.10+, VS Code, a virtual environment, internet on first run (to download tokenizer files).

## 5. Project Structure
```
Week4/
├── .vscode/settings.json
├── README.md
├── requirements.txt
├── tokenizer_comparison.py
└── viva_questions.md
```

## 6. Setup
Windows (PowerShell), venv in the parent LAB folder:
```powershell
..\.MyEnv\Scripts\Activate.ps1
pip install -r requirements.txt
```
Or create a fresh venv inside this folder:
```bash
python -m venv .venv
# Windows:      .venv\Scripts\Activate.ps1
# macOS/Linux:  source .venv/bin/activate
pip install -r requirements.txt
```

## 7–8. Run
```bash
python tokenizer_comparison.py
```

## 9. Output Format
For each language (English, Telugu, Hindi) and each tokenizer it prints `Tokens`, `Token IDs` and `Token count`. Exact values depend on the tokenizer files.
