# MLOps Assignment 2 - Hugging Face Fine-Tuning, W&B Tracking, and Model Deployment

This project implements an end-to-end MLOps workflow for fine-tuning a Hugging Face transformer model for text classification. The workflow uses Kaggle GPU for training, Weights & Biases (W&B) for experiment tracking, Hugging Face Hub for model publishing, and GitHub for reproducibility and submission artifacts.

## Project Links

- GitHub Repository: https://github.com/hemantkumarsri/mlops-assignment2
- Kaggle Notebook: https://www.kaggle.com/code/hemantkumarsri/mlops-assignment-2-fine-tuning-classification-k
- Hugging Face Model: https://huggingface.co/hemantkumarsri/distilbert-goodreads-genres
- W&B Dashboard: https://wandb.ai/hemantkumarsri-mlops/mlops-assignment2

## Model

The model used is `distilbert-base-cased`, a compact and efficient version of BERT. It is suitable for this assignment because it trains faster than full BERT while still providing strong performance for text classification tasks.

## Dataset

The notebook uses UCSD Goodreads review data by genre. Reviews are sampled across eight book genres and split into training and test sets. The task is genre classification from review text.

## Setup Instructions

Install dependencies:

```bash
pip install -r requirements.txt
```

For Kaggle execution:

1. Enable GPU accelerator.
2. Enable Internet.
3. Add Kaggle Secrets:
   - `WANDB_API_KEY`
   - `HF_TOKEN`
4. Run the notebook from top to bottom.

## Results

The previous successful run produced the following evaluation results. Re-running the final notebook will regenerate and log these metrics to W&B.

| Metric | Score |
|---|---:|
| Accuracy | 0.600625 |
| Weighted F1 Score | 0.60 |
| Eval Loss | 1.2195768356 |

## MLOps Workflow

The notebook performs the following steps:

1. Loads secrets securely from Kaggle Secrets.
2. Authenticates with W&B and Hugging Face.
3. Downloads and prepares the Goodreads dataset.
4. Loads DistilBERT tokenizer and model.
5. Fine-tunes the model using Hugging Face Trainer.
6. Logs training metrics to W&B using `report_to="wandb"`.
7. Evaluates the model using Accuracy, F1 Score, and Loss.
8. Saves the classification report as a W&B Artifact.
9. Pushes the trained model and tokenizer to Hugging Face Hub.

## Repository Contents

- `mlops_assignment2_final_fixed_kaggle.ipynb` - corrected Kaggle notebook
- `requirements.txt` - Python dependencies
- `README.md` - project documentation
- `MLOps_Assignment2_Final_Report.pdf` - final report for submission
