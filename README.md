# NLP GRU Model for Biomedical NER

This project was developed as part of a **semester coursework project** focused on applying deep learning techniques to Natural Language Processing (NLP).

It implements a **Named Entity Recognition (NER)** system using a **Bidirectional GRU (BiGRU)** architecture, enhanced with weighted loss functions and inspired by BioBERT embeddings.

---

##  Project Overview

Named Entity Recognition (NER) is a key NLP task used in:

- Information extraction  
- Medical text analysis  
- Question answering systems  
- Biomedical research  

This project focuses on:

- Building a **BiGRU-based sequence model**
- Improving **multi-token entity detection**
- Handling **class imbalance using weighted loss**
- Enhancing prediction of **I-tags (inside entity tokens)**

---

##  Model Architecture

The model consists of:

1. **Embedding Layer**
   - Converts tokens into dense vector representations  
   - Inspired by BioBERT-style embeddings  

2. **Bidirectional GRU (BiGRU)**
   - Captures both past and future context  
   - Improves sequence understanding  

3. **Fully Connected Layer**
   - Maps hidden states to tag predictions  

---

##  Methodology

- Dataset uses **IOB tagging format (B, I, O)**
- Sentences are tokenized and padded
- Class imbalance handled using:
  - **Weighted CrossEntropy Loss**
  - Higher weight for **I-tags**
- Optimizer: **Adam**
- Training done in mini-batches

---

## Results

- Consistent decrease in training & validation loss  
- Improved prediction of **multi-token entities**  
- Better continuity in entity spans  

### Key Achievement:
- Accurate detection of entities like:
  - *"New York University"* → correctly labeled as one entity  

---

##  Key Insights

- Weighted loss significantly improves **I-tag prediction**
- BiGRU captures contextual dependencies effectively
- Model generalizes well with minimal overfitting
- Early epochs contribute most to learning

---

##  Challenges

- Class imbalance (O vs B/I tags)
- Incorrect chunking leading to missing I-tags
- Sensitivity to punctuation
- Overfitting to specific sentence patterns
- Limited generalization without pre-trained embeddings

---

##  Improvements Made

- Fixed **IOB tagging issues**
- Removed **punctuation noise**
- Improved **token-label alignment**
- Enhanced **entity continuity detection**

---

##  Dataset

- Tokenized biomedical text dataset  
- Annotated using **IOB format**

>  Dataset is not included due to size constraints.

---

##  Tech Stack

- Python  
- PyTorch  
- NumPy  
- NLP preprocessing tools  

---

##  How to Run

### 1. Clone Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
---

### 2. Install Dependencies
```bash
pip install -r requirements.txt

### 3. Train Model
python train.py

### 4. Evaluate Model
python eval.py



## References

This project is developed using:

Research papers on NER and BiGRU models

BioBERT and transformer-based approaches

Open-source NLP implementations

## Disclaimer

This project is created as part of a semester academic project for learning purposes.
Some ideas and implementations are inspired by publicly available research and online resources.

## License

This project is released under the Public Domain.
