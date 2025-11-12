# DistilBERT Sentient Analysis for Mental Health

This project fine-tunes **DistilBERT (distilbert-base-uncased)** for multi-class sentiment analysis on mental-health-related text.  
The model classifies text into categories such as **Normal**, **Depression**, **Bi-Polar**, **Personality Disorder**, **Stress**, and **Suicidal**, helping identify emotional tones related to mental health expressions.

---

## Project Overview

**DistilBERT Sentient Analysis for Mental Health** applies a transformer-based NLP model to classify text into mental-health-related sentiment categories.  
The project demonstrates a complete workflow including:

- Data loading and preprocessing  
- Tokenization using the DistilBERT tokenizer  
- Model fine-tuning with Hugging Face Transformers and PyTorch  
- Model evaluation using accuracy, F1-score, and confusion matrix  
- Visualization of model performance  
- Saving trained model artifacts for reuse
- Model Size Analysis  

The model achieved approximately **82% accuracy** and a **weighted F1 score of 0.82** on the test data.

---

## Dataset

**Source:** [Kaggle – Sentiment Analysis for Mental Health](https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health)

The dataset contains mental-health-related text samples categorized into seven sentiment classes:
- Normal  
- Personality Disorder  
- Stress  
- Suicidal
- Bi-Polar
- Depression
- Personality Disorder  

---

## Model Details

- **Base Model:** distilbert-base-uncased  
- **Framework:** Hugging Face Transformers with PyTorch backend  
- **Task:** Multi-class text classification  
- **Batch Size:** 32  
- **Learning Rate:** 4e-5  
- **Weight Decay:** 0.01  
- **Epochs:** 4 (early stopping applied)  
- **Tokenizer:** DistilBertTokenizerFast  
- **Evaluation Metrics:** Accuracy, F1-score, Precision, Recall, Confusion Matrix  

**Training Summary:**
| Metric | Validation | Test |
|--------|-------------|------|
| Accuracy | 0.8183 | 0.8199 |
| F1 (weighted) | 0.8174 | 0.819 |
| Loss | 0.4572 | 0.4801 |

---

## Tools and Technologies

- Python 3.8+  
- Transformers  
- PyTorch  
- NumPy  
- Pandas  
- Scikit-learn  
- Matplotlib  
- Seaborn  
- tqdm  
- Tokenizers  
- Accelerate  
- Jupyter Notebook (Kaggle environment)

---

## Installation (Kaggle Environment)

If running this project on **Kaggle**, most dependencies are already pre-installed.  
However, to ensure compatibility, you can manually install or upgrade the following libraries at the beginning of your notebook:

```python
!pip install transformers torch numpy pandas scikit-learn matplotlib seaborn tqdm accelerate tokenizers
