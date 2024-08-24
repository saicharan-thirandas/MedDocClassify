

# Analysis of Clinical Language Models and Entity Recognizers on Medical Document Classification Task

## Project Overview

This project involves two types of tasks: 

1. **Medical Specialty Classification**
2. **Medical Document Type Classification**

Each task is designed to evaluate and compare the performance of traditional TF-IDF-based methods and domain-specific BERT-based models. Specifically, we compare:

- **NER Models with TF-IDF Baseline:** Named Entity Recognition (NER) models are employed to extract medical-specific entities like anatomy and clinical terms, which are then used as features in TF-IDF vectorization. Logistic regression is applied to these features, serving as the baseline for classification tasks.

- **Domain-Specific BERT-Based Models with Custom Heads:**
  - **BERT:** A general-purpose model trained on a vast corpus of internet text, used here with a custom classification head tailored for medical tasks.
  - **BioBERT:** A BERT model pre-trained on biomedical literature such as PubMed abstracts. BioBERT is particularly effective at understanding biomedical terminology and is fine-tuned with a custom head for medical classification.
  - **ClinicalBERT:** A BERT model pre-trained on clinical notes from electronic health records, making it adept at handling clinical language and nuances. This model is also fine-tuned with a custom classification head for our specific tasks.

### Purpose of the Project

The primary objective is to compare the performance of these approaches:

- **Traditional TF-IDF Baseline:** Using NER-based entity extraction combined with TF-IDF vectorization and logistic regression.
- **Domain-Specific BERT Models:** Fine-tuned versions of BERT, BioBERT, and ClinicalBERT with custom classification heads specifically written to optimize their performance on medical text classification tasks.

By doing so, we aim to determine which method provides the most accurate and reliable results for classifying medical transcriptions into specialties and document types.

## Conclusion & Future Work

This project demonstrates the relative strengths of traditional TF-IDF methods versus domain-specific BERT-based models in medical document classification. The comparison reveals how models like BioBERT and ClinicalBERT, with custom heads, excel in handling domain-specific language. Future work may explore additional models and further refine classifier architectures to improve classification accuracy.


