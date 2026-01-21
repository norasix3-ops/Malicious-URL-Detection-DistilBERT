# Transformer-Based NLP Model for Malicious URL Detection

This repository presents a **Transformer-based NLP system** for detecting malicious URLs using **DistilBERT**.  
The model classifies URLs into four categories: **Benign, Phishing, Malware, and Defacement**, achieving **98.89% accuracy**.

---

## 🔍 Problem Overview
Malicious URLs are widely used in phishing attacks, malware distribution, and website defacement.  
Traditional machine learning approaches rely heavily on handcrafted features, which are often ineffective against obfuscated and evolving URL patterns.

This project treats URLs as **text sequences** and leverages **transformer-based NLP** to learn contextual and structural patterns directly from raw URLs.

---

## 🚀 Solution
We fine-tune **DistilBERT**, a lightweight transformer model, to perform multi-class URL classification with:
- Minimal preprocessing
- No handcrafted feature engineering
- Fast inference suitable for real-world deployment

---

## 📊 Dataset
- **Source:** Malicious URLs Dataset (Kaggle)
- **Total URLs:** ~651,000
- **Classes:**
  - Benign
  - Phishing
  - Malware
  - Defacement
- **Split:** Stratified 70% Train / 15% Validation / 15% Test

---

## 🧠 Model Details
- **Base Model:** `distilbert-base-uncased`
- **Architecture:** DistilBERT + classification head
- **Why DistilBERT?**
  - ~40% fewer parameters than BERT
  - Faster inference
  - Strong performance on short text sequences (URLs)

---

## ⚙️ Training Configuration
- **Epochs:** 3  
- **Batch Size:** 16  
- **Optimizer:** AdamW  
- **Learning Rate:** 2e-5  
- **Loss Function:** Cross-Entropy  
- **Frameworks:** PyTorch, HuggingFace Transformers  

---

## 📈 Results
**Overall Accuracy:** **98.89%**

| Class        | Precision | Recall | F1-Score |
|--------------|-----------|--------|----------|
| Benign       | 0.9922    | 0.9944 | 0.9933   |
| Phishing     | 0.9641    | 0.9596 | 0.9619   |
| Malware      | 0.9908    | 0.9705 | 0.9805   |
| Defacement   | 0.9974    | 0.9991 | 0.9982   |
| **Macro Avg**| **0.9861**| **0.9809** | **0.9835** |

---

## 🔮 Prediction Tool
The project includes a simple interactive function that allows users to input any URL and receive a predicted class in real time.


