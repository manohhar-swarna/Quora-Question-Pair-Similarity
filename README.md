# Quora-Question-Pair-Similarity

## Project Documentation
This project focuses on solving a real-world challenge faced by Quora—identifying duplicate questions to improve user experience and information retrieval efficiency. Quora receives millions of questions, many of which are semantically similar or duplicated. This leads to fragmented answers and redundant content. The goal of this project is to build an intelligent system that can detect whether a given pair of questions are duplicates, thereby allowing the platform to consolidate answers and streamline user navigation.

The project is framed as a binary classification problem, where the system predicts if two questions have the same intent. It utilizes a blend of classic Natural Language Processing (NLP) techniques and advanced machine learning models. The development pipeline begins with extensive text preprocessing, including HTML tag removal, punctuation stripping, stopword removal, stemming, and contraction expansion. From this cleaned data, a rich set of hand-engineered features is extracted—such as token overlap ratios, fuzzy string matching scores (using FuzzyWuzzy), and word-position-based comparisons like first/last word matches and absolute length differences.

To visualize and better understand the feature space, t-SNE-based dimensionality reduction was applied to the feature vectors. Textual data was further featurized using TF-IDF weighted word vectors, and these were used in parallel with hand-crafted features. The project also explored baseline random predictions to calculate worst-case log-loss, ensuring robust evaluation metrics.

Multiple machine learning models were trained and evaluated, including Logistic Regression, Linear SVM, and XGBoost, each fine-tuned with hyperparameter optimization. The performance was assessed using log-loss and binary confusion matrices, aligned with Kaggle's official evaluation criteria.

This solution offers a scalable and interpretable approach to semantic question matching, enabling platforms like Quora to auto-detect duplicates, reduce content clutter, and enhance both answer discovery and contributor efficiency. Its impact lies in reducing cognitive load for users while maintaining a clean and consolidated knowledge base.
