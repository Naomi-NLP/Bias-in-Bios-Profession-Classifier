# 📘 Bias-in-Bios Profession Classifier

## 🔹 Overview
The **Bias-in-Bios Profession Classifier** is a Natural Language Processing (NLP) project built using the **Bias-in-Bios dataset**.  
This dataset contains short biographies of individuals alongside labels for their **profession** and **gender**.  

The project focuses on **automatically predicting a person’s profession from their biography text** while also highlighting potential **gender bias in machine learning models**.

---

## 🔹 Motivation
Machine learning models trained on human-written text often reflect **social biases**.  
For example:
- Professions like *nurse* or *teacher* may be more associated with women.  
- Professions like *engineer* or *professor* may be more associated with men.  

This project serves two purposes:  
1. **Classification Task** – Train a model that can predict the profession of a person based on their bio.  
2. **Bias Evaluation** – Measure whether the model performs equally well for male and female biographies, highlighting fairness concerns.  

---

## 🔹 Dataset (Bias-in-Bios)
- Contains **bios of individuals** downloaded from hugging face platform
- Each bio has two labels:  
  - **Profession** (28 different professions, e.g., teacher, engineer, professor, nurse, etc.)  
  - **Gender** (0 = male, 1 = female).  
- Useful for tasks like **profession classification**, **bias detection**, and **fairness benchmarking**.  

---

## 🔹 Methodology

### 1. Data Preprocessing
- Tokenization using Hugging Face `AutoTokenizer`.  
- Train/Dev/Test split (e.g., 2000 train, 200 dev, 1000 test).  

### 2. Model Training
- Fine-tuned a **Transformer-based model** (`AutoModelForSequenceClassification`).  
- Output layer trained to predict one of the 28 professions.  

### 3. Evaluation
- Overall accuracy on the test set.  
- Separate accuracy for **male vs female** bios.  
- Measured the **accuracy gap** (bias indicator).  


---

