# cyberbullying-bertweet-pipeline

An end-to-end NLP project focused on **model comparison and selection** for multi-class cyberbullying detection in tweets.

## What this project does
- Cleans and normalizes tweet text using **PySpark**
- Performs stratified train/validation/test splits
- Trains and evaluates **multiple models** to find the best performer:
  - TF–IDF + Logistic Regression (Spark ML baseline)
  - TextCNN
  - BiLSTM
  - **BERTweet (fine-tuned transformer)**
- Compares models using **Macro-F1** to handle class imbalance
- **Deploys only the best-performing model** as a live web app

## Why this matters
Rather than deploying the first model that works, this project benchmarks several approaches, analyzes their performance, and selects the strongest model before deployment.

## Tech stack
PySpark · Spark MLlib · TensorFlow/Keras · PyTorch · Hugging Face Transformers · Gradio

## Live demo
👉 https://huggingface.co/spaces/Auggie-Toff/cyberbullying-BERTweet

## Repository contents
- `cyberbullying_pipeline.ipynb` – full ETL, model training, evaluation, and comparison
- `app/` – deployment code for the selected model

## Notes
- Dataset and pretrained embeddings are not included due to size/licensing.
- Notebook runs in Google Colab or locally with Spark installed.
