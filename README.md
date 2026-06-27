# AI Therapist Bot

An emotion-aware chatbot that detects how a user feels from text and responds with supportive, therapist-style messages. Built with **DistilBERT** and **BiLSTM** models trained on the [GoEmotions](https://github.com/google-research/google-research/tree/master/goemotions) dataset (28 emotion classes).

## Features

- **Emotion classification** — Fine-tuned DistilBERT (~58% accuracy) and BiLSTM baseline on GoEmotions
- **Empathetic responses** — Rule-based therapist replies mapped to detected emotions
- **Interactive chat** — CLI loop and Gradio web UI
- **Model comparison** — Side-by-side BiLSTM vs BERT evaluation metrics

## Project structure

```
.
├── ai-therapist-bot.ipynb   # Full training & inference notebook (Google Colab)
├── requirements.txt
└── README.md
```

## Quick start

### 1. Clone the repo

```bash
git clone https://github.com/YOUR_USERNAME/ai-therapist-bot.git
cd ai-therapist-bot
```

### 2. Install dependencies

```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Run the notebook

Open `ai-therapist-bot.ipynb` in [Google Colab](https://colab.research.google.com/) (GPU recommended) or Jupyter locally.

The notebook will:

1. Download the GoEmotions dataset
2. Train BiLSTM and DistilBERT classifiers
3. Save model weights (Colab: Google Drive; local: adjust `SAVE_DIR` paths)
4. Launch a Gradio chat interface

## Models

| Model   | Accuracy | Notes                          |
|---------|----------|--------------------------------|
| BiLSTM  | ~30%     | Baseline with Keras tokenizer  |
| DistilBERT | ~58%  | Fine-tuned `distilbert-base-uncased`, 2 epochs |

## Emotion labels

admiration, amusement, anger, annoyance, approval, caring, confusion, curiosity, desire, disappointment, disapproval, disgust, embarrassment, excitement, fear, gratitude, grief, joy, love, nervousness, optimism, pride, realization, relief, remorse, sadness, surprise, neutral

## Disclaimer

This project is for **educational and research purposes only**. It is not a substitute for professional mental health care. If you or someone you know is in crisis, please contact a qualified mental health professional or emergency services.

## License

MIT

## Acknowledgments

- [GoEmotions dataset](https://arxiv.org/abs/2005.00547) — Google Research
- [Hugging Face Transformers](https://huggingface.co/docs/transformers)
