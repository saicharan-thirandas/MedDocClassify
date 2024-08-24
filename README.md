# MedClassify: Analysis of Clinical Language Models and Entity Recognizers on Medical Document Classification Task

## Project Overview

This project focuses on classifying medical transcriptions using two primary tasks:

1. **Medical Specialty Classification**
2. **Medical Document Type Classification**

The goal is to evaluate and compare the effectiveness of traditional TF-IDF-based methods against domain-specific BERT-based models. The key comparisons include:

### NER Models with TF-IDF Baseline

NER models extract medical-specific entities such as anatomy and clinical terms, which are then vectorized using TF-IDF. Logistic regression is applied as the baseline classifier.

- **Anatomy Entity Recognizer (En_ner_bionlp13cg_md):**
  - Trained on the BIONLP13CG corpus from the 2013 BioNLP Shared Task.
  - Identifies entities like Anatomical_system, Cancer, and Organ, enabling detailed anatomical and biological feature extraction.

- **Clinical Entity Recognizer (En_ner_bc5cdr_md):**
  - Trained on the BC5CDR corpus.
  - Specializes in recognizing Disease and Chemical entities, making it ideal for clinical documentation tasks.

### Domain-Specific BERT-Based Models with Custom Heads

- **BERT:** A general-purpose model trained on a vast corpus of internet text, fine-tuned with a custom classification head specifically designed for medical tasks.
  
- **BioBERT:** Pre-trained on biomedical literature, such as PubMed abstracts, BioBERT excels in understanding biomedical terminology. It is fine-tuned with a custom classification head for medical classification.

- **ClinicalBERT:** Pre-trained on clinical notes from electronic health records, ClinicalBERT is adept at handling clinical language and nuances. This model is also fine-tuned with a custom classification head for the specific tasks.

## Purpose of the Project

The primary objective is to compare the performance of these approaches:

- **Traditional TF-IDF Baseline:** Involving NER-based entity extraction combined with TF-IDF vectorization and logistic regression.
  
- **Domain-Specific BERT Models:** Involving fine-tuned versions of BERT, BioBERT, and ClinicalBERT with custom classification heads optimized for medical text classification tasks.

By comparing these methods, the project aims to identify the most accurate and reliable approach for classifying medical transcriptions into specialties and document types.

## Conclusion & Future Work

This project demonstrates the strengths of domain-specific BERT models over traditional TF-IDF methods in medical document classification. The results highlight the superior performance of models like BioBERT and ClinicalBERT, particularly when fine-tuned with custom heads tailored to medical and clinical language.

Future work may include exploring additional models and refining classifier architectures to further enhance classification accuracy.

---
