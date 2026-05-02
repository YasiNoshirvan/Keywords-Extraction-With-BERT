# Keyword Extraction with BERT

This repository contains a Natural Language Processing project focused on keyword extraction using BERT-based and transformer-based models.

The project builds upon **KeyBERT**, an unsupervised keyword extraction framework that uses contextual embeddings, and extends it in two main directions:

1. Comparing multiple embedding-based and generative models for English keyword extraction.
2. Adapting keyword extraction methods to multilingual and French-language datasets.

---

## 📌 Project Overview

Keyword extraction is an important NLP task used to identify the most relevant words or phrases from a document.  
It supports applications such as:

- Information retrieval
- Document classification
- Text summarization
- Search engines
- Content analysis
- Multilingual NLP systems

Traditional methods such as TF-IDF often fail to capture contextual meaning.  
This project investigates transformer-based approaches that use contextual embeddings to extract more meaningful and semantically relevant keywords.

---

## 🎯 Objectives

The main objectives of this project are:

- Explore and extend KeyBERT for keyword extraction.
- Compare multiple embedding and generative models.
- Evaluate keyword extraction performance using ROUGE and cosine similarity.
- Analyze different extraction configurations based on precision, recall, diversity, and coverage.
- Adapt keyword extraction to French texts.
- Improve multilingual keyword extraction using preprocessing and fine-tuning techniques.

---

## 🧠 Methodology

The project is divided into two main parts:

### 1. Embedding-Based Keyword Extraction

We evaluated several embedding-based and generative models on the **Inspec dataset**, which contains scientific abstracts and manually annotated keywords.

Models tested include:

- Sentence Transformers
- Flair
- SpaCy
- Gensim
- Universal Sentence Encoder
- RoBERTa
- BERT keyword extractor
- vlt5-base
- T5
- BART

Different configurations were tested to analyze the trade-off between keyword precision, recall, diversity, and coverage.

### 2. Multilingual Keyword Extraction

The second part focuses on adapting KeyBERT to French-language keyword extraction.

Datasets used:

- **WKC**: French news documents with annotated keywords
- **Papyrus-f**: French academic titles and abstracts with labeled keywords

Models tested:

- `paraphrase-multilingual-MiniLM-L12-v2`
- `xlm-roberta-base`
- `camembert-base`

Additional improvements included:

- Lemmatization using Stanza
- Named Entity Recognition
- Fine-tuning multilingual models on French datasets
- Positive and negative training pair generation
- Cosine similarity loss

---

## ⚙️ Keyword Extraction Configurations

Four extraction configurations were tested:

| Case | Configuration | Goal |
|---|---|---|
| Case 1 | Baseline Configuration | Balanced precision and recall |
| Case 2 | High-Diversity Extraction | More varied and diverse keywords |
| Case 3 | Conservative / High Precision | Fewer but more reliable keywords |
| Case 4 | Extreme Coverage | Larger number of keywords and wider coverage |

---

## 📊 Evaluation Metrics

The extracted keywords were evaluated using:

| Metric | Purpose |
|---|---|
| ROUGE-1 | Measures unigram overlap with reference keywords |
| ROUGE-2 | Measures bigram overlap with reference keywords |
| ROUGE-L | Measures longest common subsequence similarity |
| Cosine Similarity | Measures semantic similarity between extracted and reference keywords |

---

## 🏆 Main Results

The experiments showed that:

- **vlt5-base keywords** generally achieved the strongest ROUGE scores.
- **BART** performed very well in cosine similarity, meaning it captured semantic similarity effectively.
- Sentence Transformers also showed competitive results in several configurations.
- For French keyword extraction, model performance depended strongly on the dataset domain.
- **CamemBERT** performed slightly better on the WKC dataset.
- Fine-tuned **XLM-R** improved results on Papyrus-f compared to the base XLM-R model.
- Adding Named Entity Recognition helped improve recall in French keyword extraction.

---

## 📈 Key Insights

- Keyword extraction performance depends heavily on model selection and parameter tuning.
- High-diversity settings improve coverage but may introduce noise.
- Conservative settings improve precision but may miss relevant keywords.
- Generative models such as BART and T5 can capture semantic information beyond exact keyword overlap.
- Multilingual keyword extraction requires language-specific preprocessing and domain-aware fine-tuning.
- Named entities are important for improving recall, especially in French datasets.

---

## 💻 Technologies Used

- Python
- Natural Language Processing
- KeyBERT
- BERT
- Sentence Transformers
- RoBERTa
- XLM-RoBERTa
- CamemBERT
- T5
- BART
- Stanza
- ROUGE evaluation
- Cosine similarity
- Multilingual NLP

---

## 📄 Report

The full project report is included in this repository.

**Title:**  
Keyword Extraction with BERT

**Course:**  
Natural Language Processing

**Institution:**  
Politecnico di Torino

**Authors:**  
- Mohammad Amin Akhani  
- Amir Maleki  
- Farzaneh Masteri Farahani  
- Yasaman Noshirvanbaboli

---

## ⚠️ Note

This project was developed as part of a university Natural Language Processing course.  
The repository is intended for educational, research, and portfolio purposes.

---

## 📬 Contact

**Yasaman Noshirvanbaboli**  
GitHub: [YasiNoshirvan](https://github.com/YasiNoshirvan)
