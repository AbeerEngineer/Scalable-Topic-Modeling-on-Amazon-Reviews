# Scalable-Topic-Modeling-on-Amazon-Reviews
This project presents a comprehensive comparison of four popular topic modeling techniques:
Latent Dirichlet Allocation (LDA)
Non-Negative Matrix Factorization (NMF)
BERTopic
Top2Vec

The study evaluates how these algorithms perform on large-scale text data using 100,000 Amazon Beauty Reviews.

📖 Overview

Topic modeling is a Natural Language Processing (NLP) technique used to discover hidden themes within large collections of text.

This project investigates the trade-offs between:

Topic Quality
Training Speed
Memory Consumption
Inference Time
Topic Diversity
Topic Uniqueness
Scalability

The objective is to determine which algorithm is most suitable for real-world production deployment under different constraints.

🎯 Objectives
Compare classical and neural topic modeling techniques.
Analyze scalability across increasing dataset sizes.
Measure computational efficiency.
Evaluate topic quality using coherence metrics.
Provide deployment recommendations for industry applications.
📂 Dataset

Dataset: Amazon Product Review Dataset v2

Category Used:

All Beauty Reviews

Source:
Amazon Review Dataset (UCSD)

Dataset Statistics
Metric	Value
Total Reviews	370,946
Clean Reviews	369,821
Language	English
Subsets Tested	10k, 30k, 50k, 100k
⚙️ Preprocessing Pipeline

The following preprocessing steps were applied:

Lowercasing
URL Removal
Special Character Removal
Stopword Removal
Lemmatization
Short Word Removal
Empty Review Filtering
🧠 Algorithms Evaluated
LDA (Latent Dirichlet Allocation)

Probabilistic topic modeling using Gensim's LdaMulticore.

NMF (Non-Negative Matrix Factorization)

TF-IDF based matrix factorization approach using Scikit-Learn.

BERTopic

Transformer-based topic modeling using:

Sentence-BERT
UMAP
HDBSCAN
Top2Vec

Embedding-based topic modeling using:

Doc2Vec
UMAP
HDBSCAN
📊 Evaluation Metrics
Efficiency Metrics
Training Time
Peak Memory Usage
Inference Time
Quality Metrics
Topic Coherence (C_v)
Topic Diversity
Topic Uniqueness
Perplexity (LDA Only)
Cluster Stability (BERTopic Only)
🏆 Key Findings
Algorithm	Strength
NMF	Fastest and most scalable
LDA	Highest topic coherence
BERTopic	Best semantic understanding
Top2Vec	Improves significantly with larger datasets
Best Production Choice

✅ NMF

Training Time: 2.43 sec
Memory Usage: 63.6 MB
Inference Time: 0.033 ms/doc
Highest Topic Quality

✅ LDA

Coherence Score: 0.599



📈 Results Summary
Training Time at 100k Reviews
Algorithm	Time
NMF	2.43 s
BERTopic	355.95 s
Top2Vec	1416.58 s
LDA	1873.12 s
Peak Memory Usage
Algorithm	Memory
LDA	6.13 MB
NMF	63.60 MB
BERTopic	1389.46 MB
Top2Vec	1714.90 MB

🛠 Technologies Used
Python
Pandas
NumPy
Gensim
Scikit-Learn
BERTopic
Top2Vec
Sentence Transformers
UMAP
HDBSCAN
Matplotlib
Seaborn
NLTK

🚀 Installation
pip install gensim
pip install bertopic
pip install top2vec
pip install sentence-transformers
pip install umap-learn
pip install hdbscan
pip install scikit-learn
pip install nltk
▶️ Run Project
python topic_modeling_comparison.py
or
jupyter notebook
Open the notebook and execute all cells.
