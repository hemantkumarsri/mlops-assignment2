# mlops-assignment2
MLOps Assignment 2 - Hugging Face Fine-Tuning, W&amp;B Tracking, and Model Deployment

## Project Description

This project demonstrates a complete MLOps workflow using Hugging Face Transformers, Weights & Biases (W&B), Kaggle GPU training, and Hugging Face Hub deployment. A DistilBERT model was fine-tuned for text classification using the Goodreads dataset.

---

## Technologies Used

- Python
- Hugging Face Transformers
- Kaggle GPU
- Weights & Biases (W&B)
- Hugging Face Hub
- Scikit-learn

---

## Setup Instructions

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Kaggle notebook to:
- Train model
- Track experiments using W&B
- Evaluate performance
- Upload model to Hugging Face

---

## Results

| Metric | Score |
|---|---|
| Accuracy | 0.60 |
| F1 Score | 0.55 |
| Eval Loss | 1.21 |

---

## Links

- Kaggle Notebook: https://www.kaggle.com/code/hemantkumarsri/mlops-assignment-2-fine-tuning-classification-k
- Hugging Face Model: https://huggingface.co/hemantkumarsri/distilbert-goodreads-genres
- W&B Dashboard: https://wandb.ai/hemantkumarsri-indian-institute-of-technology-jodhpur/mlops-assignment2

---

## Model Used

DistilBERT (`distilbert-base-cased`) was used because it is lightweight, faster than BERT, and suitable for text classification tasks.
